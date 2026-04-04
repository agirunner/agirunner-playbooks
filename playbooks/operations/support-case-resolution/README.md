# Support Case Resolution

## Use When

Use this playbook when a support case needs more than triage and should
end with a customer-safe answer, internal notes, and a concrete next
step.

## Inputs

- request summary
- customer context if relevant
- known artifacts if relevant

## Output

The workflow should produce:
- case summary
- evidence reviewed
- customer-safe response
- internal notes
- open questions
- recommended next step

## Workspace Notes

This playbook can operate from ticket artifacts, screenshots, logs, and
other case evidence. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant wants a resolution packet and
customer-safe draft, not automated side effects. The authored workflow
stops at investigation and packaging; it does not execute support
actions on its own.
