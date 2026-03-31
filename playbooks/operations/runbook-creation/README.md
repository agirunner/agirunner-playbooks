# Runbook Creation

## Use When

Use this playbook when a team needs an operational runbook for
maintenance, incident response, cutover, or any other sensitive
procedure that should be safe to follow under pressure.

## Inputs

- operating goal
- system or process in scope
- risk context
- any current procedure notes or constraints

## Output

The workflow should produce a runbook draft with:
- prerequisites
- execution sequence
- validation checks
- rollback or recovery notes
- operator caution points

## Workspace Notes

This playbook is storage-agnostic. If a writable documentation workspace
is available, the draft should be written there. Otherwise the workflow
should still return a complete draft in the handoff.

## Import Notes

This playbook is strongest when the imported specialists can read
existing runbooks, system notes, or policy constraints before drafting.
