### show network interfaces
```
iw dev
```

### show informations like frequency etc
```
iw list
```

### scan nearby wifis
```
iw dev <interface> scan
```

### define multiple logical interfaces
```
iw phy phy1 <interface> add mon type monitor flags none
```

### connect to specific wifi
```
iw dev <interface> connect "<essid>"
```

### disconnect
```
iw dev <interface> disconnect
```

### analyse connections
```
iw event -t -f
```

### set device to monitor mode (set device down before executing)
```
iw dev <interface> set type [monitor|managed]
```

