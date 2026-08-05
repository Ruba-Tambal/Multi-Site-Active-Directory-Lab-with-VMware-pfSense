# Lab Topology

## Head Office

Site Name

LHO-HeadOffice-Delhi

Subnet

192.168.1.0/24

Servers

- win2k25-DC01 (192.168.1.11)
- win2k25-DC02 (192.168.1.12)

Gateway

192.168.1.1 (pfSense)

---

## Mumbai Branch

Site Name

LHO-BranchOffice-Mumbai

Subnet

192.168.10.0/24

Domain Controller

- win2k25-MUMBAI-DC01 (192.168.10.11)

Client

- CL-MUMBAI-01

Gateway

192.168.10.1

---

## Routing

pfSense routes traffic between both networks.

Outbound NAT was disabled.

Firewall rules were configured to allow Active Directory traffic between both sites.
