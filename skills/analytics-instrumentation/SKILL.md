# Skill: Analytics Instrumentation

## Purpose

Define and verify telemetry that answers product questions.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Product questions
- Approved analytics provider

## Procedure

1. Start from questions, not from an indiscriminate event dump.
2. Define event names, properties, trigger point, and expected cardinality in a tracking plan.
3. Use stable naming and avoid sending unnecessary personal data.
4. Instrument critical funnel events such as session start, tutorial completion, gameplay start/end, progression, purchases, and rewarded ad outcomes as applicable.
5. Verify events in provider debug/test tools before relying on dashboards.

## Outputs

- Tracking plan
- Analytics implementation

## Validation checklist

- [ ] Events have documented purpose
- [ ] Debug verification completed
- [ ] No secret/personal-data leak

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
