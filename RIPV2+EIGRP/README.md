
# 1. Introduction

RIPV2 and EIGRP are able to work together, but we have to basically tell them to do so, and redistribute their routes into one another.

```
router rip
 version 2
 redistribute eigrp 90 metric 1 
 network 192.169.0.0
 default-information originate
 no auto-summary
```



# Abridging the routes 
In order to reduce the number of routes, we can condense them on the interfaces as such : 
```
interface fastEthernet 0/0
ip summary-address eigrp 90 10.1.0.0 255.255.252.0
```
