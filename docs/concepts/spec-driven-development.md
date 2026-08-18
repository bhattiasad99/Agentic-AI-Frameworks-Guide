# Spec-Driven Development

Spec-driven development gives humans and coding agents an agreed description of behavior before implementation begins.

It is not “write an enormous document first.” The specification should be proportional to uncertainty and risk.

## A useful separation

| Artifact | Answers |
|---|---|
| Product brief | Why should this exist? |
| Requirements/spec | What behavior must users and systems observe? |
| Design | How will the system produce that behavior? |
| Tasks | In what safe, reviewable order will it be built? |
| Verification plan | What evidence will prove it works? |

Mixing all five into one generated document makes it difficult to review assumptions.

## A strong feature specification includes

- problem and user outcome;
- in-scope and explicitly out-of-scope behavior;
- scenarios and edge cases;
- permission and failure behavior;
- compatibility and migration requirements;
- measurable acceptance criteria;
- unresolved questions;
- links to relevant architecture and existing code.

## Spec-first versus living specs

Some frameworks create feature artifacts that guide an implementation. Others maintain a current system specification and merge change proposals into it. Neither approach stays correct automatically.

After implementation, reconcile intentional deviations and archive obsolete planning material. The code may be operational truth, while the maintained specification remains the contract humans intended.

## When to skip a formal spec

A small typo, isolated refactor, or obvious test-backed bug may need only a short plan. Formal SDD is most valuable when behavior is ambiguous, several components are affected, compatibility matters, or review cost is high.

## Framework choices

- [OpenSpec](../frameworks/openspec.md): lightweight change proposals and living specs.
- [Spec Kit](../frameworks/spec-kit.md): constitution, specification, plan, tasks, and implementation.
- [BMAD Method](../frameworks/bmad-method.md): wider product and delivery lifecycle.
- [cc-sdd](../frameworks/cc-sdd.md): explicit contracts and long-running implementation.

## Sources

- [GitHub Spec Kit](https://github.com/github/spec-kit)
- [OpenSpec](https://github.com/Fission-AI/OpenSpec)
- [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD)
- [cc-sdd](https://github.com/gotalab/cc-sdd)
