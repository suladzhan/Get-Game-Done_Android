# Skill: Android Build

## Purpose

Produce and diagnose reproducible Android builds.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Unity project
- Android target requirements

## Procedure

1. Confirm Unity Android Build Support, SDK/NDK/JDK configuration, package identifier, min/target SDK settings, architecture, orientation, and build system.
2. Keep development and release signing separate. Never commit keystores/passwords.
3. Use development builds for diagnostics when appropriate.
4. Test install/update/launch on a real device.
5. Capture build errors with full relevant logs before changing dependencies blindly.
6. For store release, produce AAB unless project requirements explicitly differ.

## Outputs

- APK/AAB build or build report

## Validation checklist

- [ ] Build result recorded
- [ ] Real device launch checked when possible
- [ ] Secrets not committed

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
