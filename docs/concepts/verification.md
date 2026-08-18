# Verification and Review

An agent saying “done” is a status claim, not evidence.

## Verification ladder

Use the cheapest reliable signal first and layer stronger checks for riskier work.

1. Formatting and syntax
2. Type-checking and static analysis
3. Focused unit tests
4. Integration and contract tests
5. Build and migration validation
6. Reproducible manual or browser verification
7. Spec-compliance review
8. Code-quality and security review
9. Human approval for material risk

## Separate two reviews

**Spec-compliance review:** Did we build the requested behavior and nothing materially different?

**Code-quality review:** Is the implementation maintainable, safe, understandable, and consistent with the repository?

An elegant solution to the wrong requirement fails the first review. A feature-complete but unsafe implementation fails the second.

## Protect the verifier

Autonomous agents sometimes optimize the measurement instead of the outcome. Establish boundaries:

- do not delete, skip, or weaken existing tests without approval;
- do not modify the acceptance criteria during implementation;
- do not mock away the behavior under test;
- do not hide warnings or failures;
- report commands and results accurately;
- require review of test changes alongside production code.

## Fresh reviewers

A fresh agent context can reduce commitment to the implementer’s assumptions, but it is not automatically independent if both use the same model and evidence. For critical work, combine different checks, security tools, domain experts, and accountable human review.

## Definition of done template

```md
- [ ] Acceptance criteria mapped to evidence
- [ ] Relevant tests pass
- [ ] Type-check, lint, and build pass
- [ ] Migration/rollback considered
- [ ] No tests weakened without approval
- [ ] Spec-compliance review complete
- [ ] Code-quality/security review complete
- [ ] Docs and decisions updated
```

## Sources

- [Cursor: reviewing and testing](https://cursor.com/learn/reviewing-testing)
- [Superpowers workflow](https://github.com/obra/superpowers#the-basic-workflow)
- [Cursor hooks](https://cursor.com/docs/hooks)
