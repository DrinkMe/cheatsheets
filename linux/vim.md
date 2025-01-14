### replace all pattern (global)
```
:%s/<oldPattern>/<newPattern>/g
```

### find pattern
```
:/<pattern>
```

### run terminal command from within vim
```
:!<command>
```

### start shell from within vim
```
:<shell>
```

### edit another file
```
:e <file>
```

### edit another file in new tab
```
:tabnew <file>
```

### visuel line mode
```
shift + v
```

### visuel char mode
```
ctrl + v
```

### for inserting
```
shift + i
type stuff
esc
```

### copy
```
y
```

### cut
```
x
```

### copy current line
```
yy
```

### copy from one vim editor to another
```
"+y or "+yy for only current line
"+p for pasting
```

### remove all lines containing pattern
```
:g/<pattern>/d
```

### undo
```
u
```

### redo
```
ctrl + r
```

### remove from current line 10 lines to the bottom
```
10dd
```

### switch line (when the line is long)
```
gj
or
gk
```

### go to next autocompletion
```
ctrl + n
```

### go to previous autocompletion
```
ctrl + p
```

### dump content as hex
```
%!xxd
```

### reverse content back from hex
```
%!xxd -r
```

### record command and typing for a (or other char)
```
esc
q
a
type whatever you want and finish recording with
q
```

### repeat recorded buffer from a (or @<otherChar>)
```
@a 
```

### repeat last used recorded buffer
```
@@
```

### repeat recorded buffer XX times
```
XX@a
```

### jump to next placeholder using ulti snips
```
ctrl + j
```

### delete chars until specific char
```
d + f + <char>
```

### split horizontal, vertical
```
Ctrl + w, v
```

### close splitted window
```
CTRl + w, q
```

### edit file as sudo after opening
```
:w !sudo tee %
```

### remove word around cursor
```
daw
```

### remove word to the right
```
dw
```

### append to end of line
```
shift + a
```

### write output of command directly to vim
```
:read ! <command>
```

### increment next integer by 1
```
1 + CTRL + A
```

