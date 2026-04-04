---
name: test-plan-execution-discipline
description: Use when a bounded test plan needs to become an explicit verification packet with run status, failures, and open gaps.
---

# Test Plan Execution Discipline

## Purpose
Turn a test plan into a stepwise verification packet without hiding
unrun items, weak evidence, or coverage gaps.

## Use When
- the workflow is asked to execute or assess a structured test plan
- a release or fix needs a verification packet
- some plan steps may be advisory-only or not directly runnable

## Do
- Restate the test scope and plan steps before execution.
- Use the strongest available evidence path for each step.
- Record pass, fail, blocked, skipped, or not-run status per step.
- Preserve failures and unverified items explicitly.
- Summarize what the plan proves and what it still does not prove.

## Do Not
- Mark the whole plan green when key steps were not run.
- Hide blocked or skipped steps in narrative summary text.
- Claim full regression coverage from a partial plan.

## Output
- `test_scope`
- `step_results`
- `failures`
- `blocked_or_skipped_steps`
- `coverage_gaps`
- `recommended_next_step`
