---
name: customer-support-triage-rubric
description: Use when incoming customer issues or requests must be classified, prioritized, and routed with minimal ambiguity.
---

# Customer Support Triage Rubric

## Purpose
Turn an inbound support item into a clear next action with sensible
priority and routing.

## Use When
- support volume needs consistent triage
- issue reports arrive with mixed quality
- an operator needs a concise severity and routing decision

## Do
- Separate bug report, usage question, access issue, billing issue, and
  feature request.
- Identify urgency, impact, and whether the issue blocks business use.
- Use impact, urgency, and any stated service commitments or SLA context
  instead of customer tone alone.
- Ask for missing facts only when they materially change priority or routing.
- Recommend the next responsible route and the next visible action.
- If the next step stays inside the authored workflow, name the playbook
  specialist literally. Otherwise use a functional route such as billing
  support, account administration, documentation, or engineering
  investigation instead of inventing a person-level assignee.

## Do Not
- Inflate severity without evidence of real impact.
- Leave the next route ambiguous.
- Promise an engineering fix when a support or documentation path is enough.

## Output
- `issue_type`
- `severity`
- `customer_impact`
- `missing_information`
- `recommended_route`
- `routing_rationale`
- `next_action`
