# Test Plan Execution

## Use When

Use this playbook when a bounded test plan needs a verification packet
that preserves what ran, what failed, and what remains unverified.

## Inputs

- test plan
- test scope if relevant
- environment notes if relevant

## Output

The workflow should produce:
- test scope
- step results
- failures
- blocked or skipped steps
- coverage gaps
- recommended next step

## Workspace Notes

This playbook can operate from test plans, logs, fixtures, and other
verification artifacts. It does not require a writable code workspace.

## Import Notes

Import this playbook when your tenant can provide the relevant test
plan, fixtures, or verification evidence path. The authored workflow is
deliberately honest about blocked, skipped, and advisory-only steps.
