### get domain name and domain controler
```
[System.DirectoryServices.ActiveDirectory.Domain]::GetCurrentDomain()
```

### get forest information
```
[System.DirectoryServices.ActiveDirectory.Forest]::GetCurrentForest()
```

### get domain trusts
```
[System.DirectoryServices.ActiveDirectory.Domain]::GetCurrentDomain().GetAllTrustRelationships()
```

### get forst trusts
```
[System.DirectoryServices.ActiveDirectory.Forest]::GetCurrentForest().GetAllTrustRelationships()
```

### query active directory domain services for specific computer object
```
$domainObject = New-Object System.DirectoryServices.DirectoryEntry "LDAP://<domainConrollerIp>", <user>, "<password>"
$searchObject = New-Object System.DirectoryServices.DirectorySearcher $domainObject
$searchObject.Filter = "(&(objectCategory=Computer)(name=<name>))"
$searchObject.FindAll().properties
```

### query active directory domain services for all computer or user object 
```
$searchObject.Filter = "(|(objectCategory=Computer)(objectCategory=User))"
$searchObject.FindAll() | Select -Expand Properties
```

