# test for SSRF vulnerability
```
GET http://<someLongString>.<domain> HTTP/1.1  
Host: <rhost>  
Pragma: no-cache  
Cache-Control: no-cache, no-transform  
Connection: close  
```

### check tcpdump for incoming traffic on DNS server
```
sudo tcpdump -i <interface> -nn -s0 -v port 53
```


