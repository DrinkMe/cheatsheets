### show saved wireless profiles
```
netsh wlan show profiles
```

### get the clear-text password 
```
netsh wlan show profile <ssid> key=clear
```

### list interfaces 
```
netsh interface ip show interfaces
```

### set new dns server
```
netsh interface ip set dns local static <rhost>
```

### list proxy settings
```
netsh winhttp show proxy
```

