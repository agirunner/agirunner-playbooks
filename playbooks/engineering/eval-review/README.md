# Eval Review

## Use When

Use this playbook when benchmark, replay, or evaluation results need a
human-readable review before a workflow, prompt, model, or revision is
adopted.

## Inputs

- evaluation subject
- benchmark packet if relevant
- comparison goal if relevant

## Output

The workflow should produce:
- evaluation scope
- baseline or comparison frame
- quality deltas
- coverage gaps
- adoption risk
- recommended disposition

## Workspace Notes

This playbook can operate entirely from artifacts, evaluation packets,
logs, and benchmark summaries. It does not require a writable code
workspace.

## Import Notes

Import this playbook when your tenant has enough evaluation evidence,
artifacts, or replay data for a reviewer to judge adoption honestly.
The authored workflow is intentionally conservative when the benchmark
scope is thin or the comparison frame is unclear.
