# Hotfix

## Use When

Use this playbook for urgent defect response where a bounded mitigation or
fix is needed quickly but still requires explicit risk and human release
judgment.

## Inputs

- incident summary
- urgency context
- acceptable risk bounds

## Output

The workflow should produce:
- urgency and impact framing
- hotfix or mitigation plan
- implemented change or advisory patch package
- review, security, and QA evidence
- explicit human release decision or pending-approval status

## Workspace Notes

This playbook is storage-agnostic, but artifact-only or read-only runs
must stay advisory.

## Import Notes

This playbook is experimental and should stay limited to narrow urgent
changes, not broad refactors under pressure.
