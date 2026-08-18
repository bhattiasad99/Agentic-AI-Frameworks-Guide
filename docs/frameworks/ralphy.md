# Ralphy Starter Guide

**Category:** autonomous coding loop  
**Best for:** objective tasks or PRDs with strong automated validation  
**Upstream:** [michaelshimeles/ralphy](https://github.com/michaelshimeles/ralphy)  
**Upstream checked:** 2026-08-18

## What it changes

Ralphy repeatedly runs a selected coding agent against a task or PRD. It supports several engines, project rules, test/build commands, task branches, parallel execution, worktrees, and optional PR creation.

## Use it when

- tasks have unambiguous completion signals;
- tests and linting are difficult to game;
- unattended iteration saves real time;
- work can be isolated and bounded.

Do not use it to delegate product ambiguity, destructive production operations, or architectural judgment.

## Start with Cursor

Prerequisites: Node.js 18+ or Bun, plus Cursor’s `agent` CLI.

```bash
npm install -g ralphy-cli
cd your-project
ralphy --init
ralphy --config
```

Review `.ralphy/config.yaml`: test, lint, build commands; durable rules; and `never_touch` boundaries.

Preview and cap the first run:

```bash
ralphy --cursor --dry-run "add a tested health endpoint"
ralphy --cursor --max-iterations 1 "add a tested health endpoint"
```

For a PRD:

```bash
ralphy --cursor --prd PRD.md --max-iterations 3
```

## First exercise

Use one low-risk, test-backed task. Inspect every commit and test change. Only then evaluate a short PRD.

## Production checklist

- Start with `--dry-run` and low iteration caps.
- Define test, lint, and build commands explicitly.
- Protect lockfiles, migrations, secrets, and legacy paths as needed.
- Avoid `--fast` for production work because it skips tests and lint.
- Use isolated branches/worktrees for parallel tasks.
- Keep human approval before merge or deployment.

## Sources

- [Ralphy README and installation](https://github.com/michaelshimeles/ralphy#install)
- [Options and requirements](https://github.com/michaelshimeles/ralphy#options)
