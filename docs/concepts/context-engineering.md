# Context Engineering for Coding Agents

Context engineering is the design of what an agent sees, when it sees it, and how it can verify that information. It is broader than prompting.

## Why context fails

Coding agents commonly fail because they receive:

- too little repository-specific knowledge;
- too much irrelevant documentation;
- contradictory instructions from several locations;
- stale architecture or setup commands;
- requirements without observable acceptance criteria;
- long conversations whose early decisions have been compressed or lost.

Larger context windows delay these problems; they do not remove them.

## A useful context hierarchy

| Scope | Content | Lifetime |
|---|---|---|
| Organization | Security and compliance policy | Long |
| Repository | Architecture, commands, global conventions | Long |
| Directory | Package- or domain-specific patterns | Medium–long |
| Feature | Approved requirements, design, and tasks | Medium |
| Session | Current question, temporary evidence | Short |
| Tool result | Test output, logs, diffs | Ephemeral |

Put information at the narrowest scope where it remains correct.

## Retrieval beats repetition

Do not paste the entire engineering handbook into every request. Keep a compact routing layer that tells the agent which deeper file to read.

```text
AGENTS.md
├── architecture → docs/architecture/index.md
├── API work → api/AGENTS.md
├── database changes → docs/standards/database.md
└── security-sensitive work → docs/standards/security.md
```

This keeps startup context small while preserving discoverability.

## Write instructions that can be followed

Weak:

> Write clean, scalable code and follow best practices.

Strong:

> Keep HTTP concerns in controllers and business rules in services. New service methods require unit tests. Run `pnpm --filter api test` and `pnpm --filter api typecheck` before reporting completion.

Strong instructions contain a boundary, an example or location, and a verification command.

## Measure context quality

In a fresh session, ask the agent to identify:

1. the correct package for a change;
2. relevant architecture and conventions;
3. the commands it must run;
4. files or systems it must not touch;
5. unanswered questions blocking a plan.

If it cannot answer, improve routing before adding more autonomous execution.

## Sources

- [Cursor: prompting agents](https://cursor.com/docs/agent/prompting)
- [Cursor: rules](https://cursor.com/docs/rules)
- [GSD Core: context engineering](https://github.com/open-gsd/gsd-core/blob/main/docs/explanation/context-engineering.md)
- [Agent Skills: progressive disclosure](https://agentskills.io/client-implementation/adding-skills-support)
