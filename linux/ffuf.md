### source
https://github.com/ffuf/ffuf  

### fuzz cgi directory (-e extensions, -t threads) - (https://raw.githubusercontent.com/danielmiessler/SecLists/master/Discovery/Web-Content/CGI-XPlatform.fuzz.txt)
```
ffuf -w <path>/SecLists/Discovery/Web-Content/CGI-XPlatform.fuzz.txt -u <rhost>/ccgi-bin/FUZZ -t <number> -e .sh,.pl,.cgi
```

