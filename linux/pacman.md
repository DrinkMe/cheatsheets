### remove a package and its dependencies which are not required by any other installed package
```
pacman -Rs <package>
```

### check if package is already installed
```
pacman -Qi <package>
```

### get a list of all installed packages
```
pacman -Qqe
```

### clean package cache 
```
paccache -r
```

### path to pacman cache
```
/var/cache/pacman/pkg
```

### downgrade a package
```
pacman -U /var/cache/pacman/pkg/<package-old_version>.pkg.tar.xz
```

### after this you sould blacklist the package temporarily inside: /etc/pacman.conf
```
IgnorePkg=<package>
```

