# Production Pipeline

This document defines the stage-by-stage workflow. `pipeline.yaml` is the machine-readable companion.

## Stage 00 — Discovery / Project Audit

**Lead:** Orchestrator + Project Auditor skill

Purpose: understand what already exists before touching it.

Required outputs: project inventory, Unity version, target platform, scenes, major systems, known errors, current build status, dependencies, save model, current stage recommendation, and `PROJECT_STATE.md`.

Exit gate: the agent can explain how to run the game, where the core loop lives, what currently works, and what blocks the next stage.

## Stage 01 — Concept & Game Design

**Lead:** Game Designer

Lock the audience, platform, orientation, core loop, controls, session length, fail/win conditions, progression, economy concept, content model, visual direction, monetization assumptions, and non-goals.

Exit gate: `GAME_DESIGN.md` is specific enough for an engineer to prototype without inventing the core rules.

## Stage 02 — Core-Loop Prototype

**Lead:** Prototype Engineer

Build the smallest playable loop using placeholders. No production polish.

Exit gate: player can start, perform the central action, reach win/fail, and restart; no blocking compile/runtime errors.

## Stage 03 — MVP / Vertical Slice

**Lead:** Gameplay & Systems Engineer

Create one complete end-to-end experience: launch → menu → gameplay → result → reward → progression/shop → replay. Add save/load and basic settings where applicable.

Exit gate: a new user can play a complete session without editor intervention.

## Stage 04 — Content, Progression & Economy

**Lead:** Content & Economy Designer + Gameplay & Systems Engineer

Expand content and long-term systems only after the loop is stable. Favor data-driven authoring. Balance progression pacing and remove arbitrary hard caps unless the design requires them.

Exit gate: target content volume exists or is generated through a maintainable content pipeline; economy has documented sources/sinks and sanity checks.

## Stage 05 — Art Direction & Asset Acquisition

**Lead:** Art Director + Asset Scout

Define one coherent art direction, inventory placeholders, create `ASSET_REQUIREMENTS.md`, research/generate/import licensed assets, and record provenance.

Exit gate: required asset categories are available or explicitly blocked; no unknown-license production asset remains.

## Stage 06 — Visual Polish & Game Feel

**Lead:** Visual Polish Engineer

Replace placeholders, improve UI hierarchy, animation, VFX, transitions, feedback, camera behavior, and reward presentation without changing core rules.

Exit gate: visual language is consistent and key actions provide clear feedback.

## Stage 07 — Audio & Haptics

**Lead:** Audio & Haptics Designer

Add music, SFX, UI feedback, gameplay cues, haptics, volume controls, and lifecycle behavior.

Exit gate: all major player actions have intentional audio/haptic treatment; mute/volume settings work.

## Stage 08 — Android / Mobile Adaptation

**Lead:** Mobile Adaptation Engineer

Verify responsive layout, safe areas, touch input, back behavior, pause/resume, orientation, density/aspect ratios, localization expansion, and real-device builds.

Exit gate: core flows pass on target Android devices/resolutions and no critical UI is obscured or unreachable.

## Stage 09 — Performance Optimization

**Lead:** Performance Engineer

Profile before changing. Optimize frame time, allocations, memory, textures, draw calls, load time, battery-heavy behavior, and build size according to project targets.

Exit gate: documented performance budget is met on target hardware or remaining misses are explicitly accepted.

## Stage 10 — QA & Regression

**Lead:** QA Engineer

Execute functional, exploratory, lifecycle, persistence, edge-case, localization, device, and regression testing. Bugs must be reproducible and prioritized.

Exit gate: no open blocker/critical defects; release-relevant tests have recorded results.

## Stage 11 — Monetization & Analytics

**Lead:** Monetization & Analytics Engineer

Integrate approved ads/IAP/analytics only after the game is stable. Define events before instrumenting them. Test test-mode purchases/ads first. Handle consent/privacy requirements applicable to the chosen stack.

Exit gate: monetization flows fail safely, analytics events are documented/verified, and no production secret is committed.

## Stage 12 — Release Preparation

**Lead:** Release Manager

Prepare signing, versioning, AAB, store assets, privacy disclosures, data safety declarations, testing track, crash checks, release notes, and rollback plan.

Publishing itself requires human approval.

Exit gate: a release candidate exists and the release checklist is complete.

## Stage 13 — Live Ops & Iteration

**Lead:** Live Ops Analyst

Use real telemetry and player feedback to identify problems, create hypotheses, propose bounded experiments/updates, and feed approved work back into earlier stages.

Exit gate: each update has a measured objective, rollback path, and post-release review.
