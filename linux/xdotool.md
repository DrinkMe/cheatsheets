### source
https://github.com/jordansissel/xdotool  

### type some string
```
xdotool type <string>
```

### press enter
```
xdotool key Return
```

### press windows key
```
xdotool key Super_L
```

### press arrow down
```
xdotool key Down
```

### press alt followed by tab
```
xdotool keydown alt Tab ; xdotool keyup alt
```

### CTRL + t
```
xdotool key ctrl+t 
```

### simulate mouse click
```
xdotool click <number>
```

### numbers
```
1 Left click
2 Middle click
3 Right click
4 Scroll wheel up
5 Scroll wheel down
```

### absolute mouse move
```
xdotool mousemove 100 100 
```

### relative mouse move (positive)
```
xdotool mousemove_relative 30 30
```

### relative mouse move (negative)
```
xdotool mousemove_relative -- -55 -10
```

### get realtime mouse position
```
while true; do xdotool getmouselocation; sleep 0.2; clear; done
```

### search for keynames
```
xev
```

### key mapping on german keyboard
```
ö -> ;
Ö -> :
: -> >
/ -> &
- -> /
( -> *
) -> (
= -> )
? -> _
+ -> ]
# -> \
; -> <
: -> >
_ -> ?
' -> |
* -> }
ß -> -
ä -> '
ü -> [
```

