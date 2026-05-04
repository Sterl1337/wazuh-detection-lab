# Screenshot Guide

Use only sanitized screenshots from the live lab.

Recommended captures:

1. Wazuh endpoint inventory showing agent `Ryozen` as `active`
2. Wazuh endpoint inventory showing both `Ryozen` and `Kali-Lab` as `active`
3. Overview dashboard with alert totals and MITRE ATT&CK widgets
4. Threat Hunting results filtered to the Windows endpoint
5. Threat Hunting results filtered to the Kali endpoint
6. Event detail view for a safe Sysmon-backed Windows process or network event
7. Event detail view for a safe Kali command, file, or network event
8. Any ATT&CK-related dashboard view that shows mapped techniques

Do not include:

- passwords
- extracted credential files
- terminal windows showing secrets
- public or private information you do not want permanently associated with the lab

Private RFC1918 IPs are generally acceptable in a lab screenshot, but cropping the browser address bar still makes the images cleaner.

Useful Threat Hunting filters:

- `agent.name: Ryozen`
- `agent.name: Kali-Lab`
- `agent.name: Ryozen AND powershell`
- `agent.name: Kali-Lab AND rule.level >= 3`
