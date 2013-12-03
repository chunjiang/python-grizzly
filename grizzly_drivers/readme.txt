###############################################################################
This file documents some of the dependencies required to make the grizzly usb
drivers work with linux. Currently only supports linux and tested on ubuntu.
###############################################################################

Library or package:			How to install:
pyusb					sudo pip install pyusb
xboxdrv					sudo apt-get install xboxdrv

Some notes:
To use this library, look at the source or look at RunGrizzly.py
Try using RunGrizzly.py:
1. Plug in xbox controller and grizzly.
2. Power on the grizzly.
3. Run sudo python RunGrizzly.py
*Note that you must run python with sudo to gain access to usb privileges.
4. Now the right analog stick in the y-direction controls the Grizzly throttle.

xbox_read.py shamelessly copypasta'd from http://github.com/zephod/lego-pi
It could use some refactoring. If somebody wants to write a good parser for it.

xboxdrv is kinda buggy. It can be annoying to try and connect to the xbox
controller. Usually it gets autoloaded when you plug it in and the driver cannot
get a usb lock on it. Try running:
    ajc ~ $ sudo rmmod xpad
then trying RunGrizzly.py

