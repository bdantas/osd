# osd
Minimalistic meter-style osd (on-screen display) for GNU/Linux

# Purpose
Create a short-lived osd; repeat calls during timeout period update the existing osd

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
The script takes four arguments: osd title, setting, minimum setting, maximum setting.

For example:
```
$ osd Volume 70 0 100
$ osd Volume 80 0 100
```
If the two calls are made within the timeout period (2 seconds by default), the second call will update the existing osd instead of creating a new one.
