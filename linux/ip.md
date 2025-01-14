### show ip address
```
ip -br a
```

### get all interface names
```
ip -o l show | awk -F': ' '{print $2}'
```

### start interface (use down for stopping)
```
ip l set <interface> up
```

### add interface with specific IP address
```
ip a add <XXX.XXX.XXX.XXX/XX> dev <interface>
```

### remove ip address interface
```
ip a del <XXX.XXX.XXX.XXX/XX> dev <interface>
```

### add a route
```
ip route add <XXX.XXX.XXX.XXX/XX> dev <interface>
```

### add a route for specific gateway
```
ip route add <XXX.XXX.XXX.XXX/XX> dev <interface> via <gatewayIp>
```

### delete all routes
```
ip route del 0/0
```

### delete specific default route
```
ip route del default via <ip> 
```

### get gateways
```
ip route | awk '/default/ { print $3 }'
```

### show arp cache for interface
```
ip neigh show dev <interface>
```

