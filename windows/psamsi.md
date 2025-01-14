### source
https://raw.githubusercontent.com/cobbr/PSAmsi/master/PSAmsiClient.ps1  

### create scanner
```
$scan = [PSAmsiScanner]::new()
```

### scan specific string
```
$scan.GetPSAmsiScanResult('<string>')
```

### scan specific url
```
$scan.GetPSAmsiScanResult([Uri]::new("<url>"))
```

### scan specific file
```
$scan.GetPSAmsiScanResult([String]::new("<file>"))
```

### discover which piece of a script is flagged as malicious
```
$signatures = Find-AmsiSignatures -ScriptUri '<url>'
$signatures
```

### obfuscate only parts of script that are flagged as malicious
```
$miniObfs = Get-MinimallyObfuscated -ScriptUri '<url>'
```

