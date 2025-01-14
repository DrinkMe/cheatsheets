### quote
```
Oracle:
ORA-01756: quoted string not properly terminated
ORA-00933: SQL command not properly ended
MS-SQL:
Msg 170, Level 15, State 1, Line 1
Line 1: Incorrect syntax near 'foo'
Msg 105, Level 15, State 1, Line 1
Unclosed quotation mark before the character string 'foo'
MySQL:
You have an error in your SQL syntax. Check the manual that corresponds to your MySQL server version for the right syntax to use near ''foo' at line X
-> Translation: For Oracle and MS-SQL, SQL injection is present, and it is almost certainly exploitable! If you entered a single quote and it altered the syntax of the database query, this is the error you'd expect. For MySQL, SQL injection may be present, but the same error message can appear in other contexts.
```

### variable
```
Oracle:
PLS-00306: wrong number or types of arguments in call to 'XXX'
MS-SQL:
Procedure 'XXX' expects parameter '@YYY', which was not supplied
MySQL:
N/A
-> Translation: You have commented out or removed a variable that normally would be supplied to the database. In MS-SQL, you should be able to use time delay techniques to perform arbitrary data retrieval.
```

### number of columns
```
Oracle:
ORA-01789: query block has incorrect number of result columns
MS-SQL:
Msg 205, Level 16, State 1, Line 1
All queries in a SQL statement containing a UNION operator must have an equal number of expressions in their target lists.
MySQL:
The used SELECT statements have a different number of columns
-> Translation: You will see this when you are attempting a UNION SELECT attack, and you have specified a different number of columns to the number in the original SELECT statement.
```

### union
```
Oracle:
ORA-01790: expression must have same datatype as corresponding expression
MS-SQL:
Msg 245, Level 16, State 1, Line 1
Syntax error converting the varchar value 'foo' to a column of data type int.
MySQL:
(MySQL will not give you an error.)
-> Translation: You will see this when you are attempting a UNION SELECT attack, and you have specified a different data type from that found in the original SELECT statement. Try using null.
```

### fieldtype
```
Oracle:
ORA-01722: invalid number
ORA-01858: a non-numeric character was found where a numeric was expected
MS-SQL:
Msg 245, Level 16, State 1, Line 1
Syntax error converting the varchar value 'foo' to a column of data type int.
MySQL:
(MySQL will not give you an error.)
-> Translation: Your input doesn't match the expected data type for the field. You may have SQL injection, and you may not need a single quote, so try simply entering a number followed by your SQL to be injected. In MS-SQL, you should be able to return any string value with this error message.
```

### return
```
Oracle:
ORA-00923: FROM keyword not found where expected
MS-SQL:
N/A
MySQL:
N/A
-> Translation: The following will work in MS-SQL: SELECT 1 But in Oracle, if you want to return something, you must select from a table. The DUAL table will do fine: SELECT 1 from DUAL
```

### from
```
Oracle:
ORA-00936: missing expression
MS-SQL:
Msg 156, Level 15, State 1, Line 1 Incorrect syntax near the keyword 'from'.
MySQL:
You have an error in your SQL syntax. Check the manual that corresponds to your MySQL server version for the right syntax to use near ' XXX , YYY from SOME_TABLE' at line 1
-> Translation: You commonly see this error message when your injection point occurs before the FROM keyword (for example, you have injected into the columns to be returned) and/or you have used the comment character to remove required SQL keywords. Try completing the SQL statement yourself while using your comment character.
```

### false sqli
```
Oracle:
ORA-00972:identifier is too long
MS-SQL:
String or binary data would be truncated.
MySQL:
N/A
-> Translation: This does not indicate SQL injection. You may see this error message if you have entered a long string. 
```

### table
```
Oracle:
ORA-00942: table or view does not exist
MS-SQL:
Msg 208, Level 16, State 1, Line 1
Invalid object name 'foo'
MySQL:
Table 'DBNAME.SOMETABLE' doesn't exist
-> Translation: Either you are trying to access a table or view that does not exist, or, in the case of Oracle, the database user does not have privileges for the table or view. Test your query against a table you know you have access to, such as DUAL. MySQL should helpfully reveal the current database schema DBNAME when this condition is encountered.
```

### where
```
Oracle:
ORA-00920: invalid relational operator
MS-SQL:
Msg 170, Level 15, State 1, Line 1
Line 1: Incorrect syntax near foo
MySQL:
You have an error in your SQL syntax. Check the manual that corresponds to your MySQL server version for the right syntax to use near '' at line 1
-> Translation: You were probably altering something in a WHERE clause, and your SQL injection attempt has disrupted the grammar.
```

### parenthesis
```
Oracle:
ORA-00907: missing right parenthesis
MS-SQL:
N/A
MySQL:
You have an error in your SQL syntax. Check the manual that corresponds to your MySQL server version for the right syntax to use near '' at line 1
-> Translation: Your SQL injection attempt has worked, but the injection point was inside parentheses. You probably commented out the closing parenthesis with injected comment characters (--).
```

### general
```
Oracle:
ORA-00900: invalid SQL statement
MS-SQL:
Msg 170, Level 15, State 1, Line 1
Line 1: Incorrect syntax near foo
MySQL:
You have an error in your SQL syntax. Check the manual that corresponds to your MySQL server version for the right syntax to use near XXX
-> Translation: A general error message. The error messages listed previously all take precedence, so something else went wrong. It's likely you can try alternative input and get a more meaningful message.
```

### feature
```
Oracle:
ORA-03001: unimplemented feature
MS-SQL:
N/A
MySQL:
N/A
-> Translation: You have tried to perform an action that Oracle does not allow. This can happen if you were trying to display the database version string from v$version but you were in an UPDATE or INSERT query.
```

### fixed
```
Oracle:
ORA-02030: can only select from fixed tables/views
MS-SQL:
N/A
MySQL:
N/A
-> Translation: You were probably trying to edit a SYSTEM view. This can happen if you were trying to display the database version string from v$version but you were in an UPDATE or INSERT query.
```

