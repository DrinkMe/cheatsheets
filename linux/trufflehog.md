### source
https://github.com/trufflesecurity/truffleHog  

### searches through git repositories for secrets
```
trufflehog --regex --entropy=False <remoteGitRepo>
```

### search for entropy
```
trufflehog --regex --entropy=True <remoteGitRepo> 
```

