---
source: https://github.com/RehanSaeed/Bash-Cheat-Sheet
---

# Bash Cheat Sheet

 A cheat sheet for bash commands.
```bash
# online services
https://linuxcontainers.org/
```
## packages
[[linux_packages]


## list of package managers
```bash
apt       # debian based   #.deb  # Ubuntu, Mint,kali, Debian, elementary OS, Zorin OS, BlackBox
dnf  or yum        #Red Hat-base     #.rpm   # Fedora, CentOS, RHEL, Amazon Linux, Oracle Linux, openSUSE
pacman    #Arch-based       #.rpm   # Arch Linux, Manjaro, EndeavourOS, ArcoLinux
portage   #Gentoo-based     #.rpm   # Gentoo
slackpkg,pkgtool   #Slackware-based    # Slackware
snap     #cross-distribution
flatpak   #cross-distribution
AppImage   #cross-distribution
zypper(ZYpp)    #openSUSE and SUSE Linux
emerge
synaptic      # graphical package manager
# Many distributions offer graphical package managers (e.g., Ubuntu Software Center, GNOME Software)
 ```

## os
```bash
cat /etc/*release             # what distro we are running 
lsb_release -a               # what distro we are running
cat /etc/os-release          # what distro we are running
```


## Doc
```bash
help                       # list of all commands + shell
help cd                    # doc for cd command == cd --help
help for                   #doc for for command in bash
man -k print              # seacrh in commands and short descriptoin like grep    **
compgen -c 
dman                      # read man page for command without installing that( apt i debian-goodies)
wman                      # text web browser for reading man page on internet
```

## man
```bash
man -k ^ls$
info sort | grep "\-s" or grep " -s"                        # Search for '-s' in the doc of sort
man ps | grep -E "ali |" -n    # you can see line number in man page by grep 
man rsync| less -p -v     #search for -v flag in rsync command
rsync -h| less -p -v      #search for -v flag in rsync command
g45                             # go to line 45 | find the line number with -n in grep | use / for search 
-N press Enter                  # toggle line numbers in man page
```

## WH
```bash
who
whoami
which
whereis
echo $USER    # display user
logname       # 
```



## List of commands
```bash
help
alias
compgen -c                 # will list all the commands you could run.
compgen -a                 # will list all the aliases you could run.
compgen -b                 # will list all the built-ins you could run.
compgen -k                 # will list all the keywords you could run.
compgen -A function        # will list all the functions you could run.
compgen -A function -abck  # will list all the above in one go.
```
## apt
```bash
apt update                   # Refreshes repository index
apt upgrade                  # Upgrades all upgradable packages
apt search vim              # Search for a package in  internet
apt search ^vim$             # apt search == google search
apt-cache search vim               #like apt search vim
apt show vim                # List information about the vim (no need to install)
apt list          # list of all packages
apt list vim                  # find
apt list --all-versions wget # List all versions of the package
apt list --installed          # List all installed packages
apt list --upgradable         # List all upgradable packages
apt list --all-versions        # This shows all available versions of each package
apt install wget             # Install the latest version of the wget package
apt install wget=1.2.3       # Install a specific version of the wget package
apt remove wget              # Removes the wget package
```


## Command History

```bash
!!            # Run the last command
history -c        # clear all history
touch foo.sh   # update timestamp of file exists
chmod +x !$   # !$ is the last argument of the last command i.e. foo.sh
```

## Creating Files

```bash
touch foo.txt          # Create file or update(touch) existing files modified timestamp 
touch foo.txt bar.txt  # Create multiple files
touch {foo,bar}.txt    # Create multiple files
touch test{1..3}       # Create test1, test2 and test3 files
touch test{a..c}       # Create testa, testb and testc files
cat > 1.txt             # start writing in a file
echo "hi" > 1.txt
printf "hi" > 1.txt
vim 1.txt | nano 1.txt
```


## Creating Directories

```bash
mkdir foo                        # Create a directory
mkdir foo bar                    # Create multiple directories
mkdir -p foo/bar       # Create nested directory
mkdir -p {foo,bar}/baz # -p --parents Create multiple nested directories
touch a; mkdir a                  #create a as a file and gets error for directory
mktemp -d| --directory            # Create a temporary directory
```

## Symbolic Links

```bash
ln -s| --symbolic 1.txt link.txt            # Create a link for 1.txt into link.txt. soft link = symbolic link
ln -s| --symbolic -f| --force foo bar # Overwrite an existing symbolic link 'bar'
ls -l                               # Show where symbolic links are pointing
ln 1.txt hlink.txt                  # Create a hard link. change 1.txt will also change hlink.txt. but delete 1.txt will not delete hlink.txt
```

## Temp files

```bash
/tmp                                 # is typically cleared on system reboots.
/var/tmp                              # might retain files across reboots.
mktemp                                 # create a random temporary file
mktemp -d myname.XXXX                  # cretae a temp diretory in current folder (-d folder)
mktemp -u /tmp/temp1.XXXXXX /tmp/temp2.XXXXXX       # create multiple temp file
```


## Navigating Directories

```bash
pwd                       # Print current directory path
cd                        # Go to home directory
cd ~                      # Go to home directory
cd -                      # toggle directory 
pushd foo                 # Go to foo sub-directory and add previous directory to stack
popd                      # Go back to directory in stack saved by `pushd`
dirs                      # list of pushd
```
## List direcoty

```bash
tree                      # List directory and file tree
tree -a                   # List directory and file tree including hidden
tree -d                   # List directory tree
ls -R                      # -R:recursive List inner folders like tree
echo *                    # echo all files in current directory 
echo ?                    # list files in current directory with one char in name like a
ls                        # List directories sort by name alphabetically
dir                       # like ls (diff in format) like win
ls -a| --all               # List directories including hidden ===> -aA show hidden but not . and ..
ls -d | ls -d */                     # List just directories
ls -l                     # List directories in long form
ls -l -h                   # List directories in long form with human readable sizes
ls -lhS                    # -S List and Sort by size
ls -lhSr                  # -Sr List and Sort then reverse
ls -lhSX                  # -SX List and Sort by extension or format
ls -lhSt                  # -St List and Sort by time
ls -t                     # List directories by modification time, newest first
ls folder                    # List files inside folder
ls -c -ltd foo            # just info of specific folder
file foo.txt              # simple file info ==> simple stat
stat foo.txt              # List size, created and modified timestamps for a file
stat foo                  # List size, created and modified timestamps for a directory
```

## ls -l cols
```bash
total (in ls -ls commnd)   # total number of bloacks ===> ls -asl ===> see block size of each file (Blocks have a fixed size :4kb)
1. file type + file permissions
3. number of hard links     # for files =1 for dir =2 
4. owner
5. group
6. size                      # 4kb for empty folder
7. last modified time
8. name
```


## wildcard

```bash
ll 1.js                  # just info of 1.js
ls *.js                   # List all .js files
ls *.???                  # List files with three chars in format like .txt
ls [12].txt               # List files with numbers in format like 1.txt and 2.txt
ls [!12].txt              # List files without this numbers
ls [1-9].txt              # List files 1.txt through 9.txt
```
## Deleting Directories and Files

```bash
rmdir foo                        # Delete empty directory (safe command)
rm -d ./*                        # Delete empty directory ==rmdir
rm -r  folder            # Delete directory including contents
rm    1.txt            # Delete file
rm -r ./*                         # -r alseo delete files
rm -f 1.txt                             # Delete file, ignore nonexistent files and never prompt
rm -i 1.txt                                         # interactively (ask question)
trash 1.txt                      # Move file to trash (you need to install)
```

## Moving Directories

```bash
cp -r foo bar                               # Copy directory
cp -n foo bar                                           #copy with no overwrite
cp -i foo bar                                           #copy with interactive question
mv foo bar                                              # Move directory

rsync -avhz source/ destination1/ dest2/                # copy and sync
rsync -z| --compress -v| --verbose /foo /bar              # Copy directory, overwrites destination
rsync -a| --archive -z| --compress -v| --verbose /foo /bar # Copy directory, without overwriting destination
rsync -v                                                #copy with result interactively
rsync -avz /foo username@hostname:/bar                  # Copy local directory to remote directory
rsync -avz username@hostname:/foo /bar                  # Copy remote directory to local directory
```

## Moving Files

```bash
cp foo.txt bar.txt                                # Copy file
mv foo.txt folder                                # Move file
mv 1.txt 1new.txt                                  # Rename file
# we do not have a command for renaming a file but we can move it
rsync -z| --compress -v| --verbose /foo.txt /bar    # Copy file quickly if not changed
rsync z| --compress -v| --verbose /foo.txt /bar.txt # Copy and rename file quickly if not changed
```
## Reading Files

```bash
cat foo.txt            # Print all contents
cat 1.txt 2.txt         # Print multiple files
cat -b foo.txt         # show line number for cat
open foo.txt           # Open file in the default editor
less foo.txt           # Print some contents at a time (g: go to top of file, G: go to bottom of file, /foo: to search for 'foo')
more foo.txt           # browse file in terminal with option more
head foo.txt           # Print top 10 lines of file
head foo.txt -n 200    # show 200 line
tail foo.txt           # Print bottom 10 lines of file
wc foo.txt             # List number of lines words and characters in the file
file foo.txt           # file type
basename /home/1.js    # gives you the last section of the path == 1.js
basename /home/1.js .js  # remove .js from the basename
dirname /home/mycomputer/project  # remove last section and return others= /home/mycomputer
```

## Writing Files

```bash
vim 1.js                        # write inside vim
cat > 1.js                      # write inside terminal (replace)
cat >> 1.js                     # write inside terminal (append)
cat >> 1.js << D                # write inside terminal until you type D and press enter
echo "this is a text" > 1.js    # write without opening the file (replace)
echo > 1.js                     # empty the content of a file with a space char
> 1.js                          # empty the content of a file with no char
truncate -s 0 1.js              # empty file 
yes "Line" | head -n 100 > my_file.txt      # create a file with 100 lines
```


## Standard Output, Standard Error and Standard Input

```bash
echo "foo" > bar.txt       # Overwrite file with content (redirection mark)
echo "foo" >> bar.txt      # Append to file with content
ls xxxNO > 1.txt            # if xxxNO does not exist the contenet of 1.txt will be delete with nothing (wrong you should use channel 2)
ls exists 1> stdout.txt    # Redirect the standard output to a file (chanel 1)
ls noexist 2> stderror.txt # Redirect the standard error output to a file (chanel 2)
ls xxx 1> output.txt 2> error.txt
ls xxx > output.txt 2> error.txt    #default output is channgel 1
ls >out.txt 2>&1            # Send channel 2 in the same file as channel 1
ls -lh > newfile.txt         #first create newfile.txt then run the command ls -h then write
ls > /dev/null             # Discard standard output and error
read foo                   # Read from standard input and write to the variable foo (foo=inpiut() in python)
tee -a foo.txt             # echo + save in file (-a append)
```

## Trnaslation
```bash
echo "this is a test" | tr ' ' '_'              # replace space with _ 
tr [a-z] [A-Z]                                     # uppercase
tr A-Z a-z < foo.txt                                       # lowercase (you can do not use [])
```

## Calculator
```bash
bc                          # basic calculator
quit                        # not <C-c>
echo "1 + 2" | bc           # use pipeline
bc < foo.txt                # use file (4 +5 inside the foo.txt) input redirection
```


## command combination
```bash
cmd1 ; cmd2 ; cmd3	# run multi commands 
cmd1 && cmd2		# cmd2 runs if cmd1 runned success
cmd1 || cmd2		# cmd2 runs if cmd1 NOT runned success
cmd  > filename		# send output to filename (ovewwrite)
cmd >> filename		# append output to filename
cmd < filename		# send input data to cmd from filename
help | more
echo "1.txt 2.txt" | xargs mkdir
echo -n "hello"; date  # print hello and date in one line===> echo -n ==> one line
{ echo -n "hello"; date;} > output.txt     # command grouping and redirect both output into a file{space needed}
```


## User Management
```bash
sh                    # become shell ==> bash is better
bash                   # become bash
sudo sh -c 'cd dirname' # run a command as a shell
su - mohamad            # become another user
sudo -s                 # become root
sudo su                 # become root
useradd ali
passwd ali               # add password for ali
userdel -r ali            # -r is for delete home directory  
useradd -m -s [shell_name] username # creates a new user -m create a home (/bin/bash)
useradd ali -g [pg_name] 		# adds user to group_name as primary group
groups                  # display groups
sudo tail /etc/group
groupadd [OPTIONS] GROUPNAME
id ali                    # show USERID for ali (username) ==> id show id of cuurent user
who                    # show who is logged on the system
w                      # like who with more details
users                   # list logged in users
cat /etc/passwd                     # list of all users
```

## passwd cols

```bash
compgen -u  # list of all users
man passwd
username:password-encrypted(x)(/etc/shadow):uid:gid:gecos(User information):home:shell
```

## File Permissions

| -r Read =4 | -w Write =2 | -x Execute =1 |
For a directory, execute means you can enter a directory.

- u - User
- g - Group
- o - Others
- a - All of the above

```bash
ls -l /foo.sh            # List file permissions
chown  username 1.txt    # change owner
chown -r ali folder      # -r change all inener folders too 
chgrp groupname 1.txt
chmod -744 foo.sh        # rwx for user+ r for group + r for others (+ or -)
chmod u+x foo.sh         # Give the user execute permission
chmod u-x,g-x foo.sh     # Take away the user and group execute permission
chmod o+rwx file # add rwx for other
chmod o=rw file  # set rw for other
chmod og-x file  # remove x from other and group
chmod a+r file   # everyone can read
chmod a+x foo.sh         # Give everybody execute permission
chmod +x foo.sh          # Give everybody execute permission
umask                    # umask 0444 : the permissions that the user does not want to be given (default :0022 or 0002)
stat 1.js                # view Inode details
```


## SUID and SGID File Permission


## shell variables

``` bash
TEST="Unix" | echo $TEST             #set a variable by user
export				    # export a VAR to sub shels and sob processe
printenv  			    # list all variables on bash like $PATH, $HOME, $DISPLAY
unset VAR_NAME			# drop VAR_NAME from bash
env 				    # list all variables on bash like $PATH, $HOME, $DISPLAY
env VAR=value cmd 		# Run cmd with new value of VAR 
echo $?                 # returns exit status code of last command
```

## Finding Files

Find binary files for a command.

```bash
type wget                                  # Find the binary
which wget                                 # Find the binary
whereis wget                               # Find the binary, source, and manual page files
compgen -c | -a                            # list of binary files

updatedb                                   # Update the index
locate foo.txt                             # Ins: Find a file (locate use index so it is fast but find didn't and it is slow)
locate --ignore-case                       # Find a file and ignore case
locate f*.txt                              # Find a text file starting with 'f'

find                                       # like tree (find -print)
find /path -name foo.txt                   # Find a file
find /path -iname foo.txt                  # Find a file with case insensitive search
find /path -name "*.txt" -or -name "*.js"   # qoutation is important
find folder/  -name 'pattern' -not -path 'folder/excluded_path/*'
find /path -name foo.txt -delete           # Find a file and delete it
find /path -name "*.png" -exec pngquant {} # Find all .png files and execute pngquant on it
find /path -type f -name foo.txt           # Find a file
find /path -type d -name foo               # Find a directory (-l for symbolic links)
find /path -type f -mtime +30              # Find files that haven't been modified in 30 days
find /path -type f -mtime +30 -delete      # Delete files that haven't been modified in 30 days
find . -type d,l,f  				# find directorys , links and files
find . -size +1k    				# size of result is > 1kB
find / -size +50M -size -100M       # Size between 50MB – 100MB
find . -type f -perm 0777 -print    # all the files whose permissions are 777
find / -type f ! -perm 777          # Find all the files without permission 777
find / -mtime +50 –mtime -100       # modified in 50-100 last days
```

## Find in Files
**note**: use -n always

```bash
grep 'foo' /bar.txt                           # Search for 'foo' in file 'bar.txt'
info sort | grep "\-s" or grep " -s" or grep -- "-s" or grep -e                       # grep [a-z] means range
man ps | grep -e "first word" -e "second word"                     # Search for multiple words 
man ps | grep -E --color "word| "              # Adding a pipe in search term with -E flag for show the whole output and highlight term in that
grep 'foo' -r ./*                             # Search for 'foo' in all files and directories
grep 'foo' -n bar.txt  | --line-number        # Add line numbers
grep 'foo' -w bar.txt                         # find exact word
grep 'Foo' /bar -i | --ignore-case            # Case insensitive search (ignore-case )
grep 'foo' -A 4 bar.txt                       # find 4 lines After the match
grep 'foo' -B 4 bar.txt                       # find 4 lines Before the match (-A 4 -B 4)
grep 'foo' -C 4 bar.txt                       # find 4 lines After and Before (content) the match (lowercase -c is for count)

grep 'foo' /bar -r | --recursive              # Search for 'foo' in directory 'bar'
grep 'foo' /bar -R | --dereference-recursive  # Search for 'foo' in directory 'bar' and follow symbolic links
grep 'foo' /bar -l | --files-with-matches     # Show only files that match
grep 'foo' /bar -L | --files-without-match    # Show only files that don't match

grep 'foo' 1.txt -x | --line-regexp            # Match only the entire match line
grep 'foo' 1.txt -v | --invert-match           # Show only lines that don't match
grep 'foo' /bar -c | --count                  # Count the number lines that match

grep 'foo' -lrc ./*                           # show count + name files that match in all of directories and subdirectories
grep '...-...-...$' bar.txt                    # use regex in grep  (as2-we1-dsa)
grep --perl-regexp| -p '\d{3}-\d{3}$' bar.txt  # use regex in grep (333-333)  
grep 'foo' /bar --colour                       # Add colour to output
man lsof | grep -e "^" -e "negated"            # display whole file and just highlight
man lsof | egrep  "^|negated"                  # display whole file and just highlight
grep 'foo\|bar' /baz -R                        # Search for 'foo' or 'bar' in directory 'baz'
grep --extended-regexp| -E 'foo|bar' /baz -R   # Use regular expressions
egrep 'foo|bar' /baz -R                        # Use regular expressions
history | grep "git commit" | grep "dotfiles"  # use pipe
```
## VIM
```bash
vim -c "/ali" 1.txt                             #take me to position that ali is. -c means commnad mode and / means search mode 
vim +14 1.txt                                  # open file at line 14
```

### Replace in Files

```bash
sed 's/fox/bear/' foo.txt               # Replace fox with bear in foo.txt. (find all fisrt matches in lines of whole file)
# (we will see the output even no match find)   s:substitute
sed 's/fox/bear/gi' foo.txt              # (-i case insensitive) -g find all matches in entire line 
sed 's/red fox/blue bear/2' foo.txt      # just second match of line
sed 's/fox/bear/3g' foo.txt > bar.txt     # Replacing from nth occurrence to all occurrences in a line
sed 's/fox/bear/g' foo.txt -i| --in-place # Replace fox with bear and overwrite foo.txt
sed '1,3 s/unix/linux/' geekfile.txt       # Just in line 1 to 3 (4,$)
sed -n 's/unix/linux/p' geekfile.txt       # -p :Print the matches twice, -n: Printing only the replaced lines
-------
sed '5d' filename.txt                     # delete line 5
sed '$d' filename.txt                     # delete last line
sed '3,6d' filename.txt                   # delete line 3 to 6
sed '/abc/d' filename.txt                 # delete line that contain abc
```


## Sort
```bash
sort 1.js                       #sort lines inside 1.js and print in terminal per first column by alphabet
sort -o output.txt file.txt     #sort lines inside 1.js and save in output.txt
sort -u filename.txt            #sort lines inside 1.js and remove repeated 
sort -k 2 1.js                  #sort lines inside 1.js per second column(key) (date > 1.txt or ls-la >1.txtj j) 
sort -k 1 -k 2 1.js             #sort lines inside 1.js per first then per second column 
sort -k 2 -n 1.js               #sort lines inside 1.js per second column numerically [ -M for month ] 
sort -t : -k 3n /etc/passwd    # sort -t for separator -k for col and 3n means third col by numerically
sort 1.js -r                   #sort reverse
sort 1.js -n                   #sort numerically
sort 1.js -f                   #sort uppercase and lowercase together
sort 1.js +4                   #ignore 4lines
sort 1.js | uniq -c            # count repeated lines
sort 1.js | uniq -c | sort -n  # sort by repeated liens
```


## cut
```bash
cut -b 1,2,3 state.txt # cutting out the column of a file (slice a file)
# Tabs and backspaces are treated like as a character of 1 byte
ps -aux | cut -b 1-3,5-7 #slice with range (2- means 2 to end) (-3 means first to col 3)
ps -aux| cut -d " " -f 1 #slice with -d delimiter and -f field
cut -d " " -f 1,2 state.txt --output-delimiter='%'
cat state.txt | head -n 3 | cut -d ' ' -f 1 > list.txt
fold -w 60 -s foo.txt    # wrap in 60 char wrap ( width) and -s for break the lines on spaces
```

## awk

```bash
/pattern/ {awk-commands}                             # syntax awk
awk -f 1.awk /etc/passwd                             # run a awk file with content "{print}"
ps | awk '{print $1}'                                # print column one
ps | awk '{print $NF}'                               # print last column
ps | awk '{print $0}'                                # print all columns (whole a row)
ps | awk '{print}'                                   # print all columns with all rows
ps | awk 'NR==1'                                     # print first row (row number one)
ps | awk '{print NR $0}'                             # print whole row with NumberRow 
ps | awk 'NR==1,NR==10 {print $0}'                   # print rows between 1 to 9 (range)
ps | awk '{print substr($1,2)}'                      # print substring
awk -F: '{print $1, $NF}' /etc/passwd                # use colon as Filed separator or -F ":"
awk -F: '{print $1 ",,,,," $NF}' /etc/passwd         # You can use separators with "
awk -F: '{print $1 "\t" $NF}' /etc/passwd            # tab as separator
awk -F: 'BEGIN {FS=":"; OFS="-----"} {print $1,$6,$7}' /etc/passwd #use formula as a separator
awk -F: '/^m/ {print $1,$6,$7}' /etc/passwd          #  awk syntax / / for using Regex pattern  
df | awk '{print $1 "\t" $2 - $3}'                      # + - * /  for math operator  
awk 'length($0) > 12' /etc/shells                    # find the lines that have more than 12 char in col $0
ps -ef | awk '{if($NF) == "/bin/fish" print $0}'     # use if
awk 'BEGIN {for ( i=1; i<10; i++ ) print "Hi" i }'
awk 'END' {print NR} /etc/shells                     # print number of line of rows
awk 'END' {print NR} /etc/shells /etc/passwd         # sum of number of rows of multiple files
```


## Important Files
```bash
cat /etc/passwd                     # list of all users
cat /etc/shells                     # list of all shells
cat /etc/services                   # list of all ports
cat /etc/crontabs                   # list of all crontabs
```


## Compressing Files

### zip


```bash
# Compresses one or more files into *.zip files.
zip foo.zip /bar.txt                # Compress bar.txt into foo.zip
zip foo.zip /bar.txt /baz.txt       # Compress bar.txt and baz.txt into foo.zip
zip foo.zip /{bar,baz}.txt          # Compress bar.txt and baz.txt into foo.zip
zip -r| --recurse-paths foo.zip /bar # Compress directory bar into foo.zip 
# Compresses a single file into *.gz files.
gzip /bar.txt foo.gz           # Compress bar.txt into foo.gz and then delete bar.txt
gzip -k| --keep /bar.txt foo.gz # Compress bar.txt into foo.gz
# Compresses (optionally) and combines one or more files into a single *.tar, *.tar.gz, *.tpz or *.tgz file.
tar -c| --create -z| --gzip -f| --file=foo.tgz /bar.txt /baz.txt # Compress bar.txt and baz.txt into foo.tgz
tar -c| --create -z| --gzip -f| --file=foo.tgz /{bar,baz}.txt    # Compress bar.txt and baz.txt into foo.tgz
tar -c| --create -z| --gzip -f| --file=foo.tgz /bar              # Compress directory bar into foo.tgz
```
### unzip

```bash
unzip foo.zip          # Unzip foo.zip into current directory
gunzip foo.gz           # Unzip foo.gz into current directory and delete foo.gz
gunzip -k| --keep foo.gz # Unzip foo.gz into current directory
tar -x| --extract -z| --gzip -f| --file=foo.tar.gz # Un-compress foo.tar.gz into current directory
tar -x| --extract -f| --file=foo.tar              # Un-combine foo.tar into current directory
```

## Disk Usage

```bash
df                     # List disks, size, used and available space
df -h| --human-readable # -m: MB -k: KB 
du                     # List current directory, subdirectories and file sizes
du /foo/bar            # List specified directory, subdirectories and file sizes
du -h| --human-readable # List current directory, subdirectories and file sizes in a human readable format
du -d| --max-depth      # List current directory, subdirectories and file sizes within the max depth
du -d 0                # List current directory size
du -ha                 # List of files and directories
du -sh                 # total
du -sh *               # total for all directory
```

## Memory Usage

```bash
free                   # Show memory usage
free -h| --human        # Show human readable memory usage
free -h| --human --si   # Show human readable memory usage in power of 1000 instead of 1024
free -s| --seconds 5    # Show memory usage and update continuously every five seconds
```

## Mounting
```bash
mount
```



## Shutdown and Reboot

```bash
uptime                        # ???
shutdown                     # Shutdown in 1 minute
shutdown now "Cya later"     # Immediately shut down
shutdown +5 "Cya later"      # Shutdown in 5 minutes

shutdown --reboot            # Reboot in 1 minute
shutdown -r now "Cya later"  # Immediately reboot
shutdown -r +5 "Cya later"   # Reboot in 5 minutes

shutdown -c                  # Cancel a shutdown or reboot

reboot                       # Reboot now
reboot -f                    # Force a reboot
last reboot                  # last reboot
last syslog
```

## Identifying Processes

```bash
top                    # List all processes interactively
htop                   # List all processes interactively
ps all                 # List all processes
ps -f                  # full list of processes with PPID
ps -e                  # entire list
ps -a                  # all users
ps -u                  # display user process
ps -x                  # show processes not attached to a terminal
ps -l                  # shows long list
ps -H                  # shows as tree
pidof foo              # Return the PID of all foo processes


CTRL+C                 # Interupt a  process
CTRL+Z                 # Suspend a process running in the foreground  ===> jobs
bg                     # Resume a suspended process and run in the background
fg                     # Bring the last background process to the foreground
fg 1                   # Bring the background process with the PID to the foreground

sleep 30 &             # Sleep for 30 seconds and move the process into the background
jobs                   # List all background jobs (you can see jobs just in terminal that used CTRL+Z)
jobs -p                # List all background jobs with their PID
fg %1                   # 1 is job id 
# if you kill a process that is inide the jobs it will kill when comes to foreground 

lsof                   # List all open files and the process using them
lsof -itcp:4000        # Return the process listening on port 4000
nohup CMD 			      # runs cmd under init ps
```

## ps cols
```bash
UID                    # user ID
PID                    # process ID
PPID                   # parent process ID
C                      # CPU utilization of process 
STIME                  # process start time
TTY                    # terminal type 
STAT                   #?
TIME                   # CPU time taken by the process
CMD                    # The command that started this process
```
## Partition
```bash
fdisk -l               # list of partitions and drivers
```


## Process Priority

Process priorities go from -20 (highest) to 19 (lowest).

```bash
nice -n -20 foo        # Change process priority by name
renice 20 PID          # Change process priority by PID
ps -o ni PID           # Return the process priority of PID
```

## Killing Processes

```bash
CTRL+C                 # Kill a process running in the foreground
kill PID               # Shut down process by PID gracefully. Sends TERM signal.
kill -9 PID            # Force shut down of process by PID. Sends SIGKILL signal.
pkill foo              # Shut down process by name gracefully. Sends TERM signal.
pkill -9 foo           # force shut down process by name. Sends SIGKILL signal.
killall foo            # Kill all process with the specified name gracefully.
```

## Date & Time

```bash
date                   # Print the date and time
date +%s               # Print timestamp
date --iso-8601        # Print the ISO8601 date
date --iso-8601=ns     # Print the ISO8601 date and time
cal                    # calender ==> apt install ncal

time tree              # Time how long the tree command takes to execute
```

## Scheduled Tasks

```pre
   *      *         *         *           *
Minute, Hour, Day of month, Month, Day of the week
```

```bash
service cron status        # status disable or running
crontab -l                 # List cron tab
crontab -u root -l         # specific user
crontab -e                 # Edit cron tab in Vim
crontab /path/crontab      # Load cron tab from a file
crontab -l > /path/crontab # Save cron tab to a file

* * * * * foo              # Run foo every minute
*/15 * * * * foo           # Run foo every 15 minutes
0 * * * * foo              # Run foo every hour
15 6 * * * foo             # Run foo daily at 6:15 AM
44 4 * * 5 foo             # Run foo every Friday at 4:44 AM
0 0 1 * * foo              # Run foo at midnight on the first of the month
0 0 1 1 * foo              # Run foo at midnight on the first of the year

# every 30 seconds
* * * * * date>> /tmp/date.log
* * * * * sleep 30; date>> /tmp/date.log

at -l                      # List scheduled tasks
at -c 1                    # Show task with ID 1
at -r 1                    # Remove task with ID 1
at now + 2 minutes         # Create a task in Vim to execute in 2 minutes
at 12:34 PM next month     # Create a task in Vim to execute at 12:34 PM next month
at tomorrow                # Create a task in Vim to execute tomorrow
```

## HTTP Requests

```bash
curl https://example.com                               # Return response body
curl -i | --include https://example.com                  # Include status code and HTTP headers
curl -L | --location https://example.com                 # Follow redirects
curl -o | --remote-name foo.txt https://example.com      # Output to a text file
curl -H | --header "User-Agent: Foo" https://example.com # Add a HTTP header
curl -X | --request POST -H "Content-Type: application/json" -d| --data '{"foo":"bar"}' https://example.com # POST JSON
curl -X POST -H --data-urlencode foo="bar" http://example.com                           # POST URL Form Encoded

wget https://example.com/file.txt .                            # Download a file to the current directory
wget -O| --output-document foo.txt https://example.com/file.txt # Output to a file with the specified name
```




## Network Troubleshooting

```bash
ping example.com            # Send multiple ping requests using the ICMP protocol
ping -c 10 -i 5 example.com # Make 10 attempts, 5 seconds apart

ip addr                     # List IP addresses on the system
ip route show               # Show IP addresses to router

netstat -i| --interfaces     # List all network interfaces and in/out usage
netstat -l| --listening      # List all open ports

traceroute example.com      # List all servers the network traffic goes through

mtr -w| --report-wide example.com                                    # Continually list all servers the network traffic goes through
mtr -r| --report -w| --report-wide -c| --report-cycles 100 example.com # Output a report that lists network traffic 100 times

nmap 0.0.0.0                # Scan for the 1000 most common open ports on localhost
nmap 0.0.0.0 -p1-65535      # Scan for open ports on localhost between 1 and 65535
nmap 192.168.4.3            # Scan for the 1000 most common open ports on a remote IP address
nmap -sP 192.168.1.1/24     # Discover all machines on the network by ping'ing them
```

## DNS

```bash
host example.com            # Show the IPv4 and IPv6 addresses

dig example.com             # Show complete DNS information

cat /etc/resolv.conf        # resolv.conf lists nameservers
```

## Hardware

```bash
lsusb                  # List USB devices
lspci                  # List PCI hardware
lshw                   # List all hardware
lscpu                   # List all cpu
lsblk                   # List block devices
lsscit                   # List scsi/sata
```

## Kernel
```bash
lsmod                   # List of modules of kernel
uname -a                # show system kernel
```

## Linux Version
```bash
uname                  # always return linux
uname -a               # Linux + distro + version + date release + cpu architecture + os
head -n1 /etc/issue    # Show distri-bution (display a banner to SSH users before the login prompt)
hostname               # show hostname (/etc/hostname)
hostname -i            # show hostname with ip
sudo hostname something # change temporary hostname to something 
```
## encrypt
```bash
gpg -c FILE         # encrypt file
gpg FILE.gpg        # decrypt file
```


## Terminal Multiplexers

Start multiple terminal sessions. Active sessions persist reboots. `tmux` is more modern than `screen`.

```bash
tmux             # Start a new session (CTRL-b + d to detach)
tmux ls          # List all sessions
tmux attach -t 0 # Reattach to a session

screen           # Start a new session (CTRL-a + d to detach)
screen -ls       # List all sessions
screen -R 31166  # Reattach to a session

exit             # Exit a session
```

## Secure Shell Protocol (SSH)

```bash
ssh hostname                 # Connect to hostname using your current user name over the default SSH port 22
ssh -i foo.pem hostname      # Connect to hostname using the identity file
ssh user@hostname            # Connect to hostname using the user over the default SSH port 22
ssh user@hostname -p 8765    # Connect to hostname using the user over a custom port
ssh ssh://user@hostname:8765 # Connect to hostname using the user over a custom port
```

Set default user and port in `~/.ssh/config`, so you can just enter the name next time:

```bash
$ cat ~/.ssh/config
Host name
  User foo
  Hostname 127.0.0.1
  Port 8765
$ ssh name
```

## Secure Copy

```bash
scp foo.txt ubuntu@hostname:/home/ubuntu # Copy foo.txt into the specified remote directory
```

## Bash Profile

- bash - `.bashrc`
- zsh - `.zshrc`

```bash
# Always run ls after cd
function cd {
  builtin cd "$@" && ls
}

# Prompt user before overwriting any files
alias cp='cp --interactive'
alias mv='mv --interactive'
alias rm='rm --interactive'

# Always show disk usage in a human readable format
alias df='df -h'
alias du='du -h'
```

