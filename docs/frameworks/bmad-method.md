# BMAD Method Starter Guide

**Category:** full AI-driven product and delivery lifecycle  
**Best for:** complex initiatives needing product, UX, architecture, development, and testing perspectives  
**Upstream:** [bmad-code-org/BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD)  
**Upstream checked:** 2026-08-18

## What it changes

BMAD makes product and technical decisions explicit, carries them through later phases, and adjusts planning depth to the work. Its wider ecosystem includes testing, unattended epic loops, creative discovery, and game-development modules.

## Use it when

- the product or user workflow is still ambiguous;
- architecture decisions must be reviewed before implementation;
- several engineering perspectives are valuable;
- a team wants durable briefs, specifications, architecture, and stories.

Avoid the full workflow for routine fixes. BMAD supports shorter build paths; use them.

## Start a project

Official prerequisites: Node.js 20.12+, Python 3.10+, and `uv`.

```bash
cd your-project
npx bmad-method install
```

Open the repository in your AI coding tool and invoke:

```text
bmad-build <describe the change>
```

Use `bmad-help` whenever you need the next recommended or optional workflow. For an established repository, follow BMAD’s dedicated established-project process rather than treating it as greenfield.

## First exercise

Choose a feature with real product uncertainty. Compare the quick path with deeper planning: record which questions materially changed scope, architecture, or acceptance criteria.

## Production checklist

- Review artifacts; generated volume is not evidence of correctness.
- Keep a single source of truth for stories and requirements.
- Use specialized perspectives selectively.
- Add the Test Architect module only when its additional process is justified.
- Reconcile learning and course corrections back into durable artifacts.

## Sources

- [BMAD README](https://github.com/bmad-code-org/BMAD-METHOD)
- [Getting started tutorial](https://docs.bmad-method.org/tutorials/getting-started/)
- [Established projects](https://docs.bmad-method.org/how-to/established-projects/)
- [Workflow map](https://docs.bmad-method.org/reference/workflow-map/)
