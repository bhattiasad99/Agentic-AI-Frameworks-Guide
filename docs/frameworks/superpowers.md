# Superpowers Starter Guide

**Category:** agent skills and disciplined implementation methodology  
**Best for:** teams that want planning, TDD, systematic debugging, worktrees, and review to happen consistently  
**Upstream:** [obra/superpowers](https://github.com/obra/superpowers)  
**Upstream checked:** 2026-08-18

## What it changes

Superpowers installs composable skills that activate around software work. Its basic workflow moves through brainstorming, isolated worktrees, small plans, implementation, red-green-refactor TDD, review, and branch completion.

## Use it when

- agents jump into code before understanding the change;
- generated code lacks tests or disciplined debugging;
- you want spec-compliance and code-quality reviews separated;
- isolated task execution is valuable.

Strict TDD and mandatory phases may be excessive for exploratory UI work or configuration-only changes.

## Start in Cursor

In Cursor Agent chat:

```text
/add-plugin superpowers
```

Alternatively, search for `superpowers` in Cursor’s plugin marketplace. Installation is separate for every harness you use.

Then describe a real feature. The framework should begin with brainstorming rather than code. Approve the design before it writes an implementation plan and executes.

## First exercise

Choose a testable bug. Confirm the agent reproduces it with a failing test, implements the minimal fix, observes the test pass, and performs both spec and quality review.

## Production checklist

- Inspect automatically selected skills.
- Confirm the baseline test suite passes before creating a worktree.
- Do not let the implementation change the approved design silently.
- Review tests for weakening or over-mocking.
- Decide which work categories may intentionally skip strict TDD.

## Sources

- [Superpowers README](https://github.com/obra/superpowers)
- [Basic workflow](https://github.com/obra/superpowers#the-basic-workflow)
- [Cursor installation](https://github.com/obra/superpowers#cursor)
