oldtime-archlinux-solution, a ArchLinux backup & restore solution based on oldtime
===================================================================================

| Homepage:      |  https://github.com/GutenYe/oldtime-archlinux-solution       |
|----------------|------------------------------------------------------       |
| Author:	       | Guten                                                 |
| License:       | MIT-LICENSE                                                |
| Issue Tracker: | https://github.com/GutenYe/oldtime-archlinux-solution/issues |

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

Note on Patches/Pull Requests
-----------------------------

1. Fork the project.
2. Make your feature addition or bug fix.
3. Add tests for it. This is important so I don't break it in a future version unintentionally.
4. Commit, do not mess with rakefile, version, or history. (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
5. Send me a pull request. Bonus points for topic branches.
6. Coding Style Guide: https://gist.github.com/1105334

Credits
-------

* [Contributors](https://github.com/GutenYe/oldtime-archlinux-solution/contributors)

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
