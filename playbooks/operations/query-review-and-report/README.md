# Query Review And Report

## Use When

Use this playbook when a proposed query or analysis packet needs a
bounded review before another operator or stakeholder relies on it.

## Inputs

- query packet
- stakeholder context if relevant
- review goal if relevant

## Output

The workflow should produce:
- review scope
- query or logic summary
- caveats
- readiness recommendation
- recommended next step

## Workspace Notes

This playbook can operate from query packets, schema notes, result sets,
and other analytical artifacts. It does not require a writable code
workspace.

## Import Notes

Import this playbook when your tenant can supply the relevant analytical
packet and data context through its own tooling or artifacts. The
authored workflow packages the review outcome and does not imply a
first-party hosted analytics surface.
