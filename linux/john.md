### source
https://github.com/openwall/john  

### show results
```
john <hashFile> --show --format=<format>
```

### generate password list with permutations
```
john --stdout --wordlist=<wordListFile.txt> --rules=korelogic > <newListName.txt>
```

### common hash type
```
krb5tgs
lm
nt
netntlmv2
mscash2 (domain cached credentials)
wpapsk (wpa2)
```

### use already cracked passwords and more CPU
```
john --loopback --fork=4
```

### file containing cracked passwords
```
~/.john/john.pot
```

### list all formats
```
john --list=formats
```

### example
```
john --wordlist=<wordlist> <fileToCrack> --rules=korelogic --format=NT
```

### convert file for john
```
rar2john
zip2john
```

