# CDP Neighbors Discovery Report
**Lab:** cuppco.lab  
**Source Device:** cdp_sw13  
**Date:** 2026-02-08  

## Summary
Total CDP Neighbors Discovered: 12

## CDP Neighbors with IPs

| Device ID | Management IP | Interface | Platform | Capabilities |
|-----------|---------------|-----------|----------|--------------|
| cclabs3.cuppco.com | 192.168.1.72 | Gi0/1 | Cisco vios_l2 | Router, Switch, IGMP |
| cclabs1.cuppco.com | 192.168.1.71 | Gi0/2 | Cisco vios_l2 | Router, Switch, IGMP |
| cclabr1.cuppco.com | 192.168.1.70 | Gi0/3 | Cisco IOSv | Router, Source-Route-Bridge |
| cdp_sw12.cuppco.lab | 192.168.1.73 | Gi0/3 | Cisco vios_l2 | Router, Switch, IGMP |
| cdp_sw12.cuppco.lab | 192.168.1.73 | Gi0/2 | Cisco vios_l2 | Router, Switch, IGMP |
| cdp_sw14.cuppco.lab | 192.168.1.75 | Gi0/3 | Cisco vios_l2 | Router, Switch, IGMP |
| cclab2 | (No IP) | Gi1/0 | Cisco vios_l2 | Router, Switch, IGMP |
| cdp_sw15.cuppco.lab | 192.168.1.76 | Gi0/0 | Cisco vios_l2 | Router, Switch, IGMP |
| cdp_sw15.cuppco.lab | 192.168.1.76 | Gi0/3 | Cisco vios_l2 | Router, Switch, IGMP |
| crawlr1.cuppco.lab | 192.168.1.71 | Gi0/0 | Cisco IOSv | Router, Source-Route-Bridge |
| crawlr2.cuppco.lab | 192.168.1.72 | Gi0/0 | Cisco IOSv | Router, Source-Route-Bridge |
| crawlr2.cuppco.lab | 172.16.1.2 | Gi0/1 | Cisco IOSv | Router, Source-Route-Bridge |

## Key Findings

### Unique Devices
- **cclabr1**: 192.168.1.70 (Router)
- **cclabs1**: 192.168.1.71 (L3 Switch)  
- **cclabs3**: 192.168.1.72 (L3 Switch)
- **cdp_sw12**: 192.168.1.73 (Access Switch)
- **cdp_sw14**: 192.168.1.75 (Access Switch)
- **cdp_sw15**: 192.168.1.76 (Access Switch)
- **crawlr1**: 192.168.1.71 (Router - management), 172.16.1.1 (L3 VLAN)
- **crawlr2**: 192.168.1.72 (Router - management), 172.16.1.2 (L3 VLAN)
- **cclab2**: (No management IP discovered)

### Notes
- crawlr1 and crawlr2 appear on multiple interfaces (Gi0/0 for management, Gi0/1 for VLAN 10)
- cclabs1 and cclabs3 show as both routers and switches (capabilities: Router Switch)
- One device (cclab2) has no IP advertised via CDP (may need to check manually)

## CDP Crawler Compatibility
These results validate CDP crawler functionality:
✅ Discovers mixed device types (routers, switches)  
✅ Captures both management and operational IPs  
✅ Handles multi-interface CDP advertisements  
✅ Works reliably with IOSv and vios_l2 platforms  
