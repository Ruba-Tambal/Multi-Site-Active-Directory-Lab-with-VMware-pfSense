# Joining Windows Client to Mumbai Site

## Machine Details
- **Hostname**: CL-MUMBAI-01
- **Network**: VMnet2 (192.168.10.0/24)
- **Role**: Domain Member (Client)
- **Site**: LHO-BranchOffice-Mumbai

## Steps Performed

1. Configured VMware Network Adapter → VMnet2 + Connected
2. Assigned static IP from the Mumbai subnet (192.168.10.0/24)
3. Set Preferred DNS to 192.168.1.11
4. Joined the computer to domain `labshandson.lan`
5. Verified the computer object appears in Active Directory
6. Confirmed site association with LHO-BranchOffice-Mumbai

This demonstrates proper client placement in a multi-site Active Directory environment.
