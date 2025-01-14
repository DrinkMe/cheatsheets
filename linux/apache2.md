### create new user and password
```
htpasswd -c /etc/apache2/.htpasswd <user>
```

### add dir for basic auth
```
vim /etc/apache2/apache2.conf
```

### basic authentication inside: /etc/apache2/apache2.conf
```
<Directory /var/www/html>
    AuthType Basic
    AuthName "Restricted Content"
    AuthUserFile /etc/apache2/.htpasswd
    Require valid-user
</Directory>
```

### disable packages
```
a2disconf <package>
systemctl reload apache2
```

### alternative remove symlink
```
rm /etc/apache2/mods-enabled/<package>
```

### manipulate header
```
a2enmod headers
```

### prevent clickjacking
```
sed -i '$ a\Header always append X-Frame-Options DENY' /etc/apache2/apache2.conf
```

### remove apache version inside: /etc/apache2/apache2.conf
```
Header unset Server
ServerSignature Off
ServerTokens Prod
```

