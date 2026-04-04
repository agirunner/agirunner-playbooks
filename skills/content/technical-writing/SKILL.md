---
name: technical-writing
description: Use when technical facts, workflows, or product behavior must be turned into clear task-oriented documentation for a defined audience.
---

# Technical Writing

## Purpose
Translate technical reality into documentation that helps the reader act.

## Use When
- writing setup, usage, troubleshooting, or operator docs
- turning internal implementation knowledge into external documentation
- cleaning up dense or expert-only drafts

## Do
- Define the target reader and what they need to accomplish.
- Define the reader's likely starting context and what they already know.
- Name the document mode early so task guide, troubleshooting, and reference content do not blur together.
- Structure the document before drafting full prose.
- Lead with the task, not the internal implementation story.
- Lead with outcome, prerequisites, and the first action the reader must take.
- Split task flow, reference detail, and troubleshooting when one document needs more than one mode.
- Name the source truth you are relying on and the trust limits around it.
- Surface prerequisites, limits, and failure conditions early.
- Prefer concrete language and examples over vague reassurance.
- Check whether a new reader could complete the task without hidden context.
- If the source truth is partial or conflicting, narrow the draft and label validation questions directly.

## Do Not
- Mix reference material, process guidance, and release notes without structure.
- Assume the reader already knows internal jargon.
- Draft sections in final prose before the overall shape is clear.
- Explain every detail at the same depth.

## Output
- `target_reader`
- `document_goal`
- `document_type`
- `source_truth_basis`
- `required_prerequisites`
- `main_steps_or_sections`
- `important_limits`
- `open_questions`
- `follow_up_docs_needed`
