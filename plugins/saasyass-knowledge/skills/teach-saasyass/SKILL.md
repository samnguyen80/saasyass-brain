---
name: teach-saasyass
description: "Teach a Saasyass B2B SaaS acquisition topic as a classroom: one situation, the learner guesses, then one move. Use when they say teach me, /teach-saasyass, or want to learn Meta ads for SaaS, demo funnels, trial onboarding or churn. Do NOT use to apply a setup to their account (saas-meta-ads-structure, saas-demo-tracking, saas-ad-audit, saas-vsl, saas-retention-flows). Do NOT lecture the playbook."
argument-hint: "What would you like to learn?"
---

# Teach Saasyass

Knowledge source is **this plugin**, not training data. The method is a classroom in the creator's own shape: a founder ("Peter") describes a painful symptom, the expert names why the obvious fix is wrong, then gives one move. Rewrite this as: **situation → learner guesses → one move**.

## Workspace

Treat **cwd** as the student workspace. Prefer `./learners/` (gitignored in this repo).

- `MISSION.md` — why they want this (spend, demo count, trial-to-paid, churn)
- `RESOURCES.md` — reel Watch URLs only
- `learning-records/*.md` — only when they restate the move correctly
- `lessons/*.html` — one situation per file
- `NOTES.md` — how they like to be taught

## First turn

Write `MISSION.md` yourself from the topic; do not grill their numbers if they asked to learn a concept. No topic → start the first lesson below. If they say their own account is stuck, ask only the few numbers that pick the scenario (spend, cost per demo, show rate, trial-to-paid, monthly churn), then pick.

## No shell

Do not run shell for teach. **Read** `${CLAUDE_PLUGIN_ROOT}/knowledge/...` with the file tool and write the workspace with the file tool.

## Every lesson

1. Read the mapped file. Open with the situation as one or two sentences and **ask one question**. Wait. Do not reveal the move in the same message.
2. Name the trap guess if they fall for it (the obvious fix the concept rejects), then give the real reading and **one** move.
3. Write `lessons/NNNN-<slug>.html`: symptom, what it is not, the move, **one** Watch URL.
4. Learning record only if they can say the move in their own words.

One situation per lesson; never two. Tag figures **claimed**. Do not paste the playbook. Do not write transcripts.

## Starter situations (symptom → file)

| Situation | Trap guess | Read |
|---|---|---|
| Demos cost $400 and the founder wants to pause | "It's too expensive" | `concepts/Unit economics calculator.md` |
| Best ad has the cheapest demos; plan: make ten more | "Clone the winner" | `concepts/Existing customer exclusion.md` |
| Meta reports fewer booked demos than the calendar | "Meta is lying" | `concepts/Conversion signal quality.md` |
| Leads get worse every week, $100/day, many ad sets | "Test properly with more ad sets" | `concepts/Conversion signal quality.md` |
| Winner crashed after adding new ads to it | "Meta hates us" | `concepts/Meta account structure.md` |
| ABO or CBO? | "CBO is always more efficient" | `concepts/ABO vs CBO.md` |
| Six hours building an audience, wrong people saw it | "Tighter targeting" | `concepts/Creative as targeting.md` |
| Funny, educational, offer ads each "failed" | "Meta ads don't work for us" | `concepts/Swarm strategy.md` |
| Co-founders disagree on positioning | "Workshop it" | `concepts/Market vote positioning.md` |
| Half of booked demos no-show | "Send more reminders" | `concepts/Hammer them retargeting.md` + `Demo funnel six levels.md` |
| Reps spend the whole demo explaining | "Train reps better" | `concepts/Video sales letter.md` |
| 400 trials, 11 paid | "Need more traffic" | `concepts/Trial onboarding flow.md` |
| Customers cancelling | "Discount them" | `concepts/Cancellation flow.md`, `Churn win-back flows.md` |
| Which ad formats | — | `concepts/SaaS ad tier list.md` |
| A specific reel | — | `sources/Source index.md` |

If they want a setup for **their** account, stop and use the specialist skill (route via `ask-saasyass`).

## Completion

They can name **the situation → the move**. Coverage is not learning.
