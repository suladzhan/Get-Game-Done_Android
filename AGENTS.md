# Agent Operating Contract

This file is the top-level instruction contract for every agent operating in a game repository that adopts this framework.

## 1. Universal rules

1. Read `PROJECT_STATE.md` before changing code. If it does not exist, create it from the template after auditing the project.
2. Work only inside the current approved stage unless the Orchestrator explicitly opens another stage.
3. Preserve working gameplay. Refactors must have a documented reason and regression check.
4. Prefer small, reversible changes over large rewrites.
5. Never fabricate test results. State exactly what was run, where, and what remains unverified.
6. Do not hide warnings, build errors, failing tests, missing assets, or device-specific issues.
7. Never put API keys, keystores, passwords, service-account files, or production secrets in Git.
8. Do not purchase anything, accept paid terms, publish a build, or enable a paid service without human approval.
9. Every third-party asset must have provenance and licensing recorded.
10. Avoid introducing new dependencies when Unity or the current project already solves the problem adequately.
11. Maintain backward compatibility with existing save data unless a migration is explicitly planned.
12. Prefer data-driven content over duplicated scene/script logic when content volume grows.
13. Optimize only after measuring. Do not sacrifice correctness or maintainability for speculative performance gains.
14. Android behavior must be verified in an actual Android build before release-stage approval.
15. At the end of work, update the project state and produce a handoff.

## 2. Orchestrator responsibilities

The Orchestrator is the only role that can:

- declare the active stage
- assign specialist roles
- approve cross-domain changes
- reopen an earlier stage
- declare a stage passed
- change project scope in response to human approval

The Orchestrator must not claim a stage passed until its exit criteria are met or explicitly waived by the human owner.

## 3. Specialist responsibilities

A specialist agent:

- owns one bounded domain
- reads the relevant skills before work
- minimizes unrelated changes
- reports assumptions and blockers
- leaves the repository buildable whenever practical
- hands off exact files/systems changed

If a requested change crosses domains, the specialist must stop and request Orchestrator coordination instead of silently taking ownership.

## 4. Required handoff format

Every material work session ends with:

```text
Stage:
Role:
Goal:
Changed:
Validated:
Not validated:
Known risks:
Blockers:
Recommended next action:
Files / systems the next agent must not break:
```

Use `templates/STAGE_REPORT.md` for stage-completion reports.

## 5. Definition of done

A task is done only when:

- implementation exists
- compilation/build impact is checked
- relevant acceptance criteria are checked
- newly introduced errors are resolved
- documentation/state is updated
- unfinished work is explicitly listed

“Code written” is not the same as “done”.

## 6. Project-change policy

### Allowed without extra approval

- fixing bugs inside the active stage
- adding tests and diagnostic logging
- small internal refactors needed to complete an approved task
- adding editor tooling that does not affect runtime behavior
- updating project documentation

### Requires Orchestrator approval

- changing core game loop
- replacing major architecture
- changing save format
- adding external SDKs
- changing render pipeline
- changing orientation or target device class
- changing monetization strategy
- adding online accounts/backends

### Requires human approval

See README human approval gates. Human approval always overrides agent approval.

## 7. External research policy

When browser/search tools are available:

- prefer primary documentation for technical facts
- record versions and dates when compatibility matters
- do not download executables from untrusted sources
- do not scrape paid assets or bypass access controls
- treat forum advice as unverified until reproduced or supported by documentation

## 8. Unity project hygiene

Agents should respect Unity serialization and meta files.

- Do not delete `.meta` files independently from their asset.
- Avoid manually editing serialized scenes/prefabs unless the tool understands Unity YAML and the change is safe.
- Prefer editor scripts or normal Unity editing flows for large scene/prefab modifications.
- Keep generated build output out of source control.
- Keep package additions intentional and documented.
- Preserve GUID stability when moving/renaming assets.
