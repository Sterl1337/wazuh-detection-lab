# Lab Architecture

## Overview

This lab uses a small Wazuh deployment to validate detection ideas against synthetic endpoint activity.

## Logical flow

- A test endpoint emits event data
- The Wazuh agent forwards telemetry to the manager
- Custom local rules inspect the event content
- Matching events generate alerts
- The dashboard is used to review the alert trail

## Design goals

- Keep the topology simple enough to explain in interviews
- Keep the sample inputs safe and reproducible
- Keep the alert narratives readable by an analyst
- Separate benign test events from the alert examples

## Components and responsibilities

- Wazuh agent
  - forwards endpoint events
  - validates that collection and transport are healthy
- Wazuh manager
  - parses incoming events
  - evaluates custom rules
  - emits alerts
- Dashboard
  - visualizes alerts and rule hits
  - supports portfolio screenshots and walkthroughs
- Sample repository content
  - provides the exact synthetic inputs and expected outputs

## Lab boundaries

- No production endpoints
- No real attacker tooling
- No sensitive credential material
- No claims that any sample alert reflects a real incident

