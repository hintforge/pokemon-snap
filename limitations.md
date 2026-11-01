# New Pokémon Snap -- Limitations & Blocked Sources

Sources I found that look useful but couldn't fully fetch -- paywalls, Cloudflare, age gates, video-only content, etc. URLs preserved so the player (or another contributor) can open them in a real browser.

## How to read this file
- Each entry: topic, URL, block type, what I could glean, best alternative I did get to.
- Each per-topic file (in `puzzles/`, `pokemon/`, `nav/`, `sections/`) also lists its own blocked sources at the bottom -- the player rarely needs to come hunting here.
- This file is the catch-all for sources that didn't fit a specific topic.

## Block types
- **paywall** -- content gated behind a subscription or article limit
- **cloudflare** -- Cloudflare bot challenge / 403 / 503 from WebFetch
- **video-only** -- YouTube or other video where the answer is shown visually; no readable text equivalent
- **age-gate** -- content blocked behind age verification
- **cookie-wall** -- popup or consent flow that broke the fetch
- **search-snippet-only** -- search engine returned a snippet but the page itself wasn't reachable
- **dead-link** -- URL was in another source but no longer resolves

## Entries

None yet (setup 2026-09-13; Stage 0 fetches of Wikipedia, Bulbapedia, and Game8 all succeeded).

## Always-blocked categories

- **Exact photo-score arithmetic.** Scores are computed in-game from pose, size, direction, placement, other Pokémon and background; published numbers are community-measured, not official. Expect `confidence: medium` on score figures.
- **Visual-only behavior triggers.** Some hidden behaviors are documented mainly in videos; where no text transcription exists, claims need manual transcription.
- **Platform achievements.** Nintendo Switch has none -- not a gap, a platform fact (see `achievements.md`).
