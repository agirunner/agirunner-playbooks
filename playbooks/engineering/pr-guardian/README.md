# PR Guardian

## Use When

Use this playbook when a proposed change needs a merge-readiness
disposition that combines review, security, and regression scrutiny.

## Inputs

- change summary
- merge goal
- available evidence if any

## Output

The workflow should produce:
- change scan
- review findings
- risk findings
- final merge-readiness recommendation

## Workspace Notes

This playbook is storage-agnostic and can operate from artifacts alone.

## Import Notes

This playbook is experimental and should stay focused on bounded change
sets rather than broad project governance.
