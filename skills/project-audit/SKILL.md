# Skill: Project Audit

## Purpose

Audit an existing Unity game before changing it.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Unity repository or working tree

## Procedure

1. Identify Unity editor version from ProjectVersion.txt and inspect Packages/manifest.json.
2. Inventory scenes, main scripts/assemblies, packages, major runtime systems, save/persistence, input, UI, audio, analytics/ads, and build configuration.
3. Run or inspect compilation/build diagnostics when tools permit. Never assume the project is healthy because files exist.
4. Locate the current entry scene and describe the core gameplay loop.
5. Identify placeholders, TODOs, hard-coded limits, platform assumptions, and obvious technical debt relevant to the next stage.
6. Recommend the current pipeline stage and record blockers in PROJECT_STATE.md.

## Outputs

- PROJECT_STATE.md
- Audit summary

## Validation checklist

- [ ] Current build status is known
- [ ] Core loop location is known
- [ ] Blocking issues are recorded

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
