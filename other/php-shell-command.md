### variant 1
```
system("whoami");
```

### variant 2
```
$output=null;
exec('whoami', $output);
print_r($output);
```

### variant 3
```
passthru ("whoami");
```

