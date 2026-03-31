---
name: vendor-assessment
description: Use when multiple vendors or products must be compared against explicit requirements, constraints, and risks.
---

# Vendor Assessment

## Purpose
Compare options against the needs that actually matter to the buyer.

## Use When
- evaluating vendors, tools, or service providers
- preparing shortlist recommendations
- a buying decision needs structured tradeoffs, not generic pros and cons

## Do
- Define the evaluation criteria before ranking vendors.
- Separate must-have requirements from nice-to-have preferences.
- Separate confirmed capability from vendor claim, roadmap promise, or assumption.
- Compare capability, implementation cost, operating risk, and lock-in.
- Check total cost of ownership, exit cost, and control-plane dependencies when they materially affect the decision.
- Note implementation assumptions or integration dependencies that materially affect ranking.
- Flag unknowns that materially affect the decision.

## Do Not
- Score vendors on invented criteria that do not serve the decision.
- Hide must-have failures inside an averaged comparison.
- Treat marketing claims as confirmed capability without evidence.
- Recommend a winner while major decision-critical gaps remain unknown.

## Output
- `decision_scope`
- `evaluation_criteria`
- `vendor_comparison`
- `material_risks`
- `unknowns`
- `recommended_option`
