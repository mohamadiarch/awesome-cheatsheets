# Postgresql

### Naming conventions

| Common Name               | Postgresql Name            |
| ------------------ | --------------------------------- | 
|table or Indexes    | Relation                             |
|Row                 | Tuple                                |
|Column              | Attribute                            |
|Data Block          | Page(when block is in disk)          |
|Page                | Buffer(when block is in memory)      |

### Page
Page: smallest unit of storage. Every table and index is stored as an array of pages of fixed sizes. default size= 8kb
All pages are logicaly equivalent and any row can be stored in any page. and we cant choose which row go to which page

| Page component                  | Description    | 
|-------------------------------- |  ------------------------------------------ |
| PageHeader Data                 | Genaral info like free space pointer, page size, version    | 
| ItemId Data                    | Pointer to a Tuple     | 
| Tuple                          | Actual items     | 
|  Free space                    | New pointers insert from top, Tupels Insert from bottom     | 
| special space                   | Index access method specific data     | 


## Postgresql architecture

poastmaster: 
the first process that get startted: 1. start proccess 2. assing buffers 3. check ip and password
when user send a requet. postmaster starts a new process (a new postgres per each client)to handle that request.

shared buffer:
when user send an sql request the result will load in shared data.(temporary location)
User can not access data files directly to read or write data
controlling by a parameter: shared_buffer located in postgresql.conf

dirty data:
the value in memory(not in disk) or uncommited data

commited transaction:
the transaction that is completed


Wal buffer:
if user send a transaction, a copy of transactions will be stored in wal buffer. When the user commit the changes the wall buffer
will involke the wal writer, which will write all the changes to the wal files on disk.



checkpointer:
checks every 5 minutes will involke the Bgwriter to save all changes (dirty buffers in shared buffer) into data files
we can change default time
it also involk when the wal buffer is full(1GB)

Archiver process: (optioal)
checks the wall file and if it is full, Archiver process copies the wal file to archive file
in test systems we dont enable it bcz it needs lot of disk space. useful for recovery. (imp for production)

CLOG buffer:
all commited transactions are marked in this buffer. So if system crashes this buffer referred to check all the commited transactions
is an area in RAM that holds the state of all transactions

stat collector:
collect and report information about server activity then update this information to the database dictionary
so db dictioanry will be updated with the latest happening information(pg_catalog)

Work memory buffer:
is memory reserved for eighter a single sort of hash table (sort of commnads) [work_mem parameter]

Maintenance Work memory:
for maintenance work [maintenance_work_mem parameter]

Temp buffers:
used for temporary tables in a user session during large sort and hash table [parameter temp_buffers]
as soon as the session ends this memory will be freed automatically

Auto vaccum launcher:
vacuum daemon to carry out the vacuum operations on fragmented tables

log collector or log writer:
ensure all logging and tracing information in the error log. exp: Postgresql does not start.

BgWriter or Writer:
Preodicaly writes the dirty buffer to a data file
(make changes to a data by transaction)

Wal writer:
writes the wal buffer to a wal file 
this happens when we do a commit




## Physical Files 


data file:
final location, pure data


wal data:
metadata information about changes to the acutal data and it is sufficent for recovery 
all transactions are written first before commit happens
wal data is stored in a physical disk in location: "WAL segment"
wal writer flushed the wal data from the buffer to wal segment
wal files write ahead log files


log files:
all server messages: stderr,csvlog,syslog


archive files(optional):
data from wal segments are writtern into archive files used for recovery


## folder layout
```bash
bin                    #
data                   #
debug_symbols          # for developers debugging
doc                    # doc of postgresql
include                # header files
installer               # for server installer
pgAdmin                 # for server admin in gui interface
share                  # sample of all config files for rebuilding
```

