# WSL-Programs
A community powered list of programs that work (and those that don't) on the Windows subsystem for Linux

Please feel free to contribute programs you have tested to the table below. If you need help with the markdown, please review [a primer](https://help.gamejolt.com/markdown)

To contribute, please make a Pull Request, I will merge if it looks good! If you have never made a pull request it is fast and easy, please check out the [Github documentation](https://help.github.com/articles/using-pull-requests/)

Then add your program below!

#The list:

Program Name  | apt name if different (blank otherwise) | Functionality rating (0-5) | website if not on apt | Notes
------------- | --------------------------------------- | -------------------------- | --------------------- | ------------------
xorg | | 4 | | Requires Configuration and an X server on Windows
nano | | 3 | | Functions correctly, but does not display correctly
ip | | 0 |  | Unable to Access Network Interfaces (Should be localhost for all connections)
ifconfig | | 0 | | Unable to Access Network Interfaces (Should be localhost for all connections)
iwconfig | | 0 | | Unable to Access Network Interfaces (Should be localhost for all connections)
Apache server | apache2 | 2 | | Must use a loopback for networking, buggy
gcc | build-essential | 4 | | more testing needed
mtr | | 0 | | doesn't run
docker | | 0 | | doesn't run / says not installed
npm | | 4 | | some packages fail due to permissions
ssh | | 4 | | ssh -i works
lynx | | 5 | | seems to work entirely
vim | | 3 | | Will open and edit Window files it cannot create new files. Issues with colorschemes.
vsftpd | | 3 | ? | Not installed with apt
swift | | 3 | ? | Everything except interactive shell works
ping | | 0 | | Fails with `ping: icmp open socket: Socket type not supported`
nethack | | 4 | | Need to run it from the /usr/games directory with "./nethack" and the default config it runs has numpad turned off so you have to use the unintuitive: y k u h l b j n
java | | 0 | | does not install
nuget | | 3 | | requires more testing
git | | 4 | | requires more testing, Basics work (clone, pull, push, fetch commit)
ssh-keygen | ssh | 4 | | -t rsa working
make | | 3 | | basic scripts working, needs more extensive testing. Tabbing for commands gets broken pipe
curl | | 4 | | curl -sS tested
php5-cli | | 4 | Working, needs more testing