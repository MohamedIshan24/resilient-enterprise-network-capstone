# Evidence Checklist

- [ ] Labeled full topology screenshot
- [ ] `show vlan brief` and `show interfaces trunk`
- [ ] `show etherchannel summary`
- [ ] `show spanning-tree root`
- [ ] `show standby brief` before and after failover
- [ ] `show ip ospf neighbor` and `show ip route ospf`
- [ ] DHCP lease details from at least three VLANs
- [ ] Guest ACL denied internal test and allowed public test
- [ ] NAT translation table
- [ ] Port-security and DHCP-snooping negative tests
- [ ] Primary WAN failure traceroute and convergence record
- [ ] HSRP failure and recovery record
- [ ] IPv6 reachability and OSPFv3 route output
- [ ] Syslog events with synchronized timestamps
- [ ] Saved `.pkt` or GNS3 project file
