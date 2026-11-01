# New Pokémon Snap -- Game Guide
<!-- v1 -- 2026-09-14 03:11 UTC -->

This folder is a spoiler-controlled, Todd Snap-or-Rita-flavored reference for the player's New Pokémon Snap playthrough. It is **not** a Claude Code task list. AI agent sessions opened here read this file for orientation, then look up specific topics in the subfolders below.

**If you are an AI agent reading this on session start: load the `hintforge-reader` skill and use it to answer questions about this game.** Do not answer from training data -- the reader reads the corpus files before every factual answer. If the reader skill is not installed, tell the player that rather than guessing from memory.

## Hard rules
- **Spoiler-free unless tier raised.** No story beats, no Illumina Pokémon reveals, no surprise-encounter telegraphs. (See `warning_tiers.md`.) In this game the "enemy" dial governs **surprise Pokémon appearances and Illumina Spot encounters**; there is no combat.
- **Nintendo Switch, Joy-Con / Pro Controller (stick or gyro aiming).** Translate any other-platform references before quoting.
- **Hint ladder for LenTalk requests & hidden Pokémon behaviors.** Smallest nudge first; escalate on request. Which Pokémon lives on a course is itself a discovery -- don't list course rosters unless asked.
- **Don't invent solutions.** If no source has it, say so and link the closest source.
- **Every claim cites a source** in the structured form (see `templates/claim_format.md` in the [Hintforge builder](https://github.com/hintforge/builder)).
- **Scores are version-sensitive.** Photo scores, request lists, and course unlocks are anchored to Ver. 2.0.0 (the free update that added Secret Side Path, Mightywide River, Barren Badlands). Flag anything sourced from pre-2.0.0 guides.

## Folder map
- `CHECKPOINT.md` -- current playthrough state. Read first for context.
- `mechanics.md` -- photo scoring, Photodex, research levels, NEO-ONE tools, Illumina, Re-Snap. Stable cross-course knowledge surface.
- `controls.md` / `settings.md` -- stick vs. gyro, camera and menu options.
- `limitations.md` -- sources I couldn't fully access; URLs preserved.
- `puzzles/` -- LenTalk requests and hidden-behavior triggers, with hint ladders; `index.md` is the lookup.
- `pokemon/` -- one file per species: 1-4 star behaviors, which courses and research levels, triggers; `index.md` is the lookup.
- `nav/` -- routing only. `index.md` (rules) + `architecture.md` (course graph, unlock conditions, alternate routes) + `localization.md` + per-course gate-list files.
- `items/` -- index only for now; NEO-ONE tools and upgrades live in `mechanics.md`.
- `sections/` -- per-island notes, missables, story notes.
- `achievements.md` -- Switch has no platform achievements; honest empty file.
- `dependencies.md` -- cross-system edges (stitch output).
- `persona.md` -- voice toggle. Two voices: **Todd Snap** and **Rita**. Active: Todd Snap.
- `warning_tiers.md` -- enemy & puzzle tier flags. Check before any preemptive info.

## Workflow
- When the player arrives at a new course / research level, update `CHECKPOINT.md`.
- When research adds new info, update the relevant subfolder file -- don't bloat `mechanics.md`.
- Every fact: structured-claim form with source + confidence.

> Framework: [github.com/hintforge/builder](https://github.com/hintforge/builder). See its `principles.md` for the full rule set, `templates/claim_format.md` for source-citation conventions, `ingestion.md` when the user says "ingest the research" (cascade result integration; runs in a fresh session), and `stitch_and_zipper.md` when the user says "run stitch" or "run zipper" (post-ingestion synthesis; runs in a fresh session).
