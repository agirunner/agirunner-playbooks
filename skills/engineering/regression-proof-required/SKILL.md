---
name: regression-proof-required
description: Use when a workflow claims a fix, safety improvement, or release candidate and needs explicit verification evidence rather than confidence alone.
---

# Regression Proof Required

## Purpose
No claimed fix is complete without evidence. The verification path may
change across workspace types, but the proof requirement does not.

## Use When
- a specialist claims a bug is fixed
- a reviewer is deciding whether evidence is enough
- a writable workspace is unavailable and the output must stay advisory

## Do
- Name the verification path actually used.
- Prefer repository-native tests or deterministic checks when they exist.
- If no runnable verification path exists, state that clearly and define
  the best available manual or advisory proof.
- Tie the proof directly to the changed behavior, not just nearby code.

## Do Not
- Treat “looks right” as verification.
- Hide missing tests behind vague confidence language.
- Claim complete regression coverage if you only proved one path.

## Output
- `verification_path`
- `evidence`
- `coverage_limits`
- `residual_risk`
- `release_recommendation`
