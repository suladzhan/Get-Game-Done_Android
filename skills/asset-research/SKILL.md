# Skill: Asset Research

## Purpose

Research third-party assets safely using browser/search access when available.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- ASSET_REQUIREMENTS.md
- ART_DIRECTION.md

## Procedure

1. Search reputable sources such as Unity Asset Store, publisher sites, or well-known open asset libraries.
2. For each candidate record exact URL, publisher/author, asset name/version, price, license, commercial-use status, attribution requirements, Unity/render-pipeline compatibility, and style fit.
3. Prefer a small number of coherent packs over many mismatched packs.
4. Never purchase or accept paid terms without human approval.
5. If license terms are unclear, mark the asset blocked instead of assuming permission.
6. If the agent cannot download/import directly, provide exact candidate names and links for a human.

## Outputs

- Asset shortlist
- docs/ASSET_REGISTER.md updates

## Validation checklist

- [ ] Every candidate has provenance
- [ ] License uncertainty is visible
- [ ] No unauthorized purchase

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
