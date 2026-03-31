---
name: customer-support-triage-rubric
description: Use when incoming customer issues or requests must be classified, prioritized, and routed to the next owner with minimal ambiguity.
---

# Customer Support Triage Rubric

## Purpose
Turn an inbound support item into a clear next action with sensible
priority and ownership.

## Use When
- support volume needs consistent triage
- issue reports arrive with mixed quality
- an operator needs a concise severity and routing decision

## Do
- Separate bug report, usage question, access issue, billing issue, and
  feature request.
- Identify urgency, impact, and whether the issue blocks business use.
- Ask for missing facts only when they materially change priority or routing.
- Recommend the next owner and the next visible action.

## Do Not
- Inflate severity without evidence of real impact.
- Leave ownership ambiguous.
- Promise an engineering fix when a support or documentation path is enough.

## Output
- `issue_type`
- `severity`
- `customer_impact`
- `missing_information`
- `recommended_owner`
- `next_action`
