# Installation Steps

## VMware

- Created VMnet1 (192.168.1.0/24)
- Created VMnet2 (192.168.10.0/24)
- Disabled DHCP

---

## pfSense

Configured:

LAN

192.168.1.1/24

OPT

192.168.10.1/24

Disabled Outbound NAT

Removed Block Private Networks

Created Allow Any firewall rules

---

## Active Directory

Installed:

- AD DS
- DNS

Promoted:

- DC01
- DC02
- Mumbai DC

Created:

- Sites
- Subnets

Configured replication.

---

## Client

Configured Windows client.

Assigned static IP.

Joined:

labshandson.lan

Verified authentication.

Verified site assignment.
