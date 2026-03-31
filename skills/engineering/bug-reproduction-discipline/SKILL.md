---
name: bug-reproduction-discipline
description: Use when a workflow must diagnose a defect, prove the current behavior, or bound an issue before changing code or configuration.
---

# Bug Reproduction Discipline

## Purpose
Bound the defect before proposing a fix. If a full reproduction is not
possible, narrow the failure surface enough that the next change is
deliberate instead of guessed.

## Use When
- a bug report is incomplete or contradictory
- the failure is intermittent
- a specialist is tempted to jump straight to code changes
- a later reviewer will need evidence that the fix addressed the right issue

## Do
- Restate the claimed defect in one sentence.
- Name the trigger, environment, and smallest known path to the failure.
- Identify the exact evidence available now: logs, tests, reports,
  screenshots, code paths, or operator notes.
- Observe the system before changing it. Inspect the rendered state, logs,
  or outputs that demonstrate the defect.
- Reproduce the issue directly when possible.
- If direct reproduction is not possible, bound the defect with the
  narrowest credible explanation and say what remains unproven.
- Name the files, modules, or behaviors most likely involved before
  proposing a fix.

## Do Not
- Claim reproduction when you only inferred the failure.
- Jump from the first plausible symptom straight to a fix.
- Expand the scope into adjacent cleanup.
- Treat a suspected root cause as proven without evidence.

## Output
- `observed_behavior`
- `expected_behavior`
- `reproduction_path`
- `evidence_used`
- `current_scope`
- `confidence`
- `next_change_target`
