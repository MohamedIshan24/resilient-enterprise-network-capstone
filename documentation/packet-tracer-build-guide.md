# Packet Tracer Build Guide

## Recommended devices

- Four Cisco 2911 routers: HQ-EDGE-R1, HQ-EDGE-R2, BRANCH-R1 and ISP-R1.
- Two Cisco 2960 core switches and two Cisco 2960 access switches.
- One infrastructure server, one public server and at least two clients per user VLAN.

## Construction order

1. Build and label the physical topology before entering configuration.
2. Configure the core VLAN database, EtherChannel, trunks and spanning-tree roots.
3. Configure access VLANs and Layer 2 security.
4. Configure router subinterfaces, HSRP and DHCP relay.
5. Configure both WAN links, OSPF area 0 and branch area 10.
6. Configure the ISP links, default routes and NAT/PAT.
7. Configure server services and DHCP scopes through the Packet Tracer Server GUI.
8. Add IPv6 addresses and OSPFv3 where supported by the selected image.
9. Verify the normal state before introducing any failure.
10. Execute failure tests one at a time, restore the topology, and verify recovery.

## Packet Tracer compatibility notes

Some Packet Tracer images implement only part of DAI, OSPFv3, IP SLA, SNMP or advanced HSRP tracking. If a command is rejected, record the image limitation and demonstrate the equivalent feature in GNS3 using an IOSv/IOSvL2 image. Do not silently remove the requirement.
