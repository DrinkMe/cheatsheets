### source
https://github.com/ShawnDEvans/smbmap  

### list mountable shares on remote host
```
smbmap -d <domain> -H <rhost>
```

### check if user is admin and skip banner for file containing hosts
```
smbmap -d <domain> --host-file <file>.txt -u <user> --prompt --admin --no-banner
```

