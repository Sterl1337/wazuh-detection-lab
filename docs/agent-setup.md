# Agent Setup

## Purpose

This document describes how to set up a single test agent for the lab.

## Enrollment checklist

- Install the agent on a test host only
- Point the agent at the local Wazuh manager
- Confirm enrollment with a unique agent name
- Verify the agent appears in the manager inventory
- Confirm heartbeat and log forwarding are active

## Recommended host profile

- A disposable VM or local sandbox
- A standard Windows or Linux test host
- No production credentials
- No business data on the machine

## Validation steps

1. Start the agent service
2. Confirm the manager receives the agent connection
3. Replay the sample events in `samples/events/`
4. Confirm the expected rule hits appear
5. Save screenshots or notes for portfolio evidence

## Operational notes

- Use a clear agent label like `lab-endpoint-01`
- Keep the sample host intentionally boring
- Record the exact event source used for each sample
- Reset the test host between demonstrations if needed

