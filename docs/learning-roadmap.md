# AI-Driven Development Learning Roadmap

Use this as a checklist, not a reading list. Each level ends with something you should be able to demonstrate in a real repository.

## How to use this roadmap

1. Choose one existing project or a small product idea.
2. Complete the levels in order.
3. Keep evidence: specs, plans, tests, reviews, and decisions.
4. Do not claim a skill is learned until you can reproduce it in a fresh session.

## Level 0 — Operate a coding agent safely

- [ ] Separate asking, planning, implementation, and review.
- [ ] Inspect diffs instead of accepting a “done” message.
- [ ] Understand tool permissions and approval modes.
- [ ] Protect secrets, production credentials, and destructive commands.
- [ ] Create reversible checkpoints with branches or commits.
- [ ] Know when the agent is guessing rather than reading evidence.

**Proof project:** Give an agent a bounded bug, review its plan, let it implement, run checks, and explain every changed file.

## Level 1 — Engineer repository context

- [ ] Create a concise root `AGENTS.md`.
- [ ] Document setup, build, test, and lint commands.
- [ ] Explain repository structure and architectural boundaries.
- [ ] Add nested instructions where applications or packages differ.
- [ ] Distinguish durable rules from temporary task context.
- [ ] Keep instructions discoverable instead of loading everything always.

Read: [Repository context](concepts/repository-context.md) and [Context engineering](concepts/context-engineering.md).

**Proof project:** Start a fresh agent session and have it identify the correct package, commands, patterns, and prohibited changes without coaching.

## Level 2 — Package repeatable capabilities

- [ ] Understand the difference between rules, skills, commands, hooks, and MCP tools.
- [ ] Create one Agent Skill with a precise trigger description.
- [ ] Move detailed references out of the always-loaded instruction body.
- [ ] Bundle deterministic scripts for repeatable checks.
- [ ] Test both correct activation and false activation.
- [ ] Version skills alongside the code or team workflow they serve.

Reference: [Agent Skills specification](https://agentskills.io/specification).

**Proof project:** Build a code-review skill that activates on review requests, applies your repository checklist, and produces consistent severity-ranked findings.

## Level 3 — Practice specification-driven development

- [ ] Write outcomes and user-visible behavior before technical tasks.
- [ ] Include edge cases, exclusions, and failure behavior.
- [ ] Separate “what and why” from implementation choices.
- [ ] Make acceptance criteria observable or executable.
- [ ] Record architecture decisions and trade-offs.
- [ ] Reconcile the specification when implementation changes the plan.

Try one: [OpenSpec](frameworks/openspec.md), [Spec Kit](frameworks/spec-kit.md), [BMAD](frameworks/bmad-method.md), or [cc-sdd](frameworks/cc-sdd.md).

**Proof project:** Implement the same medium feature once from an informal prompt and once from an approved specification. Compare rework, missed requirements, and review findings.

## Level 4 — Decompose and orchestrate work

- [ ] Break work into independently verifiable vertical slices.
- [ ] Express task dependencies and shared-file conflicts.
- [ ] Keep each task within a fresh context budget.
- [ ] Resume work from repository artifacts instead of chat history.
- [ ] Use worktrees or isolated branches for parallel execution.
- [ ] Define an integration order before launching multiple agents.

Try one: [GSD Core](frameworks/gsd-core.md), [Task Master](frameworks/task-master.md), or [AI Dev Tasks](frameworks/ai-dev-tasks.md).

**Proof project:** Pause halfway through a feature, discard the conversation, and resume correctly from versioned state.

## Level 5 — Build verification into the loop

- [ ] Convert requirements into tests or deterministic checks where possible.
- [ ] Require the agent to observe a failing test before fixing a bug.
- [ ] Run type checks, lint, tests, and builds independently.
- [ ] Review spec compliance separately from code quality.
- [ ] Prevent agents from weakening tests to manufacture success.
- [ ] Use a fresh reviewer for material changes.
- [ ] Keep a human approval gate for high-risk changes.

Read: [Verification and review](concepts/verification.md). Try [Superpowers](frameworks/superpowers.md) if you want a strict methodology.

**Proof project:** Seed three known defects in an implementation and measure which are caught by tests, static analysis, agent review, and human review.

## Level 6 — Manage memory and corrections

- [ ] Store stable knowledge in versioned, scoped files.
- [ ] Record decisions with context and trade-offs.
- [ ] Convert repeated mistakes into rules, tests, or tools.
- [ ] Archive task state instead of endlessly growing active context.
- [ ] Distinguish retrieval-based memory from model training.
- [ ] Remove obsolete instructions before they become contradictory.

Read: [Memory, corrections, and learning](concepts/memory-and-learning.md). Try [Cursor Memory Bank](frameworks/cursor-memory-bank.md) when Cursor session continuity is the main problem.

**Proof project:** Demonstrate that a correction from one feature changes the behavior of a fresh agent session on a similar feature.

## Level 7 — Use autonomous and multi-agent execution responsibly

- [ ] Launch agents only on bounded tasks with objective completion signals.
- [ ] Give each worker an isolated workspace.
- [ ] Avoid parallel tasks that edit the same architectural seam.
- [ ] Cap iterations, cost, time, and permissions.
- [ ] Use independent review rather than self-certification.
- [ ] Preserve logs, commits, and artifacts for auditability.
- [ ] Escalate ambiguity instead of letting a loop improvise product decisions.

Read: [Autonomous execution](concepts/autonomous-execution.md). Explore [Ralphy](frameworks/ralphy.md), [cc-sdd](frameworks/cc-sdd.md), or [Archon](frameworks/archon.md).

**Proof project:** Run an autonomous agent on five testable tasks. Report success rate, cost, manual corrections, review defects, and any unsafe behavior.

## Level 8 — Govern AI-driven delivery as a team

- [ ] Define ownership for specs, generated code, tests, and approvals.
- [ ] Keep organization rules separate from repository rules.
- [ ] Enforce security requirements with tooling, not prose alone.
- [ ] Track rework, escaped defects, lead time, review time, and agent cost.
- [ ] Review third-party skills, plugins, MCP servers, and install scripts.
- [ ] Establish an update and rollback policy for frameworks.
- [ ] Document when AI use is prohibited or requires disclosure.

**Proof project:** Write a one-page team policy and implement at least two controls in CI or repository settings.

## Graduation project

Build one production-quality vertical slice using this evidence chain:

```text
intent → approved spec → technical plan → bounded tasks → implementation
       → automated checks → independent review → decision record → release note
```

Publish a short retrospective covering what the framework improved, where it added friction, and what you would remove next time.
