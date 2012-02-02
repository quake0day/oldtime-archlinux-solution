oldtime-archlinux-solution, an ArchLinux backup & restore solution based on oldtime
===================================================================================

see https://github.com/GutenYe/oldtime

Getting Started
---------------

prepare

	# /etc/makepkg.conf
		PKGDEST=/home/packages  # store all the packages installed from AUR.

install

	download x

	sudo cp oldtime-archlinux-solution/* /oldtime/oldtime
	modify the files to meet your self need.

backup

	$ sudo oldtime backup archlinux


restore, in a fresh new archlinux system.

	# install oldtime
	$ mount /dev/sdb1 /backup

	# in the first terminal
	$ sudo oldtime -d /backup/oldtime.oldtime/oldtime/oldtime restore archlinux system

	# in the second terminal
	$ sudo oldtime -d /backup/oldtime.oldtime/oldtime/oldtime restore archlinux file


