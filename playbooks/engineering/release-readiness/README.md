# Release Readiness

## Use When

Use this playbook when a change or release candidate needs a single
human-facing readiness packet that combines review, security, and
verification evidence before approval.

## Inputs

- release scope
- candidate evidence if relevant
- rollout context if relevant

## Output

The workflow should produce:
- release scope summary
- blocking findings
- non-blocking callouts
- verification summary
- known risks
- rollback or recovery notes
- approval recommendation

## Workspace Notes

This playbook can work from a repository-backed workspace, an artifact
packet, or a PR/change-summary packet. A writable workspace is not
required because the goal is a release recommendation, not a code
change.

## Import Notes

Import this playbook when your tenant already has review, security, and
QA specialists configured with enough read-only evidence access to judge
the candidate honestly. This playbook is not a substitute for human
release approval.
