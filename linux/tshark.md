### source
https://github.com/wireshark/wireshark/blob/master/tshark.c  

### filter output, -T set format for output, -e field for formatted output - see https://www.wireshark.org/docs/dfref
```
tshark -i <interface> -T fields -e smb.native_lanman
```

### write output to file to import into wireshark
```
tshark -i <interface> -w <output>.pcap
```

### possible formats
```
ek
fields
json
jsonraw
pdml
ps
psml
tabs
text
```


