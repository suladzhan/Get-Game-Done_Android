# Skill: Data Driven Content

## Purpose

Scale levels/items/outcomes without duplicating logic.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Stable gameplay systems
- Content requirements

## Procedure

1. Define reusable content schemas and IDs.
2. Keep rules in systems and content differences in data.
3. Create authoring/validation tooling when manual mistakes become likely.
4. Validate references, duplicate IDs, missing assets, invalid ranges, and progression ordering.
5. Ensure adding content does not require copying gameplay scripts.

## Outputs

- Content schema
- Content data/authoring workflow

## Validation checklist

- [ ] New content can be added predictably
- [ ] Invalid content is detectable

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
