### source
https://github.com/OpenSecurityResearch/hostapd-wpe  

### general information to clone access point
```
get vendor of to clone access point
dont use the same bssid and channel -> otherwise you create conflicts and probably DOS
```

### copy example config
```
/etc/hostapd-wpe/hostapd-wpe.conf
```

### edit copied config
```
interface=<interface>
...
eap_user_file=/etc/hostapd-wpe/hostapd-wpe.eap_user
ca_cert=/etc/hostapd-wpe/certs/ca.pem
server_cert=/etc/hostapd-wpe/certs/server.pem
private_key=/etc/hostapd-wpe/certs/server.key
private_key_passwd=<password>
dh_file=/etc/hostapd-wpe/certs/dh
ssid=hostapd-wpe                                                                                   
channel=1
...
bssid=<bssid>
```

### launch evil twin attack (in config at least interface, ssid and channel must be set)
```
hostapd-wpe -c hostapd-wpe.conf
```

### create custom certificates using example certs
```
/etc/hostapd-wpe/certs
```

### delete all certificates
```
make destroycerts
```

### create new dh-param
```
./bootstrap
```

### edit certs
```
vim ca.cnf
```

### create new certificates 
```
make ca
make client
make server
```

### karma mode
```
hostapd-wpe -k <config>
```

