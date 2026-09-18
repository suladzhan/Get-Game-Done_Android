# Android Game Dev Agents & Pipeline

An open-source, vendor-neutral AI production framework for building **Unity Android games** with specialized coding agents.

The repository turns the usual “one giant prompt” workflow into a repeatable production system:

**idea → design → prototype → MVP → content → assets → polish → mobile adaptation → optimization → QA → monetization/analytics → release → live ops**

It is designed to work with tools such as Astra, Codex, Claude Code, Gemini CLI, or any other coding agent that can read project files and modify a Unity repository.

## Why this exists

AI agents are good at implementing bounded tasks, but game projects become unstable when one agent is simultaneously acting as game designer, programmer, artist, tester, build engineer, and release manager. This framework separates those responsibilities and adds written stage gates, handoffs, and safety rules.

The framework does **not** require a particular Unity architecture, render pipeline, backend, ad network, analytics provider, or AI vendor.

## Production pipeline

```text
00 Discovery / Project Audit
        ↓
01 Concept & Game Design
        ↓
02 Core-Loop Prototype
        ↓
03 MVP / Vertical Slice
        ↓
04 Content, Progression & Economy
        ↓
05 Art Direction & Asset Acquisition
        ↓
06 Visual Polish & Game Feel
        ↓
07 Audio & Haptics
        ↓
08 Android / Mobile Adaptation
        ↓
09 Performance Optimization
        ↓
10 QA & Regression
        ↓
11 Monetization & Analytics
        ↓
12 Release Preparation
        ↓
13 Live Ops & Iteration
```

A later stage may reopen an earlier stage if testing finds a blocking problem. The important rule is that the rollback is explicit and documented in `PROJECT_STATE.md`.

## Quick start

Copy this framework into your Unity repository, then create your project documents from `templates/`.

Give your coding agent this boot prompt:

```text
Read AGENTS.md, PIPELINE.md, pipeline.yaml, PROJECT_STATE.md, and the relevant agent/skill files.
Act as the Orchestrator.
Audit the Unity project, determine the current production stage, identify blockers,
and execute only the next approved stage.
Do not skip stage exit criteria.
Do not perform purchases, publish builds, change credentials, or introduce paid services without explicit human approval.
At the end, update PROJECT_STATE.md and create a stage report using templates/STAGE_REPORT.md.
```

For a new project, start by filling in `docs/GAME_DESIGN.md`. For an existing game, start with the `project-audit` skill.

## Repository structure

```text
.
├── AGENTS.md                  # global rules and agent operating model
├── PIPELINE.md                # human-readable production workflow
├── pipeline.yaml              # machine-readable orchestration map
├── agents/                    # role definitions
├── skills/                    # reusable procedures
├── templates/                 # project documents and handoff templates
├── docs/                      # place project-specific docs here
├── schemas/                   # optional machine-readable report schema
├── adapters/                  # notes for specific AI tools
└── examples/                  # example project state / reports
```

## Agent model

Agents are **roles**, not necessarily separate model processes. A single coding agent can assume different roles sequentially. If your tool supports subagents, each file in `agents/` can be mapped to a dedicated subagent.

The Orchestrator owns sequencing, scope, stage gates, and handoffs. Specialist agents own only their assigned domain. A specialist must not silently redesign unrelated systems.

## Skill model

Skills are reusable operating procedures. Each skill lives in its own folder as `SKILL.md`, so the procedure can be copied into agent systems that support skill directories.

Skills state:

- when to use them
- required inputs
- procedure
- expected outputs
- validation checks
- stop / escalation conditions

## Browser and external assets

Browser access is useful for asset research, documentation lookup, SDK compatibility checks, and store requirements. It must not become uncontrolled downloading.

The Asset Scout should record the exact source, author/publisher, license, cost, and intended use for every third-party asset. It must never purchase assets, accept paid terms, redistribute proprietary assets, or import unclear-license content without approval.

## Human approval gates

Explicit human approval is required before any of the following:

- purchasing an asset or service
- accepting a paid subscription
- publishing to Google Play or another store
- creating/rotating production credentials
- changing signing keys / keystores
- deleting production data or cloud resources
- enabling real-money purchases or live ad serving
- making a destructive migration to player save data

## Open-source usage

This framework is licensed under MIT. You can use it inside commercial games, fork it, adapt it to another engine, or build your own orchestration layer around it.

See `CONTRIBUTING.md` for contribution guidance.
