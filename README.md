# WSL-Programs
A community powered list of programs that work (and those that don't) on the Windows subsystem for Linux. The official Microsoft repository for filing bugs etc is located [here](https://github.com/Microsoft/BashOnWindows). This repo complements the offical one by providing a quick reference for how well programs run.

Please feel free to contribute programs you have tested to the table below. If you need help with the markdown, please review [a primer](https://help.gamejolt.com/markdown)

To contribute, please make a Pull Request, I will merge if it looks good! If you have never made a pull request it is fast and easy, please check out the [Github documentation](https://help.github.com/articles/using-pull-requests/)

Then add your program below!

If you need to add more details about a program then add a `+` symbol to its name and add it to the `Program_Details.md` file.

#The list:

Program Name  | apt name if different (blank otherwise) | Functionality rating (0-5) | website if not on apt | Notes  | Windows Build #
------------- | --------------------------------------- | -------------------------- | --------------------- | -------|----------
Anaconda || 0 | [Continuum.io](https://www.continuum.io/downloads) | Will not install. Fails at symbolic links.
Apache server | apache2 | 2 | | Must use a loopback for networking, buggy
apt | | 3 | | Problems with `autoremove`, `remove`, and `--fix-missing`
bash+ | | 3 | | Most functionality exists but there are problems with scripts
curl | | 4 | | curl -sS tested
docker | | 0 | | doesn't run / says not installed
fortune | | 5| | works fine
gcc | build-essential | 4 | | more testing needed
git | | 4 | | requires more testing, Basics work (clone, pull, push, fetch commit). Diff has some errors
ifconfig | | 0 | | Unable to Access Network Interfaces (Should be localhost for all connections)
ip | | 0 |  | Unable to Access Network Interfaces (Should be localhost for all connections)
iwconfig | | 0 | | Unable to Access Network Interfaces (Should be localhost for all connections)
java | | 0 | | does not install
lynx | | 5 | | seems to work entirely
make | | 3 | | basic scripts working, needs more extensive testing. Tabbing for commands gets broken pipe
mtr | | 0 | | doesn't run
Mono | mono-complete | 4 | | Supported ([more info](https://github.com/mono/website/issues/199)). Instructions added to official documentation. | 
nano | | 3 | | Functions correctly, but does not display correctly
nasm | | 4 | | more testing needed
nethack | | 4 | | Need to run it from the /usr/games directory with "./nethack" and the default config it runs has numpad turned off so you have to use the unintuitive: y k u h l b j n
nuget | | 3 | | requires more testing
npm | | 4 | | some packages fail due to permissions
ping | | 0 | | Fails with `ping: icmp open socket: Socket type not supported`
pip+ | | 0 | | **DO NOT INSTAL** with `--fix-missing`. Breaks `apt`. See documentation 
php5-cli | | 4 | | Working, needs more testing
qpidd | | 0 | | Starting the daemon fails with a socket error: "critical Unexpected error: Can't bind to port 0.0.0.0:5672: Invalid argument (qpid/sys/posix/Socket.cpp:206)"
scp | | 5 | | works for both remote to local and local to remote transfers.
screen | | 0 | | Already installed. Gives permission denied if not sudouser and doesn't start if given permissions
sed | | 4 | | didn't test all options, but everything I tested worked fine. 
ssh | | 4 | | ssh -i works
ssh-keygen | ssh | 4 | | -t rsa working
sudo | | 5 | | appears to be working as expected
swift | | 3 | ? | Everything except interactive shell works	
tail | | 3 | | Will tail files, but 'follow' (-f) reports "tail: unrecognized file system type 0x53464846"	
telnet | | 4 | | Further testing required
tensorflow | | 4 | | See [Scott Hanselman's post](http://www.hanselman.com/blog/PlayingWithTensorFlowOnWindows.aspx)
tesseract-ocr | | 4 | | No problems with command line usage
tmux | | 0| | No server starts but it installs
useradd | | 4 | | Users can be added but /etc/skel profile logout and bashrc files but no default directories
usermod | | 5 | | Seems to work correctly
vim+ | | 3 | | Will open and edit Window files it cannot create new files. Can create new linux files. Issues with colorschemes. Plugins don't work. Panes, buffers, and registers appear to be working correctly. 
vsftpd | | 3 | ? | Not installed with apt
wget | | 3 | | Simple commands work. Have only run basic commands
xorg | | 4 | | Requires Configuration and an X server on Windows
yum | | 0 | | doesn't work at all. will segfault on `yum`, hangs indefinitely with `yum install`
zsh | | 0 | | Installs and seems to switch shells but has no functionality
ADB | | 0 | android-adb-tools | Installs but it doesnt recognize any device even with the Windows aDB drivers installed
