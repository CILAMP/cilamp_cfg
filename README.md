# CILAMP configuration script

Setup a CILAMP using USB cable instead of WiFi web page


# Preconditions

This script is written for Python3 and assumes /dev/ttyUSB0 is the name of the serial port. This is the common case for Ubuntu Linux.


# Installation

Clone this repo and then:

    $ pip install -r requirements.txt
    

# Usage

From terminal:

```
$ python cilamp_cfg.py <SSID> <PASSWORD> <SYSTEMID>
```

This will send configuration specified at command line
to CILAMP connected to port /dev/ttyUSB0.
This will save credentials SSID+PASSWORD and systemid
on the device and reboot it.
