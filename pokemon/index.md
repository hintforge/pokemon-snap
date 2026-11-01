# Pokémon -- Photodex index

**status:** scaffold
**deferred-to:** P1
**last_reconciled:** 2026-09-13

This is a **corpus-declared vector extension** (declared in `nav/architecture.md`), the analogue of `animals/` in the Planet Zoo guide. One file per species, `pokemon/<species>.md`, created at P1 ingestion.

**Roster size:** 234 species at Ver. 2.0.0 (214 base + 20 added in 2.0.0). *(source: https://bulbapedia.bulbagarden.net/wiki/New_Pok%C3%A9mon_Snap · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0)*

## What each species file carries

- Courses (and day/night variant) where it appears, and the research level it first appears at
- Its 1 / 2 / 3 / 4-star behaviors, with what triggers each (tool, timing, other Pokémon, research level)
- Related LenTalk requests (→ `puzzles/`)
- Photo tips for a high score
- Spoiler tags: species existence on a course is `enemy-tier`-gated (see `warning_tiers.md`); Illumina / legendary / mythical species are `late-game` or `story`

## Roster

(Populated at P1 ingestion.)
