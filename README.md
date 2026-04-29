# Wazuh Detection Lab

Portfolio repository for a live Wazuh home lab built to practice SIEM deployment, Windows endpoint monitoring, Sysmon telemetry collection, and blue-team documentation.

## Scope

This project documents a small but real lab:

- Ubuntu Server VM hosting a single-node Wazuh deployment
- Windows 11 host enrolled as an active Wazuh agent
- Sysmon installed on the Windows endpoint for richer process and network telemetry
- safe validation activity used to confirm ingestion, visibility, and ATT&CK-relevant event coverage

No malware or destructive payloads were used. Test activity was limited to safe administrative commands and telemetry validation steps.

## What this project proves

- SIEM deployment and access validation
- Windows agent enrollment and health verification
- Sysmon integration with Wazuh
- basic threat hunting and ATT&CK-oriented analysis
- blue-team documentation discipline

## Lab components

- `Wazuh-Lab`
  - Ubuntu Server 24.04.4 LTS
  - single-node Wazuh deployment
  - bridged network access for browser and agent communication
- `Ryozen`
  - Windows 11 Home endpoint
  - Wazuh agent `v4.14.5`
  - Sysmon installed and forwarding `Microsoft-Windows-Sysmon/Operational`

## Repository layout

```text
wazuh-detection-lab/
  README.md
  setup/
    installation_notes.md
    agent_setup.md
    architecture.md
  rules/
    custom_failed_login_rules.xml
    suspicious_powershell_rules.xml
    privilege_escalation_rules.xml
  test_events/
    failed_logins.json
    powershell_events.json
    account_creation_events.json
  alerts/
    sample_alert_001.md
    sample_alert_002.md
  diagrams/
    wazuh_flow.mmd
  screenshots/
    README.md
  docs/
    mitre_mapping.md
    lessons_learned.md
    live_validation.md
```

## Live validation completed

The following items were validated in the lab:

1. Wazuh dashboard was reached from the Windows host over HTTPS
2. Windows agent `Ryozen` enrolled successfully and reported `active`
3. Sysmon was installed and confirmed running on the Windows host
4. Sysmon event channel collection was added to the Wazuh agent configuration
5. Safe test activity generated process, network, and authentication-related telemetry
6. Dashboard views populated with endpoint and ATT&CK-related data

## Safe test activity used

Examples of benign validation commands used on the Windows endpoint:

- PowerShell process execution
- encoded PowerShell execution
- `whoami`
- `nslookup example.com`
- temporary file create/delete operations

These actions were used only to validate log flow and improve the quality of threat-hunting screenshots and writeups.

## Suggested review order

1. Read `setup/installation_notes.md`
2. Read `setup/agent_setup.md`
3. Review `setup/architecture.md`
4. Read `docs/live_validation.md`
5. Review `docs/mitre_mapping.md`
6. Review `rules/` and `alerts/`

## Portfolio note

This repository is intended to show practical SIEM and endpoint-monitoring familiarity in a small, explainable lab environment. It is intentionally scoped to what can be defended clearly in an interview.
