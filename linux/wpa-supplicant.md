### connect to wifi using wpa2 passphrase
```
wpa_passphrase <essid>
```

### copy output into
```
/etc/wpa_supplicant/wpa_supplicant.conf
```

### create config
```
wpa_supplicant -B -i <interface> -c /etc/wpa_supplicant.conf
```

### example of configuration with hidden id
```
ctrl_interface=/var/run/wpa_supplicant
update_config=1
ap_scan=1
country=DE

network={  
    ssid="<essid>"  
    psk="<password>"  
    scan_ssid=1  
}  
```

### connect to enteprise network
```
wpa_supplicant -Dnl80211 -i <interface> -c <config>
```

