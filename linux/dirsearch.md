### source
https://github.com/maurosoria/dirsearch  

### extensions apsx and php, r = recursive, timeout 1 second
```
dirsearch.py -u http://<domain> -e aspx,php,html -x 403,404 -r --timeout=1 -o <pathToResult> --full-url
```

### use proxy
```
--proxy=localhost:8080
```

### use 3 seconds delay between requests of multiple threads
```
-s 3
```

