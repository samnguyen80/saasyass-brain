# Install — Codex

Catalog: `.agents/plugins/marketplace.json`. Same plugin folder as Claude and Grok: `plugins/saasyass-knowledge`.

## 1. Add the marketplace

```bash
codex plugin marketplace add /absolute/path/to/saasyass-brain
# or, once published: codex plugin marketplace add <owner>/saasyass-brain
```

## 2. Install

```bash
codex plugin add saasyass-knowledge@saasyass
```

(`add`, not `install`.) If the marketplace name differs on your build, `codex plugin marketplace list` prints it.

## 3. Check

```bash
codex plugin list
```

From any other directory ask to be taught the demo funnel; Codex should load `teach-saasyass` and Read `knowledge/`. Slash commands are host-dependent on Codex; invoke the skill by name if they are missing.

## Update

Codex has no auto-update: `codex plugin marketplace upgrade saasyass`.

## One session

```bash
codex --plugin-dir /absolute/path/to/saasyass-brain/plugins/saasyass-knowledge
```
