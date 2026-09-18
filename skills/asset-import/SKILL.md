# Skill: Asset Import

## Purpose

Import approved assets into Unity without destabilizing the project.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Approved asset files/packages
- Asset register

## Procedure

1. Back up/commit current project state before a large import.
2. Import into a clear project folder structure without breaking package ownership.
3. Inspect demo scenes/scripts before importing optional extras; avoid bringing unrelated systems into production.
4. Check render pipeline/material compatibility, texture import settings, sprite settings, audio import settings, and platform overrides.
5. Preserve license/readme files when required and update the asset register.
6. Run compilation and inspect warnings after import.

## Outputs

- Imported assets
- Updated asset register

## Validation checklist

- [ ] Project compiles
- [ ] Imported assets are traceable
- [ ] No unnecessary demo code left active

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
