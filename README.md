oldtime-archlinux-solution, a ArchLinux backup & restore solution based on oldtime
===================================================================================

It's a personal solution, eveyone can write your own config file.  

Getting Started
---------------

prepare

	# /etc/makepkg.conf
		PKGDEST=/home/packages  # store all the packages installed from AUR.

	# /oldtime/oldtimerc
		media = "/backup"

install

	$ wget https://github.com/GutenYe/oldtime-archlinux-solution/tarball/master
	$ tar xvf master
	$ sudo cp GutenYe-oldtime-archlinux-solution-xx/* /oldtime/oldtime
	# modify the files to meet your self need.

backup

	# mount /dev/sdb1 /backup
	$ sudo oldtime backup archlinux

restore, in a fresh new archlinux system.

	# install oldtime
	$ mount /dev/sdb1 /backup

	# in the first terminal
	$ sudo oldtime restore archlinux system -d /backup/archlinux.oldtime/oldtime/oldtime

	# in the second terminal
	$ sudo oldtime restore archlinux file -d /backup/archlinux.oldtime/oldtime/oldtime

for more information, please see https://github.com/GutenYe/oldtime
