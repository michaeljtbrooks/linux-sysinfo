# linux-sysinfo
A simple tool to find info about your system when you can't remember all the different little commands.

## Installation ##

Copy sysinfo.sh into your /usr/bin:
    
    sudo cp ./sysinfo.sh /usr/bin/sysinfo 
    sudo chmod +x /usr/bin/sysinfo
    
You can now call it with ```sysinfo <item>```

### Dependencies ###
For temperature sensors to work, you either need /opt/vc/bin/vcgencmd from Raspbian (Raspberry Pi), or lm-sensors installed.

## Usage ##
	Usage:
		sysinfo [item]

	Items:
		kernel        Current kernel details
		linux         Current kernel details

		hostname      Network host name
		name          Network host name

		distro        The Linux distro including version
		release       The Linux distro including version
		lsb_release   The Linux distro including version
		lsb_release   The Linux distro including version

		version       The Linux distro version and kernel version
		os            The Linux distro version and kernel version
		os-version    The Linux distro version and kernel version
		osversion     The Linux distro version and kernel version

		space         The amount of disk space available and used
		disk          The amount of disk space available and used
		storage       The amount of disk space available and used

		disk-ids      Storage devices, partitions and space used
		disk-id       Storage devices, partitions and space used
		diskids       Storage devices, partitions and space used
		diskid        Storage devices, partitions and space used
		blkids        Storage devices, partitions and space used
		lsblk         Storage devices, partitions and space used
		uuid          Storage devices, partitions and space used
		uuids         Storage devices, partitions and space used
		hdd           Storage devices, partitions and space used
		hdds          Storage devices, partitions and space used
		sdd           Storage devices, partitions and space used
		sdds          Storage devices, partitions and space used

		memory        The amount of RAM used and free
		ram           The amount of RAM used and free
		mem           The amount of RAM used and free

		signal        Wifi network and signal strength
		wifi          Wifi network and signal strength

		all           Show everything above

		signal-all    All detected wifi networks and signal strength (sudo only)
		wifi-all      All detected wifi networks and signal strength (sudo only)


### FAQs ###
_Why do I need this sysinfo programme?_

You don't really. Unless you struggle to remember infrequently used commands like ```lsblk -f``` and ```lsb_release -a```, or the difference between ```du``` and ```df```.

_What's wrong with the original unix commands?_

Nothing. Except I can never remember them.

_My wifi adaptor is called something other than wlan0. What do I do?_

Change all mentions of ```wlan0``` to the name of your wifi adaptor in sysinfo.sh.
