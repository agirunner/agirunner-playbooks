# Changelog

All notable changes to this repository will be documented in this file.

This public catalog evolves continuously. Section naming follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), but this file
is maintained as an ongoing catalog history rather than a release log.

## 2026-03-31

### Added

- Public catalog structure for community-contributed playbooks,
  specialists, and skills
- Authoring and review docs under `docs/`
- Human-readable schema references under `schemas/`
- Catalog manifests for skills, specialists, playbooks, categories, and
  tool profiles under `catalog/`
- 17 shared skills across engineering, operations, research, compliance,
  and content
- 15 shared specialists built on those skills
- 12 stable playbooks across operations, research, compliance, and
  content
- 5 experimental engineering playbooks for narrow SDLC workflows

### Changed

- Standardized specialist tool configuration around the shared
  `all-specialist-tools` profile
- Standardized playbook prose conventions around `Preferred flow`,
  `Recovery and exception handling`, `Completion rules`, and
  `Guided closure rule`
- Replaced support-triage owner language with route-oriented outputs and
  added authoring guidance to avoid invented tenant-specific assignees
  unless the named target is an authored specialist
- Strengthened content, SOP, and engineering verification skills around
  reader testing, structured drafting, reconnaissance, and evidence
  capture
- Tightened compliance and research skills around source grounding,
  claim boundaries, recency, and explicit unknowns
- Simplified specialist definitions to fields the catalog and platform
  actually use, leaving escalation and recovery behavior in prompts and
  playbook prose
- Sharpened the engineering code review skill around architectural fit,
  surrounding context, explicit assumptions, and finding severity
- Hardened playbook prose around weak-input handling, bounded outputs,
  and non-fake closure when evidence is incomplete
- Strengthened the engineering security review skill around provenance,
  privilege, injection, isolation, and governance checks
- Improved root documentation to match the current repository structure
  and contribution model
- Added explicit playbook author metadata across the catalog and aligned
  the root contribution docs and schema references with that metadata
