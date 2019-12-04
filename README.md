# osd
Minimalistic meter-style osd (on-screen display) for GNU/Linux

# Purpose
Create a short-lived osd; repeat calls during timeout period update the existing osd.

# What you need
0. GNU/Linux operating system and this script
1. **dzen2**

# Installation
```
$ sudo apt install dzen2
$ cd /tmp
$ wget https://github.com/bdantas/osd/archive/master.zip
$ unzip master.zip
$ cd osd-master
$ sudo cp osd /usr/local/bin
```
Note: If your operating system is not Debian-like, adjust the first step

# Usage
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
If subsequent calls to *osd* with the same first argument (osd title) are made within the timeout period (2 seconds by default), the subsequent calls update the existing osd instead of creating a new one.
