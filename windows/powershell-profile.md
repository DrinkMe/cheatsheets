### add a new shortcut (run when powershell starts)
```
$<variable> = New-Object -comObject WScript.Shell
$Shortcut = $WshShell.CreateShortcut("$Home\Desktop\<file>.lnk")
$Shortcut.TargetPath = "C:\Users\<user>\<file>.exe"
$Shortcut.Save()
```

