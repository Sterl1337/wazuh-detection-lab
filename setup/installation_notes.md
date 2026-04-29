# Installation Notes

## Lab Goal

Stand up a small Wazuh manager and one test agent, validate ingestion, and confirm custom local rules against safe synthetic events.

## Suggested Components

- Wazuh manager
- one Windows or Linux test endpoint
- JSON sample events for replay and alert validation

## Validation Steps

1. Confirm the manager starts cleanly.
2. Register the test agent.
3. Verify the agent appears healthy.
4. Load the custom rules.
5. Replay the sample events and confirm expected alerts.
