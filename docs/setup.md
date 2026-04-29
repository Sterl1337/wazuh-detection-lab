# Setup Notes

These notes describe a minimal, clean Wazuh lab setup for portfolio demonstration.

## Lab components

- Wazuh manager
- Wazuh dashboard
- One enrolled test endpoint
- A local rules file for custom detections
- A small collection of synthetic event samples

## Setup assumptions

- The lab is isolated from production environments.
- The endpoint data is synthetic or intentionally generated.
- Any credentials used in the lab are test-only.
- Alerts and logs are for demonstration and validation.

## Recommended setup order

1. Install the Wazuh manager
2. Install the dashboard
3. Enroll a test agent
4. Confirm the agent appears healthy
5. Load the custom local rules
6. Send the safe sample events
7. Verify the resulting alerts

## Validation checklist

- Manager service starts cleanly
- Dashboard reaches the manager
- Agent connects and reports status
- Custom rules load without parser errors
- Sample events produce expected alerts
- No rule fires on unrelated benign events

## What to keep in the portfolio writeup

- The lab objective
- The environment boundaries
- The custom detection intent
- The alert outcomes
- The MITRE mapping
- The lessons learned
