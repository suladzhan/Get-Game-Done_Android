# Skill: Google Play Release

## Purpose

Prepare a compliant, reproducible Google Play release candidate.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Release candidate
- Store account requirements

## Procedure

1. Increment version code/version name intentionally.
2. Build signed release AAB using protected signing material.
3. Prepare icon, feature graphic/screenshots, description, privacy-policy link, release notes, and support contact as applicable.
4. Complete applicable Play Console declarations such as app access, ads, content rating, target audience, data safety, and permissions based on the actual app.
5. Use internal/closed testing before production.
6. Create a rollback/previous-version plan and archive build metadata.
7. Publishing to production requires explicit human approval.

## Outputs

- docs/RELEASE_CHECKLIST.md
- Release candidate

## Validation checklist

- [ ] AAB installs through test track when available
- [ ] Checklist complete
- [ ] Human approval pending/recorded

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
