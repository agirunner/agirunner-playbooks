---
name: support-resolution-discipline
description: Use when a support case needs deeper investigation and a customer-safe resolution or escalation packet.
---

# Support Resolution Discipline

## Purpose
Turn a support case into a bounded resolution or escalation packet with
clear evidence, explicit gaps, and customer-safe guidance.

## Use When
- triage is complete but the case needs deeper investigation
- the next output should help a human resolve or escalate the case
- customer-facing wording must stay separate from internal notes

## Do
- Restate the case, impact, and current evidence before proposing resolution.
- Separate customer-safe output from internal investigation notes.
- Record what is known, what is missing, and what the next team must see.
- Recommend escalation only when the evidence supports it.
- Keep unresolved uncertainty visible in the final packet.

## Do Not
- Promise product or account actions that the workflow cannot perform.
- Hide missing evidence behind an overly confident customer answer.
- Mix internal diagnosis with customer-facing language.

## Output
- `case_summary`
- `evidence_reviewed`
- `customer_safe_response`
- `internal_notes`
- `open_questions`
- `recommended_next_step`
