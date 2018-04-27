# CILAMP configuration script

Setup a CILAMP using USB cable instead of WiFi web page. This is useful for setting up 10+ units quickly, or if you are in a severy crowded WiFi environment making the WiFi setup page unreliable.


# Preconditions - Ubuntu Linux

This script is written for Python3 and assumes /dev/ttyUSB0 is the name of the serial port. This is the common case for Ubuntu Linux.

Your user needs to be in the 'dialout' group, which is achieved via this command:

    $ sudo adduser $(whoami) dialout

In order to avoid having to login-logout for the changes to take effect, you can use `su` to get a shell with the new group active:

    $ su - $(whoami)


# Installation

Clone this repo and issue:

    $ pip install -r requirements.txt
    

# Usage

From terminal:

    $ python cilamp_cfg.py <SSID> <PASSWORD> <SYSTEMID>

Sends configuration specified at command line to CILAMP connected to port /dev/ttyUSB0.
This saves credentials SSID+PASSWORD and systemid on the device, and reboot it.

The unit should then turn green within 30 seconds. If not, you might have put the wrong
credentials on the command line - try again.

