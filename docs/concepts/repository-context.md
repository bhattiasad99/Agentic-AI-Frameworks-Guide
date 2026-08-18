# Repository Context: AGENTS.md, Rules, and Skills

These mechanisms overlap, but they should not contain the same material.

## What belongs where

| Mechanism | Use it for | Example |
|---|---|---|
| `AGENTS.md` | Durable repository instructions | Setup, structure, commands, boundaries |
| Nested `AGENTS.md` | Directory-specific context | Backend or frontend conventions |
| Cursor project rule | Scoped or always-applied IDE behavior | Rules for `*.sql` migrations |
| Agent Skill | A reusable procedure loaded when relevant | Security review or release preparation |
| Hook/CI | Requirements that must be enforced | Block secrets or failing tests |
| Task spec | Temporary change-specific intent | Acceptance criteria for dark mode |

Cursor supports root and nested `AGENTS.md` files. Parent and child instructions are combined, with more specific directory instructions taking precedence.

## Minimal AGENTS.md template

```md
# Repository Instructions

## Purpose
One paragraph describing the product and users.

## Structure
- `apps/web`: customer UI
- `apps/api`: HTTP API and business services
- `packages/contracts`: shared schemas only

## Commands
- Install: `pnpm install`
- Test: `pnpm test`
- Type-check: `pnpm typecheck`
- Build: `pnpm build`

## Architecture
- Controllers translate HTTP input/output.
- Services own business logic.
- Cross-package imports must use public package exports.

## Boundaries
- Never edit generated migrations.
- Never weaken tests to make a change pass.
- Ask before adding a production dependency.

## Definition of done
- Acceptance criteria are met.
- Relevant tests, type-checking, and linting pass.
- Documentation changes when behavior or architecture changes.
```

## Root versus nested files

Use a root file for global navigation and invariants. Add nested files only when a directory genuinely differs.

```text
repo/
├── AGENTS.md
├── apps/
│   ├── web/AGENTS.md
│   └── api/AGENTS.md
└── packages/
    └── contracts/AGENTS.md
```

Do not copy the root into every child. State only the differences.

## Rules are not controls

An LLM attempts to follow rules; it can still misunderstand or ignore them. Convert non-negotiable requirements into formatters, linters, tests, hooks, protected branches, or CI checks.

## Skills

Agent Skills package procedural knowledge in a folder containing `SKILL.md`, optionally with scripts, references, and assets. The description should say both what the skill does and when it should activate.

```text
security-review/
├── SKILL.md
├── references/checklist.md
└── scripts/scan.sh
```

Keep the core skill concise and load large references only when needed.

## Sources

- [AGENTS.md open format](https://agents.md/)
- [Cursor rules and nested AGENTS.md](https://cursor.com/docs/rules)
- [Cursor Agent Skills](https://cursor.com/docs/skills)
- [Agent Skills specification](https://agentskills.io/specification)
- [Agent Skills best practices](https://agentskills.io/skill-creation/best-practices)
