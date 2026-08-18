# Cursor Memory Bank Starter Guide

**Category:** Cursor-specific persistent context and phased workflow  
**Best for:** projects where Cursor sessions repeatedly lose active task state or design decisions  
**Upstream:** [vanzan01/cursor-memory-bank](https://github.com/vanzan01/cursor-memory-bank)  
**Upstream checked:** 2026-08-18

## What it changes

Memory Bank uses six Cursor commands and shared Markdown state: `/van`, `/plan`, `/creative`, `/build`, `/reflect`, and `/archive`. Workflow depth changes with estimated task complexity.

## Use it when

- Cursor is your primary harness;
- active state must survive conversations;
- design exploration should be explicit;
- you want progressive loading rather than one giant rules file.

The upstream maintainer describes it as a personal hobby project without an actively maintained issue tracker. Factor that into adoption.

## Start a project

Official prerequisite: Cursor 2.0+.

Clone upstream separately, then copy its `.cursor` directory into your project. Do not nest the whole repository inside your application.

```bash
git clone https://github.com/vanzan01/cursor-memory-bank.git
```

After copying `.cursor/`, start in Cursor:

```text
/van Add organization-scoped audit history
```

Follow the route selected for complexity:

```text
Level 1: /van → /build → /reflect → /archive
Level 2: /van → /plan → /build → /reflect → /archive
Level 3–4: /van → /plan → /creative → /build → /reflect → /archive
```

## First exercise

Complete and archive one Level 2 change. Start a new session and verify that active versus archived context remains clear and that irrelevant history is not loaded.

## Production checklist

- Review copied rules before trusting them.
- Keep active files concise; archive completed task details.
- Prevent conflicts with another framework’s plan/state files.
- Treat “memory” as retrieval, not model training.
- Own any local modifications because upstream support is limited.

## Sources

- [Memory Bank README](https://github.com/vanzan01/cursor-memory-bank)
- [Command documentation](https://github.com/vanzan01/cursor-memory-bank/tree/main/.cursor/commands)
