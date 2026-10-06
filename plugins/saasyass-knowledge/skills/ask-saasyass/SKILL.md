---
name: ask-saasyass
description: "Route a Saasyass (B2B SaaS paid acquisition) question to the right skill. Use when the user says /saasyass, ask Saasyass, which skill, or the ask is ambiguous. Do NOT teach a classroom lesson (teach-saasyass). Do NOT invent doctrine or the contents of comment-gated SOPs."
argument-hint: "Question"
---

# Ask Saasyass

Pick **one** skill. Then run it. Knowledge is in `${CLAUDE_PLUGIN_ROOT}/knowledge/` — skills point, they do not own facts.

| They want | Skill |
|---|---|
| Teach me / classroom / guess then job | `teach-saasyass` |
| Campaign structure, ABO vs CBO, budgets, scaling, refresh, what ads to make | `saas-meta-ads-structure` |
| Meta shows fewer demos than calendar, Conversions API, lead quality, learning limited | `saas-demo-tracking` |
| Audit my account, best ad looks too good, cost per call vs max, exclusions | `saas-ad-audit` |
| VSL / pre-call video / reps over-explaining | `saas-vsl` |
| Trial onboarding, churn, cancellation, win-back emails | `saas-retention-flows` |

No specialist yet for the full demo funnel, hammer-them ads, positioning tests or the ad tier list: Read `shared/RESOLVER.md` rows and the named concept directly, then answer from it.

Ambiguous → one clarifying question, then route. Unrelated (for example a Python function) → **no** Saasyass skill. Asked what is inside a comment-gated SOP or sheet → say it is not in the brain (`concepts/Comment-gated resources.md`).
