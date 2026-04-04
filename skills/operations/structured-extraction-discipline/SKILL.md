---
name: structured-extraction-discipline
description: Use when a messy source needs to be turned into structured fields with evidence notes, ambiguity handling, and exceptions.
---

# Structured Extraction Discipline

## Purpose
Extract structured fields from messy sources without hiding ambiguity,
missing values, or weak evidence.

## Use When
- the input is a document, filing, page set, or other semi-structured source
- the output needs to follow a schema or target field list
- low-confidence fields must stay visible

## Do
- Restate the target fields or schema before extracting.
- Keep source evidence close to each important extracted value.
- Distinguish missing, ambiguous, and not-applicable values.
- Normalize formats only when the source supports it.
- Route low-confidence or exception cases into explicit notes.

## Do Not
- Invent values because the schema expects them.
- Collapse ambiguity into one overconfident field.
- Return a clean-looking structure that hides extraction uncertainty.

## Output
- `target_schema_or_fields`
- `structured_output`
- `evidence_notes`
- `ambiguous_fields`
- `exceptions`
- `recommended_next_step`
