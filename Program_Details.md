# Program Details
------------------
This file is to document behaviour of programs. The main README will serve as a quick note and give key points
whereas this file will contain more in-depth details. 
Please place a `+` in the program name if there are more details than the notes

Program | What works | What doesnt
--------|------------|------------
bash | Normal shell works fine | Scripting has problems. When hitting backspace during a `read` command the key comes up as a ^(box with questionmark inside). This seems to be the response for any unknown unicode character. Scripting gives unusual in that running `sh script` treats echo differently than `chmod +x script; ./script`. Escape characters and variables do not properly work in the latter.
pip | nothing | Does not fully install **DO NOT** install with `--fix-missing`. This will create errors when upgrading through apt. The apt error reports back problems with `udev`, `systemd-services`, `libpam-systemd:amd64`, and `initramfs-tools`
vim | Most functionality exists. Registers, panes, and buffers work as expected under current testing. Can create new linux files. Plugins are working | Problems with colorshemes and fonts
