### source
https://github.com/aircrack-ng/aircrack-ng  

### convert cap file to hashcat format
```
aircrack-ng -J <file> <result>.cap
```

### crack wpa2 
```
aircrack-ng <result>.cap -w <wordlist>
```