## data directory folder layout
```bash
base                    # a directory for each database
global                  # cluster wide tables such: pg database, pg tablespace,pg indexes,
log                      # all logs
pg_commit_ts             # commit timestamp data
pg_dynshmem             # dynamic shared memory subsystem
pg_logical              # all logical decoding,snapshots,mappings 
pg_multixact            # multi transaction staus data
pg_notify                 # notifications status data
pg_replslot               # when we enable replication slots
pg_serial                  # commited serialiezed transaction
pg_snapshots                # exported snapshots
pg_stat                    #permanent files for stat subsystem
pg_stat_tmp                # temporary files for stat subsystem
pg_subtrans                # subtransaction status data
pg_tblspc                  # contain symbolic links to the tablespace data
pg_twophase              #state files which is for prepaid transactions
pg_wal                   # write ahead log files
archive_status             # if we enable archiver
pg_xact                    # transaction commit data, all your transactions metadat logs
pg_hba.conf                # postgresql authentification (Host Base Authentication)
pg_ident.conf              # when we map user data to postgresql user
pg_version                 # postgresql version
postgresql.conf            # postgresql server config
postgresql.auto.conf        # alter system commands will be stored here (override the postgresql.conf)
```
## postgresql default databaes
```bash
postgres                  # if you login with postgres user you will connect to this db
template0                # a pristine copy of template for new databaes ( no connection allowed) 
template1                # a pristine copy of template for new databaes ( connection allowed) 
CREATE DATABASE newbd TEMPLATE template0;
select datname,oid from pg_database;      # no datanem becarful, oid= object identifier, pg_database inside global folder
```

## cluster
db cluster: is a collection of databaes that is managed by a single instance on a server
Initdb ===> creates a new  postgresql db cluster
data directory= creating a data cluster consist of creating the directories in which data is store
we have to first initilize the storge area on the disk before we any operation on the database


## start cluster in linux
```bash
su -u postgres                                         # change user
ps -ef | grep postgres                                # check if postgres is running
initdb -D /usr/local/psql/data                  # initilize a new db -D refer to data directory location(if folder is empty we should init cluster)
# -W we can use -W to force super user to provide password before initialize db
pg_ctl -D /usr/local/pslq/data initdb     # initilize second syntax databse
pg_ctl -D /usr/local/pslq/data -p 5432     # we should set a a new  port to new created cluster
systemctl start postgresql-12              # start cluster in linuc
systemctl stop postgresql-12                # stop cluster in linux
systemctl enable postgresql-12              # enable cluster to automatically start after reboot
system reload postgresql-11                     # reload cluster in linuc
systemctl restart postgresql-11                   # restart cluster in linux
```

## start cluster in windows
```bash
pg_ctl start                                  # start cluster in windows if set in environment variable
pg_ctl stop                                    # stop cluster in windows
pg_ctl -D "C:\Program Files\PostgreSQL\12\data" start     #  start cluster in windows if you do not set the path in environment variable
pg_ctl stop -D "C:\Program Files\PostgreSQL\12\data" -m        # stop cluster in windows
ppg_ctl reload                                   # reload cluster in windows
pg_ctl restart                                  # restart cluster in windows
pg_controldata                                # information about current cluster
```

## command line
```bash
createdb -U alice -p 5432 -h localhost -d customers   # create new database for customers
createdb -U alice customers                            # create new database for customers
dropdb -U alice customers     # drop database
```

## psql

```bash
psql -U postgres -p 5432 -h localhost -d postgres     # connect to cluster -p: port -h: host -d: database
psql -U postgres                                # -U for user. default user is postgres
show data_directory                              # show data directory
show port                                       # show port
show work_mem                                   # show work memory
show max_connections                             # show something inside postgres.conf, no need to open file manually
select name,boot_val,source from pg_settings    # see something in postgres.conf
select * fomr pg_file_settings                   # data dictionary view
\d pg_settings                                   # all columns in postgres.conf
alter system set work_mem='64MB'                 # set work memory in postgresql.auto.conf
alter system reset work_mem                      # reset work memory
alter system reset all                           # reset all properties in postgresql.auto.conf
select pg_reload_conf();                          # reload cluster in pqsl
```


## sql inside psql
```bash
create database customers owner alice;            # create new database
drop database customers;                          # drop database
```

# psql comands
```bsah
exit or \q                                   # exit psql
\l                                          # list databases
\conninfo                                   # information about current database
\c postgres                                 # connect to database default database 
```
### types of shotdown
1. Smart ===>disallows new connection but let existing setions work noramally
2. Fast(default) ===> kill all current transactions
3. Immediate ====> abort all current transactions and lead to recovery on next startup

## postgres.conf
```bash
initdb                                               # installs a defaul copy of postgres.conf located in data directory

```

### pg_hba.conf
```bash
listen_addresses = '*' ==> postgresql.conf              # '*' means all ip address in file postgresql.conf (we can set multiple ip address)
host all all 0.0.0.0/0 md5 | crypt                             # 0.0.0.0/0 means all ip address and md5 means password required, crypt means encrypt
host all all ::0/0 reject                                # ::0/0 means all ip address and reject means denie access
host all all 127.0.0.1/32 trust                           # 127.0.0.1/32 means localhost and md5 means trust means password not required 
```


