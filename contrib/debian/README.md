
Debian
====================
This directory contains files used to package bitcupd/bitcup-qt
for Debian-based Linux systems. If you compile bitcupd/bitcup-qt yourself, there are some useful files here.

## bitcup: URI support ##


bitcup-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install bitcup-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your bitcup-qt binary to `/usr/bin`
and the `../../share/pixmaps/bitcup128.png` to `/usr/share/pixmaps`

bitcup-qt.protocol (KDE)

