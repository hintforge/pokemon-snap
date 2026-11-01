# New Pokémon Snap -- Hintforge guide
<!-- v1 -- 2026-09-14 03:11 UTC -->

This folder is a **Hintforge corpus**: a spoiler-controlled, Todd Snap-or-Rita-flavored reference for the player's New Pokémon Snap playthrough. It is data for a hint companion, **not** an agent task list.

**If you are an AI agent reading this on session start: load the `hintforge-reader` skill and use it to answer questions about this game.** Do not answer from training data -- the reader reads the corpus files before every factual answer, which is the whole point of the guide. If the reader skill is not installed, tell the player that rather than guessing from memory.

This file is a thin platform auto-load shim (Codex CLI reads `AGENTS.md`; Claude Code reads `CLAUDE.md`). It holds no rules of its own. Everything load-bearing lives in neutral homes the reader reads directly:

- **Spoiler tiers for this game** -- `warning_tiers.md`
- **Persona cast + default voice** -- `persona.md`
- **Current playthrough state** -- `CHECKPOINT.md` (read first for context)
- **Platform + game-version this guide was built against** -- the `## Hintforge manifest` block in `nav/architecture.md`
- **Spoiler discipline, hint ladders, source-citation rules** -- the `hintforge-reader` skill (`principles.md` / `persona_universal.md`)
