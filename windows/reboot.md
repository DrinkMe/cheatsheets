### using powershell
```
Restart-Computer -Force -ComputerName <fqdnRhost>
```

### using cmd
```
shutdown -r
```

### reboot remote device (-m remote machine, -t = wait 0 seconds, -f = force)
```
shutdown -m \<fqdnRhost> -t 0 -r -f
```

### using rundll32 (numbers: 0=logoff, 1=shutdown, 2=reboot, 4=force, 8=power off)
```
rundll32.exe user.exe,ExitWindowsExec 2
```

