### get all usernames without limit 
```
$res = ([adsisearcher]"(objectClass=user)"); $res.PageSize = 1000; $res.FindAll().Properties.samaccountname
```

### get all computer object 
```
$res = ([adsisearcher]"(objectClass=computer)"); $res.PageSize = 1000; $res.FindAll().Properties | convertto-json
```

### get domain admins
```
([adsisearcher]"(&(objectClass=user)(admincount=1))").FindAll().Properties.samaccountname
```

### query for specific user
```
([adsisearcher]"(&(objectClass=user)(samaccountname=<user>))").FindAll().Properties | convertto-json
```

### query for azure ad connect server
```
([adsisearcher]"(samaccountname=MSQL_*)").FindAll().Properties
```

### get distinguished name of specific user
```
([adsisearcher]"(&(objectClass=user)(samaccountname=<user>))").FindAll().Properties.distinguishedname
```

### print network ranges
```
$s=[adsisearcher]'(name=*)'; $s.SearchRoot = [adsi]"LDAP://cn=Subnets,cn=Sites,cn=Configuration,dc=<domainComponent>,dc=<domainComponent>"; $s.FindAll() | Select *
```

