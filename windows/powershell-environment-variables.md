### get all windows environment variables
```
gci env:
```

### print specific variable
```
echo $env:userdomain
```

### fully qualified domain name
```
echo $env:computername.$env:userdnsdomain
```

### last error message
```
echo $Error[0]
```

### current powershell profile
```
echo $profile
```

### show all variables of current scope
```
Get-ChildItem Variable:\
```

### equivalent to /dev/null
```
$null
```

### current process id
```
$PID
```

### status of last executed command
```
$?
```

