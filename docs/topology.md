# Lab Topology

## Sites

### LHO-HeadOffice-Delhi
- Subnet: 192.168.1.0/24
- Domain Controllers:
  - win2k25-DC01 → 192.168.1.11
  - win2k25-DC02 → 192.168.1.12
- Gateway: 192.168.1.1 (pfSense)

### LHO-BranchOffice-Mumbai
- Subnet: 192.168.10.0/24
- Domain Controller:
  - win2k25-MUMBAI-DC01 → 192.168.10.11
- Client:
  - CL-MUMBAI-01 (joined to labshandson.lan and associated with Mumbai site)
- Gateway: 192.168.10.1 (pfSense)

## Routing
pfSense handles routing between 192.168.1.0/24 and 192.168.10.0/24.
Outbound NAT was disabled. Firewall rules were configured to allow traffic between the two networks.
