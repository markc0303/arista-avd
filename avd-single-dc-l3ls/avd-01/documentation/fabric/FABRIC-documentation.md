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
| FABRIC | l3leaf | dc1-leaf1a | 172.16.93.101/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf1b | 172.16.93.102/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc1-leaf1c | 172.16.93.151/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2a | 172.16.93.103/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2b | 172.16.93.104/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc1-leaf2c | 172.16.93.152/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf3a | 172.16.93.105/24 | - | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf3b | 172.16.93.106/24 | - | Provisioned | - |
| FABRIC | l2leaf | dc1-leaf3c | 172.16.93.153/24 | - | Provisioned | - |
| FABRIC | spine | dc1-spine1 | 172.16.93.11/24 | - | Provisioned | - |
| FABRIC | spine | dc1-spine2 | 172.16.93.12/24 | - | Provisioned | - |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

### Fabric Switches with inband Management IP

| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

## Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | --------- | -------------- |
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
| l3leaf | dc1-leaf3a | Ethernet1 | spine | dc1-spine1 | Ethernet5 |
| l3leaf | dc1-leaf3a | Ethernet2 | spine | dc1-spine2 | Ethernet5 |
| l3leaf | dc1-leaf3a | Ethernet3 | mlag_peer | dc1-leaf3b | Ethernet3 |
| l3leaf | dc1-leaf3a | Ethernet4 | mlag_peer | dc1-leaf3b | Ethernet4 |
| l3leaf | dc1-leaf3a | Ethernet8 | l2leaf | dc1-leaf3c | Ethernet1 |
| l3leaf | dc1-leaf3b | Ethernet1 | spine | dc1-spine1 | Ethernet6 |
| l3leaf | dc1-leaf3b | Ethernet2 | spine | dc1-spine2 | Ethernet6 |
| l3leaf | dc1-leaf3b | Ethernet8 | l2leaf | dc1-leaf3c | Ethernet2 |

## Fabric IP Allocation

### Fabric Point-To-Point Links

| Uplink IPv4 Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ---------------- | ------------------- | ------------------ | ------------------ |
| 10.1.0.0/26 | 64 | 24 | 37.5 % |

### Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |
| dc1-leaf1a | Ethernet1 | 10.1.0.1/31 | dc1-spine1 | Ethernet1 | 10.1.0.0/31 |
| dc1-leaf1a | Ethernet2 | 10.1.0.3/31 | dc1-spine2 | Ethernet1 | 10.1.0.2/31 |
| dc1-leaf1b | Ethernet1 | 10.1.0.5/31 | dc1-spine1 | Ethernet2 | 10.1.0.4/31 |
| dc1-leaf1b | Ethernet2 | 10.1.0.7/31 | dc1-spine2 | Ethernet2 | 10.1.0.6/31 |
| dc1-leaf2a | Ethernet1 | 10.1.0.9/31 | dc1-spine1 | Ethernet3 | 10.1.0.8/31 |
| dc1-leaf2a | Ethernet2 | 10.1.0.11/31 | dc1-spine2 | Ethernet3 | 10.1.0.10/31 |
| dc1-leaf2b | Ethernet1 | 10.1.0.13/31 | dc1-spine1 | Ethernet4 | 10.1.0.12/31 |
| dc1-leaf2b | Ethernet2 | 10.1.0.15/31 | dc1-spine2 | Ethernet4 | 10.1.0.14/31 |
| dc1-leaf3a | Ethernet1 | 10.1.0.17/31 | dc1-spine1 | Ethernet5 | 10.1.0.16/31 |
| dc1-leaf3a | Ethernet2 | 10.1.0.19/31 | dc1-spine2 | Ethernet5 | 10.1.0.18/31 |
| dc1-leaf3b | Ethernet1 | 10.1.0.21/31 | dc1-spine1 | Ethernet6 | 10.1.0.20/31 |
| dc1-leaf3b | Ethernet2 | 10.1.0.23/31 | dc1-spine2 | Ethernet6 | 10.1.0.22/31 |

### Loopback Interfaces (BGP EVPN Peering)

| Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------- | ------------------- | ------------------ | ------------------ |
| 1.1.1.0/27 | 32 | 2 | 6.25 % |
| 10.255.0.0/27 | 32 | 6 | 18.75 % |

### Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |
| FABRIC | dc1-leaf1a | 10.255.0.3/32 |
| FABRIC | dc1-leaf1b | 10.255.0.4/32 |
| FABRIC | dc1-leaf2a | 10.255.0.5/32 |
| FABRIC | dc1-leaf2b | 10.255.0.6/32 |
| FABRIC | dc1-leaf3a | 10.255.0.7/32 |
| FABRIC | dc1-leaf3b | 10.255.0.8/32 |
| FABRIC | dc1-spine1 | 1.1.1.1/32 |
| FABRIC | dc1-spine2 | 1.1.1.2/32 |

### VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)

| VTEP Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------------ | ------------------- | ------------------ | ------------------ |
| 10.255.1.0/27 | 32 | 6 | 18.75 % |

### VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
| FABRIC | dc1-leaf1a | 10.255.1.3/32 |
| FABRIC | dc1-leaf1b | 10.255.1.3/32 |
| FABRIC | dc1-leaf2a | 10.255.1.5/32 |
| FABRIC | dc1-leaf2b | 10.255.1.5/32 |
| FABRIC | dc1-leaf3a | 10.255.1.7/32 |
| FABRIC | dc1-leaf3b | 10.255.1.7/32 |
