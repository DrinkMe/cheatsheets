### clear auth.log file
```
echo "" > /var/log/auth.log
```

### clear current user bash history
```
echo "" > ~/.bash_history
```

### clear current session history
```
history -c
```

### set history max lines to 0
```
export HISTFILESIZE=O
```

### set history max commands to 0
```
export HISTSIZE=O
```

### disable hisotry logging (need to logout to take effect)
```
unset HISTFILE
```

### kill current session
```
kill -9 $$
```

### permanently send all bash history commands to /dev/null
```
ln /dev/null ~/.bash–history -sf
```

