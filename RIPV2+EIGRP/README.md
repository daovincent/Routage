
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

