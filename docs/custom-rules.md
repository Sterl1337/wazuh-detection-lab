# Custom Rules

The rules below are intentionally narrow, lab-safe examples that show how to translate endpoint behavior into detection logic.

## Rule 100100: Suspicious PowerShell download pattern

- Intent: detect a common scripted download shape for analyst review
- Trigger concept: PowerShell command line containing `DownloadString` or `Invoke-WebRequest`
- Expected use: synthetic admin-workstation validation only
- Notes: this is a lab example, not a claim of compromise

## Rule 100110: Suspicious archive staging

- Intent: detect archive creation immediately followed by outbound transfer language
- Trigger concept: file or command telemetry mentioning `zip`, `7z`, `rar`, or `tar`
- Expected use: synthetic test events that simulate staging behavior
- Notes: keep the sample event text sanitized and explicit

## Rule 100120: Repeated failed logon burst

- Intent: detect a burst of failed authentication activity
- Trigger concept: multiple failed logon events from the same host in a short window
- Expected use: lab replay of a controlled authentication failure sequence
- Notes: the sample data should not resemble a real account or real host

## Rule writing guidance

- Keep conditions specific
- Avoid over-broad keywords
- Prefer explainable alerts over noisy matches
- Add comments in the rule file when the intent is simulation-only
- Pair each rule with one sample event and one sample alert
