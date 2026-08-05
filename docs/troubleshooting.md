# Troubleshooting

## Kerberos Error

The target principal name is incorrect

Cause

Kerberos authentication failure.

Resolution

- Checked time synchronization.
- Cleared Kerberos tickets.
- Restarted Netlogon.
- Reset Secure Channel.
- Re-promoted Domain Controller.

---

## ERROR_NO_LOGON_SERVERS

Cause

Broken Secure Channel.

Resolution

Used:

nltest /sc_reset

Corrected DNS configuration.

---

## Replication Error 8452

Cause

Missing replication links.

Resolution

Cleaned stale metadata.

Forced KCC.

Re-promoted Domain Controller.

---

## Media Disconnected

Cause

VMware adapter disconnected.

Resolution

Enabled Connected.

Selected correct VMnet.

---

## Duplicate Computer Account

Cause

Force demotion left stale account.

Resolution

Deleted computer object.

Rejoined domain.
