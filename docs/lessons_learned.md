# Lessons Learned

- Bridged networking is the cleanest choice when a Windows host needs to browse to a SIEM VM directly.
- A working agent check-in is only the baseline. The lab becomes much more valuable once Sysmon is added.
- Small labs become far more defensible when each validation step is documented: install, access, enrollment, telemetry, and screenshots.
- Safe process and network activity can generate useful endpoint telemetry without running destructive payloads.
- Credentials handling matters even in a home lab. Generated passwords should be treated as sensitive and excluded from screenshots and repo content.
