### Account Operators
```
ability to logon on domain controlers - (can not be renamed or deleted)
SID/RID:
S-1-5-32-548
```

### Administrators
```
# members have unrestricted access to the domain - (can not be renamed or deleted)
SID/RID:
1-5-32-544
```

### Allowed Read Only Domain Controler (RODC) Password Replication Group
```
used to manage a RODC password replication policy
SID/RID
S-1-5-21-<domain>-571
```

### Backup Operators
```
members have by default logon rights to domain controllers - (can not be renamed or deleted)
SID/RID
S-1-5-32-551
```

### Certificate Service DCOM Access
```
members are allowed to connect to certification authorities in the enterprise
SID/RID:
S-1-5-32-<domain>-574
```

### Cert Publishers
```
members are authorized to publish certificates for user object
SID/RID:
S-1-5-<domain>-517
```

### Distributed COM Users
```
 members are allowed to launch, activate, and use Distributed COM objects on the computer
Distributed Component Object Model (DCOM) allows applications to be distributed across locations
SID/RID:
S-1-5-32-562
```

### DnsAdmins
```
members have admin rights to AD DNS 
SID/RID:
S-1-5-21-<domain>-1102
```

### Domain Admins
```
group with full admin rights to the active directory domain and all computers
SID/RID:
S-1-5-<domain>-512
```

### Enterprise Admins
```
group with full admin rights to all active directory domains in the AD forest
SID/RID:
S-1-5-21-<rootDomain>-519
```

### Event Log Readers
```
members can read event logs from local computers
SID/RID:
S-1-5-32-573
```

### Group Policy Creators Owners
```
group with the ability to create, edit or delete group policies in the domain
SID/RID:
S-1-5-<domain>-520
```

### Hyper-V Administrators
```
members have complete and unrestricted access to all the features in Hyper-V
SID/RID:
S-1-5-32-578
```

### Pre–Windows 2000 Compatible Access
```
members have read access for all users and groups in the domain
SID/RID:
S-1-5-32-554
```

### Print Operators
```
members can manage, create, share, and delete printers connected to domain controllers - (can not be renamed or deleted)
SID/RID:
S-1-5-32-550
```

### Protected Users
```
members are afforded additional protection (cannot use CredSSP and WDigest, no cleartext credentials caching, no NTLM hash cached, Kerberos does not use DES or RC4 keys)
SID/RID:
S-1-5-21-<domain>-525
```

### Remote Desktop Users
```
used to grant users and groups permissions to remotely connect to an remote desktop session host server - (can not be renamed or deleted)
SID/RID:
S-1-5-32-555
```

### Schema Admins
```
members can modify the active directory schema - group exists only in the root domain of an active directory forest
SID/RID:
S-1-5-<rootDomain>-518
```

### Server Operators
```
members can sign in to a server interactively - (can not be renamed or deleted)
SID/RID:
S-1-5-32-549
```

### WinRMRemoteWMIUsers_
```
group allows running powershell commands remotely
SID/RID:
S-1-5-21-<domain>-1000
```

