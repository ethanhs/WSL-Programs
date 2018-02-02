# Program Details
------------------
This file is to document behaviour of programs. The main README will serve as a quick note and give key points
whereas this file will contain more in-depth details.
Please place a `+` in the program name if there are more details than the notes

Program | What works | What doesnt
--------|------------|------------
bash | Normal shell works fine | Scripting has problems. When hitting backspace during a `read` command the key comes up as a ^(box with questionmark inside). This seems to be the response for any unknown unicode character. Scripting gives unusual in that running `sh script` treats echo differently than `chmod +x script; ./script`. Escape characters and variables do not properly work in the latter.
emacs | Emacs 24 as distributed with Ubuntu will hang when connecting to an X11 server, as previously noted.  However, Emacs can be built from the FSF Git repo under WSL, and will work with X11.  Tested was the "emacs-25" branch, built with the following configure arguments: "./configure --prefix=/usr/local --program-suffix=-25 --enable-locallisppath=/usr/share/emacs:/usr/share/emacs24 --with-sound=yes --with-gnutls --with-x -with-cairo=no --with-x-toolkit=gtk2 --with-wide-int --with-m17n-flt --with-file-notification=yes".  Note that many development libraries need to be installed.  Try "apt-get build-dep emacs24" to get most of them. |  A build with the Gtk3 toolkit built and connected to X11, however the window failed to resize properly.  With Gtk2, everything seems to work so far with the exception of clipboard sharing with Windows 10.  This may be an issue with the X server.
nginx | everything but IPv6 binding | IPv6: you need to remove it from your config. Default configuration: you need to add `master_process off;` to `/etc/nginx/nginx.conf`
pip | nothing | Does not fully install **DO NOT** install with `--fix-missing`. This will create errors when upgrading through apt. The apt error reports back problems with `udev`, `systemd-services`, `libpam-systemd:amd64`, and `initramfs-tools`
+sshuttle | normal ssh works fine | It won't pass traffic properly and [there is a problem](https://github.com/Microsoft/WSL/issues/767) with accessing `iptables`. This is tested on Windows 10 Home, ver 1607, Build 14393
vim | Most functionality exists. Registers, panes, and buffers work as expected under current testing. Can create new linux files. Plugins are working | Problems with colorshemes and fonts
