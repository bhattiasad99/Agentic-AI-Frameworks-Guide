# GitHub Spec Kit Starter Guide

**Category:** formal spec-driven development  
**Best for:** greenfield products and teams wanting a constitution-to-implementation workflow  
**Upstream:** [github/spec-kit](https://github.com/github/spec-kit)  
**Upstream checked:** 2026-08-18

## What it changes

Spec Kit separates governing principles, product requirements, technical planning, task decomposition, consistency analysis, and implementation.

## Use it when

- requirements and quality principles need formal review;
- features have significant cross-component behavior;
- a team benefits from predictable artifacts and extension points;
- you want a customizable SDD process rather than a fixed prompt pack.

Its artifact and context overhead may be excessive for small maintenance work.

## Start a project

Install `uv`, then the current CLI:

```bash
uv tool install specify-cli
specify integration list
```

For a new Cursor project:

```bash
specify init my-project --integration cursor-agent
cd my-project
```

For the current directory:

```bash
specify init --here --integration cursor-agent
```

As of the checked version, Cursor consumes generated skills inside the IDE. Follow this sequence in Cursor:

```text
/speckit-constitution
/speckit-specify
/speckit-plan
/speckit-tasks
/speckit-analyze
/speckit-implement
```

Command punctuation can differ by integration; use the files installed into your project and the output of `specify integration list` as the authority.

## First exercise

Create a constitution with testing, performance, UX, and compatibility principles. Specify one medium feature, run clarification and analysis, then check whether every acceptance criterion maps to a task and test.

## Production checklist

- Keep the constitution short and enforceable.
- Run clarify before technical planning when behavior is ambiguous.
- Run analyze before implementation.
- Watch context consumption on smaller model windows.
- Define how completed feature specs evolve instead of accumulating contradictory artifacts.

## Sources

- [Spec Kit README](https://github.com/github/spec-kit)
- [Quickstart](https://github.github.io/spec-kit/quickstart.html)
- [Supported integrations](https://github.com/github/spec-kit/blob/main/docs/reference/integrations.md)
