## Outbound Filter to Advertise Only Default-Route

```
ip prefix-list DEFAULT_ONLY seq 5 permit 0.0.0.0/0

route-map BGP-OUT permit 10 
 match ip address prefix-list DEFAULT_ONLY
route-map BGP-OUT deny 20 

router bgp <>
 address-family ipv4
 neighbor <> route-map BGP-OUT out
 address-family vrf <>
 neighbor <> route-map BGP-OUT out


```

## Inbound Filter to Accept Only Default-Route

```
ip prefix-list DEFAULT_ONLY seq 5 permit 0.0.0.0/0

route-map BGP-IN permit 10 
 match ip address prefix-list DEFAULT_ONLY
route-map BGP-IN deny 20 

router bgp <>
 address-family ipv4
 neighbor <> route-map BGP-IN in
 address-family vrf <>
 neighbor <> route-map BGP-IN in


```
