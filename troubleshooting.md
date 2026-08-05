# Troubleshooting Log

## Common Issues Faced

### 1. The target principal name is incorrect (Error 2148074274 / 0x80090322)
- Cause: Kerberos authentication failure between DCs
- Solutions tried: Time sync, klist purge, netlogon restart, netdom resetpwd, force demotion + re-promotion

### 2. ERROR_NO_LOGON_SERVERS (1311)
- Secure Channel was broken
- Fixed by nltest /sc_reset and proper DNS

### 3. Media disconnected on client
- Fixed by correctly setting VMware Network Adapter to Connected + correct VMnet

### 4. Stale computer account after Force Demotion
- Error: "An account with the same name exists... Re-using the account was blocked by security policy"
- Solution: Deleted the computer account from Active Directory Users and Computers, then re-joined the domain

### 5. Replication links missing (Error 8452)
- KCC could not create replica links
- Solved after cleaning the environment and re-promoting the DC
