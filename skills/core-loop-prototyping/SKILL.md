# Skill: Core Loop Prototyping

## Purpose

Build and validate the smallest playable core loop.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Approved GAME_DESIGN.md

## Procedure

1. Use placeholders and simple geometry/UI.
2. Implement only input, core mechanic, feedback necessary to understand state, win/fail, and restart.
3. Keep code easy to replace; avoid premature frameworks.
4. Add lightweight debug controls/logging when useful.
5. Play-test the complete loop repeatedly before expanding content.

## Outputs

- Playable prototype

## Validation checklist

- [ ] Start-to-result loop works
- [ ] Restart works
- [ ] No blocking errors

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
