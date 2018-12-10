
Debian
====================
This directory contains files used to package startlifed/startlife-qt
for Debian-based Linux systems. If you compile startlifed/startlife-qt yourself, there are some useful files here.

## startlife: URI support ##


startlife-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install startlife-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your startlifeqt binary to `/usr/bin`
and the `../../share/pixmaps/startlife128.png` to `/usr/share/pixmaps`

startlife-qt.protocol (KDE)

