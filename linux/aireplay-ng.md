### source
https://github.com/aircrack-ng/aircrack-ng  

### check packet loss - simulate clients that want to connect
```
aireplay-ng --test -a <ssid> <interface>
```

### deauthenticate clients (useful to get hidden ESSIDs)
```
aireplay-ng --deauth 1 -a <ssid> <interface>
```

### replay arp packages
```
aireplay-ng <interface> --arpreplay -b <bssid>
```

