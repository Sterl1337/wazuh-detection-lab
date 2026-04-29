# Wazuh Detection Lab

Portfolio repository for a small Wazuh monitoring lab focused on setup documentation, custom detection rules, safe sample events, and analyst-facing alert notes.

## Important

Everything in this repository is lab-only and simulated. Event payloads, alerts, hostnames, and investigation notes are synthetic or sanitized for safe portfolio use.

## What this project proves

- SIEM and endpoint-monitoring familiarity
- custom rule authoring
- alert validation workflow
- ATT&CK mapping
- blue-team documentation discipline

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
```

## Suggested review order

1. Read `setup/installation_notes.md`
2. Review `setup/architecture.md`
3. Review `rules/`
4. Replay the events in `test_events/`
5. Compare the expected analyst writeups in `alerts/`
6. Use `docs/mitre_mapping.md` and `docs/lessons_learned.md` for the portfolio narrative

## Notes

The repository also contains supporting documentation under `docs/` and sample payloads under `samples/`. The canonical recruiter-facing structure is the one listed above.
