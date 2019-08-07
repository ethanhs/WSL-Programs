# WSL-Programs

[![Join the chat at https://gitter.im/ethanhs/WSL-Programs](https://img.shields.io/gitter/room/ethanhs/WSL-Programs.svg?style=flat-square)](https://gitter.im/ethanhs/WSL-Programs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) &#124; [![GitHub contributors](https://img.shields.io/github/contributors/ethanhs/WSL-Programs.svg?style=flat-square)](https://github.com/ethanhs/WSL-Programs/graphs/contributors) &#124; [![CC0 license](https://img.shields.io/badge/license-CC0-blue.svg?style=flat-square)](https://github.com/ethanhs/WSL-Programs/blob/master/LICENSE)

If you'd like to chat about the Windows Subsystem for Linux (or have a question) please use the gitter chat linked above. If you are looking for guidance on getting started with Bash on Ubuntu on Windows, check [the Ubuntu Repo](https://github.com/abergs/ubuntuonwindows).

## About

A community powered list of programs that work (and those that don't) on the Windows subsystem for Linux. The official Microsoft repository for filing bugs, etc., is located at [Microsoft's BashOnWindows repo](https://github.com/Microsoft/BashOnWindows). This repo complements the offical one by providing a quick reference for how well programs run.

Please feel free to contribute programs you have tested to the table below. If you need help with the markdown, please review [this markdown primer from gamejolt](https://help.gamejolt.com/markdown).

To contribute, please make a Pull Request; I will merge if it looks good! If you have never made a pull request, it is fast and easy. Please check out the [Github documentation](https://help.github.com/articles/using-pull-requests/).

Then add your program below!

If you need to add more details about a program, add a `+` symbol to its name and add it to the [Program_Details.md](Program_Details.md) file.

## Important Note
Because this list is community powered, the maintainer does not hold any responsibility for the accuracy of the contents of this repository. Your mileage _may_ vary.


# The list:

Program Name  | apt name | Functionality rating (0-5) | website | Notes  | Windows Build #
------------- | --------------------------------------- | -------------------------- | --------------------- | -------|----------
ADB | | 2 | [developer.android.com](https://developer.android.com/studio/command-line/adb.html) | Installs; see [this image](https://cloud.githubusercontent.com/assets/7135398/17540401/6b94e568-5ee8-11e6-8523-b3efa1e4edd8.png) for example, requires adb on Windows too.
Anaconda || 4 | [Continuum.io](https://www.continuum.io/downloads) | Simple commands work after getting listed WSL build, symlinks issue has been fixed | 14393
Apache server | apache2 | 2 | [httpd.apache.org](https://httpd.apache.org/) | Must use a loopback for networking, buggy
Apache SINGA |  | 4 | [singa.apache.org](https://singa.apache.org/) | Only CPU version is supported.
apt | | 5 | [wiki.debian.org/Apt](https://wiki.debian.org/Apt) | Works fine | 16299.19
apt-fast | | 3 | [ilikenwf/apt-fast](https://github.com/ilikenwf/apt-fast) | Simple commands work. Needs more testing | 15063.138
archey | | 3 | [djmelik/archey](https://github.com/djmelik/archey)| Works for the most part, but displays disk usage incorrectly | 15063.138
aria2c | aria2 | 3 | [aria2.github.com](https://aria2.github.io/) | Does not resolve domains, must use IP addresses. Possibly c-ares related | 14901.1000
arp | arp | 0 | | /proc/net/arp: No such file or directory
arp-scan | arp-scan | 0 | https://github.com/royhills/arp-scan | link_open: Address family not supported by protocol
AWeather | aweather | 0 | http://pileus.org/aweather/ | Crashes on launch due to OpenGL error. | 17764.55
bash+ | | 3 | [gnu.org/software/bash](https://www.gnu.org/software/bash/) | Most functionality exists but there are problems with scripts
blackfire | blackfire-agent | 5 | [blackfire.io](https://blackfire.io/) | | 16299.15
boost | | 5 | [boost](https://http://www.boost.org) | | 16299.125
byobu | | 3 | [byobu.co](http://byobu.co/) | Need to toggle the byobu charmap (run `/usr/lib/byobu/include/toggle-utf8` or `export BYOBU_CHARMAP=x ; . ~/.bashrc`). Status bar occasionally disappears. | 14901.1000
c-ares | libc-ares2 | 0 | [c-ares/c-ares](https://github.com/c-ares/c-ares) | Does not resolve domains to ip addresses. | 14901.1000
cargo | | 4 | [rust-lang/cargo](https://github.com/rust-lang/cargo) | Correctly recognizes and downloads dependencies on basic projects. Needs testing with larger projects. | 14393.67
curl | | 4 | [curl/curl](https://github.com/curl/curl) | curl -sS tested
chromium-bsu | | 0 | [chromium-bsu.sourceforge.net](http://chromium-bsu.sourceforge.net/) | Completely Fails to Launch
composer | | 5 | [getcomposer.org](https://getcomposer.org/) | doesn't seem to have issues, but could use more test.
cmake | | 4 | [cmake.org](https://cmake.org/) | Seems to work perfectly, though more testing needed.
Coq | | 4 | [coq.inria.fr](https://coq.inria.fr/) | Installed without issue, needs more testing. | 14393
docker | | 3 | [docker.com](https://www.docker.com/) | Using Docker for Windows it's possible to get the client working in WSL using the instructions [here](https://raesene.github.io/blog/2018/03/29/WSL-And-Docker/)
Electron (and any apps based on it) | | 3 | [electron.atom.io](https://electron.atom.io/) | Some apps will install, but not run. Some will not install at all. Any app that uses Chrome 53 or later as it's backend **should** in theory work, no promises | 16275
eclipse | | 4 | http://eclipse.org | occasional crashes handled internally | 17134.68
emacs | | 5 | [gnu.org/software/emacs](https://www.gnu.org/software/emacs/) | with latest WSL and Ubuntu Xenial works great in terminal mode and over X. | 16251
fakeroot | fakeroot | 3 | | works if configured to communicate over TCP | 15063
firefox |firefox| 5 |  [mozilla.org/firefox](http://mozilla.com/firefox) | Runs, without reporting any errors whatsoever, unless you bump into the negative monotonic clock problem that causes all gthread-based applications to crash. | 15063
fish | | 5 | [fish.sh](https://fish.sh/) | works fine
fortune | | 5 | [wikipedia - Fortune](https://en.wikipedia.org/wiki/Fortune_(Unix)) | works fine
fsharp | | 4 | [fsharp.org](http://fsharp.org/) | Installed without issue, needs more testing. To use fsi (F# Interactive) `fsharpi` | 14393
gazebo | | 3 | [gazebosim.org](http://gazebosim.org/) | Very laggy tested. Requries X11 server like VcXsrv and setting a few environment variables
gcc | build-essential | 4 | [gcc.gnu.org](https://gcc.gnu.org/) | Runs as expected, more testing needed | 16299.19
gedit | gedit | 5 | [wiki.gnome.org/Apps/Gedit](https://wiki.gnome.org/Apps/Gedit) | Works just fine after X Server configuration. Will throw some Dbus errors, but doesn't seem to affect performance. Can read and write files to Linux and Windows | 16275
ghc | ghc | 4 | [Haskell on Bash](https://blogs.msdn.microsoft.com/commandline/2017/02/09/haskell-on-bashwsl/) [haskell.org/ghc](https://www.haskell.org/ghc/) | Needs more tests | 15031
gimp | gimp | 5 | [gimp](https//gimp.org) | Seems to work just fine. Can read and write files to both Linux and Windows. Xming freezes, VcXsrv works fine | 16275
git | | 4 | [git-scm.com](https://git-scm.com/) | requires more testing, Basics work (clone, pull, push, fetch commit). Diff has some errors | 16299.19
gnokii | gnokii | 0 | | useless without USB | 17134.68
GNOME Web | epiphany-browser | 4 | [How-to](http://browsingthenet.blogspot.com/2016/11/how-to-run-epiphany-web-browser-in.html) | Works fine but the video is choppy | 14393
GNUStep Terminal | gnustep-terminal | 3 | | displays bold as tiny | 17134.68
gphoto2 | gphoto2 | 0 | | useless without USB | 17134.68
gnuplot | gnuplot | 5 | [gnuplot](http://www.gnuplot.info/) | Fitting data and plotting/displaying graphs of functions working fine. The qt terminal throws the following error the first time it plots: `QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-<username>' Warning: slow font initializationgnuplot> qt_processTermEvent received a GE_fontprops event. This should not have happened`, but works fine. Requires a x11 server to display plots. | 17134.228
golang | golang-go | 3 | [Golang](https://golang.org/dl/) | golang-go gets 1.6 which is not the latest version. Needs more testing | 15031 (Xenial)
gparted | | 4 | [gparted.org](https://gparted.org/) | Window opens and can be interacted with, but it can't find any devices.
The GNU Privacy Guard | gpg | 4 | [gnupg.org](https://gnupg.org/) | See [#130](https://github.com/ethanhs/WSL-Programs/issues/130) | 17763.503
grep | | 4 | [wikipedia - grep](https://en.wikipedia.org/wiki/Grep) | __WARNING: PASSWORD MAY BE SHOWN IN PLAINTEXT__;requires more testing see [this issue](https://github.com/Microsoft/BashOnWindows/issues/450) for more.
GSpdf | gnustep-gspdf | 5 | | | 17134.68
GWorkspace | gnustep-gworkspace | 3 | | problems with fonts and icons, manageable | 17134.68
haxe | | 5 | [Haxe Foundation PPA](http://haxe.org/download/linux) | Compiles programs correctly, haxelib works fine too
heroku | | 5 | [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) | Installs and works as expected, tested app listing, logs, setting config
hpx | | 5 | [ste||ar-hpx](https://stellar-group.org) | Installs and works as expected | 16299.125
htop | | 5 | [hisham.hm/htop](http://hisham.hm/htop/) |  Works as expected, though only lists processes running under WSL, not under Windows. CPU and Memory usage stats are accurate. | 16299.19
i3 | | 4 | [i3wm.org](http://i3wm.org/) | Works fine under VcXsrv Server 1.19.2.0 without `-multiwindow` command line option. Added `export DISPLAY=:0` to `.bashrc` | 15063.138
ifconfig | | 4 | [wikipedia - ifconfig](https://en.wikipedia.org/wiki/Ifconfig) | Seems to work fine | 15063.138
ip | | 4 | [man ip](http://man7.org/linux/man-pages/man8/ip.8.html) | Seems to work fine | 15063.138
ircii | | 5 | [eterna.com.au/ircii](http://www.eterna.com.au/ircii/) | Seems to work Flawlessly
irssi | | 5 | [irssi.org](https://irssi.org/) | Seems to work flawlessly
iwconfig | | 0 | [wiki.debian.org/iwconfig](https://wiki.debian.org/iwconfig) | Unable to Access Network Interfaces (Should be localhost for all connections)
java 8 | | 2 | [oracle.com/java](http://oracle.com/java/) | Runs at minimum, seems to have some functionality at least
java 7 | | 2 | [oracle.com/java](http://oracle.com/java/) | Seems to work well, if laggy.
Jupyter Notebook | | 5 | [jupyter.org](http://jupyter.org/) | Seems to work well. Requires a browser such as FireFox.
k3b | k3b | 1 | | limited use without hardware access | 17134.68
kakoune | | 5 | [kakoune.org](http://kakoune.org) | Works great, needs to be built from source
kio_camera | kio-extras5 | 0 | | useless without USB | 17134.68
krita | krita | 0 | [krita.org](https://krita.org/en/) | Cannot connect to X server (tested with Xming). Further testing required.
ltrace | ltrace | 5 | | Seems to work Flawlessly
lua | lua5.2 | 3 | [Lua](http://www.lua.org/start.html) | Just tested with interpreter. Needs more tests | 15031 (Xenial)
lynx | | 5 | [lynx.invisible-island.net](http://lynx.invisible-island.net/) | seems to work entirely
mount | | 2 | [man mount](http://man7.org/linux/man-pages/man8/mount.8.html) | unable to mount iso/cd-rom files
Maude | | 4 | [maude.cs.uiuc.edu](http://maude.cs.uiuc.edu/) | Installed without issue, needs more testing
make | | 3 | [gnu.org/software/make](https://www.gnu.org/software/make/) | basic scripts working, needs more extensive testing. Tabbing for commands gets broken pipe
Meteor | | 5 | [meteor.com](https://meteor.com) | Seems to work just fine. Can build and serve apps, create apps, and reads and writes to Windows and Linux | 16275
Metasploit | | 4 | [metasploit.com](https://metasploit.com) | Seems to work as expected.
MLton | | 0 | [mlton.org](http://mlton.org/) | BSOD | 14393
Mongo Client | | 4 | [docs.mongodb.com](https://docs.mongodb.com/getting-started/shell/client/) | Works well connecting to mongod windows service
Mono | mono-complete | 4 | [mono-project.com](http://www.mono-project.com/) | Supported ([more info](https://github.com/mono/website/issues/199)). Instructions added to official documentation. Use 4.2 for now or 4.6 when released (4.4 [has issues](https://bugzilla.xamarin.com/show_bug.cgi?id=42169))|
Minecraft | | 0 | [mincraft.net](https://minecraft.net) | Crashes during boot with an error from OpenAL - [Known Issue](https://github.com/Microsoft/BashOnWindows/issues/1006)
Minecraft Launcher | | 3 | [minecraft.net](https://minecraft.net) | Seems to work correctly, but is incredibly laggy.
mysql | | 4 | [mysql.com](https://www.mysql.com/) | Seems to work flawlessly | 15063.138
mtr | | 0 | [wikipedia - mtr](https://en.wikipedia.org/wiki/MTR_(software)) | doesn't run
nano | | 4 | [nano-editor.org](https://www.nano-editor.org/) | Functions and displays correctly | 16299.19
nasm | | 4 | [nasm.us](http://www.nasm.us/) | more testing needed
netcat | netcat-openbsd | 5 | | works as expected | 17134.68
nethack | | 4 | [nethack.org](https://www.nethack.org/) | Need to run it from the /usr/games directory with "./nethack" and the default config it runs has numpad turned off so you have to use the unintuitive: y k u h l b j n
nginx+ | | 4 | [ngix.com](https://www.nginx.com/) | Can't bind to IPv6 | 15063.138
nmap | | 0 | [nmap.org](https://nmap.org/) | AF_Netsock options not implemented [#1349](https://github.com/Microsoft/BashOnWindows/issues/1349)
[node.js](https://nodejs.org/en/) | nodejs | 4 | [nodejs.org](https://nodejs.org/en/) | Seems to work fine. Runs the React VR hello world project perfectly. | 15063.138
nuget | | 3 | [nuget.org](https://www.nuget.org/) | requires more testing
npm | | 4 | [npmjs.com](https://www.npmjs.com/) | some packages fail due to permissions - Default version is VERY old.
nvm | | 5 | [nvm](https://github.com/creationix/nvm) | Script to install newer versions of NPM and NodeJS.
OCaml | | 4 | [ocaml.org](https://ocaml.org/) | Works fine with Core, needs more testing. | 15063.540
octave | | 3 | [GNU Octave](https://www.gnu.org/software/octave/) | GUI opens with X11, command line calculations are fine, plotting has libgl errors
[OpenCoarrays] | | 4 | [opencoarrays.org] | Installed from source but needs more testing. See [the OpenCoarrays install instructions] for more details |
OpenFOAM | openfoam5 | 5 | [openfoam.org](https://openfoam.org/download/windows-10/) | Works well and comes with Paraview, which has working X11 GUI |
OpenRCT2 | | 0 | [openrtc2.org](https://openrct2.org/) | Fails with errors to do with Sharing Memory with X, Possibly due to VcXsrv.
osc | osc | 5 | | no problems | 17134.68
ping | | 5 | [man ping](http://man7.org/linux/man-pages/man8/ping.8.html) | Works fine
pip+ | | 0 | [pip.pypa.io](https://pip.pypa.io/en/stable/) | **DO NOT INSTALL** with `--fix-missing`. Breaks `apt`. See documentation
php5-cli | | 4 | [php.net/manual](http://php.net/manual/en/features.commandline.php) | Working, needs more testing
php7.0| | 4 | [php.net](http://php.net/) | Installed without issue, needs more testing
postgresql | | 0 | | crashes on start-up after trying to read something from /proc | 14366
python | | 5 | [python.org](https://www.python.org/) | Works even for very difficult and memory intensive workloads such as compiling PyPy | 14366
pypy | | 5 | [pypy.org](https://pypy.org/) | Works even when translating itself | 14366
qpidd | | 0 | [man qpidd](https://linux.die.net/man/1/qpidd) | Starting the daemon fails with a socket error: "critical Unexpected error: Can't bind to port 0.0.0.0:5672: Invalid argument (qpid/sys/posix/Socket.cpp:206)"
qtorrent | qtorrent | 0 | | unable to configure UPnP, may work if not behind NAT | 14366
R | r-base  | 4 |  [r-project.org](https://www.r-project.org/) | devtools, doParallel and foreach works. May be numerically a little different from other system. More tests needed.  | 14393
rbenv | | 4 | [rbenv/rbenv](https://github.com/rbenv/rbenv) | works for the most part, but permissions of folders are wrong after installing (world writable), spawning warnings when running e.g. Rubygems | 14366
reboot | | 0 | [man reboot](http://man7.org/linux/man-pages/man2/reboot.2.html) | Unable to shutdown system.
redis | | 4 | [Redis](https://redis.io/download) | Able to start server and interact with built-client. Did part of tutorial and worked great. | 15031 (Xenial)
rmw | | 5 | [rmw](https://remove-to-waste.info/) | Remove to waste. Safely remove files to a trash folder from the cli.
rsync | | 4 | [rsync.samba.org](https://rsync.samba.org/) | works with ssh tunneling and with same file system. Needs more testing
ruby | | 4 | [ruby-lang.org](https://www.ruby-lang.org/) | works for Sinatra and Rails development using C extension gems for the most part, but `rails new testapp` works with `WeBrick` (the default), but hangs with `thin` | 14986
rustc | | 4 | [rust-lang.org](https://www.rust-lang.org/downloads.html) | Can compile basic programs. Needs testing with more complex programs | 14393.67
Sage Math | | 4 | [http://www.sagemath.org/](http://www.sagemath.org/) | Able to do a good portion of the Sage Math tutorial. There is a RunTime warning but does not stop Sage from working | 15031
scp | | 5 | [man scp](http://man7.org/linux/man-pages/man1/scp.1.html) | works for both remote to local and local to remote transfers.
screen | | 4 | [gnu.org/software/screen](https://www.gnu.org/software/screen/) | Already installed. [Simple fix needed.](https://www.systutorials.com/qa/1639/screen-reporting-cannot-directory-screen-permission-denied?show=1640#a1640) | 15063 (Xenial)
seamonkey | | 4 | | see firefox | 17134.68
sed | | 4 | [gnu.org/software/sed](https://www.gnu.org/software/sed/) | didn't test all options, but everything I tested worked fine.
singularity | | 0 | [singularity](https://singularity.lbl.gov) | doesn't run / can not make mountspace
SMLNJ | | 0 | [smlnj.org](http://www.smlnj.org/) | Installed. Will not start correctly. | 14393
SNMP Tools | snmp | 5 | [www.net-snmp.org](http://www.net-snmp.org) | Seems to work fine | 15063.138
sqlite | | 4 | [sqlite.org](https://www.sqlite.org/) | [File locking is broken](https://github.com/Microsoft/BashOnWindows/issues/2395), which can lead to database corruption
ssh | | 5 | [wikipedia - ssh](https://en.wikipedia.org/wiki/Secure_Shell) | ssh works as expected
ssh-keygen | ssh | 4 | [man ssh-keygen](http://man7.org/linux/man-pages/man1/ssh-keygen.1.html) | -t rsa working
strace | strace | 5 | | Seems to work Flawlessly
sudo | | 5 | [wikipedia - sudo](https://en.wikipedia.org/wiki/Sudo) | appears to be working as expected | 16299.19
SWI-Prolog | | 4 | [swi-prolog.org](http://www.swi-prolog.org/) | Installed without issue, needs more testing. See: [(Installing from PPA (Ubuntu Personal Package Archive))](http://www.swi-prolog.org/build/PPA.txt) | 14393
swift | | 3 | [developer.apple.com/swift](https://developer.apple.com/swift/) | Everything except interactive shell works
systemd | | 0 | useless, invoke rc scripts instead | | 17134.68
tail | | 3 | [man tail](http://man7.org/linux/man-pages/man1/tail.1.html) | Will tail files, but 'follow' (-f) reports "tail: unrecognized file system type 0x53464846"
tea | | 4 | http://semiletov.org | desktop icon missing | 17134.68
tcc | | 3 | [bellard.org/tcc](https://bellard.org/tcc/) | tcc run and scripted "#!/usr/bin/tcc -run" files work correctly
telnet | | 4 | [wikipedia - telnet](https://en.wikipedia.org/wiki/Telnet) | Further testing required
tensorflow | | 4 | [tensorflow/tensorflow](https://github.com/tensorflow/tensorflow) | See [Scott Hanselman's post](http://www.hanselman.com/blog/PlayingWithTensorFlowOnWindows.aspx)
terminator | | 4 | | Multi-terminal emulator. Tested using VcXsvr. | 16299.551
tesseract-ocr | | 4 | [tesseract-ocr/tesseract](https://github.com/tesseract-ocr/tesseract) | No problems with command line usage
texlive | | 5 | [tug.org/texlive](https://www.tug.org/texlive/) | No problems so far | 14366
tmux | | 4 | [tmux/tmux](https://github.com/tmux/tmux) | Works well for the most part, mouse mode doesn't seem to work  | 14366
torproject | tor | 5 | [torproject.org](https://www.torproject.org/) | Tor is a free software that prevents people from learning your location or browsing habits by letting you communicate anonymously on the Internet. | 14393
ufw | | 0 | [help.ubuntu.com/community/UFW](https://help.ubuntu.com/community/UFW) | Fails with an error about iptables | 15063.138
upx | | 1 | [https://upx.github.io/](https://upx.github.io/) | Can't run upx within WSL, but can run ELF binaries compressed with upx, see https://github.com/upx/upx/issues/201 | 18362.113
useradd | | 4 | [man useradd](http://man7.org/linux/man-pages/man8/useradd.8.html) | Users can be added but /etc/skel profile logout and bashrc files but no default directories
usermod | | 5 | [man usermod](http://man7.org/linux/man-pages/man8/usermod.8.html) | Seems to work correctly
vim+ | | 3 | [vim/vim](https://github.com/vim/vim) | Will open and edit Window files it cannot create new files. Can create new linux files. Issues with colorschemes. Plugins don't work. Panes, buffers, and registers appear to be working correctly.
Visual Studio Code | code && code-insider | 5 | [Visual Studio Code](https://code.visualstudio.com) | Will install, but does not launch due to issues relating to Google Chrome with WSL. See: [#758](https://github.com/Microsoft/BashOnWindows/issues/758) Update: [#2760](https://github.com/microsoft/WSL/issues/2760). Redundant, due to the release of VSCode Remote Development (https://code.visualstudio.com/docs/remote/remote-overview) | 16275
vncserver | | 4 | | no sound (did not try too hard) | 17134.68
vsftpd | | 3 | ? | Not installed with apt
wget | | 3 | | Simple commands work. Have only run basic commands
wireshark | | 5 | [wireshark](https://www.wireshark.org) | Works just as expected
WindowMaker | | 5 | | default window manager for Xrdp | 17134.68
xfce4-terminal | | 5 | | Seems to work Perfectly | 15063
startxfce4 (and all subsequent programs) | | 5 | | Everything seems to work, I didn't find anything wrong with it. | 15063
xorg | | 4 | | As Xrdp or Xvnc | 17134.68
xrdp | xrdp | 3 | | due to failing systemd, sesman must be started by hand; the default init script does not work | | 17134.68
xterm | xterm | 4 | | insufficiently tested | | 17134.68
yarn | | 3 | [yarnpkg.com](https://yarnpkg.com/lang/en/) | Works mostly fine. Sometimes really slow due to Windows Defender (whitelisting helps). Global package installations are not always working properly. [wsl performance problems](https://github.com/Microsoft/WSL/issues/1932) [yarn issue](https://github.com/yarnpkg/yarn/issues/990)
YaST | yast2 | 4 | | No icons, otherwise OK | 17134.68
yum | | 0 | | doesn't work at all. will segfault on `yum`, hangs indefinitely with `yum install`
youtube-dl | | 5 | | Works Perfectly
Zipper | gnustep-zipper | 5 | | | 17134.68
zsh | | 4 | | Simple commands work after getting listed WSL build, also checked oh-my-zsh | 14393

[the OpenCoarrays install instructions]: https://github.com/sourceryinstitute/opencoarrays/blob/master/INSTALL.md#windows
[OpenCoarrays]: https://github.com/sourceryinstitute/opencoarrays
[opencoarrays.org]: http://opencoarrays.org
