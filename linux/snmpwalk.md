### enumerate entire MIC Tree
```
snmpwalk -c public -v1 <rhost>
```

### enumerate windows user (processNumber example 1.3.6.1.4.1.77.1.2.25)
```
snmpwalk -c public -v1 <rhost> <processNumber>
```

### enumerate windows processes (processNumber example 1.3.6.1.2.1.25.4.2.1.2)
```
snmpwalk -c public -v1 <rhost> <processNumber>
```

### enumerate windows processes (processNumber example 1.3.6.1.2.1.25.6.3.1.2)
```
snmpwalk -c public -v1 <rhost> <processNumber>
```

