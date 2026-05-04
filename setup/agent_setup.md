# Agent Setup

## Objective

Enroll a test endpoint, confirm connectivity, and verify that local telemetry reaches the manager before replaying sample events.

## Checklist

1. Install the Wazuh agent on the test host.
2. Point the agent at the manager.
3. Confirm the endpoint registers successfully.
4. Verify heartbeat and log flow.
5. Run a known-safe test event before enabling custom rules.

## Endpoints enrolled in this lab

### Windows 11 host

- Agent name: `Ryozen`
- Manager address used: `10.0.0.252`
- Validation focus:
  - agent heartbeat
  - Sysmon event channel collection
  - safe PowerShell and network telemetry

### Kali Linux VM

- Agent name: `Kali-Lab`
- Manager address used: `10.0.0.252`
- Validation focus:
  - Linux agent enrollment
  - command execution visibility
  - `/tmp` file activity
  - basic network activity
