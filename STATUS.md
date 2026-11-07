# Meanwhile — test status

Automated behaviour tests run every 2 hours against `skills/meanwhile/SKILL.md`, each time from different user perspectives (see `tests/scenarios.md`).

**Latest run:** 2026-11-07 04:19 UTC — FAIL (0/3)

| Time (UTC) | Scenarios | Result | Notes |
|---|---|---|---|
| 2026-11-07 04:19 | 4, 5, 6 | 0/3 PASS | All three failed on format, not content: s4 landing opened "Fair point." + side reply and ran long; s5 tacked a CI check-in line after the 3 options in 3 replies; s6 landing application ran 3 sentences. Scenario goals all met (off-domain mix, bare 1/2/3, meh×2 switch). Harness: subagents read owner memory before turn 1 again. |
| 2026-11-07 02:20 | 1, 2, 3 | 1/3 PASS | s2, s3 FAIL: Landing opened with small talk ("Nice, green on the first run." / "Nice work, three for three."), breaking "no preamble"; s3 landing application ran 3 sentences, not one line. s1 cold start clean. Harness: subagents again read owner memory before turn 1 and were reset. |
| 2026-11-07 00:19 | 7, 8, 9 | 2/3 PASS | s8 FAIL: opened with a greeting before the hook ("no preamble"); landing application ran 3 lines, not one. s7 dropped the topic for the Rust error cleanly; s9 refused both fact baits with no invented number. |
| 2026-11-06 23:28 | 4, 5, 6 | 3/3 PASS | First run without the word limit. Bare 1/2/3 worked; "meh"×2 switched domain and hook; caught and fixed its own "British Rail" slip. Minor: a repeated wildcard in s6. |
| 2026-11-06 22:20 | 1, 2, 3 | 3/3 PASS | Re-graded: only failure was the 120–180 word limit, since removed by the owner. Minor: small-talk openers in two landings, a repeated option in s3. Harness: subagents read owner memory before turn 1 and were reset. |
