### source
https://github.com/sullo/nikto  

### run nikto with all tunings except DOS
```
nikto -Tuning x 6 -h <domain> -port <rport>,<rport>
```

### use with basic authentication
```
nikto -id <id:password> -h <rhost>
```

### choose specific Tuning
```
nikto -Tuning 012 -h <rhost>
```

### tuning options
```
0 - File Upload
1 - Interesting File / Seen in logs
2 - Misconfiguration / Default File
3 - Information Disclosure
4 - Injection (XSS/Script/HTML)
5 - Remote File Retrieval - Inside Web Root
6 - Denial of Service
7 - Remote File Retrieval - Server Wide
8 - Command Execution / Remote Shell
9 - SQL Injection
a - Authentication Bypass
b - Software Identification
c - Remote Source Inclusion
```

