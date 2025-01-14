### generate gpg key
```
gpg --cert-digest-algo SHA512 --full-gen-key
```

### get private id -> uid
```
gpg --list-secret-keys
```

### get fingerprint of gpg keys
```
gpg --list-keys --with-fingerprint --with-colons
```

### consider storing revocation file for key
```
gpg --output <file>.asc --gen-revoke <keyId>
gpg --list-secret-keys
gpg --keyserver <keyserver> --send-key <keyId>
```

### export public key to file
```
gpg -a --export <keyId> > <file>.asc
```

### import public gpg key
```
gpg --keyserver <keyserver> --search-keys <email>
```

### export private key
```
gpg --armor --export-secret-key <keyId> > <file>.asc
```

### import private key
```
gpg --import <file>.asc
```

### change password of gpg
```
gpg --edit-key <keyId>
gpg> passwd
gpg> save
```

### decrypt file
```
gpg --decrypt <encryptedFile>.gpg > <decryptedFile>
```

### import key remotely
```
gpg --recv-key <id>
```

### or import local key
```
gpg --import <file>.key