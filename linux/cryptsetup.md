### create new encrypted device
```
cryptsetup luksFormat <device> -s 512 -h sha512 -i 5000 --type luks2
```

### decrypt device
```
cryptsetup open <device> <encryptedDev>
```

### encrypt device
```
cryptsetup close /dev/mapper/<encryptedDev>
```

### add keyslot with new 1000 iterations
```
cryptsetup -i 1000 --key-slot <slot> luksAddKey <dev>
```

### list keys
```
cryptsetup luksDump  <device>
```

### remove key
```
cryptsetup luksKillSlot <device> <slot>
```

### create backup of luks header
```
cryptsetup luksHeaderBackup <device> --header-backup-file <file>
```

### use luks backuped header
```
cryptsetup luksHeaderRestore <device> --header-backup-file <file>
```

