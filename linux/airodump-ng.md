### source
https://github.com/aircrack-ng/aircrack-ng  

### 2.4 GHz
```
Channel n = 1,2,...,13
```

### 5 GHz
```
Channel n = 36,40...64; 100,...,144; 149-165
```

### sniff on 5GHz band (possible band values: a b g)
```
airodump-ng --band a
```

### sniff on specific channel 
```
airodump-ng <interface> -w <result> -c <channel>
```

### -a list only associated devices - IOS und android uses ranodmized mac addresses as far as they are not connected to wifi 
```
airodump-ng <interface> -a
```

### get uptime and vendor 
```
airodump-ng <interface> --uptime --manufacturer
```

### get into interactive mode
```
tab
```

### pause execution
```
blank
```

### highlight current ssid with color
```
m
```

