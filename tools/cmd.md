## CMD


# mother
```bash
help   # list of all commands
help dir
```


## package manager
```bash
scoop install gsudo
choco install gsudo
winget install gerardog.gsudo
```

## file management
```bash
dir               # display files
tree              # tree
mk | mkdir my cat      # create two folders
mkdir "my cat"      # create one folder
rmdir | rm folder             # delete a folder
DEL | ERASE 1.txt # - Deletes files
notepad 1.txt
vim 1.txt          # if you have installed vim
copy con 1.txt     # edit a file in cmd ----> finish with C_Z
type 1.txt         # display a file in cmd
type nul > filename.txt # crate a new file in cmd
echo nul > filename.txt  #create and echo nul inside that
echo. > filename.txt  #create a new file and echo nothing
echo append text >> filename.txt  #append text inside a file

fc C:\Users\Martin\Desktop\1.txt C:\Users\Martin\Desktop\2.txt # file compare between two files
move  1.js folder              # Moves files from one folder to another
copy  1.js folder              # Moves files from one folder to another
PRINT               # Prints out the text file contents
ren | rename cat dog        # Renames a file or folder
explorer .\         # open in explorer

```


## redirects
```bash
command1 && command2        # run command2 if command1 runs successfully
command1 & command2          # run command2 regardless if command1 returns an error
command1 || command2          # run command2  if command1 fails
command1 | command2          # redirects output for input of command2
```

## system info
```bash
DATE                  # - Outputs or sets the current date
TIME                  # - Displays or sets the system time
driverquery           # Displays the current state and properties of the device driver
HOSTNAME              # Displays name of the computer
SYSTEMINFO            # Shows configuration information about your computer
VER                   # Allows you to view the Windows version
GPRESULT              # Displays current applied group policies (RSoP)
GPUPDATE              # Updates group policies
tasklist              # like task manager but more
taskkill -im chrome.exe  # kill with name
taskkill -pid 132       # kill with pid
```

## find
```bash
find  "word" 1.js
findstr    # like grep in pipeline
```

## command line
```bash
powershell
cmd
ubuntu                      # if you have installed linux subsystem
exit
color -a
cls
title NAME_YOU_WANT
tasklist | more           # more option
F7                        # popup history
doskey /history           # display history
date | clip               # output as a clipboard
```

## network
```bash
netstat
curl
IPCONFIG                 #  Shows information about network interfaces
ipconfig /release + ipconfig /renew  # create a new ip
ipconfig /flushdns        # refresh ip and dns
ping                     #  Sends ICMP requests to the target host, checks host availability
pathping                 # pro ping with router paths
TRACERT                  #  Finds the path for packets traveling over the network with ICMP 
NSLOOKUP  www.google.com               #  Finds IP address by resource name
route print                    #  Displays network route tables
ARP                      #  hows a table with IP addresses converted into physical addresses
NETSH                    #  Starts is a network settings control program
GETMAC                   #  Shows the MAC address of the network adapter
TFTP                     #  Starts TFTP client in console

```



## apps
```bash
explorer
assoc                   # format list 
start cmd
start vlc
start powershell
start chrome
start firefox
code .   # vscode
set pot="C:\Program Files\DAUM\PotPlayer\PotPlayerMini64.exe"
```
## encrypt
```bash
cipher /e 1.txt       #encrypt a file
cipher /d 1.txt       #dycrypt a file
cipher /w C:\         # delete drive c and unrecoverable 
```

## shutdown
```bash
shudown
shudown -a
shutdown -r       

```


## batch script
```bash
# .bat format
@echo off # do not display first echos
set var=1 # variable
echo %var% # show var
set /p var=Enter a number  # input
echo %var% # show var
if %var% ==3 (echo var is three babe) # if statement
else if %var% ==4 (echo var is 4)
else (echo not 3 and 4)
:functionName echo I am a function # define a function
Goto functionName   # declare a function
for /L %%A In (1,1,100) Do (echo %%A)       # loop
pause # stop script
```