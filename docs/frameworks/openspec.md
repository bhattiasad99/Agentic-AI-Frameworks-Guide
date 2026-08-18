# OpenSpec Starter Guide

**Category:** lightweight, change-oriented specification  
**Best for:** brownfield products and incremental cross-component changes  
**Upstream:** [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec)  
**Upstream checked:** 2026-08-18

## What it changes

OpenSpec moves requirements out of chat and into reviewable Markdown. A change can contain a proposal, requirements, design, and tasks, then be archived into maintained project specifications.

## Use it when

- requirements repeatedly drift during implementation;
- an existing product changes incrementally;
- several repositories or packages share one behavior contract;
- you want specifications without a large virtual-team process.

OpenSpec does not replace tests, architecture review, or task execution discipline.

## Start a project

Official prerequisite: Node.js 20.19+.

```bash
npm install -g @fission-ai/openspec@latest
cd your-project
openspec init
```

Select your coding tools during initialization. Cursor uses hyphenated commands, while other agents may render them differently. Start with:

```text
/opsx-explore
/opsx-propose Add organization-scoped audit history
```

Review the created change artifacts before implementation. Use the expanded profile if you want additional new/continue/verify/onboard workflows:

```bash
openspec config profile
openspec update
```

## First exercise

Specify an existing feature change with one modified behavior and one compatibility constraint. After implementation, run verification and archive the change. Confirm the maintained specs describe the new current state.

## Production checklist

- Write observable scenarios, not implementation slogans.
- Keep proposals small enough for meaningful review.
- Reconcile intentional implementation deviations.
- Run `/opsx-verify` when available in the selected profile.
- Treat cross-repository Stores as beta and test the workflow before standardizing it.

## Sources

- [OpenSpec README and quickstart](https://github.com/Fission-AI/OpenSpec#quick-start)
- [Getting started](https://github.com/Fission-AI/OpenSpec/blob/main/docs/getting-started.md)
- [Existing projects](https://github.com/Fission-AI/OpenSpec/blob/main/docs/existing-projects.md)
- [Supported tools](https://github.com/Fission-AI/OpenSpec/blob/main/docs/supported-tools.md)
