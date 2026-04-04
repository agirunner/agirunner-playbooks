---
name: evaluation-review-rubric
description: Use when evaluation or benchmark results need to be reviewed before a change, model, or workflow revision is adopted.
---

# Evaluation Review Rubric

## Purpose
Review an evaluation packet for quality deltas, missing coverage, weak
evidence, and adoption risk.

## Use When
- a benchmark or replay packet is ready for review
- a workflow, model, or prompt revision needs a go or no-go recommendation
- the available results may be incomplete or misleading

## Do
- Restate what was evaluated, against what baseline, and why it matters.
- Check whether the coverage actually matches the claimed decision.
- Separate quality gains, regressions, and inconclusive areas.
- Flag benchmark gaps, weak sample size, and missing failure analysis.
- Recommend adoption only when the evidence is strong enough for the scope.

## Do Not
- Treat a small win on a narrow benchmark as broad proof.
- Ignore regressions because the average score improved.
- Hide missing coverage behind optimistic summary language.

## Output
- `evaluation_scope`
- `baseline_or_comparison`
- `quality_deltas`
- `coverage_gaps`
- `adoption_risk`
- `recommended_disposition`
