# osd
Minimalistic meter-style osd (on-screen display) for GNU/Linux

# Purpose
Create meter-style osd that can be dynamically updated during user-defined timeout period

# What you need
0. GNU/Linux operating system and this script
1. **dzen2**

# Installation
```
$ sudo apt install dzen2
$ cd /tmp
$ wget https://github.com/bdantas/osd/archive/master.zip
$ unzip master.zip
$ sudo cp ./osd-master/osd /usr/local/bin
$ sudo chmod a+x /usr/local/bin/osd
```
Note: If your operating system is not Debian-like, adjust the first step

# Usage examples
The script takes four arguments: osd title, setting to display, minimum possible setting, maximum possible setting.

Examples:
```
$ osd Volume 70 0 100
$ osd Volume 80 0 100
$ osd Volume 90 0 100
```
```
$ osd Brightness 10 0 15
$ osd Brightness 11 0 15
$ osd Brightness 12 0 15
```
If subsequent calls to *osd* have the same first argument (osd title) and are made within the user-defined timeout period, the existing osd will be updated (i.e., there will not be multiple osd's stacked on top of one another).

# Application
If you use a shell script to change your volume, display brightness, or other system setting, calling *osd* from your script is a convenient way to display the current setting.
