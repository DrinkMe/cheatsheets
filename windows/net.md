### get domain name and information about administrator
```
net user administrator /domain
```

### get all users in domain
```
net user /domain
```

### unlock domain user account
```
net user <user> /ACTIVE:yes /domain
```

### change domain user password
```
net user <user> "<newpassword>" /domain
```

### create new user
```
net user <user> <password> /add /domain
```

### delete user
```
net user <user> /delete /domain
```


### get all groups in domain
```
net group /domain
```

### get users of a group
```
net group "<group>" /domain
```

### get domain controller
```
net group "Domain Controllers" /domain
```

### add user to group
```
net group "<group>" <user> /add /domain
```


### get domain password policy
```
net accounts /domain
```


### get all user in local admin group
```
net localgroup administrators
```

### add user to a local group
```
net localgroup "<group>" <user> /add
```


### list current SMB shares
```
net share
```

### mount smb share
```
net use <localDrive> \\<rhost>\<remoteDrive>
```

### or 
```
net use * \\<lhost>\<share>
```

### unmount smb share
```
net use <localDrive> \\<rhost>\<remoteDrive> /delete
```

### get active SMB sessions
```
net session
```

### terminate all running sessions
```
net use /delete *
```


### get remote shares
```
net view \\<rhost> /all
```

