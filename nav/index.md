# Nav -- Index

**status:** scaffold <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-13

Sequential gate lists per course. The persona consults files in this folder first for nav-class questions ("how do I unlock X?", "how do I get onto the other path?", "I just started <course>").

For the cross-course structural backbone -- course graph, unlock conditions, support topology, locks-and-keys -- see [`architecture.md`](architecture.md). For behavior triggers and request solutions, see `../puzzles/` and `../pokemon/`. For per-island missables, see `../sections/`. **This folder is routing only.**

## Files in this folder

| File | Type | Linear? | Status |
|---|---|---|---|
| [`architecture.md`](architecture.md) | course graph + cascade outputs | n/a | scaffold |
| [`localization.md`](localization.md) | landmark → course resolution | n/a | scaffold |

(Add one row per course at P2 ingestion. Course-id matches the canonical id in `architecture.md`.)

## Routing rules (apply to ALL nav files in this folder)

### NEVER use left/right -- anchor to features

The NEO-ONE's camera can face any direction, so left/right is meaningless. Describe spots by what's there ("at the big hollow tree", "once the pod enters the cave mouth"), and forks by what they lead to.

- If a spot has no distinctive feature to name, ask the player to describe what they see and route from their description -- don't guess.

### Save / checkpoint mechanism

On-rails expeditions have no mid-course saves; progress is recorded after an expedition. Confirm at P1 and name it on course entry if it differs.

### Hint format on course entry

When the player starts a course and asks for help, **before any behavior solutions**, give **2-3 short tips** max: which research level unlocks something new, whether an alternate route exists (not how to open it unless asked), and which tools are worth having ready. Respect the enemy dial -- no species names at tier 0.

## Scaffold-file fallback

When the player asks about a course whose nav file is still a scaffold, **web-search before asking a clarifying question**.

## Localization toolkit

This game is `hybrid`: see [`localization.md`](localization.md).
