# cilamp_cfg
Setup a CILAMP using USB cable instead of WiFi web page

# Usage

From terminal:

```
$ python cilamp_cfg.py <SSID> <PASSWORD> <SYSTEMID>")
```

This will send configuration specified at command line
to CILAMP connected to port /dev/ttyUSB0.
This will save credentials SSID+PASSWORD and systemid
on the device and reboot it.
