# AI Dev Tasks Starter Guide

**Category:** minimal PRD-to-task workflow  
**Best for:** learning structured AI-assisted development without installing a large framework  
**Upstream:** [snarktank/ai-dev-tasks](https://github.com/snarktank/ai-dev-tasks)  
**Upstream checked:** 2026-08-18

## What it changes

AI Dev Tasks provides Markdown prompts for creating a PRD, converting it into a granular task list, and implementing one task at a time with visible completion tracking.

## Use it when

- you are moving beyond one-shot prompting;
- you want to understand the mechanics before adopting automation;
- manual review after each task is desirable;
- your coding tool can reference Markdown prompt files.

It intentionally lacks advanced memory, multi-agent orchestration, and enforcement.

## Start a project

Clone upstream into a separate temporary location and copy the relevant Markdown prompt files into your project or a central prompt directory:

```bash
git clone https://github.com/snarktank/ai-dev-tasks.git
```

Workflow:

1. Use `create-prd.md` with your feature description.
2. Review and save the generated PRD.
3. Use `generate-tasks.md` and reference the PRD.
4. Review task order and acceptance checks.
5. Use `process-task-list.md` to implement one task at a time.
6. Review the diff and verification before marking a task complete.

## First exercise

Choose a three-task feature. Require a review checkpoint after each task. Record which missing PRD detail caused the most rework.

## Production checklist

- Keep the PRD specific and bounded.
- Add repository commands and conventions to the prompts.
- Make each task independently reviewable.
- Do not confuse checked boxes with verification.
- Graduate to a larger framework only when a named limitation recurs.

## Sources

- [AI Dev Tasks README](https://github.com/snarktank/ai-dev-tasks)
- [Workflow prompt files](https://github.com/snarktank/ai-dev-tasks/tree/main)
