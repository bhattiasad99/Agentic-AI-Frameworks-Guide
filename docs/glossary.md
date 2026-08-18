# Glossary

**Agent harness** — The application that provides a model with repository access, tools, permissions, context, and an execution loop. Cursor, Claude Code, and Codex are harnesses.

**Agent Skill** — A portable folder of instructions and optional scripts/references loaded when a relevant task appears.

**Agentic coding** — Software development in which an AI agent can inspect a repository, plan, edit files, run commands, and iterate toward a result.

**AI-driven development (AiDD)** — A development approach in which AI participates across requirements, design, implementation, testing, review, and maintenance—not only autocomplete.

**Brownfield** — An existing codebase with accumulated behavior, constraints, and conventions.

**Context engineering** — Designing what information and tools an agent receives, at which scope and time, with mechanisms for verification.

**Context rot** — Degradation in agent performance as a session accumulates irrelevant, compressed, or contradictory context.

**Durable context** — Versioned information that survives conversations, such as rules, specs, decisions, and state files.

**Greenfield** — A new project without an established codebase.

**Hook** — A deterministic process triggered before or after an agent action or lifecycle event.

**Living specification** — A maintained description of current system behavior updated as changes are accepted.

**MCP (Model Context Protocol)** — A protocol through which agents can discover and call external tools or access resources.

**Memory bank** — Structured files used to preserve project knowledge or task state between agent sessions.

**Ralph loop** — Repeatedly invoking a coding agent against a persistent task/spec and repository state until completion criteria or a limit is reached.

**Spec-driven development (SDD)** — Defining and reviewing intended behavior before using the specification to drive planning and implementation.

**Subagent** — A delegated agent running with its own context, usually for a bounded research, implementation, or review task.

**Vibe coding** — Building primarily through conversational generation and iteration, often with less explicit planning or review. It can be productive for exploration but becomes risky when ambiguity and impact grow.

**Worktree** — A Git mechanism that allows multiple checked-out branches in separate directories, useful for isolating concurrent agent tasks.
