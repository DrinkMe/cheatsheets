### mount remote share
```
mount -t <filesystem> <rhost>:<port>/<share>
```

### mount nfs share (port 2049), -o vers=2 for nfs protocol version 2
```
mount vers=2 -t nfs <rhost>:<share> nolock
```

### set complete filesystem to read write
```
mount -o remount, rw /
```

