### source
https://github.com/darkoperator/dnsrecon  

### d domain, D dictionary, t type standard, gb google bing
```
dnsrecon -d <domain> -D <file> -t <std> -gb
```

### enumerate subdomains
```
dnsrecon -t <brt> -d <domain> 
```

### zonewalking
```
dnsrecon -d <domain> -t zonewalk
```

### zone transfer
```
dnsrecon -d <domain> -a -n <dnsIp>
```

### reverse lookup for IP range
```
dnsrecon -r <192.168.0.0-192.168.0.255>
```

### top level domain enumeration
```
dnsrecon -d <domain> -t tld
```

