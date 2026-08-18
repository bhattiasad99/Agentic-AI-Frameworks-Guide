# cc-sdd Starter Guide

**Category:** contract-oriented SDD and long-running implementation  
**Best for:** approved specs that need per-task implementation, independent review, and automatic debugging  
**Upstream:** [gotalab/cc-sdd](https://github.com/gotalab/cc-sdd)  
**Upstream checked:** 2026-08-18

## What it changes

cc-sdd treats specs as contracts between system boundaries while keeping code as operational truth. It can produce requirements, design, tasks, and autonomous task execution with fresh implementers, reviewer passes, TDD, feature flags, and debugging.

## Use it when

- a large initiative needs explicit cross-component contracts;
- approved task sets should run for longer periods;
- independent review per task is valuable;
- your team is comfortable maintaining specification gates.

Cursor Skills support is currently marked beta upstream; test it before team-wide adoption.

## Start in Cursor

Prerequisite: Node.js.

```bash
cd your-project
npx cc-sdd@latest --cursor-skills
```

Begin in Cursor with discovery:

```text
/kiro-discovery Photo albums with upload, tagging, and sharing
/kiro-spec-init photo-albums
/kiro-spec-requirements photo-albums
/kiro-spec-design photo-albums
/kiro-spec-tasks photo-albums
/kiro-impl photo-albums
```

Command rendering may follow Cursor’s installed skill naming. Use the generated skills as the authority.

## First exercise

Choose a feature spanning an API and UI. Review the generated requirements for observable acceptance criteria and the design for explicit interface boundaries before running implementation.

## Production checklist

- Treat Cursor integration as beta and keep rollback simple.
- Approve contracts at phase gates.
- Inspect feature-flag behavior and test changes.
- Confirm reviewer contexts are fresh and task-scoped.
- Use `npx cc-sdd@latest --dry-run` before updating an installation.

## Sources

- [cc-sdd README and quickstart](https://github.com/gotalab/cc-sdd#quick-start)
- [Skill reference](https://github.com/gotalab/cc-sdd/blob/main/docs/guides/skill-reference.md)
- [Why cc-sdd](https://github.com/gotalab/cc-sdd/blob/main/docs/guides/why-cc-sdd.md)
