# Skill: Audio Haptics

## Purpose

Add intentional audio and haptic feedback.

## Use when

The active pipeline stage assigns this skill, or the Orchestrator explicitly invokes it to resolve a blocker.

## Required inputs

- Gameplay event list
- Art/game feel direction

## Procedure

1. Map major events to SFX, music states, and haptic patterns.
2. Avoid haptics for every tap; reserve stronger feedback for meaningful events.
3. Implement master/music/SFX controls and persist them.
4. Handle app pause/resume, focus loss, and audio interruptions.
5. Record licenses/provenance for external audio.

## Outputs

- Audio/haptic event map
- Implementation

## Validation checklist

- [ ] Major events covered
- [ ] Settings persist
- [ ] Lifecycle behavior checked

## Stop / escalate when

Stop and report to the Orchestrator when required inputs are missing, the task would cross an approval gate, the requested change conflicts with approved design, or validation cannot be performed reliably.
