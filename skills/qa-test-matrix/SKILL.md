# Skill: Qa Test Matrix

## Purpose

Create and execute repeatable functional/regression testing.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Current stage acceptance criteria
- Supported devices/locales

## Procedure

1. Create cases for fresh install, first launch, tutorial, core loop, win/fail, restart, save/load, shop/progression, settings, localization, offline/poor network if relevant, rapid input, background/foreground, device rotation if supported, and long sessions.
2. Record expected result, actual result, build/version, device, and reproducible steps.
3. Classify defects by severity and release impact.
4. Retest fixes and run focused regression around changed systems.
5. Do not close critical defects based only on code review.

## Outputs

- docs/QA_CHECKLIST.md
- Bug reports

## Validation checklist

- [ ] Release-critical tests recorded
- [ ] No blocker remains open

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
