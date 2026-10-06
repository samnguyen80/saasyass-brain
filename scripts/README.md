# scripts

| File | What |
|---|---|
| `check-parity.mjs` | Claude/Codex manifest drift gate. `node scripts/check-parity.mjs` |
| `rebuild-graph.py` | Rebuilds `graphify-out/` from `[[wikilinks]]`; `--check` also lints broken links |

## Re-ingesting new reels

There is no daily auto-ingest script here (the Chase brain's one is YouTube-specific).

1. List reels already indexed: shortcodes appear in `knowledge/sources/*.md` (`shortcode:` frontmatter, and the Watch URL `https://www.instagram.com/reel/<shortcode>/`).
2. Find new ones. Enumerating the profile **needs a logged-in Chrome session**: `yt-dlp` on `https://www.instagram.com/saasyass/` fails anonymously (`Unable to extract data`) and `--cookies-from-browser chrome` needs Chrome running and logged in (it can hang on a keychain prompt). Alternative: export a `cookies.txt` and pass `--cookies`.
3. A **single reel URL works anonymously**: `yt-dlp https://www.instagram.com/reel/<shortcode>/` (info JSON gives caption, date, likes). Audio is transcribed locally for reading only.
4. Distil into a new card (`Saasyass - <Title>.md`), add a row to `Source index.md` and links to concepts, then update counts in `index.md`.
5. **Never commit transcripts** or media; keep them outside the repo.
6. `python3 scripts/rebuild-graph.py --check`, bump version in both `plugin.json` and `.claude-plugin/marketplace.json`, `node scripts/check-parity.mjs`.

Carousels and image posts have no audio; distil from caption and slide text.
