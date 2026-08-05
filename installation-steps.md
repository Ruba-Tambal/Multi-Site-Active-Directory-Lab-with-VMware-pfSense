# Installation & Configuration Steps

## 1. VMware Network Setup
- Created VMnet1 (Host-only) → 192.168.1.0/24 (DHCP disabled)
- Created VMnet2 (Host-only) → 192.168.10.0/24 (DHCP disabled)

## 2. pfSense Configuration
- Interface 1 (LAN) → 192.168.1.1/24 (connected to VMnet1)
- Interface 2 (WAN/OPT) → 192.168.10.1/24 (connected to VMnet2)
- Disabled Outbound NAT
- Added Pass Any rules on both interfaces
- Removed "Block private networks" rule on WAN

## 3. Domain Controllers
- Promoted DC01 and DC02 in Head Office site
- Promoted win2k25-MUMBAI-DC01 in Mumbai site
- Configured Sites and Subnets in Active Directory Sites and Services

## 4. Client Machine (CL-MUMBAI-01)
- Placed on VMnet2 (Mumbai network)
- Assigned static IP in 192.168.10.0/24 range
- Joined to domain labshandson.lan
- Associated with LHO-BranchOffice-Mumbai site
