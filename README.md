# Saasyass Brain

Unofficial teaching plugin for Instagram creator [@saasyass](https://www.instagram.com/saasyass/) ("Advanced marketing simplified"): B2B SaaS paid acquisition on Meta, demo funnels, trial onboarding and churn. Same shape as the Chase Chappell brain and Avada Joy brain: knowledge lives next to skills; the agent **reads the file** instead of guessing.

| Command | Job |
|---|---|
| `/saasyass` | Router: which skill |
| `/teach-saasyass` | Classroom: one situation, you guess, one move |
| `/saas-meta-ads-structure` | One campaign, many different ads, ABO vs CBO, scale and refresh |
| `/saas-demo-tracking` | Conversions API for booked and qualified demos |
| `/saas-ad-audit` | Existing-customer leakage, cost per call vs max |
| `/saas-vsl` | Five-part video sales letter |
| `/saas-retention-flows` | Trial onboarding, churn flows, cancellation, win-back |

**Not affiliated.** Numbers are *claimed*. Watch the originals. Not financial advice. Many reels end with "comment X for the SOP/sheet"; those files were never received, so the brain records them as promised only (`concepts/Comment-gated resources.md`).

## Install

```
# Claude Code
/plugin marketplace add https://github.com/samnguyen80/saasyass-brain.git
/plugin install saasyass-knowledge@saasyass
```

```bash
# Codex
codex plugin marketplace add samnguyen80/saasyass-brain
codex plugin add saasyass-knowledge@saasyass
# Grok
grok plugin marketplace add samnguyen80/saasyass-brain
grok plugin install saasyass-knowledge --trust
```

Guides: [`docs/install-claude-code.md`](docs/install-claude-code.md) · [`docs/install-codex.md`](docs/install-codex.md) · [`docs/install-grok.md`](docs/install-grok.md). Cloning does not install the skills.

One session: `claude --plugin-dir /absolute/path/to/saasyass-brain/plugins/saasyass-knowledge`.

## What ships

Markdown is the brain: [`plugins/saasyass-knowledge/knowledge/`](plugins/saasyass-knowledge/knowledge/) — `index.md`, `foundations/` (playbook, glossary), `concepts/` (16), `sources/` (19 reel cards + index). Open as an Obsidian vault. `graphify-out/` (if present) is only a wikilink map.

Student files land in `learners/` (gitignored).

| Path | What |
|---|---|
| [`CLAUDE.md`](CLAUDE.md) | invariants |
| [`shared/RESOLVER.md`](shared/RESOLVER.md) | topic → skill → first file |
| [`CONTEXT.md`](CONTEXT.md) | shared language |
| [`scripts/README.md`](scripts/README.md) | parity gate, graph, how to re-ingest new reels |

```
node scripts/check-parity.mjs
```

## Doctrine in one screen

1. Know max cost per call before judging ad cost.
2. One campaign, broad, 20-30 genuinely different ads.
3. Creative is the targeting.
4. Send booked and rep-qualified events via Conversions API.
5. Check your best ad is not just reaching existing customers.
6. Trials win on the aha moment; retention flows react to behaviour.
