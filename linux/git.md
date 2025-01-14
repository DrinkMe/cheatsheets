### set email and username for all repositories (remove --global for current repository)
```
git config --global user.email "<mail>"
git config --global user.name "<user>"
```

### sign files with given key
```
git config --global commit.gpgsign true
```

### list config of current repository
```
git config --list --local
```

### show version history
```
git log
```

### show available tags
```
git fetch --tags
```

### show information about specific tag
```
git log <tagName>
```

### switch to specific version
```
git checkout <tagName>
```

### switch to newest commit (new repos use main)
```
git checkout master
```

### get path to project
```
git remote get-url origin
```

### set custom timestamp
```
git commit --date="Wed Feb 13 15:00 2019 +0100" -m "<message>"
```

### generate access token
https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token  

### ignore certificate errors
```
git -c http.sslVerify=false
```

### get all repositories of specific user
```
curl -s "https://api.github.com/users/<user>/repos?per_page=100" | grep -o 'git@[^"]*' | grep "git"
```

