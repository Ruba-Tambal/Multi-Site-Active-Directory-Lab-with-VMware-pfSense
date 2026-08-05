# Kerberos Authentication

Issue

The target principal name is incorrect

Troubleshooting

- Verified DNS.
- Verified time synchronization.
- Purged Kerberos tickets.
- Restarted Netlogon.
- Reset machine password.
- Verified SPNs.
- Re-promoted Domain Controller.

Commands

```powershell
klist purge

w32tm /query /status

netdom resetpwd
```

Result

Kerberos authentication restored successfully.
