### add registry entry
```
reg add <path> /v <value> /t <type> /d <pathToFile>
```

### delete registry entry 
```
reg delete "<path>" /v <value> /f
```

### add example (REG_SZ UTF-16 LE string)
```
reg add "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run" /v someRegistry /t REG_SZ /d "C:\Users\username\persist.exe"
```

### delete example
```
reg delete HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run /v someRegistry /f
```

### get information about registry key
```
reg query "<path>"
```

### write security hive to file
```
reg save hklm\security <file>
```


### re-enable command prompt
```
reg add HKCU\Software\Policies\Microsoft\Windows\System /v DisableCMD /t REG_DWORD /d 0 /f
```

### disable remote user account control (UAC) local account token filter policy
```
reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\system /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1 /f
```

### enable remotely RDP
```
reg add "\\<rhost>\HKLM\SYSTEM\CurentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f
```

### read configured Windows defender exclusions
```
reg query "HKLM\SOFTWARE\Microsoft\Windows Defender\Exclusions" /s
```

