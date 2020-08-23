# Single-Area OSPF Configuration on Cisco Routers
You can find the full OSPF configuration for both the IPv4 and IPv6 labs below.

## IPv4

### R1
```router ospf 1
router-id 1.1.1.1
network 10.1.1.0 0.0.0.255 area 0
network 172.16.1.0 0.0.0.3 area 0

interface lo0
ip ospf 1 area 0
```
### R2
router ospf 1
router-id 2.2.2.2
network 10.1.2.0 0.0.0.255 area 0
network 172.16.1.0 0.0.0.3 area 0
network 172.16.2.0 0.0.0.3 area 0

interface lo0
ip ospf 1 area 0

### R3
router ospf 1
router-id 3.3.3.3
network 172.16.2.0 0.0.0.3 area 0
network 10.1.3.0 0.0.0.255 area 0
network 172.16.3.0 0.0.0.3 area 0

interface lo0
ip ospf 1 area 0

### R4
router ospf 1
router-id 4.4.4.4
network 172.16.3.0 0.0.0.3 area 0
network 10.1.4.0 0.0.0.255 area 0

interface lo0
ip ospf 1 area 0

## IPv6

