### show if network manager manages interface
```
nmli device
```

### disable interface for network manager
```
nmcli device set <interface> managed no
```

### show all connections
```
nmcli connection
```

### list available wifis (passiv)
```
nmcli device wifi list
```

### rescan for available wifis (active)
```
nmcli device wifi rescan
```

