### start bluetooth interface
```
hciconfig
hciconfig hci0 up
```

### scan for devices
```
hcitool scan -all
```

### will write results into current directory
```
btscanner
```

### for scanning over long period of time
```
bluelog -v
```

### get position of target device
```
blueranger.sh hci0 <address>
```

### debug connections
```
btmon
```

