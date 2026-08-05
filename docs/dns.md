# DNS Configuration

DNS is essential for Active Directory.

Configuration

Preferred DNS

192.168.1.11

Verification

```powershell
nslookup

dcdiag /test:dns
```

Results

- Domain name resolved correctly.
- Domain Controllers registered automatically.
- Dynamic DNS updates successful.
- Client located the nearest Domain Controller.
