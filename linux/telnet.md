### execute command reading from a file (example send mail using smtp) - bash <file>.sh
```
{
    sleep 3;
    echo "HELO <domain>"
    sleep 3;
    echo "MAIL FROM: <mai1>"
    sleep 3;
    echo "RCPT TO: <mail2>"
    sleep 3;
    echo "DATA"
    sleep 3;
    echo "<text>"
    sleep 3;
    echo ""
    sleep 3;
    echo "."
    sleep 3;
    echo "QUIT"
} | telnet <rhost> 25
```

