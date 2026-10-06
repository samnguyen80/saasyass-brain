# Install — Grok

Grok reads the same `.claude-plugin/marketplace.json` as Claude Code. No `.grok-plugin/`.

## 1. Add the marketplace

```bash
grok plugin marketplace add /absolute/path/to/saasyass-brain
```

## 2. Install and trust

```bash
grok plugin install saasyass-knowledge --trust
grok plugin enable saasyass-knowledge
```

`--trust` is required the first time; the plugin has no hooks or MCP servers. Start a **new** Grok session afterward.

## 3. Check

```bash
grok plugin list
grok plugin details saasyass-knowledge
```

Then `/teach-saasyass demo funnel` from any directory. Grok must Read a file under `knowledge/`.

## Update

```bash
grok plugin marketplace update saasyass
grok plugin update saasyass-knowledge
```

## Knowledge path

Skills Read `${CLAUDE_PLUGIN_ROOT}/knowledge/…`; Grok aliases it to `GROK_PLUGIN_ROOT`. Do not rewrite skills to the Grok variable only.
