# Bug Fix

## Use When

Use this playbook for a bounded software defect that should go through a
disciplined fix, review, verification, and human release decision.

## Inputs

- issue summary
- reproduction context if available
- acceptance scope

## Output

The workflow should produce:
- reproduced or bounded defect scope
- implemented fix or advisory patch plan
- code review and security review findings
- verification evidence and limits
- release recommendation
- explicit human release decision or pending-approval status

## Workspace Notes

This playbook is storage-agnostic.
- `git`: mutate, verify, and push when appropriate
- `host_directory`: mutate and verify in place
- `artifact` or read-only: produce an advisory fix package instead of
  claiming implementation or release

## Import Notes

This playbook is experimental. It should be used for bounded defects,
not large autonomous feature delivery.
