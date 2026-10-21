# 📊 ANTA Report <a id="anta-report"></a>

**Table of Contents:**

- [ANTA Report](#anta-report)
  - [Test Results Summary](#test-results-summary)
    - [Summary Totals](#summary-totals)
    - [Summary Totals Device Under Test](#summary-totals-device-under-test)
    - [Summary Totals Per Category](#summary-totals-per-category)
  - [Test Results](#test-results)

## 📉 Test Results Summary <a id="test-results-summary"></a>

>💡 **Note:** This report was generated with **Expanded Results** enabled. The summary sections below aggregate results at the test level, so individual checks (atomic results) are not counted in these totals.

### 🔢 Summary Totals <a id="summary-totals"></a>

| Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error |
| :- | :- | :- | :- | :- |
| 184 | 184 | 0 | 0 | 0 |

### 🔌 Summary Totals Device Under Test <a id="summary-totals-device-under-test"></a>

| Device | Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error | Categories Skipped | Categories Failed |
| :- | :- | :- | :- | :- | :- | :- | :- |
| **dc1-leaf1a** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-leaf1b** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-leaf2a** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-leaf2b** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-leaf3a** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-leaf3b** | 25 | 25 | 0 | 0 | 0 | - | - |
| **dc1-spine1** | 17 | 17 | 0 | 0 | 0 | - | - |
| **dc1-spine2** | 17 | 17 | 0 | 0 | 0 | - | - |

### 🗂️ Summary Totals Per Category <a id="summary-totals-per-category"></a>

| Test Category | Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error |
| :- | :- | :- | :- | :- | :- |
| **BGP** | 8 | 8 | 0 | 0 | 0 |
| **Configuration** | 16 | 16 | 0 | 0 | 0 |
| **Connectivity** | 38 | 38 | 0 | 0 | 0 |
| **Interfaces** | 44 | 44 | 0 | 0 | 0 |
| **MLAG** | 18 | 18 | 0 | 0 | 0 |
| **Routing** | 14 | 14 | 0 | 0 | 0 |
| **STP** | 8 | 8 | 0 | 0 | 0 |
| **System** | 32 | 32 | 0 | 0 | 0 |
| **VXLAN** | 6 | 6 | 0 | 0 | 0 |

## 🧪 Test Results <a id="test-results"></a>

| Device | Categories | Test | Description | Result | Messages |
| :- | :- | :- | :- | :- | :- |
| dc1-leaf1a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.0 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.97 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf1a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf1a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf1b Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf1b Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b) from 10.255.0.3 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.0 (dc1-spine1_Ethernet1) from 10.1.0.1 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.2 (dc1-spine2_Ethernet1) from 10.1.0.3 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.0 (dc1-spine1_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.2 (dc1-spine2_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.97 (dc1-leaf1b_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| dc1-leaf1a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf1a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf1a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf1a | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf1a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf1a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf1a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf1b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.4 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.6 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.96 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf1b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf1b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf1a Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf1a Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b) from 10.255.0.4 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.4 (dc1-spine1_Ethernet2) from 10.1.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.6 (dc1-spine2_Ethernet2) from 10.1.0.7 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.4 (dc1-spine1_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.6 (dc1-spine2_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.96 (dc1-leaf1a_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| dc1-leaf1b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf1b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf1b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf1b | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf1b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf1b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf1b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf2a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.8 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.10 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.101 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf2a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf2a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf2b Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf2b Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf2a | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2a | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b) from 10.255.0.5 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.8 (dc1-spine1_Ethernet3) from 10.1.0.9 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.10 (dc1-spine2_Ethernet3) from 10.1.0.11 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2a | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.8 (dc1-spine1_Ethernet3) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.10 (dc1-spine2_Ethernet3) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.101 (dc1-leaf2b_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| dc1-leaf2a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf2a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf2a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf2a | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf2a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf2a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf2a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf2b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.12 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.14 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.100 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf2b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf2b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf2a Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf2a Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf2b | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2b | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b) from 10.255.0.6 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.12 (dc1-spine1_Ethernet4) from 10.1.0.13 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.14 (dc1-spine2_Ethernet4) from 10.1.0.15 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2b | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.12 (dc1-spine1_Ethernet4) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.14 (dc1-spine2_Ethernet4) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.100 (dc1-leaf2a_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| dc1-leaf2b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf2b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf2b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf2b | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf2b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf2b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf2b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf3a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.16 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.18 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.105 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf3a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf3a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf3a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf3b Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf3b Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf3a | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3a | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b) from 10.255.0.7 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.16 (dc1-spine1_Ethernet5) from 10.1.0.17 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.18 (dc1-spine2_Ethernet5) from 10.1.0.19 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3a | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.16 (dc1-spine1_Ethernet5) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.18 (dc1-spine2_Ethernet5) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.105 (dc1-leaf3b_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf3a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| dc1-leaf3a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf3a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf3a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf3a | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf3a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf3a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf3a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf3a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf3a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf3a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf3b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 1.1.1.2 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.20 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.22 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.1.104 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf3b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf3b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf3b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-spine1 Neighbor Port: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-spine2 Neighbor Port: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf3a Neighbor Port: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf3a Neighbor Port: Ethernet4 | ✅&nbsp;Success | - |
| dc1-leaf3b | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3b | Connectivity | VerifyReachability | Verifies VTEP fabric-wide underlay reachability. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.7 (dc1-leaf3a) from 10.255.0.8 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.20 (dc1-spine1_Ethernet6) from 10.1.0.21 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.22 (dc1-spine2_Ethernet6) from 10.1.0.23 in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3b | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;5&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.1 (dc1-spine1_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 1.1.1.2 (dc1-spine2_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.20 (dc1-spine1_Ethernet6) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.22 (dc1-spine2_Ethernet6) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.1.104 (dc1-leaf3a_Vlan4093) in VRF default | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;10&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;14&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Loopback1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4093 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Vlan4094 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Vxlan1 | ✅&nbsp;Success | - |
| dc1-leaf3b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | ✅&nbsp;Success | All&nbsp;3&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| dc1-leaf3b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-leaf3b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ✅&nbsp;Success | - |
| dc1-leaf3b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ✅&nbsp;Success | - |
| dc1-leaf3b | Routing | VerifyIPv4RoutePresencePerVRF | Verifies that the provided IPv4 prefixes are present in the routing table. | ✅&nbsp;Success | All&nbsp;11&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.1/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 1.1.1.2/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.4/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.6/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.7/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.0.8/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.3/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Prefix: 10.255.1.5/32 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Prefix: 10.255.1.7/32 VRF: default | ✅&nbsp;Success | - |
| dc1-leaf3b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf3b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | All&nbsp;2&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Port-Channel5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Port-Channel8 | ✅&nbsp;Success | - |
| dc1-leaf3b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf3b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf3b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf3b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf3b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ✅&nbsp;Success | - |
| dc1-spine1 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;12&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.1 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.5 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.9 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.13 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.17 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.21 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.3 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.4 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.5 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.6 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.7 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.0.8 VRF: default | ✅&nbsp;Success | - |
| dc1-spine1 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-spine1 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;6&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-leaf1a Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-leaf1b Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf2a Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf2b Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet5 Neighbor: dc1-leaf3a Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet6 Neighbor: dc1-leaf3b Neighbor Port: Ethernet1 | ✅&nbsp;Success | - |
| dc1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-spine1 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;6&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.1 (dc1-leaf1a_Ethernet1) from 10.1.0.0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.5 (dc1-leaf1b_Ethernet1) from 10.1.0.4 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.9 (dc1-leaf2a_Ethernet1) from 10.1.0.8 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.13 (dc1-leaf2b_Ethernet1) from 10.1.0.12 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.17 (dc1-leaf3a_Ethernet1) from 10.1.0.16 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.21 (dc1-leaf3b_Ethernet1) from 10.1.0.20 in VRF default | ✅&nbsp;Success | - |
| dc1-spine1 | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;12&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.1 (dc1-leaf1a_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.5 (dc1-leaf1b_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.9 (dc1-leaf2a_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.13 (dc1-leaf2b_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.17 (dc1-leaf3a_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.21 (dc1-leaf3b_Ethernet1) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| dc1-spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-spine1 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-spine2 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ✅&nbsp;Success | All&nbsp;12&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.3 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.7 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.11 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.15 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.19 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.1.0.23 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.3 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.4 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.5 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.6 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Peer: 10.255.0.7 VRF: default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Peer: 10.255.0.8 VRF: default | ✅&nbsp;Success | - |
| dc1-spine2 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-spine2 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | All&nbsp;6&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet1 Neighbor: dc1-leaf1a Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet2 Neighbor: dc1-leaf1b Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet3 Neighbor: dc1-leaf2a Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet4 Neighbor: dc1-leaf2b Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Port: Ethernet5 Neighbor: dc1-leaf3a Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Port: Ethernet6 Neighbor: dc1-leaf3b Neighbor Port: Ethernet2 | ✅&nbsp;Success | - |
| dc1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | ✅&nbsp;Success | All&nbsp;4&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.6 from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-spine2 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ✅&nbsp;Success | All&nbsp;6&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.3 (dc1-leaf1a_Ethernet2) from 10.1.0.2 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.7 (dc1-leaf1b_Ethernet2) from 10.1.0.6 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.11 (dc1-leaf2a_Ethernet2) from 10.1.0.10 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.15 (dc1-leaf2b_Ethernet2) from 10.1.0.14 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.19 (dc1-leaf3a_Ethernet2) from 10.1.0.18 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.1.0.23 (dc1-leaf3b_Ethernet2) from 10.1.0.22 in VRF default | ✅&nbsp;Success | - |
| dc1-spine2 | Connectivity | VerifyReachability | Verifies reachability to BGP neighbors. | ✅&nbsp;Success | All&nbsp;12&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.3 (dc1-leaf1a_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.7 (dc1-leaf1b_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.11 (dc1-leaf2a_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.15 (dc1-leaf2b_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.19 (dc1-leaf3a_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.1.0.23 (dc1-leaf3b_Ethernet2) in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.3 (dc1-leaf1a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.4 (dc1-leaf1b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.5 (dc1-leaf2a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.6 (dc1-leaf2b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Destination 10.255.0.7 (dc1-leaf3a_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Destination 10.255.0.8 (dc1-leaf3b_Loopback0) from Loopback0 in VRF default | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Management0 | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ✅&nbsp;Success | All&nbsp;7&nbsp;checks&nbsp;passed |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet1 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet2 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet3 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet4 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet5 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;├──&nbsp;Interface: Ethernet6 | ✅&nbsp;Success | - |
| | | | &nbsp;&nbsp;└──&nbsp;Interface: Loopback0 | ✅&nbsp;Success | - |
| dc1-spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-spine2 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
