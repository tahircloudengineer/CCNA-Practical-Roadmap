# Lab 06 - Inter-VLAN Routing (Router-on-a-Stick)

## Overview

This lab demonstrates the configuration of **Inter-VLAN Routing** using the **Router-on-a-Stick** method. A Cisco router was connected to a Layer 2 switch through a single IEEE 802.1Q trunk link, enabling communication between devices located in different VLANs.

---

## Objectives

* Configure VLAN 10 (Engineering), VLAN 20 (HR), and VLAN 30 (Sales).
* Configure a trunk link between the router and switch.
* Create router subinterfaces using IEEE 802.1Q encapsulation.
* Assign default gateway addresses for each VLAN.
* Verify successful communication between VLANs.

---

## Network Topology

**Devices Used**

* 1 × Cisco Router (2911)
* 1 × Cisco Switch
* 6 × PCs

**VLANs**

| VLAN | Department  | Gateway    |
| ---- | ----------- | ---------- |
| 10   | Engineering | 10.0.0.62  |
| 20   | HR          | 10.0.0.126 |
| 30   | Sales       | 10.0.0.190 |

---

## Configuration Summary

The following tasks were completed:

* Created VLANs 10, 20 and 30.
* Assigned switch access ports to the appropriate VLANs.
* Configured the switch-to-router link as an IEEE 802.1Q trunk.
* Created router subinterfaces for each VLAN.
* Assigned IP addresses to each subinterface.
* Configured the default gateway on all PCs.
* Verified interface status and VLAN configuration.
* Tested end-to-end connectivity using ICMP (ping).

---

## Verification

The lab was successfully verified using the following checks:

* `show ip interface brief`
* `show vlan brief`
* `show interfaces g0/1 switchport`
* Successful ping to each VLAN gateway.
* Successful communication between devices in different VLANs.

---

## Troubleshooting

### Issue

The router interface remained down because the physical connection between the router and the switch was not established correctly.

### Root Cause

The router and switch were not connected through the correct interfaces, preventing the trunk link from becoming operational.

### Resolution

The router was connected to the correct switch port using a copper straight-through cable. After enabling the router interface, the trunk link came up automatically, all router subinterfaces became operational, and connectivity was restored.

---

## Skills Demonstrated

* VLAN Configuration
* Access Port Configuration
* IEEE 802.1Q Trunking
* Router-on-a-Stick
* Router Subinterfaces
* IPv4 Addressing
* Inter-VLAN Routing
* Cisco IOS CLI
* Network Troubleshooting
* Connectivity Verification

---

## Files Included

```
README.md
Router-on-a-Stick.pkt
topology.png
show-ip-interface-brief.png
show-vlan-brief.png
show-interfaces-g0-1-switchport.png
ping-success.png
commands.txt
```

---

## Outcome

The network was successfully configured to allow communication between VLAN 10, VLAN 20, and VLAN 30 through a single router interface using the Router-on-a-Stick architecture.
