### blacklist by default
```
ufw default deny
```

### unblock port
```
ufw allow <port>/tcp
```

### block ip address or range
```
ufw deny from <rhost>
```

### whitelist ip address or range
```
ufw allow from <rhost>
```

### limit connections (default 6 connection per 30 seconds)
```
ufw limit <port>/tcp
```

### list all rules
```
ufw status numbered
```

### delete rule
```
ufw delete <id>
```

