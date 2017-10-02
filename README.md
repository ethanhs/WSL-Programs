# WSL-Programs

[![Join the chat at https://gitter.im/ethanhs/WSL-Programs](https://img.shields.io/gitter/room/ethanhs/WSL-Programs.svg?style=flat-square)](https://gitter.im/ethanhs/WSL-Programs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) &#124; [![GitHub contributors](https://img.shields.io/github/contributors/ethanhs/WSL-Programs.svg?style=flat-square)](https://github.com/ethanhs/WSL-Programs/graphs/contributors) &#124; [![CC0 license](https://img.shields.io/badge/license-CC0-blue.svg?style=flat-square)](https://github.com/ethanhs/WSL-Programs/blob/master/LICENSE)

If you'd like to chat about the Windows Subsystem for Linux (or have a question) please use the gitter chat linked above. If you are looking for guidance on getting started with Bash on Ubuntu on Windows, check [here](https://github.com/abergs/ubuntuonwindows).

## About

A community powered list of programs that work (and those that don't) on the Windows subsystem for Linux. The official Microsoft repository for filing bugs etc is located [here](https://github.com/Microsoft/BashOnWindows). This repo complements the offical one by providing a quick reference for how well programs run.

Please feel free to contribute programs you have tested to the table below. If you need help with the markdown, please review [a primer](https://help.gamejolt.com/markdown)

To contribute, please make a Pull Request, I will merge if it looks good! If you have never made a pull request it is fast and easy, please check out the [Github documentation](https://help.github.com/articles/using-pull-requests/)

Then add your program below!

If you need to add more details about a program then add a `+` symbol to its name and add it to the [Program_Details.md](Program_Details.md) file.

## Important Note
Because this list is community powered, the maintainer does not hold any responsibility for the accuracy of the contents of this repository. Your mileage _may_ vary.


# The list:

Program Name  | apt name | Functionality rating (0-5) | website | Notes  | Windows Build #
------------- | --------------------------------------- | -------------------------- | --------------------- | -------|----------
ADB | | 2 | android-adb-tools | Installs; see [this image](https://cloud.githubusercontent.com/assets/7135398/17540401/6b94e568-5ee8-11e6-8523-b3efa1e4edd8.png) for example, requires adb on Windows too.
Anaconda || 4 | [Continuum.io](https://www.continuum.io/downloads) | Simple commands work after getting listed WSL build, symlinks issue has been fixed | 14393
Apache server | apache2 | 2 | | Must use a loopback for networking, buggy
apt | | 5 | | Works fine | 15063.138
apt-fast | | 3 | [ilikenwf/apt-fast](https://github.com/ilikenwf/apt-fast) | Simple commands work. Needs more testing | 15063.138
archey | | 3 | | Works for the most part, but displays disk usage incorrectly | 15063.138
aria2c | aria2 | 3 | | Does not resolve domains, must use IP addresses. Possibly c-ares related | 14901.1000
atom | atom | 0 | [Atom.io](https://atom.io) | Does not install, causes `apt` and `dpkg` to lock up trying to install | 16275
bash+ | | 3 | | Most functionality exists but there are problems with scripts
blackfire.io | | 0 | | Error while trying to listen for connections on 'unix:///var/run/blackfire/agent.sock'
byobu | | 3 | | Need to toggle the byobu charmap (run `/usr/lib/byobu/include/toggle-utf8` or `export BYOBU_CHARMAP=x ; . ~/.bashrc`). Status bar occasionally disappears. | 14901.1000
[c-ares](https://github.com/c-ares/c-ares) | libc-ares2 | 0 | | Does not resolve domains to ip addresses. | 14901.1000
cargo | | 4 | [rust-lang.org](https://www.rust-lang.org/downloads.html) | Correctly recognizes and downloads dependencies on basic projects. Needs testing with larger projects. | 14393.67
curl | | 4 | | curl -sS tested
composer | | 5 | | doesn't seem to have issues, but could use more test.
cmake | | 4 | | Seems to work perfectly, though more testing needed.
Coq | | 4 | | Installed without issue, needs more testing. | 14393
docker | | 0 | | doesn't run / says not installed
Electron (and any apps based on it) | | 3 | [electron.atom.io](https://electron.atom.io/) | Some apps will install, but not run. Some will not install at all. Any app that uses Chrome 53 or later as it's backend **should** in theory work, no promises | 16275
emacs | | 5 | | with latest WSL and Ubuntu Xenial works great in terminal mode and over X. | 16251 
firefox |firefox| 3 | | Able to get working using firefox on X server. Sandbox eror unexpected multithreading found, this prevents using namespace sandboxing. Error GDK_BACKEND does not match available displays |14393
fish | | 5 | | works fine
fortune | | 5| | works fine
fsharp | | 4 | | Installed without issue, needs more testing. To use fsi (F# Interactive) `fsharpi` | 14393
gazebo | | 3 | | Very laggy tested. Requries X11 server like VcXsrv and setting a few environment variables
gcc | build-essential | 4 | | more testing needed
gedit | gedit | 5 | | Works just fine after X Server configuration. Will throw some Dbus errors, but doesn't seem to affect performance. Can read and write files to Linux and Windows | 16275
ghc | ghc | 4 | [Haskell on Bash](https://blogs.msdn.microsoft.com/commandline/2017/02/09/haskell-on-bashwsl/) | Needs more tests | 15031
gimp | gimp | 5 | [gimp](https//gimp.org) | Seems to work just fine. Does throw some UI and Dbus errors, but performance doesn't seem affected. Can read and write files to both Linux and Windows | 16275
git | | 4 | | requires more testing, Basics work (clone, pull, push, fetch commit). Diff has some errors
GNOME Web | epiphany-browser | 4 | [How-to](http://browsingthenet.blogspot.com/2016/11/how-to-run-epiphany-web-browser-in.html) | Works fine but the video is choppy | 14393
golang | golang-go | 3 | [Golang](https://golang.org/dl/) | golang-go gets 1.6 which is not the latest version. Needs more testing | 15031 (Xenial)
gparted | | 2 | | Window opens and can be interacted with, but it can't find any devices and the close button doesn't work so you have to Ctrl + C in bash. Requires X server, only tested after [dbus fix](https://www.reddit.com/r/Windows10/comments/4rsmzp/bash_on_windows_getting_dbus_and_x_server_working/) with [VcXserv](https://sourceforge.net/projects/vcxsrv/). | 14393.187
grep | | 4 | | __WARNING: PASSWORD MAY BE SHOWN IN PLAINTEXT__;requires more testing see [this issue](https://github.com/Microsoft/BashOnWindows/issues/450) for more.
haxe | | 5 | [Haxe Foundation PPA](http://haxe.org/download/linux) | Compiles programs correctly, haxelib works fine too
heroku | | 5 | [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) | Installs and works as expected, tested app listing, logs, setting config
htop | | 5 | |  Works as expected, though only lists processes running under WSL, not under Windows. CPU and Memory usage stats are accurate.
i3 | | 4 | [i3wm.org](http://i3wm.org/) | Works fine under VcXsrv Server 1.19.2.0 without `-multiwindow` command line option. Added `export DISPLAY=:0` to `.bashrc` | 15063.138
ifconfig | | 4 | | Seems to work fine | 15063.138
ip | | 4 |  | Seems to work fine | 15063.138
ircii | | 1 |  | terminal handling is broken, once the window fills, it only uses the bottom 3 lines
irssi | | 5 |  | seems to work flawlessly
iwconfig | | 0 | | Unable to Access Network Interfaces (Should be localhost for all connections)
java | | 2 | | 1.8 runs at minimum, seems to have some functionality at least
lua | lua5.2 | 3 | [Lua](http://www.lua.org/start.html) | Just tested with interpreter. Needs more tests | 15031 (Xenial)
lynx | | 5 | | seems to work entirely
mount | | 2 | | unable to mount iso/cd-rom files
Maude | | 4 | | Installed without issue, needs more testing
make | | 3 | | basic scripts working, needs more extensive testing. Tabbing for commands gets broken pipe
Meteor | | 5 | [meteor.com](https://meteor.com) | Seems to work just fine. Can build and serve apps, create apps, and reads and writes to Windows and Linux | 16275
MLton | | 0 | | BSOD | 14393
Mongo Client | | 4 | | Works well connecting to mongod windows service
Mono | mono-complete | 4 | | Supported ([more info](https://github.com/mono/website/issues/199)). Instructions added to official documentation. Use 4.2 for now or 4.6 when released (4.4 [has issues](https://bugzilla.xamarin.com/show_bug.cgi?id=42169))|
mysql | | 4 | | Seems to work flawlessly | 15063.138
mtr | | 0 | | doesn't run
nano | | 4 | | Functions and displays correctly | 15063.138
nasm | | 4 | | more testing needed
nethack | | 4 | | Need to run it from the /usr/games directory with "./nethack" and the default config it runs has numpad turned off so you have to use the unintuitive: y k u h l b j n
nginx+ | | 4 | | Can't bind to IPv6 | 15063.138
nmap | | 0 | | AF_Netsock options not implemented [#1349](https://github.com/Microsoft/BashOnWindows/issues/1349)
node.js | nodejs | 4 | | Seems to work fine. Runs the React VR hello world project perfectly. | 15063.138
nuget | | 3 | | requires more testing
npm | | 4 | | some packages fail due to permissions
OCaml | | 4 | | Works fine with Core, needs more testing. | 15063.540
[OpenCoarrays] | | 4 | [opencoarrays.org] | Installed from source but needs more testing. See [the OpenCoarrays install instructions] for more details |
OpenRCT2 | | 0 | | Fails with errors to do with Sharing Memory with X, Possibly due to VcXsrv.
ping | | 1 | | Works if run as admin (not root), otherwise fails with `ping: icmp open socket: Socket type not supported`
pip+ | | 0 | | **DO NOT INSTALL** with `--fix-missing`. Breaks `apt`. See documentation
php5-cli | | 4 | | Working, needs more testing
php7.0| | 4 | | Installed without issue, needs more testing
python | | 5 | | Works even for very difficult and memory intensive workloads such as compiling PyPy | 14366
pypy | | 5 | | Works even when translating itself | 14366
qpidd | | 0 | | Starting the daemon fails with a socket error: "critical Unexpected error: Can't bind to port 0.0.0.0:5672: Invalid argument (qpid/sys/posix/Socket.cpp:206)"
R | r-base  | 4 | | devtools, doParallel and foreach works. May be numerically a little different from other system. More tests needed.  | 14393
rbenv | | 4 | | works for the most part, but permissions of folders are wrong after installing (world writable), spawning warnings when running e.g. Rubygems | 14366
reboot | | 0 | | Unable to shutdown system.
redis | | 4 | [Redis](https://redis.io/download) | Able to start server and interact with built-client. Did part of tutorial and worked great. | 15031 (Xenial)
rsync | | 4 | | works with ssh tunneling and with same file system. Needs more testing
ruby | | 4 | | works for Sinatra and Rails development using C extension gems for the most part, but `rails new testapp` works with `WeBrick` (the default), but hangs with `thin` | 14986
rustc | | 4 | [rust-lang.org](https://www.rust-lang.org/downloads.html) | Can compile basic programs. Needs testing with more complex programs | 14393.67
Sage Math | | 4 | [http://www.sagemath.org/](http://www.sagemath.org/) | Able to do a good portion of the Sage Math tutorial. There is a RunTime warning but does not stop Sage from working | 15031
scp | | 5 | | works for both remote to local and local to remote transfers.
screen | | 4 | | Already installed. [Simple fix needed.](https://www.systutorials.com/qa/1639/screen-reporting-cannot-directory-screen-permission-denied?show=1640#a1640) | 15063 (Xenial)
sed | | 4 | | didn't test all options, but everything I tested worked fine.
SMLNJ | | 0 | | Installed. Will not start correctly. | 14393
sqlite | | 4 | | [File locking is broken](https://github.com/Microsoft/BashOnWindows/issues/2395), which can lead to database corruption
ssh | | 5 | | ssh works as expected
ssh-keygen | ssh | 4 | | -t rsa working
sudo | | 5 | | appears to be working as expected
SWI-Prolog | | 4 | | Installed without issue, needs more testing. See: [(Installing from PPA (Ubuntu Personal Package Archive))](http://www.swi-prolog.org/build/PPA.txt) | 14393
swift | | 3 | ? | Everything except interactive shell works
tail | | 3 | | Will tail files, but 'follow' (-f) reports "tail: unrecognized file system type 0x53464846"
tcc | | 3 | | tcc run and scripted "#!/usr/bin/tcc -run" files work correctly
telnet | | 4 | | Further testing required
tensorflow | | 4 | | See [Scott Hanselman's post](http://www.hanselman.com/blog/PlayingWithTensorFlowOnWindows.aspx)
tesseract-ocr | | 4 | | No problems with command line usage
texlive | | 5 | | No problems so far | 14366
tmux | | 4 | | Works well for the most part, mouse mode doesn't seem to work  | 14366
torproject | tor | 5 | | Tor is a free software that prevents people from learning your location or browsing habits by letting you communicate anonymously on the Internet. | 14393
ufw | | 0 | | Fails with an error about iptables | 15063.138
useradd | | 4 | | Users can be added but /etc/skel profile logout and bashrc files but no default directories
usermod | | 5 | | Seems to work correctly
vim+ | | 3 | | Will open and edit Window files it cannot create new files. Can create new linux files. Issues with colorschemes. Plugins don't work. Panes, buffers, and registers appear to be working correctly.
Visual Studio Code | code && code-insider | 2 | [Visual Studio Code](https://code.visualstudio.com) | Will install, but does not launch due to issues relating to Google Chrome with WSL. See [#758](https://github.com/Microsoft/BashOnWindows/issues/758) | 16275
vsftpd | | 3 | ? | Not installed with apt
wget | | 3 | | Simple commands work. Have only run basic commands
xfce4-terminal | | 5 | | Seems to work Perfectly | 15063
startxfce4 (and all subsequent programs) | | 5 | | Everything seems to work, I didn't find anything wrong with it. | 15063
xorg | | 4 | | Requires Configuration and an X server on Windows
yum | | 0 | | doesn't work at all. will segfault on `yum`, hangs indefinitely with `yum install`
zsh | | 4 | | Simple commands work after getting listed WSL build, also checked oh-my-zsh | 14393

[the OpenCoarrays install instructions]: https://github.com/sourceryinstitute/opencoarrays/blob/master/INSTALL.md#windows
[OpenCoarrays]: https://github.com/sourceryinstitute/opencoarrays
[opencoarrays.org]: http://opencoarrays.org
