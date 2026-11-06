# Meanwhile — test status

Automated behaviour tests run every 2 hours against `skills/meanwhile/SKILL.md`, each time from different user perspectives (see `tests/scenarios.md`).

**Latest run:** 2026-11-06 22:20 UTC — FAIL (0/3)

| Time (UTC) | Scenarios | Result | Notes |
|---|---|---|---|
| 2026-11-06 22:20 | 1, 2, 3 | 0/3 PASS | All served ideas ran 205–237 words, over the 180 cap; other checks mostly OK. Harness: subagents read owner memory before turn 1 and were reset. |
