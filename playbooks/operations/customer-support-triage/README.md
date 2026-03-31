# Customer Support Triage

## Use When

Use this playbook when an inbound support issue needs a consistent
classification, severity decision, and routing recommendation.

## Inputs

- request summary
- customer context if available
- attached evidence such as screenshots, logs, or prior notes

## Output

The imported workflow should produce:
- issue classification
- severity and impact rationale
- missing information list when needed
- recommended owner
- next visible action

## Workspace Notes

This playbook is storage-agnostic. It can run entirely from request
artifacts without a writable repository.

## Import Notes

Best results come from giving the specialist access to the same customer
context and artifacts that a human triage lead would use.
