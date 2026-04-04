# Support Escalation Investigation

## Use When

Use this playbook when a support case needs a deeper escalation packet
for another team or operator instead of a simple routing note.

## Inputs

- request summary
- customer context if relevant
- known artifacts if relevant

## Output

The workflow should produce:
- case summary
- escalation rationale
- evidence reviewed
- open questions
- recommended route
- next action

## Workspace Notes

This playbook can operate from ticket artifacts, screenshots, logs, and
other case evidence. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant wants a structured escalation
packet, not automated escalation-side effects. The authored workflow
stops at investigation and packaging; it does not execute support
actions or ticket mutations on its own.
