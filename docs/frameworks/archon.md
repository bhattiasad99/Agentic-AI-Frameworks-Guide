# Archon Starter Guide

**Category:** deterministic workflow engine for coding agents  
**Best for:** teams encoding repeatable plan, implement, validate, review, approval, and PR workflows  
**Upstream:** [coleam00/Archon](https://github.com/coleam00/Archon)  
**Upstream checked:** 2026-08-18

## What it changes

Archon defines coding workflows in YAML. It mixes AI nodes with deterministic Bash/scripts, loops, fresh contexts, worktrees, and human approval gates. The current TypeScript workflow engine replaced an earlier task-management/RAG product preserved on an archive branch.

## Use it when

- a team needs the same delivery sequence every time;
- workflows must be committed and reviewed as code;
- deterministic and AI steps need explicit dependencies;
- multiple interfaces should launch the same workflow.

This is a platform to own, not a small prompt pack.

## Start a project

The upstream full setup requires Bun, Claude Code, and GitHub CLI:

```bash
git clone https://github.com/coleam00/Archon
cd Archon
bun install
claude
```

Then ask Claude Code: `Set up Archon` and follow the guided wizard. It installs the Archon skill into target repositories.

After setup, open Claude Code from the target repository—not the Archon checkout:

```bash
cd /path/to/your-project
claude
```

```text
What Archon workflows do I have, and when would I use each one?
Use Archon to implement issue #42.
```

## First exercise

Create a minimal workflow with plan → implement → deterministic tests → review → human approval. Do not begin with parallel execution or chat integrations.

## Production checklist

- Pin and review workflow definitions.
- Prefer deterministic nodes wherever a script can decide.
- Require approval before push, PR, migration, or deployment.
- Review telemetry and opt-out settings for your organization.
- Test failure, cancellation, retry, and recovery paths.
- Understand the difference between current Archon and archived v1 tutorials.

## Sources

- [Archon README](https://github.com/coleam00/Archon)
- [Getting started](https://archon.diy/getting-started/installation/)
- [Workflow example](https://github.com/coleam00/Archon#what-it-looks-like)
