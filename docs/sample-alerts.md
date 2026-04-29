# Sample Alerts

These are expected alert shapes for the synthetic sample events in this repository.

## Sample alert 1

- Rule ID: 100100
- Title: Suspicious PowerShell download pattern
- Severity: Medium
- Source: synthetic PowerShell command line
- Outcome: matched on download-related command content

## Sample alert 2

- Rule ID: 100110
- Title: Suspicious archive staging
- Severity: Medium
- Source: synthetic file or process activity
- Outcome: matched on archive-staging terms

## Sample alert 3

- Rule ID: 100120
- Title: Repeated failed logon burst
- Severity: High
- Source: synthetic authentication failures
- Outcome: matched on repeated failures within the lab window

## How to use this file

- Compare the alert metadata against dashboard output
- Use it as a validation checklist after sample replay
- Capture screenshots only after confirming the sample is synthetic
