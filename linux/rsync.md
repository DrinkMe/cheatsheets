### source
https://github.com/WayneD/rsync  

### list files 
```
rsync -av --list-only rsync://<rhost>/<share> 
```

### copy files via rsync without authentication
```
rsync -av rsync://<rhost>:<rport>/<share> <localDir>
```

### copy files via rsync with authentication
```
rsync -av rsync://<user>@<rhost>:<rport>/<share> <localDir>
```

### upload ssh key file
```
rsync -av ~/.ssh/ rsync://<user>@<rhost>/<rhome>/.ssh
```

