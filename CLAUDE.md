# saasyass-brain

Marketplace plugin: unofficial **@saasyass** teaching corpus (B2B SaaS paid acquisition on Meta, demo tracking, funnels, trial onboarding, churn). Works from **any directory**, not only inside this repo.

Profile: https://www.instagram.com/saasyass/ — **not affiliated**.

## Three runtimes, two manifests

| Runtime | Reads |
|---|---|
| **Claude Code** | `.claude-plugin/` |
| **Codex** | `.agents/plugins/` + `.codex-plugin/` |
| **Grok** | `.claude-plugin/` (same files as Claude) |

## Structure

| Path | What |
|---|---|
| `.claude-plugin/marketplace.json` | catalog — Claude **and Grok** |
| `.agents/plugins/marketplace.json` | catalog — Codex |
| `plugins/saasyass-knowledge/` | skills + commands + `knowledge/` |
| `shared/RESOLVER.md` | which task reads what first |
| `graphify-out/` | committed knowledge graph (if built) |
| `learners/` | gitignored student workspace |
| `scripts/` | parity gate, graph rebuild, re-ingest notes |

**Install:** [`docs/install-claude-code.md`](docs/install-claude-code.md) · [`docs/install-codex.md`](docs/install-codex.md) · [`docs/install-grok.md`](docs/install-grok.md). Do not add a third `.grok-plugin/` marketplace — Grok reads `.claude-plugin/`.

**Content is markdown** in `plugins/saasyass-knowledge/knowledge/` (playbook, glossary, concepts, one card per reel). Open that folder as an **Obsidian vault**. `graphify-out/` is only a wikilink map.

## Invariants

1. Marketplace is named `saasyass`.
2. A registry change touches **both** `marketplace.json` files. A plugin change touches **both** `plugin.json` files.
3. A skill change bumps `version` in both `plugin.json` and `.claude-plugin/marketplace.json` (the Codex marketplace carries no version).
4. Every `plugin.json` needs `author`.
5. Every frontmatter `description` and `argument-hint` is a **quoted YAML scalar**.
6. **Distil, never copy transcripts.** No transcript files in the repo; no quoted passages longer than ~15 words. Two copies of doctrine (skill + knowledge) is a bug — skills point, knowledge owns.
7. Figures are **claimed** (creator's own, unaudited). A "comment X" lead magnet whose contents we never saw is recorded as promised, never reconstructed.
8. No binaries over 1 MB.

## Boundaries

| This brain | Not this brain |
|---|---|
| Saasyass doctrine, Watch links | Raw transcripts |
| How to *teach* and *apply* B2B SaaS Meta acquisition | Live ad-account spend / publishing |
| Claimed figures, labelled claimed | Avada, Joy, other products |

## Publishing

1. Bump version in both `plugin.json` and `.claude-plugin/marketplace.json`
2. `node scripts/check-parity.mjs`
3. `claude plugin validate ./plugins/saasyass-knowledge --strict` and `claude plugin validate . --strict` if those CLIs exist
4. Commit, push
