### start of string
```
^
```

### 0 or more
```
+
```

### 1 or more
```
*
```

### 0 or 1
```
?
```

### any char but \n
```
.
```

### exactly 3
```
{3}
```

### 3 or more
```
{3,}
```

### 3 or 4 or 5
```
{3,5}
```

### 3 or 5
```
{3|5}
```

### 3 or 4 or 5
```
[345]
```

### not 3 or 4
```
[^34]
```

### lowercase a-z
```
[a-z]
```

### uppercase A-Z
```
[A-Z]
```

### digit 0-9
```
[0-9]
```

### digit
```
\d
```

### not digit
```
\D
```

### A-Z,a-z,0-9
```
\w
```

### not A-Z,a-z,0-9
```
\W
```

### white space (\t\r\n\f)
```
\s
```

### not (\t\r\n\f)
```
\S
```

### "rege" or "regx"
```
reg[ex]
```

### ''rege'' or ''regex''
```
regex?
```

### ''rege'' w/ 0 or more x
```
regex*
```

### ''rege'' w/ 1 or more x
```
regex+
```

### ''Regex'' or ''regex''
```
[Rr]egex
```

### exactly 3 digits
```
\d{3}
```

### 3 or more digits
```
\d{3,)
```

### any vowel
```
[aeiou]
```

### numbers 03-25
```
(0[3-9] | 1[0-9] | 2[0-5])
```

