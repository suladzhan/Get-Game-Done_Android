# Skill: Monetization Integration

## Purpose

Integrate approved ads/IAP without breaking gameplay or player trust.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Approved monetization design
- Chosen SDK/provider

## Procedure

1. Use provider test mode and test IDs first.
2. Define placement rules and failure behavior before integration.
3. For rewarded ads, grant reward only after verified completion according to SDK semantics.
4. For IAP, make purchase restoration and duplicate/retry behavior explicit.
5. Keep monetization failure non-blocking for core gameplay unless the product explicitly requires otherwise.
6. Handle consent/privacy requirements relevant to the selected providers and regions.
7. Human approval is required before enabling live ads or real-money IAP.

## Outputs

- Monetization implementation
- Test report

## Validation checklist

- [ ] Test flows pass
- [ ] Failure path safe
- [ ] Live mode not enabled without approval

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
