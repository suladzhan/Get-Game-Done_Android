# Generic Coding Agent Adapter

For agents without native subagent/skill support, run the roles sequentially in one conversation/session.

Before each task:

1. Read `AGENTS.md`.
2. Read the active role in `agents/`.
3. Read every `SKILL.md` assigned by `pipeline.yaml`.
4. Read `PROJECT_STATE.md` and relevant project docs.
5. Execute the bounded task.
6. Update state and handoff before switching roles.

This preserves the same workflow even when the AI tool exposes only one agent process.
