# GSD Core Starter Guide

**Category:** lifecycle orchestration and context engineering  
**Best for:** solo developers and teams shipping multi-phase work across fresh agent contexts  
**Upstream:** [open-gsd/gsd-core](https://github.com/open-gsd/gsd-core)  
**Upstream checked:** 2026-08-18

## What it changes

GSD Core drives a milestone through **Discuss → Plan → Execute → Verify → Ship**. Heavy work runs in fresh-context subagents while durable files preserve decisions and state between sessions.

## Use it when

- a long feature degrades as the conversation fills;
- research, planning, execution, and verification need distinct phases;
- you must resume work reliably after a new session;
- tasks can be split into parallel, isolated waves.

Do not start here for a few straightforward edits. First fix repository instructions and verification.

## Start a project

Prerequisite: Node.js and a supported coding agent.

```bash
cd your-project
npx @opengsd/gsd-core@latest
```

Use the installer rather than copying the upstream `agents/` or `commands/` directories; it adapts files to the selected runtime. Choose Cursor, Claude Code, Codex, Copilot, Windsurf, or another offered runtime and select local or global installation.

Then open your coding agent in the repository:

```text
/gsd-new-project   # greenfield
/gsd-onboard       # existing codebase
```

Follow the generated discussion and planning flow. Review requirements and phase boundaries before execution.

## First exercise

Choose one vertical slice touching two components. Complete one phase, close the session, and use the framework’s resume flow. Verify that the new session recovers decisions without you retelling the story.

## Production checklist

- Keep generated state and plans in version control.
- Inspect parallel task boundaries for shared-file conflicts.
- Require deterministic checks during Verify.
- Review cost and token usage before enabling broad parallelism.
- Use `git diff` and full-system checks before Ship.

## Sources

- [GSD Core README and quickstart](https://github.com/open-gsd/gsd-core#quickstart)
- [First project tutorial](https://github.com/open-gsd/gsd-core/blob/main/docs/tutorials/your-first-project.md)
- [Onboarding an existing codebase](https://github.com/open-gsd/gsd-core/blob/main/docs/tutorials/onboarding-an-existing-codebase.md)
