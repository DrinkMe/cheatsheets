### send mail without authentication
```
sendmail -f "<sender@domain>" -t "<receiver@domain>" -u "<subject>" -o message-file=<content.html> -o message-content-type=<html> -o message-charset=<utf8> -s <mailServerIp>
```

