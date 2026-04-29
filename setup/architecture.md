# Lab Architecture

## Components

- Test endpoint
- Wazuh agent
- Wazuh manager
- Local rules
- Analyst review workflow

## Flow

1. Endpoint generates telemetry.
2. Agent forwards relevant data to the manager.
3. Custom rules evaluate the event.
4. Matching alerts are reviewed against the expected analyst notes.
