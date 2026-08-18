# Build Your Own Lightweight AI Development Framework

You may not need a third-party framework. Modern coding agents can follow a small, versioned system built from Markdown, scripts, and CI.

## Minimal structure

```text
repo/
├── AGENTS.md
├── docs/
│   ├── product.md
│   ├── architecture/
│   ├── decisions/
│   ├── specs/
│   └── corrections/
├── .agents/skills/
│   ├── plan-feature/SKILL.md
│   ├── review-change/SKILL.md
│   └── finish-task/SKILL.md
└── scripts/
    └── verify.sh
```

## Define one lifecycle

```text
clarify → specify → plan → implement → verify → review → record
```

For each phase, document:

- entry conditions;
- required inputs;
- permitted actions;
- output artifact;
- completion evidence;
- escalation conditions.

## Example planning skill

```md
---
name: plan-feature
description: Create a repository-grounded implementation plan for multi-file features. Use before implementing a feature, migration, or architectural change.
---

1. Read applicable `AGENTS.md` files.
2. Locate existing implementation patterns.
3. Restate behavior, scope, exclusions, and unresolved questions.
4. Map affected components and compatibility risks.
5. Produce ordered tasks with exact verification for each.
6. Stop for approval before changing code.
```

## Keep deterministic work outside the model

Use scripts and CI for formatting, schemas, dependency rules, security scans, tests, and builds. Let the model interpret evidence and make bounded judgments; do not ask it to simulate checks that can actually run.

## Add complexity only in response to evidence

Add a task tracker when work is repeatedly lost. Add living specs when requirements drift. Add subagents when tasks are genuinely parallel. Add autonomous loops after verification is difficult to game.

The goal is reliable delivery, not the most elaborate agent organization chart.
