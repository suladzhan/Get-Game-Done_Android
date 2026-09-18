# Skill: Progression Economy

## Purpose

Design progression and economy that support long-term play without arbitrary accidental ceilings.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Core loop
- Content plan
- Monetization assumptions if approved

## Procedure

1. List every currency/resource source and sink.
2. Define unlock pacing, upgrade curves, price curves, reward curves, and intended session progression.
3. Check for deadlocks, runaway inflation, impossible goals, and unintended hard caps.
4. Use simulations/spreadsheets when curves become non-trivial.
5. Separate tuning values from code so balancing does not require logic rewrites.

## Outputs

- Economy specification
- Tuning data

## Validation checklist

- [ ] Sources/sinks documented
- [ ] No accidental hard cap
- [ ] Progression sanity checked

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
