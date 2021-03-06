oldtime-archlinux-solution, a ArchLinux backup & restore solution based on oldtime
===================================================================================

| Homepage:      |  https://github.com/GutenYe/oldtime-archlinux-solution       |
|----------------|------------------------------------------------------       |
| Author:	       | Guten                                                 |
| License:       | MIT-LICENSE                                                |

This solution is based on [oldtime](https://github.com/GutenYe/oldtime). And it's a personal solution, eveyone can write your own config file.  

Getting Started
---------------

prepare

	# /etc/makepkg.conf
		PKGDEST=/home/pkg  # store all the packages installed from AUR.

	# /oldtime/oldtimerc
		media = "/backup"

install

	$ wget https://github.com/GutenYe/oldtime-archlinux-solution/tarball/master
	$ tar xvf master
	# cp GutenYe-oldtime-archlinux-solution-xx/* /oldtime/oldtime
	modify the files to meet your need.

backup

	# mount /dev/sdb1 /backup
	# oldtime backup archlinux

restore, in a fresh new archlinux system.

	install oldtime
	# mount /dev/sdb1 /backup

	in the first terminal
	# oldtime restore archlinux system -d /backup/archlinux.oldtime/oldtime/oldtime
	uncomment custom source in /etc/pacman.conf
	# pacman -S `cat pkg.lst` -f
	# pacman -S `cat aur.lst` -f
	# oldtime restore etc -d /backup/archliniux.oldtime/oldtime/oldtime
	manual restore /backup/archlinux.machine_etc

	in the second terminal
	# oldtime restore archlinux root -d /backup/archlinux.oldtime/oldtime/oldtime

Resources
---------

*	[oldtime](https://github.com/GutenYe/oldtime): The backup & restore system that fits you well.

Copyright
---------

(the MIT License)

Copyright (c) 2011 Guten

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
