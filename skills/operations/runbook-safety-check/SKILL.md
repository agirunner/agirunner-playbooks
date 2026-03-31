---
name: runbook-safety-check
description: Use when a procedural runbook or operational workflow must be reviewed for safety, rollback readiness, and operator clarity.
---

# Runbook Safety Check

## Purpose
Make sure an operator can follow the runbook safely under pressure.

## Use When
- creating or updating an operational runbook
- reviewing incident or maintenance procedures
- preparing a workflow that includes manual operator steps

## Do
- Check prerequisites, permissions, and environmental assumptions.
- Check validation steps, communication checkpoints, and blast-radius notes.
- Check whether rollback or recovery steps are explicit.
- Check whether irreversible actions are clearly marked.
- Check whether the sequence is safe if an operator joins halfway through.

## Do Not
- Assume expert tribal knowledge fills in missing steps.
- Hide dangerous steps inside long paragraphs.
- Treat verification and rollback as optional.

## Output
- `safety_findings`
- `missing_prerequisites`
- `rollback_gaps`
- `operator_clarity_notes`
- `recommended_changes`
