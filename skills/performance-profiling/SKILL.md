# Skill: Performance Profiling

## Purpose

Optimize measured Android bottlenecks against explicit budgets.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Target devices
- Current build

## Procedure

1. Define budgets for FPS/frame time, memory, load time, build size, and battery-sensitive behavior appropriate to the game.
2. Profile representative gameplay on target hardware or the closest available device.
3. Identify whether bottlenecks are CPU, GPU, memory, GC, I/O, asset size, overdraw, physics, or rendering related.
4. Change one bottleneck category at a time and remeasure.
5. Use pooling, batching, compression, LOD, reduced overdraw, texture sizing, or algorithmic changes only when measurements justify them.
6. Check visual/gameplay regression after optimization.

## Outputs

- Performance report
- Optimizations

## Validation checklist

- [ ] Before/after measurements recorded
- [ ] Budgets checked
- [ ] No unapproved quality regression

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
