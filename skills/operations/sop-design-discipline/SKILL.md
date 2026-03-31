---
name: sop-design-discipline
description: Use when a team needs a standard operating procedure that can be followed consistently by different operators across normal and exception cases.
---

# SOP Design Discipline

## Purpose
Write procedures that stay useful after the original author is gone.

## Use When
- converting a repeated workflow into a standard process
- cleaning up an inconsistent or tribal-knowledge-driven procedure
- defining ownership, checkpoints, and exception handling

## Do
- Define scope, trigger, owner, inputs, and expected outputs.
- Keep each step at one clear level of abstraction.
- Call out decision points and exception paths explicitly.
- Specify what “done” means for the procedure.

## Do Not
- Mix policy rationale, operator steps, and troubleshooting without structure.
- Leave exception handling to “use judgment” unless the judgment boundary
  is made explicit.
- Write steps that only make sense to the original author.

## Output
- `scope`
- `roles_or_owners`
- `inputs`
- `procedure_steps`
- `exceptions`
- `completion_definition`
