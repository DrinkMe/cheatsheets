### check if RSN is required (could cause problems for older clients)
```
Wireshark > Beacon Frame > RSN Capabilitise > Managment Frame Protection Required: <true|false> 
```

### check if RSN is enabled but not required (mostly better option if old clients are using the AP)
```
Wireshark > Beacon Frame > RSN Capabilitise > Managment Frame Protection Capable: <true|false>
```

