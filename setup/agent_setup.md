# Agent Setup

## Objective

Enroll a test endpoint, confirm connectivity, and verify that local telemetry reaches the manager before replaying sample events.

## Checklist

1. Install the Wazuh agent on the test host.
2. Point the agent at the manager.
3. Confirm the endpoint registers successfully.
4. Verify heartbeat and log flow.
5. Run a known-safe test event before enabling custom rules.
