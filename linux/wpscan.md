### source
https://github.com/wpscanteam/wpscan  

### scan for vulnerable themes, timthumbs, user, all plugins
```
wpscan -e vt,tt,u,ap --disable-tls-checks --no-banner --url http://<rhost>
```

### bruteforce login
```
wpscan --passwords <file>.txt -U <user> --url <rhost>
```

