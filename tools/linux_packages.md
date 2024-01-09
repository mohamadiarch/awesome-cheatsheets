# Linux Packages

## tmux
```bash
tmux          # start a session
exit          # kill a session
tmux ls        # list of sessions 
tmux kill-server   # kill all sessions
```


## screen
```bash
screen     # take me to screen terminal
ctrl_a + d # disconnect
screen -l  # list of screen
screen -r  # reconnect
screen -X -S [ session you want to kill ] quit
ctrl_a + c  # create a new window
ctrl_a + n/p   # next window / previous window
ctrl_a + |   # split vertically
ctrl_a + s   # split horizontally
ctrl_a + tab  # jump to next split tab
```

## pandoc
```bash
pandoc -s file.tex -o file.docx
```

## taskset
```bash
taskset -c 2 gimp         # run gimp just in core 2
taskset -c 0,1,2,3 gimp     # use core 0,1,2,3 for running gimp
taskset -c 1-7 steam      # run steam with 2nd core - 8th core
taskset -p PID            # this PID works with which cpus 
taskset -cp 3-5 PID            # use 4th-6th cpu for this PID 
```