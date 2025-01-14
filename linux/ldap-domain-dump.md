### source
https://github.com/dirkjanm/ldapdomaindump  

### basic usage
```
python3 ldapdomaindump -u <domain>\\<user> -p <password> <ipOfDomainController> -d "|"
```

### using LDAPS
```
python3 ldapdomaindump -u <domain>\\<user> -p <password> ldaps://<ipOfDomainController> -d "|" 
```

### operating system overview
```
grep -v ACCOUNT_DISABLE domain_computers.grep | cut -d \| -f4 | sort | uniq -c | sort -n
```

### list valid account names
```
grep -v ACCOUNT_DISABLED domain_users.grep | cut -d \| -f3
```

### convert data to import into bloodhound
```
python3 ldapdomaindump/convert.py domain_users.json domain_groups.json
```

