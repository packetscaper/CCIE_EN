## BGP configuration

```
show run | sec router bgp 
```
## Neighborship

````
show bgp summary

show bgp all summary

show ip bgp 
show ip bgp neighbor 

debug ip bgp 

access-list 100 permit tcp any any eq bgp
access-list 100 permit tcp any eq bgp any
debpg ip packet detail 100

debug ip icmp 

show log
````

## Routes

````
show ip bgp 
show ip bgp vpnv4 vrf <>
show ip bgp neighbors <> advertised
show ip bgp neighbors <> received
show ip bgp <>
show ip bgp regex ^$
show ip bgp community
````

## Clearing BGP routes
````
clear ip bgp * <> out
clear ip bgp * <> in 

````
