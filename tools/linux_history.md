
---
source: https://github.com/l0b0/tilde
---
## linux history




ack-grep --all --ignore-dir .jhw-cache --ignore-dir .sass-cache --ignore-dir log --ignore-dir public --ignore-dir tmp "pattern" . # search rails 
ack-grep "pattern" . # search 
acpi_listen # events power configuration 
alias ls 
align_image_stack -vl -a aligned ./*.jpg # graphics 
alsamixer # audio input output volume 
amixer --card 2 # list audio hardware device configuration 
amixer set 'Beep' 0% mute || amixer set 'PC Beep' 0% mute || amixer set 'PC Speaker' 0% mute # mute speaker 
aplay --list-devices # list audio hardware 
aplay --list-pcms # list audio output speaker 
aplay recording.wav # audio output 
appres XTerm # list x application resource database 
apropos . # all help man 
apropos bash # help man 
apropos --exact mv # help man 
arandr & # screen layout graphics hardware 
arch # hardware 
arecord --duration 5 --format dat recording.wav # record audio file 
arecord --format dat | aplay # test audio input capture output playback default microphone speakers 
arecord --list-devices # list audio input capture microphones 
ash -o noexec ~/dev/makeThin/makeThin.ash # verify syntax 
aticonfig --initial=check # graphics amd x configuration 
autoconf # compile 
autoreconf --install # compile 
avahi-browse-domains --terminate # network domains scan 
avahi-browse --terminate --all # network services scan local remote 
avahi-browse --terminate --ignore-local _workstation._tcp # network tcp workstations scan remote 
avconv -i %04d.jpg -vcodec libx264 -bf 0 -crf 12 -an -r 25 -s hd1080 timelapse2.mp4 # video convert 
avconv -i input.mov -codec copy -ss 15 output.mov # video cut 
avconv -i input.mov -codec:video libx264 -codec:audio copy -filter transpose=clock output.mov # video rotate 
awesome --check # configuration verify parse 
awk '{ print $22 }' /proc/1/stat # process start time jiffies since boot 
basename -- "$PWD" # current directory name 
bashdb example.sh # debug shell script 
bash --noprofile --norc -x # test trace shell 
bash -o noexec ~/.bash_history # verify shell script syntax 
bash -o xtrace # debug shell 
bc <<< '2+2' # calculator math 
bchunk image.bin image.cue image.iso 
bc --mathlib <<< 'e(1)' # calculator math e power 
bc <<< 'scale = 10; sqrt ( 2 )' # calculator math precision scale float decimal 
bg # background job 
bind -P | grep --fixed-strings ' can be found on ' | perl -pe 's/((?<!\\)(?:\\\\)*)\\C/\1Ctrl/g;s/((?<!\\)(?:\\\\)*)\\e/\1Esc,/g' # keyboard shortcuts 
bind -p | grep --invert-match --regexp '^$' --regexp '^#' --regexp 'self-insert$' | sed "s/\(.*\)/bind '\1'/" | tr --squeeze-repeats '\n' ';' # shortcuts code 
builtin # bash list 
bundle help # rails 
bundle init # rails 
bundle install # rails 
bundle package 
bundle update # rails 
bunzip2 file.bz2 # compression bzip 
cap deploy:check # rails 
cap deploy:login 
cap deploy:migrations # rails 
cap deploy # rails 
cap deploy:rollback # rails 
cap deploy:setup # rails 
capify . # rails 
cap # rails 
cat ~/contacts/*.vcf > ~/all.vcf # concatenate vcard 
cat /dev/zero > /tmp/ramdisk.XXXXXXXXXX/full.log # fill ramdisk partition file tmpfs 
cat /etc/papersize # print 
cat /etc/*release # os 
cat /proc/cpuinfo # hardware 
cat /proc/devices # hardware 
cat /proc/filesystems # hardware 
cat /proc/misc # hardware 
cat /proc/stat # hardware 
cat /proc/sys/dev/cdrom/info 
cat /proc/sys/kernel/pid_max # process 
cat /proc/vmstat # hardware 
cat /sys/class/hwmon/hwmon0/device/fan1_output # hardware macmini4,1 speed 
cd - # back 
cd -- "$(mktemp --directory)" # create temporary directory 
certutil # help 
checkbashisms ./*.sh 
chmod u+x example.sh # permission executable 
clamtk & # antivirus 
cmp --print-bytes "$(which arch)" "$(which uname)" # binary diff 
coffee -v # coffeescript 
comm -23 <(grep --no-filename ^FN: ~/contacts.vcf | sort --unique) <(grep --no-filename ^FN: ~/contacts/*.vcf | sort --unique) # compare vcard names 
comm -23 --nocheck-order <(alias -p) <(bash -lc 'alias -p') # list session aliases 
./configure --help | less # packaging 
./configure # packaging 
convert -density 150 -quality 100 input.pdf output.jpg # graphics extract image 
convert ./*.jpg output.pdf # graphics combine image 
convert ./name-*.gif name-%04d.png # format number graphics 
count . # filesystem 
cp --archive dir target # recursive owner permissions 
cp file{,.orig} # filesystem 
cppcheck foo.c # lint c code 
createdb --template template0 --username username dbname # postgresql 
cronlist 
cronlist --help 
cronlist --system 
cronlist --to '23:59:59' 
crontab -e # edit 
crontab -l # list 
csplit --prefix contact- --suffix-format %02d.vcf --elide-empty-files --quiet ~/contacts.vcf '/BEGIN:VCARD/' '{*}' # split vcard file 
csplit --prefix header- --suffix-format %02d.txt --elide-empty-files --quiet headers.txt '/----------------------------------------------------------/1' '{*}' # split file 
csvtool col 3 example.csv # csv column 
csvtool --help | less 
cucumber --dry-run # rails 
cucumber # rails 
cucumber --version # rails 
curl https://aur.archlinux.org/packages/tt/ttf-source-sans-pro/ttf-source-sans-pro.tar.gz | tar -zx 
curl --insecure --location http://xrl.us/perlbrewinstall | bash # development perl 
curl --version 
cut --delimiter ':' --fields 1 /etc/group | sort 
date --date="2001-09-09 03:46:40+02:00" +%s # convert timestamp 
date --date="6 months ago" # past time 
date --date="6 months" # future time 
date --date="Friday" # today future midnight 
date --date="Monday" # today future midnight 
date --date="now" # time 
date --date="Saturday" # today future midnight 
date --date="Sunday" # today future midnight 
date --date="Thursday" # today future midnight 
date --date="Tuesday" # today future midnight 
date --date="Wednesday" # today future midnight 
date --date="yesterday" # time 
date +%FT%T.%N # iso time 
date --rfc-3339=ns --date="2001-02-03T04:05:06.7 + 1 year 2 months 3 days 4 hours 5 minutes 6.7 seconds" # dst time iso 
date --rfc-3339=seconds --date="@1000000000" # convert timestamp 
date +%Y-%m-%dT%H:%M:%S # iso time 
dd if=/dev/cdrom of=cdrom.iso # rip cd 
dd if=/dev/null of=/file/to/truncate seek=1 bs=1024 # truncate file bytes 
dd if=/dev/urandom bs=1kB count=1 | ent # calculate entropy 
dd if=/dev/zero of="${sandbox}/zeros.bin" bs=1000 count=5 # create file size 
deactivate # virtualenv 
declare -a # arrays 
declare -f function_name # function definition 
declare -F # functions 
declare -p # color variables functions 
declare # variables functions 
deluge & # bittorrent gui 
~/dev/awmtt/awmtt start --config ~/.config/awesome/rc.lua # debug awesome configuration 
~/dev/awmtt/awmtt stop # debug awesome configuration 
~/dev/meta2jpeg/meta2jpeg.sh ./*.CR2 # copy metadata graphics image 
~/dev/minecraft-scripts/backup.sh # game directory 
~/dev/minecraft-scripts/backup.sh ~/.techniclauncher # game directory 
~/dev/minecraft-scripts/install-lwjgl.sh 
~/dev/minecraft-scripts/install-Minecraft.sh # game 
~/dev/minecraft-scripts/install-Minecraft.sh -o 1.4.6 # game old version 
~/dev/schemaspy2svg/schemaspy2svg.sh ~/db # database graphics convert svg 
~/dev/tilde/scripts/make-links.sh --verbose --diff meld ~/settings/.* ~ # filesystem symlink 
~/dev/vcard/format-TEL.sh ~/contacts/*.vcf # format telephone number vcard 
~/dev/vcard/sort-lines.sh ~/dev/vcard/sorts/Gmail.re ~/contacts/*.vcf # sort vcard files 
~/dev/vcard/split.sh ~/contacts/*.vcf # split vcard files 
~/dev/xterm-color-count/xterm-color-count.sh -v # xterm color 
~/dev/xterm-color-count/xterm-color-count.sh # xterm color 
df --human-readable . # filesystem current directory 
df --human-readable # filesystem list all 
! df --portability | awk '{print $5}' | grep --fixed-strings --line-regexp --quiet '100%' # disk space available 
df --portability . | tail --lines 1 | cut --delimiter ' ' --fields 1 | grep --fixed-strings --invert-match --line-regexp --regexp '-' # directory partition 
difff --help 
diff --unified file{.orig,} # files 
diff --unified <(hexdump -C /bin/uname) <(hexdump -C /usr/bin/arch) 
diff --unified <(sudo sh -c env | sort) <(sudo -i sh -c env | sort) # environment variables root login shell 
dig example.org # dns lookup internet network 
dig example.org mx # dns email lookup internet network 
dirname -- "$PWD" # parent directory 
disown # job 
dmesg | less # debug os startup 
dos2unix example.txt # convert newline 
dot -O -Tsvg ./*.dot # graphics 
dot -Tsvg graph.dot # graphics 
dotty graph.dot # graphics 
dot -V 
dropdb --username username dbname # postgresql 
du --si --summarize . # disk size 
echo 0 61 62 63 | xxd -revert # hex dump convert string character byte 
echo $BASHPID # shell subshell pid 
echo "body" > ~/.events/summary # notify 
echo "${COLUMNS}x${LINES}" # terminal size dimensions 
(echo 'ctrl_interface=/var/run/wpa_supplicant' && wpa_passphrase ssid passphrase) | sudo tee /etc/wpa_supplicant.conf # configuration wireless network wpa supplicant 
echo example | xclip # clipboard mouse copy 
echo example | xclip -selection clipboard # clipboard keyboard copy 
echo $? # exit code 
echo 'LC_PAPER="en_GB.UTF-8"' | sudo tee --append /etc/environment # print 
echo "$OSTYPE" 
echo "${paths[0]}" # array 
echo "${paths[@]: -1}" # array 
echo "${paths[@]}" # array 
echo "$PATH" | tr ':' $'\n' # user path 
echo "${PIPESTATUS[@]}" | tr --squeeze-repeats ' ' + | bc # array sum 
echo "$PROMPT_COMMAND" # shell 
echo "$REPLY" # read 
echo return _VERSION | awesome-client # lua version 
echo $$ # shell pid 
echo "$TERM" # shell 
echo "$WINEPREFIX" 
eject # hardware cd dvd 
enable -a # builtins 
enable -n # disabled builtins 
env - HOME="$HOME" LOGNAME="$USER" PATH="/usr/bin:/bin" SHELL="$(which sh)" command # emulate cron command 
env --ignore-environment bash -c 'printf "%s\n" "${?+?=$?}" "${#+#=$#}" "${*+*=$*}" "${@+@=$@}" "${-+-=$-}" "${!+!=$!}" "${_+_=$_}" "${$+$=$$}"; env' 
env # variable 
eval "$(resize -s 24 80)" # terminal 
eval "$(ssh-agent)" && ssh-add 
eval "$traps" # signal 
evince /usr/share/doc/gnu-standards/maintain.pdf.gz # help maintenance 
evince /usr/share/doc/gnu-standards/standards.pdf.gz # help 
evince /usr/share/doc/msort/msort.pdf.gz & # help 
evince /usr/share/doc/quilt/quilt.pdf.gz # help 
ex -c '1' -c '?^[[:space:]]*[^[:space:]#]?' -c $'a\n# New comment' -c 'wq' ~/.bashrc # insert after last match 
exec "$SHELL" # replace 
exit 
exiv2 print IMG_1234.exv # metadata 
expand --tabs=4 example.txt # convert tab space 
export DISPLAY=:0.0 # remote x display 
facter # hardware os 
facter --help 
facter id # user 
fc-cache # refresh fonts 
fc # edit command history 
fc-list | sort # list fonts 
fc -l # list commands history 
fc -s # execute last command history 
feh --auto-zoom --scale-down --recursive . # images viewer resize 
feh --fullscreen --hide-pointer ./* # images viewer 
ffmpeg -i %04d.jpg -vcodec libx264 -bf 0 -crf 12 -vpre medium -an -r 25 -s hd1080 timelapse.mp4 # video convert 
ffmpeg -i %04d.jpg -vcodec libx264 -bf 0 -crf 12 -vpre medium -an -r 25 -s hd1080 -vf "transpose=2" timelapse.mp4 # video convert rotate 
fg && command # append command continue 
fg # foreground job 
fgit gc -- ~/*/.git/.. ~/.*/.git/.. ~/dev/*/.git/.. /media/*/*/.git/.. /run/media/"$USER"/*/*/.git/.. 
fgit --help 
fgit pull -- ~/*/.git/.. ~/.*/.git/.. ~/dev/*/.git/.. /media/*/*/.git/.. /run/media/"$USER"/*/*/.git/.. 
fgit push -- ~/*/.git/.. ~/.*/.git/.. ~/dev/*/.git/.. 
fgit status -- ~/*/.git/.. ~/.*/.git/.. ~/dev/*/.git/.. /media/*/*/.git/.. /run/media/"$USER"/*/*/.git/.. 
file README.markdown 
find . -empty 
find . -empty -delete # remove files 
find . -exec printf '%s\0' {} + | while read -r -d ''; do printf %q "$REPLY"; printf '\n'; done 
find . -group 1000 -exec chgrp "$(id --group)" {} + # update files permissions 
find -L . -type l # broken symlinks 
find . -mindepth 1 -exec printf '%s\0' {} + | shuf --head-count 10 --zero-terminated # random shuffle files 
find . -mindepth 1 -exec printf x \; | wc -c # count files posix safe 
find . -name '*.marks' -delete # remove jedit temp files 
find . -path ./.git -prune -o \( -type f -exec grep --files-with-matches $'\t' {} + \) # exclude vcs directories tab files 
find /proc -regex '/proc/[0-9].*' -prune -o -print # not process number 
find . -regex '.*\.\(orig$\|\(BACKUP\|BASE\|LOCAL\|REMOTE\)\..*\)' -delete # remove git rebase temp files 
find . -type f -executable # files 
find . -type f -name '*.*' | sed -e 's/.*\.//' | sort | uniq --count | sort --general-numeric-sort # file extensions count 
find -version 
firefox -no-remote -P secondary & 
firefox -profilemanager & # config 
firefox -safe-mode & 
firefox /tmp/xterm-screenshot.*.html 
firefox /usr/share/doc/c-cpp-reference/html/C/cref.html # help c dev 
firefox /usr/share/doc/c-cpp-reference/html/CPLUSPLUS/cref.html # help c++ cpp dev 
firefox /usr/share/doc/debian-policy/policy.html/index.html # packaging linux dev 
firefox /usr/share/doc/developers-reference/index.html # packaging linux dev 
firefox /usr/share/doc/git-doc/index.html # dev help 
firefox /usr/share/doc/ipython/html/index.html # dev help 
firefox /usr/share/doc/maint-guide/html/index.en.html # packaging linux dev help 
firefox /usr/share/doc/nethack-spoilers/gazetteer/index.html # game 
firefox /usr/share/doc/ntp-doc/html/ntpq.html # help 
firefox /usr/share/doc/python-doc/html/index.html # dev help 
firefox /usr/share/doc/python-matplotlib-doc/html/index.html # dev help 
firefox /usr/share/doc/python/python-policy.html/index.html # debian dev help 
firefox /usr/share/doc/w3-recs/html/www.w3.org/TR/2003/REC-SVG11-20030114/index.html # help reference svg 2d graphics 
fold --width 1 <<< foo # split characters lines 
for path in ./*.jpg; do mv --verbose "$path" "$(printf "%04d" "$index").jpg"; let index+=1; done; unset index 
for path in ~/.minecraft/saves/*; do overviewer.py --rendermodes=smooth-lighting,smooth-night,spawn "$path" "$path"/map; done 
for path in ./*.sass; do sass-convert "$path" "${path%.*}.scss"; done 
for path in ./*.zip; do unzip "$file"; done # all 
fortune 
for vcard in ./*.vcf; do msort --bp 'BEGIN:VCARD.*?END:VCARD\r\n\r\n' --sp '^N:(.*)$' < "$vcard" > "$vcard"2; mv "$vcard"2 "$vcard"; done 
free --human # memory 
fromdos -- file # convert newline 
fuseiso -p file.bin "/media/mountpoint" # mount 
fusermount -u "/media/mountpoint" # unmount 
gcc --version 
gcc -Wall -o a.out foo.c # compile 
gdb program # debug 
gem install bundler 
gem list --local 
gem server 
gem uninstall foo # remove 
getconf ARG_MAX # arguments 
getconf -a # system configuration 
getent ahosts example.org # dns hosts internet ipv4 decimal 
getent hosts example.org # dns hosts internet ipv6 hex 
gethostip -d example.org # dns hosts internet ipv4 decimal 
git 
git add . 
git add .gitignore 
git add --interactive 
git add LICENSE 
git add Makefile 
git add --patch 
git add README.markdown 
git add tools.mk 
git bisect bad 
git bisect good 
git bisect reset 
git bisect run ./bisect.sh 
git bisect start HEAD HEAD~10 
git blame 1234abcd filename # revision 
git blame filename 
git branch 
git branch --all # list 
git branch --delete topic # local 
git branch --remotes 
git branch --set-upstream master origin/master # track 
git branch --track topic master 
git checkout -b topic remotes/origin/topic # branch change create 
git checkout master # branch change 
git checkout . # revert 
git cherry-pick HEAD@{5} 
git cherry-pick master:HEAD 
git clean --dry-run -d # directories 
git clean --dry-run -dx # directories .gitignore 
git clone git://libdivecomputer.git.sourceforge.net/gitroot/libdivecomputer/libdivecomputer 
git clone --recurse-submodules https://github.com/l0b0/cronlist.deb ~/dev/cronlist-0.1 && cd ~/dev/cronlist-0.1 && git remote add upstream git://github.com/l0b0/cronlist.git && git fetch upstream && git branch upstream && wget --output-document ~/dev/cronlist_0.1.orig.tar.gz https://github.com/l0b0/cronlist/tarball/v0.1 && git-import-orig --pristine-tar ~/dev/cronlist_0.1.orig.tar.gz 
git clone --recurse-submodules https://github.com/l0b0/mkgithub.git 
git commit 
git commit --all --message "Example" 
git config diff.minimal 
git config diff.minimal false 
git config diff.minimal invalid 
git config diff.minimal true 
git config --global github.user l0b0 
git config --global mergetool.prompt false 
git config --list 
GIT_CURL_VERBOSE=1 git pull # debug 
git diff 
git diff --cached # stage 
git diff --color-words 
git diff | diff-ignore-moved-lines 
git diff --exit-code # check 
git diff 'HEAD@{2013.04.30 08:00}' # date 
git diff HEAD^ -- README.markdown # last commit 
git diff --ignore-all-space 
git diff --ignore-all-space --no-color | git apply --cached 
git diff --ignore-space-change 
git diff master origin/master 
git diff origin/master..HEAD # remote 
git diff --raw 
git diff --staged 
[[ "$(git diff --staged | grep --count ^-)" -eq "$(git diff --staged | grep --count ^+)" ]] # verify sort 
git diff --staged --ignore-space-at-eol 
git diff --staged --stat 
git difftool old new # gui 
git diff --word-diff 
git fetch 
git fetch && git merge FETCH_HEAD # pull 
git format-patch --find-renames HEAD^ 
git gc # garbage collect 
git grep -I --name-only --null -e '' | xargs --null sed --in-place 's/[ \t]\+\(\r\?\)$/\1/;$a\' -- # git whitespace eol eof 
git gui & 
git help add 
git help bisect 
git help blame 
git help branch 
git help checkout 
git help cherry-pick 
git help clean 
git help clone 
git help commit 
git help config 
git help diff 
git help difftool 
git help fetch 
git help format-patch 
git help gc # garbage collection 
git help grep 
git help gui 
git help help 
git help ignore 
git help init 
git help instaweb 
git help log 
git help ls-files 
git help ls-tree 
git help merge 
git help mergetool 
git help mv 
git help pull 
git help push 
git help rebase 
git help reflog 
git help remote 
git help request-pull 
git help reset 
git help revert 
git help show 
git help stash 
git help status 
git help submodule 
git help tag 
git init 
git instaweb start 
git instaweb stop 
gitk --all . & # gui 
git log 
git log --after '2012-01-20 17:06' --before '2012-04-03 16:15' # date range 
git log Makefile 
git log --oneline --decorate 
git log origin/master..HEAD # remote 
git log --patch-with-stat 
git log --stat 
git ls-files '*.py' # list files 
git ls-tree --long HEAD ./* | awk '{print $4 " " $5}' # file size commit 
git merge --abort # cancel revert 
git merge origin/master 
git mergetool & 
git merge topic # local branch 
git mv README{,.markdown} 
git pull 
git pull origin master 
git push 
git push --force 
git push origin :dead-branch # delete remote branch 
git push origin :refs/tags/name # delete remote 
git push --set-upstream origin master 
git push --tags 
git rebase --abort 
git rebase --continue 
git rebase --interactive HEAD~20 
git rebase master 
git rebase origin/master # avoid empty merge commit 
git reflog 
git reflog show --patch-with-stat 
git remote add -f origin ssh://user@example.org/home/user/repo 
git remote --verbose # list 
git reset --soft HEAD~1 # commit undo 
git reset v0.1 
git revert 123abc # commit undo 
git show commit:./path > path.old 
git stash drop stash@{0} # delete 
git stash && git merge origin/master && git stash pop 
git stash && git pull && git stash pop 
git stash && git rebase --interactive HEAD~20 
git stash list --date=local 
git stash list --patch # diff 
git stash --patch # diff create 
git stash pop 
git stash pop stash@{1} 
git stash save --keep-index "message" 
git stash save "message" 
git stash save --patch "message" # diff create 
git stash show 
git stash show --patch # diff 
git stash show --patch stash@{1} # diff 
gitstats ~/dev/tilde ~/gitstats && x-www-browser ~/gitstats/index.html # statistics history repo 
git status 
git submodule add --force git://github.com/l0b0/make-includes.git 
git submodule add --force git://github.com/l0b0/shell-includes.git 
git submodule update --init 
git tag --delete name # local 
git tag v0.1 
git --version 
glabels & # graphics 
glc-capture --out recording.glc minecraft 
glc-play recording.glc 
glc-play recording.glc -a 1 -o recording.wav # audio 
glc-play recording.glc -y 1 -o - | mencoder -demuxer y4m - -ovc lavc -lavcopts vcodec=mpeg4:vbitrate=3000 -audiofile recording.wav -oac mp3lame -o recording.avi # video encoding mp4 mpeg4 
glxgears # 3d graphics benchmark 
glxinfo 
gpg --allow-secret-key-import --import ~/secring.gpg 
gpg --import ~/pubring.gpg 
gpg --keyserver keys.gnupg.net --recv-keys 55D0C732 # import pgp signature 
gpg --verify ./*.sig # pgp signature 
gphoto2 --auto-detect # camera hardware 
gphoto2 --list-files # camera list photo 
gphoto2 --summary # camera hardware 
grep '\(\b\|^\)command\b.* .*help' ~/.bash_history # search 
grep --files-with-matches --null --regexp "pattern1" ./* | xargs -0 grep --files-with-matches --regexp "pattern2" # search and patterns 
grep --files-with-matches --null --regexp "pattern" ./* 2>/dev/null | tr --complement --delete '\000' | wc --chars # count occurrences pattern 
grep --fixed-strings --recursive --exclude-dir .git --regexp 'foo' . # search literal source 
grep --invert-match --file ~/dev/vcard/sorts/Gmail.re < ~/contacts.vcf | grep --invert-match --regexp '^ ' 
(grep --invert-match '^nameserver' /etc/resolv.conf; echo nameserver 208.67.222.222; echo nameserver 208.67.220.220) | sudo tee /etc/resolv.conf # dns configuration 
grep --recursive --no-filename --only-matching 'foo' . | wc --lines # sum count search 
grep --regexp ^ --regexp "^$USER:" /etc/passwd # context highlight 
grep ":$USER\$" /etc/group 
grep "^$USER:" /etc/passwd # password 
grep --version 
grive --auth # authenticate google drive 
grive # upload download sync files google drive 
groups 
groups nobody 
groups "$USER" 
gs -q -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sOutputFile=unencrypted.pdf -c .setpdfwrite -f encrypted.pdf # pdf remove password 
gunzip example.gz 
gzip example.txt # compress 
hash # list program recent 
help alias 
help bg 
help bind 
help builtin 
help command 
help continue 
help declare 
help disown 
help echo 
help enable 
help exit 
help fc 
help fg 
help help 
help history 
help jobs 
help kill 
help # list all 
help local 
help printf 
help [r]ead # read 
help [s]et # set 
help shift 
help shopt 
help . # source 
help test 
help [t]ime # time 
help trap # signal 
help [t]ype 
help typeset 
help ulimit 
help umask 
help unset 
help until 
help wait 
history | less 
host example.org # dns lookup internet network ipv4 ipv6 
hostname # internet network 
hostname --ip-address # internet network address dns 
hostname --short # internet network 
hp-setup # printer 
hp-wificonfig # printer 
htop # monitor processes system 
hugin & # panorama 2d photo stitch 
iconv --from-code=utf-8 --to-code=iso-8859-1 utf8.txt > latin1.txt # convert encoding 
id --group 
id # group user 
id --user 
id "$USER" 
if [[ -r /proc/sys/kernel/ns_last_pid ]]; then while true; do while read; do if [[ "$REPLY" != "$old" ]]; then printf '%(%s)T %d\n' -1 "$REPLY"; old="$REPLY"; fi; done < /proc/sys/kernel/ns_last_pid; read -t 1 || true; done; fi # processes pids log 
IFS=':' read -a paths <<< "$PATH" # tokenize array 
imapfilter 
indent ./*.c 
indentect --help 
indentect --verbose < "$(which indentect)" 
indentect < "$(which indentect)" 
infocmp -1 # list terminal 
info --raw-escapes --subnodes autoconf | less --raw-control-chars # help 
info --raw-escapes --subnodes automake | less --raw-control-chars # help 
info --raw-escapes --subnodes date | less --raw-control-chars # help 
info --raw-escapes --subnodes dd | less --raw-control-chars # help 
info --raw-escapes --subnodes find | less --raw-control-chars # help 
info --raw-escapes --subnodes ls | less --raw-control-chars # help 
info --raw-escapes --subnodes mktemp | less --raw-control-chars # help examples temporary files 
info --raw-escapes --subnodes sed | less --raw-control-chars # help 
inkscape & # editor svg 
iostat 
ip addr show dev eth0 # ipv4 ipv6 device address 
ip addr show # ipv4 ipv6 network address 
ipcalc 0.0.0.0/0 # network 
ipcalc 192.168.0.1/24 # network 
ip link show down # network 
ip link show up # network 
ip -oneline -family inet addr show dev eth0 # ipv4 address 
ip route show dev eth0 # network 
ipython 
irb # interactive ruby shell 
iwconfig # wireless network configuration 
java -jar ~/schemaSpy.jar -dp /usr/share/java/mysql.jar -hq -t mysql -host localhost:3306 -db database -u user -p password -o ~/db && x-www-browser file://"$HOME"/db/index.html # mysql db visualization 
java -jar ~/schemaSpy.jar -dp /usr/share/java/postgresql.jar -hq -t pgsql -host localhost:5432 -db database -s public -u user -p password -o ~/db && x-www-browser file://"$HOME"/db/index.html # postgresql db visualization 
java -Xmx1024M -Xms512M -classpath ~/.minecraft/minecraft.jar net.minecraft.LauncherFrame 
jedit -reuseview & # dev editor 
jhead -da2010:11:12/13:14:15-2005:01:01 ./*.jpg # adjust date time image 
jobs -l # list all background 
journalctl --since=today --output=short-iso # systemd service log 
json_xs < example.json # prettify json 
json_xs -t null < example.json # verify json format 
kdesu etherape & # network traffic visualization 
kdesu java -jar jdivelog-installer-*.jar & 
kdesu nm-connection-editor & # network configuration 
kdesu wifi-radar & 
keepassx & 
kill -0 "$!" # check background process pid 
killall process 
kill -INT $$ # signal 
kill -l # list signals 
komodo & 
kvm -boot d -m 512 -cdrom archlinux-*.iso # vm 
kvm -hda /tmp/my.img -cdrom boot.iso -boot d # vm 
l 
l ~ 
la 
la ~ 
lastlog # login users 
ldconfig --print-cache # list all libraries 
ldd "$(which bash)" 
less /etc/issue 
less /etc/passwd # password 
less Makefile 
less /proc/bus/input/devices 
less --RAW-CONTROL-CHARS filename # color 
less --raw-control-chars typescript 
less /sys/class/dmi/id/product_name 
less /sys/class/dmi/id/sys_vendor 
less /usr/share/doc/nethack-common/Guidebook.txt.gz # help 
less /var/log/auth.log 
less /var/log/dmesg 
less /var/log/kern.log 
less /var/log/messages 
less /var/log/syslog 
less /var/log/Xorg.0.log 
libreoffice & 
/lib/udev/findkeyboards 
livestreamer http://www.twitch.tv/foo best & # video web 
ll 
ln --symbolic -- target source 
locale 
locale --all-locales 
localectl list-keymaps # keyboard layout list 
localectl list-x11-keymap-layouts # keyboard layout list 
localectl list-x11-keymap-models # keyboard list 
localectl list-x11-keymap-variants us # keyboard list 
locate file 
lpstat -d # default printer cups 
lpstat -v # list all printers cups 
lsblk # list block device disk 
lsb_release --all # linux version distro 
lscpu | grep '^CPU op-mode' # detect cpu bit mode 
lscpu # hardware architecture processor 
ls --directory /proc/[^0-9]* # metadata 
lshw 
ls -l --all # list 
ls -l --block-size 1 # list files size bytes 
ls -l --directory ./*/ # list directories 
lslocks # list file locks 
ls -l --reverse # list 
ls -lt /var/log/ # sort time list 
lsmod # kernel modules 
lsof +c 0 | grep process-name | wc --lines # count files 
lsof -i :22 # internet port network 
lsof -i tcp # internet network 
lsof # list open files 
lsof -p $$ # files process 
lspci | grep --ignore-case audio 
lspci # list pci hardware 
lsusb | grep --ignore-case cam 
lsusb # list usb hardware 
lyx file.lyx 
m4 --version # compile dev 
make 2>&1 | tee > make_compile.out~ # compile dev 
make clean # dev 
make # compile dev 
make configure # dev 
 make --directory ~/dev/tilde clean 
