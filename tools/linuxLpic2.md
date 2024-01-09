## LPIC 101


### Linux boot process
```bash
""""""""""""""""""""""""""BIOS or UEFI
power button ==> SMPS send electricity to all device ===>
cpu get electricity ===> cpu run programs inside ROM ====>
cpu run BIOS ===>BIOS is a firmware in motherboard ===>
BIOS runs in two stpes:
    1-POST(Power On Self-Test) ==> find all health devices like keyboard and use horn if they heve problem
    2-Bootstrap: select first bootable device
BIOS loals MBR(512 first byte in HARD: firt boot loader) from first bootable devicee ===>
""""""""""""""""""""""""""MBR
MBR call second boot loader (GRUB)
""""""""""""""""""""""""""GRUB or LILIO
GRUB loads in RAM ===> GRUB can boot multiple os(dual boot) ==> GRUB select defult os by loading its img ===> GRUB loads Kernel img and initrd img inside RAM ===> 
"""""""""""""""""""""""""" kernel
Kernel loads and unzip initrd file ===> Kernel uses iniitrd for loading partitions  then unmount it ===>
then Kernel uses root partition in read only mode ===>
"""""""""""""""""""""""""" init process
when kernel starts the first process (mother process =init or systemd with pid=1) ====>
init run script for environmnt, file system, path, time end etc ===> the texts you can see on the screen before seeing your desktop ===>
"""""""""""""""""""""""""" run level
init read a file and select a run level [0:6] ===> in that run level, runs specific process and scripts
```


### Hard Disk Format
```bash
Types of partitions:
    MBR = Master Boot Loader
    GPT = GUID Partition Table ===> more acess level

Types of Drivers:
    Primary ===> install os
    Logical ===> if breaks Primary
    Extended ===> collection of Logical drivers

Formats for Hard:
    NTFS
    FAT32
    exFat

" Partition is part of driver that saves data
```




MBR : 
+ older
+ Limitation 4 Primary driver
+ Limitation 2 Tra HARD 
+ Backup is difficult 
+ Information about partitions saves in the firstsection of Hard disk -
+ Use just BIOS for boot loader not UEFI
+ Support both 32bit and 64bit OS 
+ [if you have 3GB RAM or lower you can just install 32bit os]

GPT:
+ Limitation 128 Primary driver
+ Limitation 9.5 ZB
+ Information about partitions saves in first section and copy in various other sections so it can use them for Backup 
+ Use both BIOS and UEFI
+ Suitable for Backup
+ Suitable for debuging
+ Support just 64bit OS with no dependenceis
+ windows 7,8 need UEFI for support GPT
+ windows 8,10 32bit need UEFI for suppor GPT
+ windows 7 and vista in 32bit can not use GPT

------------
FAT32:
+ File Allocation Table 32
+ lots of FLASH USBs
+ older from Win95
+ Limitation for 4GB uniq files
+ Win 10 do not support FAT32 anymore
+ Best format for USBs bcz best compability

NTFS:
+ NT File System
+ defult format of windows
+ XP introduce NTFS

EXFAT:
+ EXtended File Allocation Table
+ intrduce from 2006 for USBs with no limitation of FAT32
+ has no complativity with all hardwares
+


-----


## apt
Whenever you call apt-get update the repositories contained in the sources.list get read, this tells apt-get from where to get packages lists. This list get downloaded and stored in /var/lib/apt/lists for posterior use. These are lists of all packages available from the repositories you selected. Even if you remove your sources.list, this list will be available for APT. That's why you should always do update whenever you add/remove/modify a repository, to keep these lists updated.


Actions of the apt command, such as installation and removal of packages, are logged in the /var/log/dpkg.



////////////////



/bin (and /sbin) were intended for programs that needed to be on a small / partition before the larger /usr, etc. partitions were mounted. These days, it mostly serves as a standard location for key programs like /bin/sh, although the original intent may still be relevant for e.g. installations on small embedded devices.

/sbin, as distinct from /bin, is for system management programs (not normally used by ordinary users) needed before /usr is mounted.

/usr/bin is for distribution-managed normal user programs.

There is a /usr/sbin with the same relationship to /usr/bin as /sbin has to /bin.

/usr/local/bin is for normal user programs not managed by the distribution package manager, e.g. locally compiled packages. You should not install them into /usr/bin because future distribution upgrades may modify or delete them without warning.

/usr/local/sbin, as you can probably guess at this point, is to /usr/local/bin as /usr/sbin to /usr/bin.