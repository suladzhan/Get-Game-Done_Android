# Astra Adapter Notes

This framework does not assume a specific Astra product version or tool interface.

Use the repository files as the source of truth. If your Astra environment supports project instructions, skills, subagents, browser tools, or MCP-style integrations, map them as follows:

- global project instructions → `AGENTS.md`
- orchestrator prompt → `agents/orchestrator.md`
- specialist/subagent prompts → individual files in `agents/`
- reusable skills → `skills/*/SKILL.md`
- workflow state → `PROJECT_STATE.md`
- stage graph → `pipeline.yaml`

## Recommended bootstrap prompt

```text
Read AGENTS.md, PIPELINE.md, pipeline.yaml, PROJECT_STATE.md, and all files referenced by the active stage.
Act as the Orchestrator. Do not skip exit criteria.
Use specialist roles for bounded work and keep a written handoff.
If browser access is available, use it only under the external-research and approval rules.
```

## Browser access

Do not assume Astra has browser access just because it can edit a Unity project. Browser/search capabilities depend on the specific environment and tools connected to it.

When browser access is available, the `asset-research` skill defines what the agent may do. Keep purchase, licensing acceptance, production account changes, and publishing behind human approval.
