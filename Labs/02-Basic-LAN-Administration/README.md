# CCNA Practical Lab 02 - Basic LAN Administration

## Objective

Configure and administer a basic enterprise LAN consisting of one Cisco 2911 router, two Cisco Catalyst 2960 switches, and four end devices. The focus of this lab was to practice Cisco IOS CLI, Layer 2 switching, basic Layer 3 configuration, verification, and network documentation.

## Topology

See `topology.png`.

## Devices Used

* Cisco 2911 Integrated Services Router (ISR)
* 2 × Cisco Catalyst 2960-24TT Switches
* 4 × Packet Tracer PCs

## IP Addressing

| Device | Interface | IP Address        |
| ------ | --------- | ----------------- |
| R1     | G0/0      | 172.16.255.254/16 |
| PC1    | Fa0       | 172.16.255.1/16   |
| PC2    | Fa0       | 172.16.255.2/16   |
| PC3    | Fa0       | 172.16.255.3/16   |
| PC4    | Fa0       | 172.16.255.4/16   |

## Skills Demonstrated

* Cisco IOS CLI
* Router configuration
* Switch configuration
* IPv4 addressing
* Interface descriptions
* Speed and duplex configuration
* Disabling unused switch ports
* Network verification
* Basic troubleshooting

## Verification

* Verified router interface status using `show ip interface brief`
* Confirmed all required interfaces reached the **up/up** state
* Successfully tested connectivity between all PCs using ICMP
* Saved the running configuration to startup configuration

## Key Concepts Learned

* Devices within the same subnet communicate through switches without requiring routing.
* Routers are required only when traffic moves between different Layer 3 networks.
* Interface descriptions improve network documentation and troubleshooting.
* Verification is an essential step after every configuration change.

## Files Included

* Basic-LAN-Administration.pkt
* topology.png

## Cloud Connection

The networking principles in this lab directly relate to cloud networking. Communication within the same subnet is similar to communication between instances inside an AWS VPC subnet or an Azure VNet subnet. Understanding default gateways and routing lays the foundation for learning cloud route tables, virtual networking, and hybrid cloud connectivity.
