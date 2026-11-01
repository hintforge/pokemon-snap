# Localization toolkit -- New Pokémon Snap

**status:** scaffold <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-13
**research_run:** none

The persona reads this file when CHECKPOINT.md's `player_position.confidence < high`. It tells the persona how to ask the player where they are, and how to map their answer to a `current_zone` in `architecture.md`.

## Landmark → zone resolution

| Landmark / feature | Resolves to zone-id | Notes |
|---|---|---|
| (populate at P2 -- 3-6 distinctive in-course landmarks per course, with day/night disambiguation) | | |

## Ask-the-player prompts

- "Which course are you on, and is it day or night?"
- "What research level is that course at? (It's shown when you pick the course.)"
- "Roughly where along the track are you -- near the start, a fork, the end? What's the last big thing the NEO-ONE passed?"

## Map-element prompts (`hybrid`)

- "Which island is highlighted on your Lental map?"
- "Which courses show as unlocked on that island?"
