### load native module
```
rundll32 dsquery
```

### list users on domain with no limit on results
```
rundll32 dsquery user -limit 0
```

### list groups for given distinguished name
```
rundll32 dsquery group "cn=users, dc=<domainComponent>, dc=<domainComponent>"
```

### list domain admin accounts
```
rundll32 dsquery group -name "<domain admins>" | rundll32 dsget group -members -expand
```

### list all groups for a specific user
```
rundll32 dsquery user -name <user>* | rundll32 dsget user -memberof -expand
```

### list all operating systems on domain
```
rundll32 dsquery * "DC=<domainComponent>,DC=<domainComponent>" -scope subtree -attr "en" "operatingSystem" "operatingSystemServicePack" -filter "(&(objectclass=computer) (objectcategory=computer) (operatingSystem=Windows*))"
```

### find servers in the domain
```
rundll32 dsquery * domainroot -filter "(&(objectCategory=Computer) (objectClass=Computer) (operatingSystem=*Server*))" -limit 0
```

