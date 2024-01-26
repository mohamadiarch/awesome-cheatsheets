
# Linux 

## Notation

```bash
bind -p
^c         # ^ means ctrl
\C          # means ctrl
\e          # means escape
sudo apt-get install screen     ## check please
```

## IMP
```bash
ctrl shift - ==> undo
alt + d ==> delete after cursor
alt + backspace ==> delete word by word
```

## shortkeys
```bash
Ctrl+C – Kill current process
Ctrl+D – Close Terminal
Ctrl+Z – Suspend. Use “fg process” to return
Ctrl+S – Suspend output to screen
Ctrl+Q – Resume output to screen
Tab – Completion for file/folder names

Command History
Ctrl+P or Up Arrow - Previous Command
Ctrl+N or Down Arrow - Next Command
Ctrl+R - Recall command matching search
Ctrl+O - Run the command you found with Ctrl+R
Ctrl+G - Leave history searching mode without running a command

!! - Repeat previous command
!-2 - Repeat 2th previous command
!:n – Repeat specific argument from previous command  ==> echo hi woman; man !:2;
!:n:m – Repeat range of arguments from previous command
!:n:$ - Repeat range of arguments from n to end from previous command
!* - Repeat All arguments from previous command
!word -Execute the most recent command starting with word (like !ls for ls -laASr)
Alt + . - Show Last argument from previous command (like -l in ls -l)
^abc­^­def -  Run previous command, replacing abc with def

Move Cursor
Ctrl+A or Home – Beginning of the Line
Ctrl+E or End – End of the Line
Ctrl+B or Left Arrow – Back one Character
Ctrl+F or Right Arrow – Forward one Character
Ctrl+Left Arrow or Alt+B – Back one Word
Ctrl+Right Arrow or Alt+F – Forward one Word
Ctrl+XX – Toggle between Beginning and End of Line
Ctrl+M - Enter

Deleting Text
Ctrl+L – Clear Screen
Ctrl+D or Delete – Delete character under the cursor
Ctrl+H or Backspace – Delete character before the cursor
Alt+D – Delete the Word after the cursor

Fix Typos
Alt+T or Esc+T - Swap current word with previous word (press between gaps)
Ctrl+T Swap the last two characters before the cursor with each other
Ctrl+_ (Ctrl+Shift+-)  - Undo your last key press
Ctrl+U – Clear all text from Cursor to Beginning of Line
Alt+R – Revert line

Capitalisation
Alt+C – Capitalise current Character
Alt+U – Capitalise current Word  from cursor
Alt+L – Lowercase current Word from cursor

Cut and Paste from Bash Clipboard
Ctrl+W - Cut the Word before the cursor
Ctrl+K - all text from Cursor to End of Line
Ctrl+U - Cut all text from Cursor to Beginning of Line
Ctrl+Y – Paste

Cut and Paste from System Clipboard
Ctrl+Alt+C – Copy highlighted text
Ctrl+Alt+V or Middle Click – Paste
```
### vim mode

```bash
set -o vi      # set +o vim for exit
```
### emacs mode

```bash
set -o emacs

```

## vim

```bash
:help index                        # list of all mappings
:map                                # list of all mappings inside .vimrc (verbose map)
ctrl + wv                          # open current buffer as new vertical split
Ctrl + wT                          # open current buffer as new tab
ctrl + u | ctrl + d                 # scroll up and down as page
```

## NANO

```bash

```


## LESS

```bash

```



