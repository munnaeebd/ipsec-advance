# ipsec-advance

For Pfsense

```

cloud end LAN 10.10.10.0/24
remote end LAN 0.0.0.0/0

target: any network can connect to 10.10.10.0/24 
```
```
advance-->networking--> check the following
Disable hardware checksum offload

disable bogon


firewall rules --> allow 


ipsec:
1) configure phase1
2) for phase2 assign local IP in left side and 0.0.0.0/0 for right side.


If we are able to set default route or specific route from cloud end host to pfsense for VPN tunnel, we do not need any NAT
without route we have to NAT. 

Firewall-->NAT-->Outbound -->Hybrid Outbound 

interface(LAN, 10.10.10.0/24 interface), source any, destination any(or the specific IP from 10.10.10.0/24, could be in interface or Virtual-IP) , address (Interface Address).



```









