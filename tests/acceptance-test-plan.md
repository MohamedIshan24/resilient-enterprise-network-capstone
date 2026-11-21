# Acceptance Test Plan

| ID | Category | Test | Expected result |
|---|---|---|---|
| T01 | VLAN | Verify VLAN and access-port membership | Every endpoint is placed in the documented VLAN |
| T02 | Trunk | Verify allowed/native VLAN consistency | All trunks allow only required VLANs and use VLAN 999 native |
| T03 | EtherChannel | Verify LACP bundle | Po1 is up and both member links are bundled |
| T04 | STP | Verify per-VLAN roots | SW1 is root for 10/20/50/99; SW2 for 30/40/60 |
| T05 | HSRP | Verify virtual gateways | R1 is active and R2 standby in normal state |
| T06 | DHCP | Renew a client lease | Correct subnet, gateway and DNS data are assigned |
| T07 | Inter-VLAN | Ping permitted internal networks | Routed traffic succeeds through the HSRP gateway |
| T08 | Guest ACL | Test private and public destinations | Private access fails; public access succeeds |
| T09 | OSPF | Verify neighbors and learned routes | Both WAN adjacencies are FULL and branch summary is present |
| T10 | Path selection | Traceroute from branch to HQ | Primary low-cost WAN is selected |
| T11 | WAN failover | Disable primary WAN | OSPF reconverges through secondary WAN |
| T12 | Gateway failover | Disable R1 trunk | R2 becomes active and client connectivity recovers |
| T13 | NAT | Access PublicServer | Translation appears and return traffic succeeds |
| T14 | Port security | Introduce excess source MACs | Violation counter rises and frames are restricted |
| T15 | DHCP snooping | Send offer on untrusted port | Rogue DHCP message is dropped |
| T16 | BPDU Guard | Attach a switch to an edge port | Port becomes error-disabled |
| T17 | IPv6 | Ping and trace dual-stack networks | IPv6 path succeeds and OSPFv3 routes appear |
| T18 | Monitoring | Generate routing and security events | Timestamped syslog/SNMP-visible events are recorded |
| T19 | Recovery | Restore failed interfaces | Preferred paths and redundancy roles return |
| T20 | Persistence | Reload saved devices | Configuration and expected operation persist |
