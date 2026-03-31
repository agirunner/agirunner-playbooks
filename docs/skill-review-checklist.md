# Skill Review Checklist

Shared skills are leverage points. A weak shared skill can degrade many
playbooks at once, so review them more strictly than one-off prompt
text.

## Review Questions

- Is the skill narrow enough to be reusable?
- Does the title describe a real operator or specialist capability?
- Does the `description` clearly tell the importer when to use it?
- Does the body produce reviewable outputs instead of vague good
  intentions?
- Does it tell the specialist what to verify before claiming completion?
- Does it avoid hidden workflow semantics that belong in a playbook?
- Does it avoid technology assumptions unless the skill is intentionally
  technology-specific?
- If it recommends a next responsible party, does it use authored
  specialist names only when the playbook actually provides them, and
  otherwise stick to route or function language instead of invented
  assignees?
- Does it avoid copying third-party skill text verbatim?

## Skill Content Standard

Every shared skill should make these things clear:
- purpose
- when to use it
- what to do
- what not to do
- required evidence or output shape
- failure and escalation cues when relevant
- a concise form factor, usually at or under 100 lines
- standard industry frameworks or quality bars when they genuinely help
  the reader act more consistently

## Reject Skills That

- are just role prompts disguised as skills
- depend on one repository layout
- depend on one named playbook
- require nonstandard frontmatter fields in `SKILL.md`
- mostly repeat generic advice without a concrete reviewable method
