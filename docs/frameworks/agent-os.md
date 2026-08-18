# Agent OS Starter Guide

**Category:** standards discovery, injection, and spec shaping  
**Best for:** established repositories with undocumented conventions or teams seeking consistent agent behavior  
**Upstream:** [buildermethods/agent-os](https://github.com/buildermethods/agent-os)  
**Upstream checked:** 2026-08-18

## What it changes

Agent OS v3 focuses on discovering engineering standards, indexing them, injecting relevant standards into work, establishing product context, and shaping persistent specs. It intentionally leaves most implementation orchestration to modern coding agents.

## Use it when

- repository patterns exist but are not documented;
- every prompt has to reteach the same conventions;
- several projects need shared but overridable standards;
- plans should reflect product mission and engineering constraints.

Do not select Agent OS expecting a complete autonomous delivery engine; v3 deliberately retired that responsibility.

## Start a project

The current official installation page distributes setup instructions after free access registration. Because those commands can change, use the official page rather than copying an old v1/v2 shell command:

1. Open [Agent OS installation](https://buildermethods.com/agent-os/installation).
2. Install the current v3 release into the repository.
3. In Claude Code, use the installed slash commands. In Cursor or another tool, reference the generated Markdown under `agent-os/` directly.
4. Begin by discovering standards from a well-implemented area.

```text
/discover-standards
/inject-standards
/plan-product
/shape-spec
```

Exact invocation outside Claude Code depends on the installed files and agent. Agent OS documents Cursor as file-based rather than a fully native slash-command integration.

## First exercise

Run standards discovery on one backend module. Review every extracted rule, remove accidental patterns, add evidence links, then inject the standards into a new feature plan.

## Production checklist

- Treat discovered patterns as candidates, not automatically good standards.
- Keep the standards index accurate and scoped.
- Separate organization defaults from project exceptions.
- Do not duplicate all standards in `AGENTS.md` and Agent OS.
- Pin or document the installed version.

## Sources

- [Agent OS v3 overview](https://buildermethods.com/agent-os)
- [Installation](https://buildermethods.com/agent-os/installation)
- [Workflow](https://buildermethods.com/agent-os/workflow)
- [v3 migration notes](https://buildermethods.com/agent-os/migration)
