### extract from .p12 file
```
openssl pkcs12 -info -nodes -in <file>.p12
```

### create .p12 file
```
openssl pkcs12 -export -inkey <privateKey>.key -in certificates.pem -name <file>.p12
```

### decrypt
```
openssl smime -decrypt -in <mail>.asc -inkey <privateKey>.key
```

### verfiy signature
```
openssl smime -decrypt -in <mail>.asc -inkey <privateKey>.key | openssl smime -verify
```

