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
| FABRIC | l3leaf | dc1-leaf1a | 172.16.93.101/24 | 7050X3 | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf1b | 172.16.93.102/24 | 7050X3 | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2a | 172.16.93.103/24 | 7050X3 | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf2b | 172.16.93.104/24 | 7050X3 | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf3a | 172.16.93.105/24 | 7050X3 | Provisioned | - |
| FABRIC | l3leaf | dc1-leaf3b | 172.16.93.106/24 | 7050X3 | Provisioned | - |
| FABRIC | spine | dc1-spine1 | 172.16.93.11/24 | 7060X5 | Provisioned | - |
| FABRIC | spine | dc1-spine2 | 172.16.93.12/24 | 7060X5 | Provisioned | - |
| FABRIC | spine | dc1-spine3 | 172.16.93.13/24 | 7060X5 | Provisioned | - |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

### Fabric Switches with inband Management IP

| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

## Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | --------- | -------------- |
| l3leaf | dc1-leaf1a | Ethernet49/1 | spine | dc1-spine1 | Ethernet1/1 |
| l3leaf | dc1-leaf1a | Ethernet50/1 | spine | dc1-spine2 | Ethernet1/1 |
| l3leaf | dc1-leaf1a | Ethernet51/1 | spine | dc1-spine3 | Ethernet1/1 |
| l3leaf | dc1-leaf1a | Ethernet53/1 | mlag_peer | dc1-leaf1b | Ethernet53/1 |
| l3leaf | dc1-leaf1a | Ethernet54/1 | mlag_peer | dc1-leaf1b | Ethernet54/1 |
| l3leaf | dc1-leaf1b | Ethernet49/1 | spine | dc1-spine1 | Ethernet1/3 |
| l3leaf | dc1-leaf1b | Ethernet50/1 | spine | dc1-spine2 | Ethernet1/3 |
| l3leaf | dc1-leaf1b | Ethernet51/1 | spine | dc1-spine3 | Ethernet1/3 |
| l3leaf | dc1-leaf2a | Ethernet49/1 | spine | dc1-spine1 | Ethernet1/5 |
| l3leaf | dc1-leaf2a | Ethernet50/1 | spine | dc1-spine2 | Ethernet1/5 |
| l3leaf | dc1-leaf2a | Ethernet51/1 | spine | dc1-spine3 | Ethernet1/5 |
| l3leaf | dc1-leaf2a | Ethernet53/1 | mlag_peer | dc1-leaf2b | Ethernet53/1 |
| l3leaf | dc1-leaf2a | Ethernet54/1 | mlag_peer | dc1-leaf2b | Ethernet54/1 |
| l3leaf | dc1-leaf2b | Ethernet49/1 | spine | dc1-spine1 | Ethernet1/7 |
| l3leaf | dc1-leaf2b | Ethernet50/1 | spine | dc1-spine2 | Ethernet1/7 |
| l3leaf | dc1-leaf2b | Ethernet51/1 | spine | dc1-spine3 | Ethernet1/7 |
| l3leaf | dc1-leaf3a | Ethernet49/1 | spine | dc1-spine1 | Ethernet2/1 |
| l3leaf | dc1-leaf3a | Ethernet50/1 | spine | dc1-spine2 | Ethernet2/1 |
| l3leaf | dc1-leaf3a | Ethernet51/1 | spine | dc1-spine3 | Ethernet2/1 |
| l3leaf | dc1-leaf3a | Ethernet53/1 | mlag_peer | dc1-leaf3b | Ethernet53/1 |
| l3leaf | dc1-leaf3a | Ethernet54/1 | mlag_peer | dc1-leaf3b | Ethernet54/1 |
| l3leaf | dc1-leaf3b | Ethernet49/1 | spine | dc1-spine1 | Ethernet2/3 |
| l3leaf | dc1-leaf3b | Ethernet50/1 | spine | dc1-spine2 | Ethernet2/3 |
| l3leaf | dc1-leaf3b | Ethernet51/1 | spine | dc1-spine3 | Ethernet2/3 |

## Fabric IP Allocation

### Fabric Point-To-Point Links

| Uplink IPv4 Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ---------------- | ------------------- | ------------------ | ------------------ |
| 10.255.255.0/24 | 256 | 36 | 14.07 % |

### Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |
| dc1-leaf1a | Ethernet49/1 | 10.255.255.1/31 | dc1-spine1 | Ethernet1/1 | 10.255.255.0/31 |
| dc1-leaf1a | Ethernet50/1 | 10.255.255.3/31 | dc1-spine2 | Ethernet1/1 | 10.255.255.2/31 |
| dc1-leaf1a | Ethernet51/1 | 10.255.255.5/31 | dc1-spine3 | Ethernet1/1 | 10.255.255.4/31 |
| dc1-leaf1b | Ethernet49/1 | 10.255.255.7/31 | dc1-spine1 | Ethernet1/3 | 10.255.255.6/31 |
| dc1-leaf1b | Ethernet50/1 | 10.255.255.9/31 | dc1-spine2 | Ethernet1/3 | 10.255.255.8/31 |
| dc1-leaf1b | Ethernet51/1 | 10.255.255.11/31 | dc1-spine3 | Ethernet1/3 | 10.255.255.10/31 |
| dc1-leaf2a | Ethernet49/1 | 10.255.255.13/31 | dc1-spine1 | Ethernet1/5 | 10.255.255.12/31 |
| dc1-leaf2a | Ethernet50/1 | 10.255.255.15/31 | dc1-spine2 | Ethernet1/5 | 10.255.255.14/31 |
| dc1-leaf2a | Ethernet51/1 | 10.255.255.17/31 | dc1-spine3 | Ethernet1/5 | 10.255.255.16/31 |
| dc1-leaf2b | Ethernet49/1 | 10.255.255.19/31 | dc1-spine1 | Ethernet1/7 | 10.255.255.18/31 |
| dc1-leaf2b | Ethernet50/1 | 10.255.255.21/31 | dc1-spine2 | Ethernet1/7 | 10.255.255.20/31 |
| dc1-leaf2b | Ethernet51/1 | 10.255.255.23/31 | dc1-spine3 | Ethernet1/7 | 10.255.255.22/31 |
| dc1-leaf3a | Ethernet49/1 | 10.255.255.25/31 | dc1-spine1 | Ethernet2/1 | 10.255.255.24/31 |
| dc1-leaf3a | Ethernet50/1 | 10.255.255.27/31 | dc1-spine2 | Ethernet2/1 | 10.255.255.26/31 |
| dc1-leaf3a | Ethernet51/1 | 10.255.255.29/31 | dc1-spine3 | Ethernet2/1 | 10.255.255.28/31 |
| dc1-leaf3b | Ethernet49/1 | 10.255.255.31/31 | dc1-spine1 | Ethernet2/3 | 10.255.255.30/31 |
| dc1-leaf3b | Ethernet50/1 | 10.255.255.33/31 | dc1-spine2 | Ethernet2/3 | 10.255.255.32/31 |
| dc1-leaf3b | Ethernet51/1 | 10.255.255.35/31 | dc1-spine3 | Ethernet2/3 | 10.255.255.34/31 |

### Loopback Interfaces (BGP EVPN Peering)

| Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------- | ------------------- | ------------------ | ------------------ |
| 10.255.0.0/26 | 64 | 9 | 14.07 % |
| 10.255.0.0/27 | 32 | 9 | 28.13 % |

### Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |
| FABRIC | dc1-leaf1a | 10.255.0.4/32 |
| FABRIC | dc1-leaf1b | 10.255.0.5/32 |
| FABRIC | dc1-leaf2a | 10.255.0.6/32 |
| FABRIC | dc1-leaf2b | 10.255.0.7/32 |
| FABRIC | dc1-leaf3a | 10.255.0.8/32 |
| FABRIC | dc1-leaf3b | 10.255.0.9/32 |
| FABRIC | dc1-spine1 | 10.255.0.1/32 |
| FABRIC | dc1-spine2 | 10.255.0.2/32 |
| FABRIC | dc1-spine3 | 10.255.0.3/32 |

### VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)

| VTEP Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------------ | ------------------- | ------------------ | ------------------ |
| 10.255.1.0/27 | 32 | 6 | 18.75 % |

### VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
| FABRIC | dc1-leaf1a | 10.255.1.4/32 |
| FABRIC | dc1-leaf1b | 10.255.1.4/32 |
| FABRIC | dc1-leaf2a | 10.255.1.6/32 |
| FABRIC | dc1-leaf2b | 10.255.1.6/32 |
| FABRIC | dc1-leaf3a | 10.255.1.8/32 |
| FABRIC | dc1-leaf3b | 10.255.1.8/32 |
