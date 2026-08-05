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

## What I Built

1. Configured two isolated Host-only networks in VMware (VMnet1 & VMnet2)
2. Deployed pfSense as a router between the two subnets
3. Promoted multiple Domain Controllers across different sites
4. Configured Active Directory Sites and Services (Sites + Subnets)
5. Successfully joined Windows client **CL-MUMBAI-01** to the domain and associated it with the Mumbai site
6. Troubleshot complex replication, Kerberos, DNS, and Secure Channel issues

## Key Challenges & Solutions

- "The target principal name is incorrect" (Kerberos error) during replication
- Cross-subnet Domain Controller promotion
- DNS registration failures after promotion
- Secure Channel broken (ERROR_NO_LOGON_SERVERS)
- Media disconnected / network connectivity issues in VMware
- Firewall rules on pfSense blocking AD traffic
- Time synchronization problems
- Stale computer account after force demotion

## Lessons Learned

- Correct DNS configuration is critical for multi-site AD
- Kerberos is highly sensitive to time differences and SPNs
- Always configure Sites and Subnets properly
- Force demotion can leave stale computer accounts that must be cleaned manually
- pfSense default "Block private networks" rule on WAN can break lab traffic
- Clients should be placed in the correct AD Site for optimal authentication

## Author

Built as a hands-on learning project for Active Directory, Networking, and System Administration skills.
