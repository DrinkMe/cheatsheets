### use # as separating char, print 2. and 3. argument
```
cat <file> | awk -F '#' '{print $2,$3}'
```

### get all user in group vboxusers
```
awk -F ':' '/vboxusers/{print $4}' /etc/group
```

### convert to lower case
```
awk '{print tolower($0)}'
```

### print line if less 10 chars
```
awk 'length($0) < 10 { print $0 }'
```

