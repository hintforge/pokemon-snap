# New Pokémon Snap -- Architecture

**status:** scaffold <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-13
**research_run:** none (Stage 0 skeleton only -- P1 replaces/confirms)

Cross-course structural primitives. The persona reads this file for all cross-course reasoning -- lookahead warnings (Rule 2), backtrack queries (Rule 3), reachability checks (Rule 4), locks-and-keys notifications (Rule 5). Per-course gate lists live in `nav/<course-id>.md` and reference this file's graph by edge. Drift between this file and per-course files is a bug; run a consistency pass after each ingestion.

## Hintforge manifest

<!-- Read by the reader at session start (see docs/corpus-format.md §3). game-version-* fields describe the game build the corpus was authored against (player-supplied at setup); orthogonal to corpus-core-version (the schema axis). -->

```
corpus-core-version: 5
game-version: "2.0.0"
game-version-platform: "Nintendo Switch"
game-version-as-of: 2026-09-13
vector-extensions: [puzzles, pokemon]
```

## Vector extensions

- `puzzles/` -- LenTalk requests and hidden-behavior triggers, one file per course with hint ladders, indexed by `puzzles/index.md`
- `pokemon/` -- **corpus-declared extension** (not canonical). Photodex bestiary: one file per species with star-tier behaviors, courses, triggers, and photo tips. Indexed by `pokemon/index.md`. Species facts route here (tag `vector: item` in research, destination `pokemon/<species>.md`).

## Zone Graph

**status:** scaffold -- Stage 0 skeleton from Bulbapedia; unlock conditions to confirm at P1 (`confidence: medium`, spoiler tags pending).

**Game-type label:** on-rails
**Localization-mechanism class:** hybrid (course chosen from the Lental map menu; in-run position resolved by landmarks)
**Entry node:** florio-park-day
**Hub nodes:** research-camp / Lental map menu (all courses launch from it; no in-world travel between courses)
**Source-language set:** Japanese (dev) + English, French, German, Spanish

**Nodes (zone-id -- canonical name):**
- florio-park-day -- Florio Nature Park (Day)
- florio-park-night -- Florio Nature Park (Night)
- florio-illumina -- Florio Island Illumina Spot
- florio-side-path-day / florio-side-path-night -- Secret Side Path (2.0.0)
- belusylva-jungle-day / belusylva-jungle-night -- Founja Jungle
- belusylva-forest -- Elsewhere Forest
- belusylva-illumina -- Belusylva Island Illumina Spot
- belusylva-river-day / belusylva-river-night -- Mightywide River (2.0.0)
- maricopia-beach-day / maricopia-beach-night -- Blushing Beach
- maricopia-reef-day / maricopia-reef-evening -- Maricopia Reef
- maricopia-undersea -- Outaway Cave / Undersea (name to confirm)
- maricopia-illumina -- Maricopia Islands Illumina Spot
- voluca-sands-day / voluca-sands-night -- Sweltering Sands
- voluca-volcano -- Fireflow Volcano
- voluca-illumina -- Voluca Island Illumina Spot
- voluca-badlands-day / voluca-badlands-night -- Barren Badlands (2.0.0)
- durice-snowfields-day / durice-snowfields-night -- Shiver Snowfields
- durice-cave -- Durice cave course (name to confirm)
- durice-illumina -- Durice Island Illumina Spot
- aurus-ruins -- Aurus Island ruins course (name to confirm)
- aurus-illumina -- Aurus Island Illumina Spot

<!-- Course display names other than the Bulbapedia short names are from general knowledge and MUST be confirmed at P1; treat as aliases, not canonical, until then. -->

**Edges (unlock conditions, per Bulbapedia 2026-09-13):**

| From | To | Type | Direction | Condition | Point of no return | Notes |
|---|---|---|---|---|---|---|
| florio-park-day | florio-park-night | conditional | one-way src→tgt | Park research level 2 | none | |
| florio-park-night | florio-illumina | story-gate | one-way src→tgt | play Park (Night) once | none | |
| florio-illumina | belusylva-jungle-day | story-gate | one-way src→tgt | complete Florio Illumina Spot | none | |
| belusylva-jungle-day | belusylva-jungle-night | conditional | one-way src→tgt | Jungle research level 2 | none | |
| belusylva-jungle-day | maricopia-beach-day | conditional | one-way src→tgt | both Jungle variants at level 2 | none | Beach and Sands unlock together |
| belusylva-jungle-day | voluca-sands-day | conditional | one-way src→tgt | both Jungle variants at level 2 | none | |
| maricopia-beach-day | maricopia-reef-day | conditional | one-way src→tgt | Beach (Day) level 2 | none | |
| maricopia-reef-day | maricopia-undersea | conditional | one-way src→tgt | Reef (Day) level 2 | none | |
| maricopia-undersea | maricopia-illumina | story-gate | one-way src→tgt | Undersea level 2+ | none | |
| voluca-sands-night | voluca-volcano | conditional | one-way src→tgt | Sands (Night) level 2 | none | |
| voluca-volcano | voluca-illumina | story-gate | one-way src→tgt | Volcano level 2 | none | |
| voluca-volcano | belusylva-forest | conditional | one-way src→tgt | Volcano level 2 | none | Cross-island unlock |
| belusylva-forest | belusylva-illumina | story-gate | one-way src→tgt | play Forest once | none | |
| (hub) | durice-snowfields-day | conditional | one-way src→tgt | photograph four Illumina Pokémon | none | |
| durice-snowfields-night | durice-cave | conditional | one-way src→tgt | Snowfields (Night) level 2 | none | |
| durice-cave | durice-illumina | story-gate | one-way src→tgt | Cave level 2 | none | |
| durice-illumina | aurus-ruins | story-gate | one-way src→tgt | complete Durice Illumina Spot | none | |
| aurus-ruins | aurus-illumina | story-gate | one-way src→tgt | light six crystablooms in the ruins | none | Final Illumina Spot |
| florio-park-day | florio-side-path-day | conditional | one-way src→tgt | Ver. 2.0.0 installed (exact trigger to confirm) | none | |
| (post-game) | maricopia-reef-evening | conditional | one-way src→tgt | complete main story | none | |
| (post-game) | belusylva-river-day | conditional | one-way src→tgt | Ver. 2.0.0 + complete main story | none | |
| (post-game) | voluca-badlands-day | conditional | one-way src→tgt | Ver. 2.0.0 + complete main story | none | |

**Point-of-no-return note:** courses are replayable from the map menu at any research level, so no permanent lockouts are expected. P1 must confirm.

## Chapter ↔ Zone Mapping

| Chapter | Zones | Notes |
|---|---|---|
| (to populate at P1) | | |

## Optional Content

| Name | Unlock condition | Access window | Parent zone | Recommended chapter | Failure mode |
|---|---|---|---|---|---|
| (to populate at P1 -- alternate routes within courses, post-game courses, Photodex completion) | | | | | |

## Support Topology

### Save stations

| Zone | Locations |
|---|---|
| (all) | To confirm at P1 -- expected: progress saves between expeditions at the Lab / Research Camp, not mid-course. |

### Fast-travel network

None expected -- every course launches directly from the map menu. Confirm at P1.

### Hub access

Return to the Lab / Research Camp after each expedition for photo evaluation. Confirm at P1.

## Locks and Keys

| Lock location | Key required | Key source | Visible before key? | Notes |
|---|---|---|---|---|
| (to populate at P2 -- alternate routes gated by research level, Scan, Illumina Orbs, or other tools) | | | | |
