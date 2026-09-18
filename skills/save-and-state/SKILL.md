# Skill: Save And State

## Purpose

Implement safe local persistence for player progress/settings.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- State model
- Existing save system if any

## Procedure

1. List what must persist and what must reset per session.
2. Define a versioned save schema before storing long-lived progress.
3. Use safe defaults for missing/corrupt data.
4. Plan migrations before changing released save formats.
5. Test fresh install, save, reload, partial/corrupt data behavior, and upgrade path when applicable.

## Outputs

- Persistence implementation
- Schema/version notes

## Validation checklist

- [ ] Fresh state works
- [ ] Reload works
- [ ] Failure path is safe

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
