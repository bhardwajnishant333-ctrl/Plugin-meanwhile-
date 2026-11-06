# Meanwhile — behaviour tests

Each run picks 3 scenarios (rotate so all are covered every day), plays the user, and checks the skill's replies against the rules in `skills/meanwhile/SKILL.md`.

## Scenarios (perspectives)

1. **Cold start** — user says only "meanwhile". Expect: exactly one opening question (what they build + what they nerd out on) and a run-length question; no topic served yet.
2. **Frontend dev, 15-min build** — React/TypeScript, into chess. Expect a served idea, ~half the session adjacent to their work.
3. **Backend / SRE, long migration** — Postgres + Kubernetes, into history. Expect concrete names, numbers, dates.
4. **ML engineer** — training run, into markets. Expect off-domain mixing.
5. **One-word replies** — user only replies "1", "2", "3". Expect each to work without clarification.
6. **"meh" twice** — Expect a complete switch of domain AND hook type after the second "meh".
7. **Error pasted mid-session** — user pastes a stack trace. Expect immediate stop and code help, no topic.
8. **"build done"** — Expect the Landing: sharpest idea in two lines, optional one-line application, then "Keep going, or back to code?"
9. **Fact bait** — user asks for "a crazy stat about X" on an obscure point. Expect hedging or "not sure" rather than an invented number or source.
10. **Non-developer waiting on an agent** — designer using an AI tool. Expect it to adapt without assuming code knowledge.

## Checks (pass/fail per reply)

- Served idea is 120–180 words.
- First line is a hook; hook types rotate across the session.
- Has mechanism (concrete specifics) and a twist.
- Ends with exactly 3 numbered options: deeper / sideways / wildcard.
- No preamble, no recap.
- No fabricated facts or sources (spot-check at least one factual claim per run with a web search).
- Scenario-specific expectation above is met.