make && echo finished > ~/.events/compilation || echo failed > ~/.events/compilation 
make explain 2>&1 | grep MAKE # dev 
make explain-MAKE # dev 
make install # dev 
make METHOD=git python-pep8 
makepkg --syncdeps # package build tarball 
make python-lint 
make python-pep8 
make python-pychecker 
make python-pyflakes 
make python-pylint 
make release # dev 
make --silent python-pep8 | cut --delimiter=: --fields=4- | grep --invert-match '^$' | sort | uniq --count | sort --numeric-sort 
make test 2>&1 | tee > make_test.out~ # dev 
make test # dev 
make variables # dev 
make variable-SHELL # dev 
man 1p mv # posix help 
man 1p sort # posix help 
man 1p xargs # posix help 
man 2 open # help 
man 3 exit # help 
man 3 printf # help format %d %f %s 
man 5 crontab # help 
man 5 passwd # help password 
man 7 glob # help 
man ack-grep # help 
man acpid # help 
man acpi_listen # help 
man addgroup # help 
man adduser # help 
man align_image_stack # help 
man alsamixer # help 
man amixer # help 
man aplay # help 
man appres # help 
man apropos # help 
man arandr # help 
man arch # help 
man arecord # help 
man ascii # help 
man ash # help 
man asn1parse # help 
man avahi-browse # help 
man avahi-daemon # help 
man avconv # help 
man awk # help 
man basename # help 
man bashdb # help 
man bash # help 
man bc # help 
man blkid # help 
man builtins # help bash 
man bunzip2 # help 
man cal # help 
man charsets # help 
man checkbashisms # help 
man chfn # help 
man chgrp # help 
man chmod # help 
man chown # help 
man chroot # help 
man clamtk # help 
man cloc # help 
man cmp # help 
man comm # help 
man convert # help 
man cp # help 
man cppcheck # help 
man createdb # help postgresql 
man createuser # help 
man crond # help 
man crontab # help 
man csplit # help 
man curl # help 
man cut # help 
man debhelper # help 
man delgroup # help 
man deluge # help 
man deluser # help 
man df # help 
man dhclient # help 
man dh_make # help 
man diff # help 
man dig # help 
man dirname # help 
man dmidecode # help 
man dos2unix # help 
man dot # help 
man dotty # help 
man download-mibs # help 
man dropdb # help postgresql 
man dropuser # help 
man dsa # help 
man du # help 
man eject # help 
man ent # help 
man env # help 
man errno # help 
man etherape # help 
man exiv2 # help 
man expand # help 
man expect # help 
man extundelete # help 
man fakeroot # help 
man fc-cache # help 
man fc-list # help 
man fdisk # help 
man feh # help 
man ffmpeg # help 
man file # help 
man find # help 
man firefox # help 
man fmt # help 
man fold # help 
man fortune # help 
man free # help 
man fuseiso # help 
man fusermount # help 
man gcc # help 
man gdb # help 
man genrsa # help 
man getconf # help 
man getent # help 
man gethostip # help 
man getopt # help 
man gfortran # help 
man git # help 
man gitk # help 
man gitstats # help 
man glabels # help 
man gnome-keyring-daemon # help 
man gpasswd # help 
man gpg # help 
man gphoto2 # help 
man graphviz # help 
man grep # help 
man grive # help 
man groups # help 
man grub-mkconfig # help 
man gs # help 
man gunzip # help 
man gvfs # help 
man hash # help 
man head # help 
man <(help2man help2man) # help 
man hexdump # help 
man hier # help 
man history # help 
man host # help 
man hostname # help 
man hosts # help 
man htop # help 
man hugin # help 
man id # help 
man ifdown # help 
man iftop # help 
man ifup # help 
man imake # help 
man imapfilter_config # help 
man imapfilter # help 
man indent # help 
man infocmp # help 
man initdb # help postgresql server database 
man inkscape # help 
man inotify # help 
man inotifywait # help 
man install # help 
man interfaces # help 
man ionice # help 
man iostat # help 
man iotop # help 
man ipcalc # help 
man ip # help 
man iptables # help 
man iwconfig # help 
man java # help 
man jedit # help 
man jhead # help 
man join # help 
man journalctl # help 
man json_pp # help 
man json_xs # help 
man kdesu # help 
man keepassx # help 
man keytool # help 
man kill # help 
man kvm # help 
man lastlog # help 
man ldconfig # help 
man ldd # help 
man ld # help 
man less # help 
man libreoffice # help 
man lighttpd # help 
man line # help 
man lintian # help 
man ln # help 
man localectl # help 
man locate # help 
man logger # help 
man lpadmin # help 
man lpstat # help 
man lsblk # help 
man lsb_release # help 
man lscpu # help 
man lslocks # help 
man lsmod # help 
man lsof # help 
man lspci # help 
man lsusb # help 
man lynx # help 
man make # help 
man makepkg # help 
man man # help 
man markdown # help 
man md5sum # help 
man mencoder # help 
man mkdir # help 
man mkfifo # help 
man mktemp # help 
man modinfo # help 
man mount # help 
man mp3fs # help 
man mutt # help 
man mv # help 
man nautilus # help 
man ncal # help 
man nc # help 
man nethogs # help 
man netstat # help 
man NetworkManager # help 
man nfs # help 
man nice # help 
man nl # help 
man nmap # help 
man nm-applet # help 
man nmcli # help 
man nm # help 
man node # help 
man notify-send # help 
man nslookup # help 
man ntpdate # help 
man ntpd # help 
man ntpq # help 
man objdump # help 
man od # help 
man openssl # help 
man pacman # help 
man paperconfig # help 
man passwd # help 
man paste # help 
man patch # help 
man pbuilder # help 
man pdebuild # help 
man pdfimages # help 
man pdfinfo # help 
man pdftk # help 
man pep8 # help 
man perldoc # help 
man perl # help 
man perlrun # help 
man pg_dumpall # help postgresql backup 
man pg_dump # help postgresql backup 
man pgrep # help 
man php # help 
man pidgin # help 
man pidof # help 
man ping # help 
man pkcs12 # help 
man pkcs8 # help 
man pngcrush # help 
man pod2man # help 
man postgres # help postgresql server 
man powertop # help 
man ppc386 # help 
man proc # help 
man ps # help 
man psql # help 
man psql # help postgresql 
man pstree # help 
man pts # help 
man puppet # help 
man python # help 
man qemu # help 
man quilt # help 
man rawtherapee # help 
man readelf # help 
man readlink # help 
man reboot # help 
man recordmydesktop # help 
man rename # help 
man req # help 
man reset # help 
man resize # help 
man rm # help 
man route # help 
man rrdcreate # help 
man rrddump # help 
man rrdgraph # help 
man rrdinfo # help 
man rrdlast # help 
man rrdtool # help 
man rrdupdate # help 
man rsa # help 
man rsync # help 
man ruby # help 
man runlevel # help 
man sane-find-scanner # help 
man scanimage # help 
man scp # help 
man screen # help 
man script # help 
man scrot # help 
man seq # help 
man service # help 
man setkeycodes # help 
man setxkbmap # help 
man sha1sum # help 
man sha512sum # help 
man sh # help 
man showkey # help 
man shred # help 
man shuf # help 
man shunit2 # help 
man shutdown # help 
man signal # help 
man simple-scan # help 
man sipcalc # help 
man sleep # help 
man sloccount # help 
man snmpd # help 
man snmpget # help 
man snmptranslate # help 
man snmpwalk # help 
man sort # help 
man speaker-test # help 
man splint # help 
man ssh-agent # help 
man ssh_config # help 
man ssh-copy-id # help 
man sshd # help 
man sshfs # help 
man ssh # help 
man ssh-keygen # help 
man stat # help 
man stdlib.h # help dev c header 
man stellarium # help 
man strace # help 
man strfile # help 
man strftime # help format string date 
man stty # help 
man sudoers # help 
man sudo # help 
man su # help 
man sweethome3d # help 
man synclient # help 
man syndaemon # help 
man sysctl # help 
man system-config-printer # help 
man systemctl # help 
man systemd-analyze # help 
man tac # help 
man tail # help 
man tar # help 
man tcpdump # help 
man tee # help 
man tig # help 
man timedatectl # help 
man time # help 
man timeout # help 
man tkmib # help 
man tofrodos # help 
man top # help 
man touch # help 
man tput # help 
man traceroute # help 
man trash # help 
man tr # help 
man tty # help 
man udevadm # help 
man umask # help 
man umount # help 
man uname # help 
man unetbootin # help 
man unexpand # help 
man unicode # help 
man uniname # help 
man uniq # help 
man unix2dos # help 
man unzip # help 
man updatedb # help 
man uptime # help 
man urandom # help 
man usermod # help 
man utf8 # help 
man valgrind # help 
man vim # help 
man vipw # help 
man virtualbox # help 
man visudo # help 
man vncpasswd # help 
man vncserver # help 
man vncviewer # help 
man watch # help 
man wavemon # help 
man wc # help 
man wdiff # help 
man wget # help 
man whatis # help 
man w # help 
man which # help 
man who # help 
man whois # help 
man wifi-radar # help 
man wireshark-filter # help 
man wireshark # help 
man wnpp-alert # help 
man wpa_passphrase # help 
man wpa_supplicant.conf # help 
man wpa_supplicant # help 
man x509 # help 
man xargs # help 
man xautolock # help 
man xclip # help 
man xdg-desktop-menu # help 
man xdotool # help 
man xev # help 
man xinput # help 
man xmkmf # help 
man xmllint # help 
man xmodmap # help 
man Xorg # help 
man xprop # help 
man xrandr # help 
man xrdb # help 
man xscreensaver-command # help 
man xscreensaver-demo # help 
man xscreensaver # help 
man xsltproc # help 
man xterm # help 
man xwininfo # help 
man xxd # help 
man yes # help 
man youtube-dl # help 
man zip # help 
markdown README.markdown 
markdown README.markdown | lynx -stdin 
markdown README.markdown > README.html 
md5sum --check md5sums.txt # checksum 
md5sum file # checksum 
meld . & # diff 
meld original mine & # diff 
meld other original mine & # diff 
meld <(ssh example.org cat /etc/hosts) <(ssh example2.org cat /etc/hosts) # diff 
meld <(wget --output-document - http://git.gnome.org/browse/meld/plain/.gitignore?id=250066249e06241e3bfd3863c1a233fb45f40a12) <(wget --output-document - http://git.gnome.org/browse/meld/plain/.gitignore) # diff 
mencoder -fps 10 -nosound -ovc copy timelapse.mp4 -o timelapse-slow.mp4 # video 
mian ~/.minecraft/saves/New\ World 
minecraft & 
mkdir -- example # create directory 
mkdir mp3 
mkfifo pipe1 pipe2 
mkgithub --configure --https --verbose --user l0b0 
mkgithub --configure --ssh --verbose --user l0b0 
mkgithub ~/dev/algorithms 
mkgithub ~/dev/arm 
mkgithub ~/dev/awmtt 
mkgithub ~/dev/bm 
mkgithub ~/dev/bookmarklets 
mkgithub ~/dev/bookmarklets-janmoesen 
mkgithub ~/dev/CERN-Central-Library-bookmark 
mkgithub ~/dev/coffeescript-jedit 
mkgithub ~/dev/coin-sorter 
mkgithub ~/dev/ComputerCraft 
mkgithub ~/dev/count 
mkgithub ~/dev/cronlist 
mkgithub ~/dev/crumbling-beaker 
mkgithub ~/dev/csv2zarafa-contacts 
mkgithub ~/dev/cvsignore2svn 
mkgithub ~/dev/dialogue 
mkgithub ~/dev/dialogue.wiki 
mkgithub ~/dev/difff 
mkgithub ~/dev/diff-ignore-moved-lines 
mkgithub ~/dev/digbuild 
mkgithub ~/dev/dsa3helden 
mkgithub ~/dev/duplicates 
mkgithub ~/dev/export 
mkgithub ~/dev/fgit 
mkgithub ~/dev/filterous 
mkgithub ~/dev/git 
mkgithub ~/dev/git-bisect-example 
mkgithub ~/dev/graphics 
mkgithub ~/dev/hello-world 
mkgithub ~/dev/highlight 
mkgithub ~/dev/https-everywhere 
mkgithub ~/dev/Hypervolume 
mkgithub ~/dev/img2scad 
mkgithub ~/dev/img2vcard 
mkgithub ~/dev/indentect 
mkgithub ~/dev/ipcalc 
mkgithub ~/dev/job-board 
mkgithub ~/dev/l0b0.github.io 
mkgithub ~/dev/lfmcol2csv 
mkgithub ~/dev/lines 
mkgithub ~/dev/logitech-access-keyboard-bindings 
mkgithub ~/dev/lwpb 
mkgithub ~/dev/make-includes 
mkgithub ~/dev/make-links 
mkgithub ~/dev/makeThin 
mkgithub ~/dev/meta2jpeg 
mkgithub ~/dev/metal-book 
mkgithub ~/dev/mian 
mkgithub ~/dev/minecraft-scripts 
mkgithub ~/dev/mkgithub 
mkgithub ~/dev/mount-image 
mkgithub ~/dev/msort 
mkgithub ~/dev/nestable-tube-table 
mkgithub ~/dev/offlickr 
mkgithub ~/dev/OpenDUNE 
mkgithub ~/dev/OpenSCAD-Minimizer 
mkgithub ~/dev/oshw-logo 
mkgithub ~/dev/paperless 
mkgithub ~/dev/paperless.wiki 
mkgithub ~/dev/parametric-box 
mkgithub ~/dev/paths2openscad 
mkgithub ~/dev/peel 
mkgithub ~/dev/Platonic-solids 
mkgithub ~/dev/progit 
mkgithub ~/dev/Project-Euler 
mkgithub ~/dev/pspipe 
mkgithub ~/dev/qr2scad 
mkgithub ~/dev/random 
mkgithub ~/dev/RAYT 
mkgithub ~/dev/ruler 
mkgithub ~/dev/samsung-tools 
mkgithub ~/dev/schemaspy2svg 
mkgithub ~/dev/screensaver-info 
mkgithub ~/dev/see-colon 
mkgithub ~/dev/shell-includes 
mkgithub ~/dev/shunit-ng 
mkgithub ~/dev/SICP 
mkgithub ~/dev/Smooth-CoffeeScript 
mkgithub ~/dev/spark 
mkgithub ~/dev/Standardy 
mkgithub ~/dev/startssl4java 
mkgithub ~/dev/subsurface 
mkgithub ~/dev/svn_ps1 
mkgithub ~/dev/teaching_C 
mkgithub ~/dev/tilde 
mkgithub ~/dev/trim 
mkgithub ~/dev/txt2cloud 
mkgithub ~/dev/unflickr 
mkgithub ~/dev/unrarr # compress 
mkgithub ~/dev/urlwatcher 
mkgithub ~/dev/vcard 
mkgithub ~/dev/vcard2mutt 
mkgithub ~/dev/vcard4 
mkgithub ~/dev/vcf 
mkgithub ~/dev/worktime 
mkgithub ~/dev/xbug 
mkgithub ~/dev/xdg-menu-to-awesome-wm 
mkgithub ~/dev/xFormsCal 
mkgithub ~/dev/xkcd1110 
mkgithub ~/dev/xkillthis 
mkgithub ~/dev/xml 
mkgithub ~/dev/xspf2csv 
mkgithub ~/dev/xterm-color-count 
mkgithub --help 
modinfo i915 # kernel module 
mogrify -crop 2316x1303+0+0 ./*.jpg 
mogrify -format jpg ./*.CR2 # convert 
mount-image ./*.iso 
mount # list all 
mount --no-mtab --options remount,defaults /dev/sda1 / 
mountpoint /home 
mp3fs -obitrate=256 ~/music/ ~/mp3 # mount 
mutt 
mutt -d 5 
mutt -i <(git request-pull HEAD https://github.com/l0b0/project) -s "Pull request" address@example.org # email 
mutt-ldap.pl name # ldap search 
mutt -v 
mutt -vv 
mv file{.orig,} 
ncal -3bM 
nc -l 12345 & netstat --tcp --all | grep :12345 && kill "$!" # test network listen port 
neato -O -Tsvg ./*.dot 
nethack-qt & 
netstat 
netstat --all # internet connections sockets 
nice --adjustment 19 ionice --class 3 du | sort --numeric-sort --key 1 # priority cpu io 
nl ~/.bashrc 
nmap -p 22 --open 192.168.0.0/24 # search list ssh hosts network 
nm-applet & # network gui 
nmap -T Aggressive -A -v 192.168.0.1 
nmap -v -sP 192.168.0.0/24 
nmcli con # network connections list 
nmcli dev # network devices list 
nmcli dev wifi connect SSID password PASSWORD # connect network wireless 
nmcli nm # network manager status 
nm libfoo.so | grep '^ *U ' # dev undefined object 
node # javascript 
node -v 
notify-send "summary" "body" 
npm config set registry http://registry.npmjs.org/ 
npm install -g coffee-script # coffeescript 
npm ls -g 
npm -v 
nslookup example.org # dns internet lookup network 
ntpq -p # query list peers 
openscad ~/dev/crumbling-beaker/beaker.scad & 
openssl asn1parse -in ~/.ssh/id_?sa # decode key 
openssl genrsa -des3 -out private.pem 4096 # create des3 encrypted private rsa key hex 
openssl pkcs12 -export -inkey name.key.pem -in name.crt.pem -out name.p12 # merge certificate key 
openssl pkcs12 -info -in name.p12 -noout # list verify 
openssl req -new -key private.pem -out request.pem # create x509 certificate signing request hex 
openssl req -text -in name.csr.pem # list certificate request properties 
openssl rsa -text -in name.key.pem # list key properties 
openssl x509 -req -days 1 -in request.pem -signkey private.pem -out certificate.pem # create self-signed x509 certificate hex 
openssl x509 -text -in name.crt.pem -noout # list x509 certificate properties 
/opt/android-sdk/platform-tools/adb devices # list 
/opt/android-sdk/platform-tools/adb push cm.zip /sdcard # upload 
/opt/android-sdk/platform-tools/adb reboot bootloader 
/opt/android-sdk/platform-tools/adb reboot download 
/opt/android-sdk/platform-tools/adb shell 
pacman --query bash # package version 
pacman --query --info bash # package info 
pacman --query --info | grep -e '^Name' -e '^Required By' | grep -B 1 '^Required By.*\bbash\b' # list reverse dependencies 
pacman --query --list bash # list all package files 
pacman --query --owns "$(which bash)" # file package owner 
pacman --sync --search bash # search packages 
paman & # pulseaudio manager 
paprefs & # pulseaudio preference 
passwd # password user 
patch --strip 0 < patch.diff 
(path=$'--$`!*@\a\b\E\f\r\t\v\\\'"\360\240\202\211 \n'; diff <(ssh foo 'cat -- '"$(printf %q "$path")") <(ssh bar 'cat -- '"$(printf %q "$path")")) # remote 
PATH=$(IFS=':'; echo "${paths[*]}") 
pavucontrol & # pulseaudio volume 
pdfimages -j ./*.pdf . 
pdfinfo file.pdf 
pdftk A=first.pdf B=second.pdf C=third.pdf cat A B C output target.pdf # concatenate files 
pdftk A=source.pdf cat A1-2 A4-end output target.pdf # remove page 
pep8 --help 
pep8 setup.py 
perlbrew switch 
perl -c file.pl # check syntax 
perl -d -e 1 # interactive console 
perldoc file.pl # help 
perldoc -f kill # help function 
perl -ne 'print join("\n", split(/:/));print("\n");' input # split join 
perl -pe 'chomp if eof' input > output # remove newline eof 
perl --version 
pgrep -P $$ # child processes pids 
pgrep -u root cron 
php --interactive 
php --syntax-check index.php # verify 
php --version 
pidof bash | wc --words # count processes 
pidof init # process pid 
pid=$! # process pid 
ping -c 4 example.org 
ping example.org 
pip2 freeze > requirements.txt # save python dependencies 
pip freeze > requirements.txt # save python dependencies 
pip help 
pip help install 
pngcrush -brute -d target ./*.png # graphics compress 
PREFIX=~ sudo make install 
printf '\0' | uniname -bcepu # 1 nul escape quote 
printf "\0" | uniname -bcepu # 1 nul escape quote 
printf $"\0" | uniname -bcepu # 1 nul escape quote 
printf \\0 | uniname -bcepu # 1 nul escape quote 
printf \0 | uniname -bcepu # 1 zero escape quote 
printf $'\0' | wc --chars # 0 escape quote 
printf %q "$IFS" # escape bash 
printf %q "$PS1" # escape bash 
printf %s $'--$`!*@\a\b\E\f\r\t\v\\\'"\360\240\202\211 \n' | uniname -bcp # test unicode 
printf %s $'--$`!*@\a\b\E\f\r\t\v\\\'"\360\240\202\211 \n' | xclip; cmp --verbose <(printf %s $'--$`!*@\a\b\E\f\r\t\v\\\'"\360\240\202\211 \n') <(xclip -out) # clipboard copy test 
printf %s "${IFS:0:1}" 
printf %s "$IFS" | od --format x1 # string character byte convert hex dump posix 
printf %s "$IFS" | xxd -groupsize 1 # string character byte convert hex dump 
printf "${USER}%.0s" {1..5} # repeat string 
prove 
prove --recurse 
pry 
ps afux | less -S # processes list all tree tty 
ps -eo user= | sort | uniq --count | sort --reverse --numeric-sort # processes users 
ps --pid $$ # current shell 
ps --pid "$(find -L /proc/[0-9]*/exe ! -type l | cut --delimiter '/' --fields '3' | paste --serial --delimiters ',')" # non-kernel processes 
ps -p $$ o ppid= # parent pid 
psql --host localhost --port 15432 --dbname postgres --username postgres <<< "COPY(SELECT datname FROM pg_database WHERE datistemplate = FALSE) TO STDOUT;" # forwarding list all postgresql network 
psql --version # postgresql 
ps -U root -u root fu | less -S # processes list user tree 
ps uw -p $$ # process single pid 
pulseaudio --kill && pulseaudio --start 
puppet describe --short user 
puppet resource --help 
puppet resource --types 
puppet resource user 
puppet resource user root 
pwd # current directory 
pychecker --help 
pyflakes --help 
pylint --help 
python -m py_compile script.py # verify code script 
python -m timeit -s 'text = "sample string"; char = "g"' 'char in text' # timing benchmark 
qemu-img create -f qcow2 /tmp/my.img 10G 
qgit --all . & # gui 
qr2scad < ~/dev/qr2scad/tests/example_big.png > big.scad 
qtpfsgui & # hdr photo editor 
rails console 
rails new project_name # create 
rails server # start service web 
rawtherapee & # raw photo editor 
rbash # restricted 
readelf --all "$(which readelf)" # executable binary 
readlink /proc/$$/fd/0 # symlink source pipe file descriptor pseudo terminal 
read < "/path" 
read -r var 
read <<< "$text" 
recordmydesktop --windowid "$(xdotool selectwindow)" --no-cursor --full-shots --fps 25 --no-wm-check --no-frame -o ~/out.ogv 
rename --no-act 's/([^-]+)-.*-([^-]+)/$1-$2/' ./*.xml | grep --only-matching ' renamed as .*' | sort | uniq --repeated # safe 
rename --no-act --verbose 's/(\d{4})(\d{2})(\d{2})/$1-$2-$3/' ./* # date 
rename --no-act --verbose 's#/([^/]+)$#/prefix $1#' ./* # prefix 
rename --no-act --verbose 's/.*/sprintf "%04d.jpg", ++$main::Mad/e' ./*.jpg # video 
rename --no-act --verbose 's/\.txt$/\.html/' ./*.txt # extension suffix 
reset # clear log remove terminal text 
rmdir ./* 
rm -- example.txt 
route 
rsync --archive --human-readable --progress --verbose host:/path /target # network transfer 
ruby -c test.rb # check verify syntax 
ruby --verbose 
runlevel # kernel 
sandbox="$(mktemp --directory)" 
sane-find-scanner # list device 
sass-convert all.s{a,c}ss 
scanimage --list-devices # scanner 
schemaspy2svg ~/db 
schemaspy2svg --help 
scp example.org:/home/jdoe/example.txt . 
scp -i ~/.ssh/server.pem example.txt user@example.org: # alternative key 
scp -P 2222 example.org:/home/jdoe/example.txt . 
scp -r file example.org:~ 
screen 
screen -dRR name # resume 
screen -dRR # resume 
screen -list 
screen -S compile-project 
script --quiet --command "$SHELL" 
scrot --delay 5 # screenshot 
sed '9d' file # delete line one-indexed 
sed '/^$/d' file # delete empty lines 
sed '/pattern/r./input.txt' example.txt # insert merge file pattern 
sed --quiet '/^START$/,/END^$/{/^START$/d;/^END$/d;p;}' <<< $'START\nfirst\nEND\nSTART\nsecond\nEND' # extract delimiter lines 
sed '/^[[:space:]]*$/d' file # delete whitespace line 
service snmpd status 
set -o noclobber # file error 
set +o noclobber # file error 
set -o nounset # variable error 
set +o nounset # variable error 
set -o pipefail # error 
set +o pipefail # error 
(set -o posix; set) | grep --only-matching '^COMP[^=]*' 
(set -o posix; set) # list all options 
set +o xtrace # disable 
set -o xtrace # enable 
./setup.py test 
setxkbmap -device 10 -layout us -variant dvorak-alt-intl # keyboard layout config 
setxkbmap -option compose:caps # keyboard 
setxkbmap -print # keyboard settings 
setxkbmap -verbose | awk -F '+' '/^symbols:/ {print $2}' # keyboard layout settings 
sh 
sha1sum --check sha1sums.txt # verify checksum 
sha1sum file # checksum 
sha512sum --check sha512sums.txt # checksum 
sha512sum file # checksum 
shopt nullglob # option get 
shopt # options 
shopt -s dotglob # option set .* 
shopt -s extglob # option set ?(a|b) *(a|b) +(a|b) @(a|b) !(a|b) 
shopt -s globstar # option set ** 
shopt -s globstar && wc --lines ./**/**.ext # count recursive lines 
shopt -s nullglob # option set * 
shopt -u nullglob # option unset * 
shred --remove filename # overwrite delete file 
shuf --input-range 0-1 --head-count 1 # random number range 
simple-scan & 
sipcalc 0.0.0.0/0 
sipcalc 192.168.0.1/24 
sleep 1m 
sleep 5s && xprop # x window properties fullscreen 
slideshow -f http://github.com/geraldb/slideshow-s6-blank/raw/master/s6blank.txt 
slideshow -t s6blank presentation.md 
sloccount . 
snmpget -v 2c -c public localhost .1.3.6.1.2.1.1.1.0 
snmptranslate -Of .1.3.6.1.2.1.1 # OID 
snmptranslate -On .iso.org.dod.internet.mgmt.mib-2.system # symbol 
snmptranslate -Tl # list all mib oids 
snmpwalk -v 2c -c public localhost .1.3.6.1.2.1.1 # system 
snmpwalk -v 2c -c public localhost # all 
sort --unique --output result.txt source.txt 
source ~/.bash_aliases 
source ~/.bash_aliases_local 
source ~/.bashrc 
source virtualenv/bin/activate 
speaker-test --channels 2 
speaker-test --device plughw:2,3 # test audio device 
splint foo.c 
sqlite3 -line db/development.sqlite3 "select * from table_name" 
ssh-copy-id example.org 
ssh example.org 
ssh example.org < example.sh # execute shell script remote 
ssh example.org uptime 
ssh -i ~/.ssh/server.pem user@example.org # alternative key 
ssh-keygen -f ~"/.ssh/known_hosts" -R '[1.2.3.4]:1234' # remove public key 
ssh-keygen -l -f /etc/ssh/ssh_host_ecdsa_key.pub # host id ecdsa fingerprint 
ssh-keygen -l -f /etc/ssh/ssh_host_rsa_key # host id rsa fingerprint 
ssh -L 15432:localhost:5432 example.org # local port forwarding postgresql 
ssh -L 5902:localhost:5901 example.org # local port forwarding vnc 
ssh -p 2222 example.org 
ssh -R 9000:localhost:9000 example.org 
ssh -t localhost sudo -u nobody env # tty 
ssh -vvv example.org 
ssh -Y example.org # trusted x11 forwarding 
stat --format '%A %U %G %s %y %n' ./* # list permissions user group file 
stat --format %i / # inode 
stat --printf '%A %U %G %s %y %n\0' ./* # list permissions user group file nul 
stellarium & 
strace -Cf bash -lc true # count calls profile summary 
strace -fe open ./example.sh 2>&1 >/dev/null | grep --only-matching '^\(\[pid\s\+[0-9]*\] \)\?open("[^"]\+' | grep --only-matching '".*' | cut --characters 2- | sort --unique # script dependencies 
strings "$(which strings)" 
stty --all # terminal settings 
stty sane # restore terminal state 
sudo addgroup example 
sudo addgroup "$USER" group 
sudo adduser example 
sudo blkid -o list 
sudo chfn -f "My Name" "$USER" # full name 
sudo chgrp --recursive nogroup -- example.txt # set group file 
sudo chown nobody "$sandbox" 
sudo chown "$USER":"$(printf %q "$(groups | awk '{print $1}')")" "/media/mountpoint" 
sudo chroot /var/jail/"$USER" su --login "$USER" # jail 
sudo cpanm Net::LDAP # install ldap 
sudo cp /sys/class/hwmon/hwmon0/device/fan1_max /sys/class/hwmon/hwmon0/device/fan1_output # hardware macmini4,1 speed 
sudo crontab -e # edit 
sudo delgroup example # delete group 
sudo deluser example # delete user 
sudo ~/dev/tilde/scripts/install-all.sh 
sudo ~/dev/tilde/scripts/suspend-on-close.sh 
sudo dmidecode 
sudo dmidecode --string system-product-name 
sudo dmidecode --string system-serial-number 
sudo dmidecode --type 1 
sudo dmidecode --type system 
sudo download-mibs 
sudo /etc/init.d/postgresql reload 
sudo extundelete --restore-directory /dir/ /dev/sda1 
sudo fdisk -l # list all disks 
sudo gpasswd --add "$USER" group # user add group 
sudo grub-install /dev/sda # fix boot mbr 
sudo hdparm -I /dev/sda # harddisk hardware properties 
sudo ifdown wlan0 # network interface disable 
sudo iftop # bandwidth network interface monitor 
sudo ifup wlan0 # network interface enable 
sudo iotop --batch --iter 1 # i/o storage 
sudo iotop # i/o storage repeat 
sudo ip addr add 1.2.3.4/24 dev eth0 # network address 
sudo ip addr del 1.2.3.4/24 dev eth0 # network address delete 
sudo ip link set dev eth0 up # network enable device 
sudo ip route add default via 1.2.3.4 dev eth0 
sudo ip route del default via 1.2.3.4 dev eth0 
sudo iptables --list # list all firewall rules networ 
sudo ldconfig 
sudo ln --force --symbolic /usr/share/zoneinfo/Europe/London /etc/localtime # set system timezone 
sudo ln --symbolic /media/windows/Windows/Fonts /usr/share/fonts/WindowsFonts # enable windows fonts 
sudo loadkeys dvorak # keyboard layout vt terminal 
sudo localectl --no-convert set-keymap dvorak # x11 console vt keyboard layout 
sudo localectl --no-convert set-x11-keymap us '' dvorak-alt-intl 
sudo lpadmin -d printername # set default printer cups 
sudo lshw | less 
sudo make distclean 2>&1 | tee make_distclean.out~ 
sudo make docinstall 2>&1 | tee make_docinstall.out~ 
sudo make install 
sudo make install 2>&1 | tee make_install.out~ 
sudo make pkginstall 2>&1 | tee make_pkginstall.out~ 
sudo make topclean 2>&1 | tee make_topclean.out~ 
sudo make uninstall 
sudo mandb # update apropos database manual 
sudo mkdir "/media/mountpoint" 
sudo mount --all 
sudo mount --options remount,ro /dev/sda1 # readonly restore 
sudo mount --options remount,rw /dev/sda1 # writeable 
sudo mount --types tmpfs --options size=1m tmpfs -- "$(mktemp --directory --tmpdir -- ramdisk.XXXXXXXXXX)" # create ramdisk partition 
sudo nethogs wlan0 # network monitor 
sudo netstat --listening --tcp --numeric-ports --program | grep '\(^[A-Z]\|^\([^[:space:]]\+[[:space:]]\+\)\{3\}[^[:space:]]\+:22\b\)' # internet connections server search 
sudo ntpdate pool.ntp.org # update date time clock 
sudo pacman --sync --needed --refresh acpid alsa-plugins alsa-utils aspell-de aspell-en aspell-fr awesome base-devel bash-completion batti bc cups cups-filters dos2unix ekiga esmtp evince feh file-roller firefox flashplugin fortune-mod fuse-exfat gimp git gnome-icon-theme gnome-keyring gparted gphoto2 graphviz gutenprint gvfs gvfs-gphoto2 htop hugin hunspell-de hunspell-en hunspell-fr inkscape intellij-idea-community-edition ipython iw jedit keepassx libreoffice-calc libreoffice-draw libreoffice-en-GB libreoffice-impress libreoffice-math libreoffice-writer livestreamer lsb-release lsof markdown meld mlocate mutt net-tools network-manager-applet networkmanager ntfs-3g ntp numlockx offlineimap openssh pidgin polkit-gnome powertop pychecker python-pip rawtherapee rsync scrot sshfs simple-scan slim system-config-printer tcpdump thunar thunar-archive-plugin thunar-volman tigervnc tk ttf-bitstream-vera ttf-dejavu ttf-droid ttf-freefont ttf-inconsolata ttf-ubuntu-font-family vim vlc whois wireshark-gtk xorg-server xorg-server-common xorg-xinit xorg-xkill xorg-xmodmap xorg-xprop xorg-xrandr xorg-xrdb xournal xscreensaver xterm youtube-dl # desktop 
sudo pacman --sync --needed --refresh deluge pygtk # torrent gui 
sudo pacman --sync --needed --refresh eog mcomix # graphics viewer 2d 
sudo pacman --sync --needed --refresh python2-pip 
sudo pacman --sync --needed --refresh steam # games gui 
sudo pacman --sync --needed --refresh stellarium # planetarium gui 
sudo pacman --sync --needed --refresh wine winetricks # windows 
sudo pacman --sync --needed --refresh xf86-input-synaptics xf86-video-intel # laptop drivers touchpad graphics 
sudo pacman --sync --refresh --sysupgrade # upgrade system 
sudo pacman --upgrade ./*.pkg.tar.xz # install 
sudo paperconfig --paper a4 # set print size 
sudo passwd --delete root # disable account user 
sudo perl -n -e 'use DateTime::Format::Strptime; my $parser = DateTime::Format::Strptime->new( pattern => "%B %d %Y"); m/^(\w+ \d+ )(.*)/; print ($parser->parse_datetime("$1" . DateTime->now->year)->ymd, " ", $2, "\n");' /var/log/syslog # date format iso 
sudo pip2 install --upgrade vcard # validator 
sudo pip install --upgrade https://github.com/l0b0/qr2scad/tarball/master 
sudo pip install --upgrade pep8 
sudo pip install --upgrade pip # python 
sudo pip install --upgrade pyflakes 
sudo pip install --upgrade pylint 
sudo pip install --upgrade virtualenv 
sudo pip uninstall vcard # validator 
sudo powertop # power monitoring configuration 
sudo reboot # restart 
sudo sed --in-place 's/^#LEDS=/LEDS=/' /etc/kbd/config # enable capslock boot 
sudo sed --in-place 's/^mibs/#mibs/' /etc/snmp/snmp.conf # disable 
sudo service cups restart 
sudo service postgresql reload 
sudo service postgresql status 
sudo sh -c 'dhclient -r wlan0 && dhclient wlan0' # request refresh dhcp ip 
sudo sh -c 'ip addr add 192.168.0.99/16 dev wlan0 && dhclient wlan0' # set ip address network 
sudo sh -c 'systemctl enable slim.service && systemctl start slim.service' # x11 display server slim 
sudo sh -c 'systemctl start acpid && systemctl enable acpid' 
sudo sh -c 'systemctl start avahi-daemon && systemctl enable avahi-daemon' # printer discovery service 
sudo sh -c 'systemctl start cronie && systemctl enable cronie' # cron service 
sudo sh -c 'systemctl start cups && systemctl enable cups' # printer service 
sudo sh -c 'systemctl start NetworkManager && systemctl enable NetworkManager' # network service 
sudo sh -c 'tail --follow name --retry --lines 0 "$(find /var/log/ -type f -exec file -- {} + | grep ":.*\(ASCII\|UTF\)" | cut --delimiter : --field 1)"' # text 
sudo sh -c 'vim /etc/default/grub && grub-mkconfig --output=/boot/grub/grub.cfg' # edit boot kernel parameters 
sudo sh -c 'wpa_supplicant -d -Dwext -i wlan0 -c /etc/wpa_supplicant.conf 2>&1 >> /var/log/wpa_supplicant.log' # wireless network 
sudo showkey # keyboard 
sudo sshfs host:/path /run/mount/host 
sudo strace -p 123 # process 
sudo sysctl --all # list kernel parameters 
sudo systemctl enable NetworkManager # network gui configuration 
sudo systemctl enable sshd.service 
sudo systemctl restart dhcpcd.service 
sudo systemctl start sshd.service 
sudo tail --follow=name --retry --lines 0 /var/log/syslog 
sudo tcpdump # network debug log packets 
sudo tcpdump tcp # network debug log packets protocol 
sudo tcpdump 'tcp[tcpflags] & (tcp-syn|tcp-fin) != 0 and not src and dst net 127.0.0.1' # network debug log packets internet 
sudo tee /sys/class/hwmon/hwmon0/device/fan1_output <<<5500 # hardware macmini4,1 speed 
sudo traceroute -4 -p 1234 -T example.org # ipv4 port tcp network 
sudo umount "/media/mountpoint" 
sudo umount ~/mp3 
sudo updatedb 
sudo update-grub 
sudo -u postgres createuser --pwprompt username 
sudo -u postgres dropuser username 
sudo -u postgres pg_dumpall > backup.sql # postgresql backup 
sudo -u postgres pg_dump postgres > backup.sql # postgresql backup 
sudo -u postgres psql <<< "COPY(SELECT datname FROM pg_database WHERE datistemplate = FALSE) TO STDOUT;" # list all postgresql 
sudo -u postgres psql <<< "COPY(SELECT extract(epoch from now())::Integer) TO STDOUT;" # unix integer timestamp 
sudo -u postgres psql --dbname my_db <<< "\dt my_schema.*" # database schema tables list all postgresql 
sudo -u postgres psql --dbname postgres < dump.sql # postgresql import 
sudo -u postgres psql --dbname postgres # postgresql login interactive 
sudo -u postgres psql <<< "\dn" # schemas list all postgresql 
sudo -u postgres psql <<< "\dt" # public schema tables list all postgresql 
sudo -u postgres psql <<< "\du" # users list all postgresql 
sudo -u postgres psql <<< "\encoding" # postgresql db encoding 
sudo -u postgres psql <<< "SELECT * FROM pg_stat_activity;" # list sessions processes postgresql 
sudo -u postgres psql --single-transaction --file backup.sql # restore postgresql 
sudo -u postgres psql --variable name="Robert'); DROP TABLE Students; --" <<< "COPY(SELECT :'name') TO STDOUT;" # test escape literal postgresql 
sudo -u postgres service postgresql reload # configuration 
sudo usermod --gid group "$USER" # change default group 
sudo usermod --groups "$(id --name --groups | sed 's/ \?group \?/ /g;s/ /,/g;s/^,//;s/,$//')" "$USER" # remove group 
sudo vim /etc/default/keyboard 
sudo vim /etc/fstab # mount points 
sudo vim /etc/hosts # network 
sudo vim /etc/network/interfaces 
sudo vim /etc/postgresql/*/main/pg_hba.conf 
sudo vim /etc/rc.local 
sudo vim /etc/resolv.conf # dns network 
sudo vim /etc/X11/xorg.conf 
sudo vipw # edit password users 
sudo vipw --group # edit groups users members 
sudo visudo # permissions security 
sudo wavemon 
sudo wifi-menu 
sudo Xorg :1 -configure 
sum <<< '2 2' 
sweethome3d & 
synclient SHMConfig=1 -m 100 | tee synaptics.log # synaptics touchpad debug 
system-config-printer & 
systemctl is-enabled cronie.service 
systemctl status slim.service 
systemd-analyze blame # list boot service time 
systemd-analyze # boot time kernel user 
systemd-analyze critical-chain # boot process dependency time 
systemd-analyze dot | dot -Tsvg > startup-dependencies.svg # 2d startup process dependencies 
systemd-analyze plot > startup-timing.svg # time startup process 
TAGS=all guard 
TAGS="$USER" guard 
tail --follow=name --retry --lines 0 /var/log/wpa_supplicant.log 
tar --create --gzip --exclude-vcs --directory ~/dev --file ~/tilde.tar.gz tilde # compress gzip 
tar --extract --gzip --file ~/tilde.tar.gz # decompress gzip 
tar --extract --gzip --transform 's#.*/##' --file ~/tilde.tar.gz # decompress flatten gzip 
tar --list --gzip --file ~/tilde.tar.gz 
telnet localhost 1234 # network 
thunar-volman-settings & # mount removable storage 
tig 
time bash -lc true # benchmark startup login shell 
timedatectl status 
time make test 
timeout 1 sleep 2 
tkmib & 
todos -- file # convert newline 
top 
top -c # command line 
top -p "$(pgrep -d ',' bash)" 
tput colors 
traceroute example.org 
trap # signal 
traps="$(trap)" # signal 
tty 
txt2cloud 
txt2cloud --min 3 < "$(which txt2cloud)" > cloud.xhtml 
type -a true 
udevadm info --export-db 
udevadm monitor --environment kernel # live events 
ulimit -a 
ulimit -c unlimited 
umask 
umask 0077 && ssh-keygen -b 4096 -f ~/.ssh/id_rsa -t rsa && openssl pkcs8 -topk8 -v2 des3 -in ~/.ssh/id_rsa -out ~/.ssh/id_rsa.pk8 && shred --remove ~/.ssh/id_rsa && mv --no-clobber ~/.ssh/id_rsa.pk8 ~/.ssh/id_rsa # create encrypted private public rsa pkcs8 ssh key pair 
umask -S # symbolic 
umount-image ./*.iso 
umount /mnt/foo # unmount device drive 
uname --all 
uname --kernel-name --kernel-release --kernel-version --machine --processor --hardware-platform --operating-system # anonymized 
unetbootin 
unetbootin & 
unexpand --tabs=4 example.txt # convert space tab 
unix2dos contacts.vcf # newline convert 
unset -f function 
unset variable_or_function 
unset -v variable 
unzip file.zip # decompress zip 
unzip -l file.zip # list zip 
uptime 
/usr/local/JDiveLog/bin/jdivelog 
vagrant box add precise32 http://files.vagrantup.com/precise32.box 
vagrant box list # show all 
vagrant destroy # delete vm 
vagrant --help 
vagrant init precise32 # ubuntu vm 
vagrant ssh 
vagrant status 
vagrant up # update vm 
vainfo 
valgrind foo # check memory binary 
vcard ~/contacts/*.vcf 
vim ~/.bash_aliases_local # shell 
vim ~/.bash_aliases # shell 
 vim ~/.bash_history # shell 
vim ~/.bashrc_local # shell 
vim ~/.bashrc # shell 
vim ~/.config/awesome/rc.lua 
vim -c "setfiletype sh" example.txt 
vim ~/dev/fgit/fgit.sh # dev 
vim ~/dev/indentect/indentect.sh # dev 
vim ~/dev/mkgithub/mkgithub.sh # dev 
vim ~/dev/tilde/.muttrc # email 
vim ~/dev/tilde/scripts/cleanup.sh 
vim ~/dev/tilde/scripts/install-all.sh 
vim ~/dev/tilde/scripts/make-links.sh 
vim ~/.gitconfig # dev 
vim .git/config # dev 
vim .gitignore # dev 
vim ~/.imapfilter/config.lua 
vim /lib/udev/rules.d/95-keymap.rules # keyboard 
vim Makefile # dev 
vim ~/.mkgithub # dev 
vim ~/.mozilla/firefox/*/chrome/userContent.css 
vim ~/.muttrc # email 
vim ~/.muttrc_local # email 
vim README.markdown # dev 
vim ~/.ssh/config 
vim ~/.vimrc 
vim ~/.wine/system.reg 
vim ~/.wine/user.reg 
vim ~/.xinitrc 
virtualbox & 
virtualenv --help 
virtualenv --python=python2.7 virtualenv 
vlc --ffmpeg-hw --verbose 2 file.1080p.x264.mkv # video h.264 
vlc --full-help | less 
vlc --fullscreen --deinterlace -1 --deinterlace-mode yadif2x --video-filter postproc --postproc-q 6 --audio-language ja --sub-language en --verbose 2 --advanced dvdsimple:///dev/dvd & 
vlc --fullscreen --deinterlace -1 --deinterlace-mode yadif2x --video-filter postproc --postproc-q 6 --verbose 2 --advanced ./*.avi 
vlc http://www.lynnepublishing.com/surround/www_lynnemusic_com_surround_test.ac3 # audio 
vlc --spdif http://www.lynnepublishing.com/surround/www_lynnemusic_com_surround_test.ac3 # audio 
vmware 
vncpasswd 
vncserver -kill :1 # stop service 
vncserver -list # all 
vncserver -localhost -geometry "$(xrandr | sed --quiet 's/.*current \([0-9]*\) x \([0-9]*\).*/\1x\2/p')" # start service remote desktop 
vncviewer :1 # local desktop 
vncviewer :2 # remote desktop 
w 
wait # process pid 
watch --color --differences -- git diff --color=always # change 
wc --lines -- example.txt # line count 
wdiff -w "$(tput bold && tput setaf 1)" -x "$(tput sgr0)" -y "$(tput bold && tput setaf 2)" -z "$(tput sgr0)" path1 path2 # color word diff 
wget --output-document - http://user:password@host/function?id=foo 2>service.log | json_pp # web service 
wget --server-response --output-document=/dev/null http://example.org/ # web header 
whatis mv # exact help man 
which make 
while IFS= read -r -d '' -u 9; do if [[ "$(file --brief --special-files --mime-type -- "$REPLY")" = text/* ]]; then sed --in-place 's/[ \t]\+\(\r\?\)$/\1/;$a\' -- "$REPLY"; else echo "Skipping $REPLY" >&2; fi; done 9< <(find . \( -type d -regex '^.*/\.git$' -prune -false \) -o -type f -exec printf '%s\0' {} +) # text whitespace eol eof 
while IFS= read -r -d '' -u 9; do jedit -reuseview "$REPLY"; done 9< <(grep --null --files-with-matches --recursive --exclude-dir .git --regexp 'pattern' .) # search open files 
while IFS= read -r -d '' -u 9; do printf '%q\n' "${REPLY#* }"; done 9< <(find . -printf '%T@' -exec printf ' %s\0' {} \; | sort --general-numeric-sort --zero-terminated) # sort file list modification date 
while IFS= read -r -d '' -u 9; do sed --in-place '/\x0/{q;}; s/[ \t]\+\(\r\?\)$/\1/;$a\' -- "$REPLY"; done 9< <(find . \( -type d -regex '^.*/\.git$' -prune -false \) -o -type f -exec printf '%s\0' {} +) # file whitespace eol eof 
while IFS= read -r -u 9; do if [[ "$REPLY" =~ .*\.dot$ ]]; then dot -O -Tsvg "$REPLY"; fi; done 9< <(inotifywait --event close_write --format %f --monitor .) 
while read; do xdotool windowactivate "$REPLY"; xdotool key F5; done < <(xdotool search --name "Mozilla Firefox") # refresh 
while sleep 1; do (shopt -s nullglob; events_dir="${HOME}/.events"; for path in "$events_dir"/*; do notify-send --icon="${HOME}/dev/graphics/${USER}.png" "$(basename "$path")" "$(cat "$path")" && rm "$path"; done;) done 
whois example.org # dns lookup internet network 
who # logins users 
wine --version 
wireshark & 
wnpp-alert # Debian packaging 
worktime --end="$(date --date=Thursday +%Y-%m-%d)" > ~/week.xhtml && x-www-browser ~/week.xhtml 
xclip filename.txt # mouse clipboard copy 
xclip -out # mouse clipboard print stdout 
xclip -selection clipboard filename.txt # keyboard clipboard copy 
xclip -selection clipboard -out # keyboard clipboard print stdout 
xev 
xinput # all keyboard device list 
xinput --list 10 # keyboard device info 
xinput --list-props 10 # keyboard device properties 
xkill 
xmllint --shell input.xml # interactive shell xpath xml 
xmodmap -pm # list keyboard modifiers 
xmodmap -pp # list mouse buttons 
xmodmap ~/.Xmodmap # read configuration keyboard mouse 
xprop | grep --color=none "WM_CLASS\|^WM_NAME" 
xprop # x window properties 
xrandr --verbose # graphics hardware 
xrdb -load ~/.Xresources 
xrdb -query # list 
xscreensaver-command -lock 
xscreensaver-command -version 
xscreensaver-demo & # settings configuration 
xsltproc --output file.xml ~/dev/xml/filter/filter.xslt file.xml # filter xml xslt replace 
xsltproc --output file.xml file.xslt file.xml # transform xslt xml replace 
xterm -version 
xwininfo -id "$(xdotool selectwindow)" 
xwininfo -id "$(xprop -root | awk '/_NET_ACTIVE_WINDOW\(WINDOW\)/{print $NF}')" # current window 
xxd "$(which xxd)" | head --lines=1 # binary hex 
(yes a & yes b) | cat >/dev/null & ~/dev/pspipe/fdpid.sh 0 "$!" # process pid pipe stdin 
yes | dh_make --single && printf %s $'*.EX\n*.ex\n' > debian/.gitignore && git add debian 
yes -- example # repeat string 
youtube-dl --output "${HOME}/download/%(upload_date)s-%(title)s-%(id)s.%(ext)s" --continue 'https://www.youtube.com/watch?v=' # download video files 
zip --update file.zip input # add file compress zip 
zless /usr/share/doc/autotools-dev/README.Debian.gz # help 
zless /usr/share/doc/devscripts/README.gz # help 
zess /usr/share/doc/rar/rar.txt.gz # help compress git mergetool l
