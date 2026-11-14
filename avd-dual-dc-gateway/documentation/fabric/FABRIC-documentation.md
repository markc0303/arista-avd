# FABRIC

## Table of Contents

- [Fabric Switches and Management IP](#fabric-switches-and-management-ip)
  - [Fabric Switches with inband Management IP](#fabric-switches-with-inband-management-ip)
- [Fabric Topology](#fabric-topology)
- [Fabric IP Allocation](#fabric-ip-allocation)
  - [Fabric Point-To-Point Links](#fabric-point-to-point-links)
  - [Point-To-Point Links Node Allocation](#point-to-point-links-node-allocation)
  - [Loopback Interfaces (BGP EVPN Peering)](#loopback-interfaces-bgp-evpn-peering)
  - [Loopback0 Interfaces Node Allocation](#loopback0-interfaces-node-allocation)
  - [VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)](#vtep-loopback-vxlan-tunnel-source-interfaces-vteps-only)
  - [VTEP Loopback Node allocation](#vtep-loopback-node-allocation)

## Fabric Switches and Management IP

| POD | Type | Node | Management IP | Platform | Provisioned in CloudVision | Serial Number |
| --- | ---- | ---- | ------------- | -------- | -------------------------- | ------------- |
| FABRIC | l3leaf | dc1-borderleaf1 | 172.20.96.105/24 | cEOSLab | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf1a | 172.20.96.101/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf1b | 172.20.96.102/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc1-leaf1c | 172.20.96.111/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2a | 172.20.96.103/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2b | 172.20.96.104/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc1-leaf2c | 172.20.96.112/24 | - | Provisioned | - |
| FABRIC | spine | dc1-spine1 | 172.20.96.11/24 | - | Provisioned | - |
| FABRIC | spine | dc1-spine2 | 172.20.96.12/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc2-borderleaf1 | 172.20.96.205/24 | cEOSLab | Provisioned | - |
| FABRIC | l3leaf | dc2-leaf1a | 172.20.96.201/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc2-leaf1b | 172.20.96.202/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc2-leaf1c | 172.20.96.211/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc2-leaf2a | 172.20.96.203/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc2-leaf2b | 172.20.96.204/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc2-leaf2c | 172.20.96.212/24 | - | Provisioned | - |
| FABRIC | spine | dc2-spine1 | 172.20.96.21/24 | - | Provisioned | - |
| FABRIC | spine | dc2-spine2 | 172.20.96.22/24 | - | Provisioned | - |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

### Fabric Switches with inband Management IP

| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

## Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | --------- | -------------- |
| l3leaf | dc1-borderleaf1 | Ethernet1 | spine | dc1-spine1 | Ethernet5 |
| l3leaf | dc1-borderleaf1 | Ethernet2 | spine | dc1-spine2 | Ethernet5 |
| l3leaf | dc1-borderleaf1 | Ethernet49 | l3leaf | dc2-borderleaf1 | Ethernet49 |
| l3leaf | dc1-leaf1a | Ethernet1 | spine | dc1-spine1 | Ethernet1 |
| l3leaf | dc1-leaf1a | Ethernet2 | spine | dc1-spine2 | Ethernet1 |
| l3leaf | dc1-leaf1a | Ethernet3 | mlag_peer | dc1-leaf1b | Ethernet3 |
| l3leaf | dc1-leaf1a | Ethernet4 | mlag_peer | dc1-leaf1b | Ethernet4 |
| l3leaf | dc1-leaf1a | Ethernet8 | l2leaf | dc1-leaf1c | Ethernet1 |
| l3leaf | dc1-leaf1b | Ethernet1 | spine | dc1-spine1 | Ethernet2 |
| l3leaf | dc1-leaf1b | Ethernet2 | spine | dc1-spine2 | Ethernet2 |
| l3leaf | dc1-leaf1b | Ethernet8 | l2leaf | dc1-leaf1c | Ethernet2 |
| l3leaf | dc1-leaf2a | Ethernet1 | spine | dc1-spine1 | Ethernet3 |
| l3leaf | dc1-leaf2a | Ethernet2 | spine | dc1-spine2 | Ethernet3 |
| l3leaf | dc1-leaf2a | Ethernet3 | mlag_peer | dc1-leaf2b | Ethernet3 |
| l3leaf | dc1-leaf2a | Ethernet4 | mlag_peer | dc1-leaf2b | Ethernet4 |
| l3leaf | dc1-leaf2a | Ethernet8 | l2leaf | dc1-leaf2c | Ethernet1 |
| l3leaf | dc1-leaf2b | Ethernet1 | spine | dc1-spine1 | Ethernet4 |
| l3leaf | dc1-leaf2b | Ethernet2 | spine | dc1-spine2 | Ethernet4 |
| l3leaf | dc1-leaf2b | Ethernet8 | l2leaf | dc1-leaf2c | Ethernet2 |
| l3leaf | dc2-borderleaf1 | Ethernet1 | spine | dc2-spine1 | Ethernet5 |
| l3leaf | dc2-borderleaf1 | Ethernet2 | spine | dc2-spine2 | Ethernet5 |
| l3leaf | dc2-leaf1a | Ethernet1 | spine | dc2-spine1 | Ethernet1 |
| l3leaf | dc2-leaf1a | Ethernet2 | spine | dc2-spine2 | Ethernet1 |
| l3leaf | dc2-leaf1a | Ethernet3 | mlag_peer | dc2-leaf1b | Ethernet3 |
| l3leaf | dc2-leaf1a | Ethernet4 | mlag_peer | dc2-leaf1b | Ethernet4 |
| l3leaf | dc2-leaf1a | Ethernet8 | l2leaf | dc2-leaf1c | Ethernet1 |
| l3leaf | dc2-leaf1b | Ethernet1 | spine | dc2-spine1 | Ethernet2 |
| l3leaf | dc2-leaf1b | Ethernet2 | spine | dc2-spine2 | Ethernet2 |
| l3leaf | dc2-leaf1b | Ethernet8 | l2leaf | dc2-leaf1c | Ethernet2 |
| l3leaf | dc2-leaf2a | Ethernet1 | spine | dc2-spine1 | Ethernet3 |
| l3leaf | dc2-leaf2a | Ethernet2 | spine | dc2-spine2 | Ethernet3 |
| l3leaf | dc2-leaf2a | Ethernet3 | mlag_peer | dc2-leaf2b | Ethernet3 |
| l3leaf | dc2-leaf2a | Ethernet4 | mlag_peer | dc2-leaf2b | Ethernet4 |
| l3leaf | dc2-leaf2a | Ethernet8 | l2leaf | dc2-leaf2c | Ethernet1 |
| l3leaf | dc2-leaf2b | Ethernet1 | spine | dc2-spine1 | Ethernet4 |
| l3leaf | dc2-leaf2b | Ethernet2 | spine | dc2-spine2 | Ethernet4 |
| l3leaf | dc2-leaf2b | Ethernet8 | l2leaf | dc2-leaf2c | Ethernet2 |

## Fabric IP Allocation

### Fabric Point-To-Point Links

| Uplink IPv4 Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ---------------- | ------------------- | ------------------ | ------------------ |
| 10.255.103.0/24 | 256 | 20 | 7.82 % |
| 10.255.203.0/24 | 256 | 20 | 7.82 % |

### Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |
| dc1-borderleaf1 | Ethernet1 | 10.255.103.17/31 | dc1-spine1 | Ethernet5 | 10.255.103.16/31 |
| dc1-borderleaf1 | Ethernet2 | 10.255.103.19/31 | dc1-spine2 | Ethernet5 | 10.255.103.18/31 |
| dc1-borderleaf1 | Ethernet49 | 192.168.12.0/31 | dc2-borderleaf1 | Ethernet49 | 192.168.12.1/31 |
| dc1-leaf1a | Ethernet1 | 10.255.103.1/31 | dc1-spine1 | Ethernet1 | 10.255.103.0/31 |
| dc1-leaf1a | Ethernet2 | 10.255.103.3/31 | dc1-spine2 | Ethernet1 | 10.255.103.2/31 |
| dc1-leaf1b | Ethernet1 | 10.255.103.5/31 | dc1-spine1 | Ethernet2 | 10.255.103.4/31 |
| dc1-leaf1b | Ethernet2 | 10.255.103.7/31 | dc1-spine2 | Ethernet2 | 10.255.103.6/31 |
| dc1-leaf2a | Ethernet1 | 10.255.103.9/31 | dc1-spine1 | Ethernet3 | 10.255.103.8/31 |
| dc1-leaf2a | Ethernet2 | 10.255.103.11/31 | dc1-spine2 | Ethernet3 | 10.255.103.10/31 |
| dc1-leaf2b | Ethernet1 | 10.255.103.13/31 | dc1-spine1 | Ethernet4 | 10.255.103.12/31 |
| dc1-leaf2b | Ethernet2 | 10.255.103.15/31 | dc1-spine2 | Ethernet4 | 10.255.103.14/31 |
| dc2-borderleaf1 | Ethernet1 | 10.255.203.17/31 | dc2-spine1 | Ethernet5 | 10.255.203.16/31 |
| dc2-borderleaf1 | Ethernet2 | 10.255.203.19/31 | dc2-spine2 | Ethernet5 | 10.255.203.18/31 |
| dc2-leaf1a | Ethernet1 | 10.255.203.1/31 | dc2-spine1 | Ethernet1 | 10.255.203.0/31 |
| dc2-leaf1a | Ethernet2 | 10.255.203.3/31 | dc2-spine2 | Ethernet1 | 10.255.203.2/31 |
| dc2-leaf1b | Ethernet1 | 10.255.203.5/31 | dc2-spine1 | Ethernet2 | 10.255.203.4/31 |
| dc2-leaf1b | Ethernet2 | 10.255.203.7/31 | dc2-spine2 | Ethernet2 | 10.255.203.6/31 |
| dc2-leaf2a | Ethernet1 | 10.255.203.9/31 | dc2-spine1 | Ethernet3 | 10.255.203.8/31 |
| dc2-leaf2a | Ethernet2 | 10.255.203.11/31 | dc2-spine2 | Ethernet3 | 10.255.203.10/31 |
| dc2-leaf2b | Ethernet1 | 10.255.203.13/31 | dc2-spine1 | Ethernet4 | 10.255.203.12/31 |
| dc2-leaf2b | Ethernet2 | 10.255.203.15/31 | dc2-spine2 | Ethernet4 | 10.255.203.14/31 |

### Loopback Interfaces (BGP EVPN Peering)

| Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------- | ------------------- | ------------------ | ------------------ |
| 10.255.101.0/24 | 256 | 7 | 2.74 % |
| 10.255.201.0/24 | 256 | 7 | 2.74 % |

### Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |
| FABRIC | dc1-borderleaf1 | 10.255.101.8/32 |
| FABRIC | dc1-leaf1a | 10.255.101.4/32 |
| FABRIC | dc1-leaf1b | 10.255.101.5/32 |
| FABRIC | dc1-leaf2a | 10.255.101.6/32 |
| FABRIC | dc1-leaf2b | 10.255.101.7/32 |
| FABRIC | dc1-spine1 | 10.255.101.1/32 |
| FABRIC | dc1-spine2 | 10.255.101.2/32 |
| FABRIC | dc2-borderleaf1 | 10.255.201.8/32 |
| FABRIC | dc2-leaf1a | 10.255.201.4/32 |
| FABRIC | dc2-leaf1b | 10.255.201.5/32 |
| FABRIC | dc2-leaf2a | 10.255.201.6/32 |
| FABRIC | dc2-leaf2b | 10.255.201.7/32 |
| FABRIC | dc2-spine1 | 10.255.201.1/32 |
| FABRIC | dc2-spine2 | 10.255.201.2/32 |

### VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)

| VTEP Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------------ | ------------------- | ------------------ | ------------------ |
| 10.255.102.0/24 | 256 | 5 | 1.96 % |
| 10.255.202.0/24 | 256 | 5 | 1.96 % |

### VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
| FABRIC | dc1-borderleaf1 | 10.255.102.8/32 |
| FABRIC | dc1-leaf1a | 10.255.102.4/32 |
| FABRIC | dc1-leaf1b | 10.255.102.4/32 |
| FABRIC | dc1-leaf2a | 10.255.102.6/32 |
| FABRIC | dc1-leaf2b | 10.255.102.6/32 |
| FABRIC | dc2-borderleaf1 | 10.255.202.8/32 |
| FABRIC | dc2-leaf1a | 10.255.202.4/32 |
| FABRIC | dc2-leaf1b | 10.255.202.4/32 |
| FABRIC | dc2-leaf2a | 10.255.202.6/32 |
| FABRIC | dc2-leaf2b | 10.255.202.6/32 |
