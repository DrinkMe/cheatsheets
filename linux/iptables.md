### target description
```
DNAT - Destination Network Address Translation (Destinationadress and -ports)
SNAT - Source Network Address Translation (Sourceaddress and -ports)
MASQUERADE - Route between networks
DROP - drop packets
Reject - drop packets with icmp respsonse (INPUT OUTPUT FORWARD)
```

### debugging
```
watch iptables -t nat -L -v -n
```

### traffic redirection
```
iptables -t nat -A PREROUTING -p tcp --dport <port> -j DNAT --to-destination <ip>
```

### drop all outgoing packets (use -A for append, -I for insert)
```
iptables -I OUTPUT -o <interface> -j DROP
```

### remove rules
```
iptables -t nat -L --line-numbers
iptables -L OUTPUT --line-numbers
```

### delete first rule of given chain (OUTPUT).
```
iptables -D OUTPUT 1
```

### rate limiting ssh connections
```
iptables -I INPUT -p tcp --dport 22 -i eth0 -m state --state NEW -m recent --set
iptables -I INPUT -p tcp --dport 22 -i eth0 -m state --state NEW -m recent --update --seconds 60 --hitcount 4 -j DROP
```

### configure limiting ssh connections for ipv6
```
ip6tables -I INPUT -p tcp --dport 22 -i eth0 -m state --state NEW -m recent --set
ip6tables -I INPUT -p tcp --dport 22 -i eth0 -m state --state NEW -m recent --update --seconds 60 --hitcount 4 -j DROP
```

