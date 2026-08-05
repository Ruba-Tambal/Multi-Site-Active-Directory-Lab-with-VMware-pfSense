# Multi-Site Active Directory Lab with VMware & pfSense

A complete home lab project simulating a real-world multi-site Active Directory environment using VMware Workstation and pfSense as the router between sites.

## Lab Overview

| Item                    | Details                                      |
|-------------------------|----------------------------------------------|
| Domain                  | labshandson.lan                              |
| Site 1                  | LHO-HeadOffice-Delhi (192.168.1.0/24)         |
| Site 2                  | LHO-BranchOffice-Mumbai (192.168.10.0/24)     |
| Domain Controllers      | win2k25-DC01 (192.168.1.11)<br>win2k25-DC02 (192.168.1.12)<br>win2k25-MUMBAI-DC01 (192.168.10.11) |
| Router                  | pfSense (192.168.1.1 / 192.168.10.1)          |
| Client in Mumbai        | **CL-MUMBAI-01** (joined to domain and placed in Mumbai site) |
| Hypervisor              | VMware Workstation                           |

## Technologies Used

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- Active Directory Sites and Services
- DNS
- pfSense Firewall/Router
- VMware Workstation (Host-only networking)
- Windows Client

## Network Topology
