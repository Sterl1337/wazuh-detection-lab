# Live Validation

## Summary

This lab was validated against a live Wazuh deployment rather than only sample files.

## Verified components

### Wazuh manager stack

- `wazuh-manager` installed and running
- `wazuh-indexer` installed and running
- `wazuh-dashboard` installed and running

### Network access

- dashboard reachable from the Windows host over HTTPS
- Ubuntu VM required bridged networking for direct browser access

### Windows endpoint

- Windows 11 host enrolled as agent `Ryozen`
- agent status observed as `active`
- host inventory and basic events visible in the dashboard

### Sysmon integration

- Sysmon installed from Microsoft Sysinternals
- Wazuh-compatible `sysmonconfig.xml` used during install
- Wazuh agent configured to collect:

```xml
<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>
```

- Sysmon service verified running on the Windows host
- fresh Sysmon events observed locally after install

## Safe validation activity

The following benign activity was used to generate additional endpoint telemetry:

- PowerShell execution with `-ExecutionPolicy Bypass -NoProfile`
- encoded PowerShell execution
- `whoami`
- `nslookup example.com`
- temporary directory and file create/delete operations

## Why this matters

Without Sysmon, the lab still shows basic Windows and Wazuh telemetry. With Sysmon, the environment becomes far more useful for:

- process creation visibility
- command-line review
- network connection visibility
- ATT&CK-oriented threat hunting
- future custom rule testing
