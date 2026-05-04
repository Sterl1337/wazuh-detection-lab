# Threat Hunting Queries

Use these queries in the Wazuh Threat Hunting view to create cleaner portfolio screenshots and to validate both endpoints are producing useful telemetry.

## Windows endpoint

- `agent.name: Ryozen`
- `agent.name: Ryozen AND powershell`
- `agent.name: Ryozen AND nslookup`
- `agent.name: Ryozen AND rule.level >= 5`

## Kali endpoint

- `agent.name: Kali-Lab`
- `agent.name: Kali-Lab AND whoami`
- `agent.name: Kali-Lab AND curl`
- `agent.name: Kali-Lab AND sudo`

## Multi-endpoint checks

- `agent.name: (Ryozen OR Kali-Lab)`
- `rule.level >= 3`
- `mitre.id:*`

## Safe validation activities behind these queries

Windows:

- PowerShell execution
- encoded PowerShell execution
- `whoami`
- `nslookup example.com`
- temporary file creation and deletion

Kali:

- `whoami`
- `id`
- `uname -a`
- `sudo -l`
- `/tmp` file creation and deletion
- `curl -I https://example.com`
- `nslookup example.com`
