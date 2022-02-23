### allow specific tcp port for ingoing traffic
```
New-NetFirewallRule -DisplayName "<name>" -Direction Inbound -LocalPort <port> -Protocol TCP -Action Allow
```

### block specific tcp port for ingoing traffic
```
New-NetFirewallRule -DisplayName "<name>" -Direction Inbound -LocalPort <port> -Protocol TCP -Action Block
```

### list firewall rule
```
Get-NetFirewallRule -DisplayName "<name>"
```

### remove firewall rule
```
Get-NetFirewallRule -DisplayName "<name>"
```
