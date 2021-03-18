# Single-Area OSPF Configuration on Cisco Routers
You can find the full OSPF configuration for both the IPv4 and IPv6 labs below. See more at https://www.nicksnetwork.com.

## IPv4

### R1
```
router ospf 1
  router-id 1.1.1.1
  network 10.1.1.0 0.0.0.255 area 0
  network 172.16.1.0 0.0.0.3 area 0

interface lo0
  ip ospf 1 area 0
```
### R2
```
router ospf 1
  router-id 2.2.2.2
  network 10.1.2.0 0.0.0.255 area 0
  network 172.16.1.0 0.0.0.3 area 0
  network 172.16.2.0 0.0.0.3 area 0

interface lo0
  ip ospf 1 area 0
```
### R3
```
router ospf 1
  router-id 3.3.3.3
  network 172.16.2.0 0.0.0.3 area 0
  network 10.1.3.0 0.0.0.255 area 0
  network 172.16.3.0 0.0.0.3 area 0

interface lo0
  ip ospf 1 area 0
```
### R4
```
router ospf 1
  router-id 4.4.4.4
  network 172.16.3.0 0.0.0.3 area 0
  network 10.1.4.0 0.0.0.255 area 0

interface lo0
  ip ospf 1 area 0
```

## IPv6

### R1
```
ipv6 router ospf 1
  router-id 1.1.1.1

interface Loopback0
  ipv6 address 2001:1234:1::1/64
  ipv6 ospf 1 area 0

interface GigabitEthernet0/0
  ipv6 address 2001:1::1/64
  ipv6 ospf 1 area 0
```
### R2
```
ipv6 router ospf 1
  router-id 2.2.2.2

interface Loopback0
  ipv6 address 2001:1234:2::1/64
  ipv6 ospf 1 area 0

interface GigabitEthernet0/0
  ipv6 address 2001:1::2/64
  ipv6 ospf 1 area 0

interface GigabitEthernet0/1
  ipv6 address 2001:2::1/64
  ipv6 ospf 1 area 0
```
### R3
```
ipv6 router ospf 1
  router-id 3.3.3.3
  
interface Loopback0
  ipv6 address 2001:1234:3::1/64
  ipv6 ospf 1 area 0

interface GigabitEthernet0/1
  ipv6 address 2001:2::2/64
  ipv6 ospf 1 area 0

interface GigabitEthernet0/2
  ipv6 address 2001:3::1/64
  ipv6 ospf 1 area 0
```
### R4
```
ipv6 router ospf 1
  router-id 4.4.4.4
  
interface Loopback0
  ipv6 address 2001:1234:4::1/64
  ipv6 ospf 1 area 0
 
interface GigabitEthernet0/2
  ipv6 address 2001:3::2/64
  ipv6 ospf 1 area 0
```
