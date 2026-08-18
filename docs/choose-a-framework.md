# Choose an AI-Driven Development Framework

The best framework is the smallest one that removes a recurring failure mode without hiding the engineering from you.

## Answer these questions first

1. Is the repository new or established?
2. Is your main problem requirements, context, task tracking, code quality, or autonomy?
3. Are you working alone or coordinating a team?
4. Can correctness be checked automatically?
5. How much process will you consistently maintain?

## Decision matrix

| Framework | Greenfield | Brownfield | Solo | Team | Cursor | Autonomous execution | Main trade-off |
|---|:---:|:---:|:---:|:---:|:---:|:---:|---|
| GSD Core | Strong | Strong | Strong | Good | Yes | Strong | More generated state and agent activity |
| BMAD Method | Strong | Good | Good | Strong | Yes | Optional module | Deep process can overwhelm small work |
| OpenSpec | Good | Strong | Strong | Strong | Yes | Limited | Requires discipline to keep specs current |
| Spec Kit | Strong | Good | Good | Strong | Yes | Good | Formal artifacts and phase overhead |
| Superpowers | Good | Strong | Strong | Good | Plugin | Strong | Strict workflow, especially TDD |
| Agent OS | Good | Strong | Strong | Strong | File-based | No | Solves standards, not full delivery |
| Task Master | Strong | Good | Strong | Good | Strong | Loop available | Task tracking is not quality assurance |
| cc-sdd | Strong | Strong | Good | Strong | Beta skills | Strong | More contracts, gates, and moving parts |
| Cursor Memory Bank | Good | Good | Strong | Limited | Native | Limited | Cursor-specific and documentation-heavy |
| Ralphy | Good | Good | Strong | Limited | CLI | Strong | Unsafe without objective checks and caps |
| Archon | Good | Strong | Limited | Strong | Indirect | Strong | Platform ownership and setup cost |
| AI Dev Tasks | Strong | Good | Strong | Limited | Yes | Manual loop | Intentionally minimal |

## Recommendations by scenario

### New solo SaaS

Begin with `AGENTS.md`, tests, and **AI Dev Tasks**. Move to **GSD Core** if context and phase management become painful. Choose **OpenSpec** if changing product requirements—not task execution—are the real issue.

### Existing monorepo

Use root and nested `AGENTS.md` files. Consider **Agent OS** to document existing standards, then **OpenSpec** for cross-package changes. Add **GSD Core** only if multi-phase execution regularly loses context.

### Product discovery is unclear

Use **BMAD Method** for deeper product, UX, architecture, and testing perspectives. Do not carry its heaviest workflow into trivial fixes.

### Regulated or high-risk system

Prefer explicit specifications, deterministic gates, traceable decisions, and human approval. **Spec Kit**, **OpenSpec**, or a carefully governed **Archon** workflow can help, but none replaces security review, compliance evidence, or accountable ownership.

### High-volume, well-specified backlog

Use **Task Master** for dependency management. Add **Ralphy** or **cc-sdd** only when tasks have reliable tests, isolated workspaces, bounded permissions, and independent review.

## Safe combinations

Combine frameworks by assigning non-overlapping ownership:

| Layer | Example owner |
|---|---|
| Repository conventions | `AGENTS.md` or Agent OS |
| Product behavior and change history | OpenSpec |
| Implementation discipline | Superpowers |
| Deterministic enforcement | CI, hooks, tests |

This combination can work because each component has a distinct responsibility.

## Combinations to avoid

- **BMAD + Spec Kit + OpenSpec for every feature:** three competing specification processes.
- **GSD Core + Task Master without a mapping:** two sources of task truth.
- **Memory Bank + several framework state directories:** more context to reconcile than to use.
- **Ralphy on an ambiguous PRD:** a faster loop around an unclear target.
- **Agent rules as security controls:** prose can be ignored; enforce critical policy mechanically.

## A two-feature evaluation

Before standardizing a framework:

1. Select two similar, medium-sized features.
2. Record planning time, implementation time, tokens/cost, rework, escaped defects, and review effort.
3. Use the framework on one feature and your current workflow on the other.
4. Compare outcomes, not generated document volume.
5. Keep, simplify, or remove the framework based on evidence.

Framework adoption should be reversible. Commit configuration, pin versions when possible, and understand what files an installer changes.
