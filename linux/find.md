### remove all files with a specific extension
```
find . -type f -name "*.<bak>" -exec rm -f {} \;
```

### remove empty directories (f for files)
```
find . -type d -empty -delete
```

