### source
https://raw.githubusercontent.com/SecureAuthCorp/impacket/master/examples/GetADUsers.py  

### list all user inside the domain (-dc-ip must only be passed if DNS is not available)
```
impacket-GetADUsers -dc-ip <domainController> <domain>/<user>:<password> -all
```

