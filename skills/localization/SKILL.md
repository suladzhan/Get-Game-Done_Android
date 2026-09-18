# Skill: Localization

## Purpose

Prepare and validate localization without hard-coded UI breakage.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Supported locales
- UI/content strings

## Procedure

1. Externalize player-facing strings and use stable keys.
2. Define fallback locale behavior.
3. Avoid concatenating translated fragments when grammar may vary.
4. Handle plural/number/date formatting where needed.
5. Test text expansion, missing keys, fonts/glyph coverage, and RTL only if supported.
6. For auto-locale selection, allow the player to override language manually.

## Outputs

- Localization data
- Localization QA notes

## Validation checklist

- [ ] No critical hard-coded strings
- [ ] Fallback works
- [ ] Key screens survive text expansion

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
