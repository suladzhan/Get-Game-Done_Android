# Skill: Responsive Ui

## Purpose

Make Unity UI robust across Android aspect ratios and safe areas.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Current UI
- Target orientation/device range

## Procedure

1. Choose a reference resolution and configure Canvas Scaler intentionally.
2. Use anchors/layout groups/content sizing deliberately instead of fixed-position assumptions.
3. Implement safe-area handling for cutouts/system bars where relevant.
4. Test common phone aspect ratios, long localization strings, large text where supported, and navigation/back behavior.
5. Ensure touch targets are practical and no critical UI is clipped or unreachable.

## Outputs

- Responsive UI changes
- Device/aspect test notes

## Validation checklist

- [ ] Critical screens pass target aspect ratios
- [ ] Safe area verified
- [ ] Touch targets usable

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
