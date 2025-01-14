## wmic uses port 135 to determine a random port for further communication - appears to not work with Fully Qualified Domain Names

### enable WinRM remotely
```
wmic /node:"<rhost>" process call create "powershell enable-psremoting -force"
```

### get user accounts
```
wmic useraccount get name,fullname
```

### get password expire value of accounts
```
wmic useraccount get name,passwordexpires /Value
```

### unlock user account
```
wmic useraccount where name='username' set disabled=true
```

### get os informations
```
wmic os list Brief /format:list
wmic os get ServicePackMajorVersion,Caption,OSArchitecture
```

### list all patches
```
wmic qfe
```

### get domain name
```
wmic computersystem get domain
```

### display architecture (32/64 bit)
```
wmic cpu get DataWidth /format:list
```

### list services that start automatically
```
wmic SERVICE WHERE StartMode="Auto" GET Name, State
```

### execute process
```
wmic process call create "<processName>"
```

### kill process
```
wmic process where name="<processName>" call terminate
```

### view logical shares
```
wmic logicaldisk get description,name
```

### remotely determine logged in user
```
wmic /node:"<rhost>" computersystem get username
```

### execute file hosted over SMB on remote system with specified credential
```
wmic /node:"<rhost>" /user:"<domain>\<user>" /password:<password> process call create "\\<rhost>\<share>\<file.exe>"
```

### remotely start RDP
```
wmic /node:"<rhost>" path Win32_TerminalServiceSetting where AllowTSConnections="0" call SetAllowTSConnections "1"
```

### execute command
```
wmic /node:"<rhost>" /user:"<domain>\<user>" /password:"<password>" process call create "powershell <command>"
```

