### show message from boot
```
sudo journalctl -b -1
```

### check disk usage of journalctl
```
journalctl --disk-usage
```

### delete log entries that are older then 2 days
```
sudo journalctl --vacuum-time=2d
```

