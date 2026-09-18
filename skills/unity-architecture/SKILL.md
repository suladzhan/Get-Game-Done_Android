# Skill: Unity Architecture

## Purpose

Keep Unity runtime architecture understandable and maintainable.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Existing codebase
- Approved system requirements

## Procedure

1. Prefer clear ownership of game state and explicit dependencies over hidden scene lookups.
2. Use ScriptableObjects/config data where they simplify authoring; do not force them everywhere.
3. Separate configuration/data from runtime state.
4. Avoid duplicated business/gameplay rules across UI and gameplay components.
5. Keep scene/prefab dependencies intentional and preserve GUID/meta integrity.
6. Add abstractions only when there are multiple real implementations or a clear testing/maintenance benefit.

## Outputs

- Maintainable runtime changes

## Validation checklist

- [ ] No circular ownership introduced
- [ ] Core systems have clear responsibility
- [ ] Project remains buildable

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
