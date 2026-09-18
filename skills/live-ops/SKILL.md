# Skill: Live Ops

## Purpose

Use evidence from released builds to plan bounded improvements.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Analytics
- Crash reports
- Player feedback
- Current roadmap

## Procedure

1. Review retention/funnel/economy/crash data only if the data is actually available and sufficiently reliable.
2. Identify a specific problem and separate observation from hypothesis.
3. Define one measurable update objective and success/guardrail metrics.
4. Prefer reversible tuning/content changes before risky architecture changes.
5. Plan rollout and rollback when remote configuration or staged rollout is available.
6. After release, compare results to the stated hypothesis and record learning.

## Outputs

- Live-ops brief
- Next iteration proposal

## Validation checklist

- [ ] Objective measurable
- [ ] Evidence cited internally
- [ ] Rollback path defined

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
