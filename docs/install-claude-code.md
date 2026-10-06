# Install — Claude Code

This repo is a **plugin marketplace**, not a folder Claude auto-loads. Cloning it does **not** install the skills. They live under `plugins/saasyass-knowledge/skills/` in marketplace format, so add the marketplace, then install.

Codex and Grok: [`install-codex.md`](install-codex.md) · [`install-grok.md`](install-grok.md).

After install: **`/teach-saasyass`** (classroom) or **`/saasyass`** (router).

## 1. Add the marketplace

```
/plugin marketplace add https://github.com/samnguyen80/saasyass-brain.git
```

**The `.git` suffix is required.** Without it, Claude Code treats the URL as a file to HTTP GET. (No remote exists yet; use a local path until you publish.)

## 2. Install the plugin

```
/plugin install saasyass-knowledge@saasyass
```

Turn on **Enable auto-update** in `/plugin`.

## 3. Check it loaded

```
/plugin list
```

You should see `saasyass-knowledge` from marketplace `saasyass`. Then, from **any other directory**:

```
/teach-saasyass demo funnel
```

Claude must load skill `teach-saasyass` and **Read** a file under `knowledge/` — not answer from memory.

| Ask | Expected |
|---|---|
| `/teach-saasyass` (no topic) | one situation, a question, wait for a guess |
| *"Meta says 12 demos, my calendar says 31"* | `saas-demo-tracking` → `Conversion signal quality.md` |
| *"What is in the funnel flowchart he sends?"* | says it is comment-gated and not in the brain |
| *"Write a Python function to reverse a string"* | **no** Saasyass skill fires |

## Update

```
/plugin marketplace update saasyass
```

Runtime detects updates by **`version`**, not commit. Bump `plugin.json` when a skill changes.

## Try without installing (one session)

```bash
claude --plugin-dir /absolute/path/to/saasyass-brain/plugins/saasyass-knowledge
```

Run from another directory for the real test. Plugin skills are namespaced `saasyass-knowledge:teach-saasyass`.

## Obsidian

Open as vault: `plugins/saasyass-knowledge/knowledge`. Start at `index.md`.
