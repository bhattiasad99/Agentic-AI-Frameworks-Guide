# Memory, Corrections, and “Learning”

Most coding frameworks do not retrain the model when you correct it. They make prior information retrievable in future sessions.

That is **durable context**, not reinforcement learning.

## Convert feedback into the right artifact

| Feedback | Durable form |
|---|---|
| “Use the existing error wrapper.” | Scoped repository rule with a code reference |
| “This architecture decision has trade-offs.” | Architecture decision record |
| “This regression must never recur.” | Automated test |
| “Always perform these release steps.” | Agent Skill or deterministic script |
| “This feature is halfway complete.” | Temporary state or task file |
| “The product must behave this way.” | Maintained specification |

## Corrections log pattern

Keep a corrections log only as an intake queue. Promote stable lessons into rules, tests, skills, or decisions, then archive the original entry.

```md
## 2026-08-18 — Business logic placed in controller

- Context: supplier matching endpoint
- Wrong behavior: controller performed ranking and persistence
- Correct pattern: controller validates/translates; service owns the use case
- Evidence: `apps/api/src/matching/matching.service.ts`
- Promoted to: `apps/api/AGENTS.md` and architecture test
```

## Avoid an ever-growing memory file

Large undifferentiated memory becomes stale, contradictory, and expensive to load. Separate active state, durable standards, product behavior, and historical decisions. Archive completed task details.

## A practical feedback loop

```text
observe failure → diagnose cause → choose durable artifact
                → test in a fresh session → remove stale guidance
```

The fresh-session test matters. If the correction works only inside the conversation where it was explained, the system has not learned operationally.
