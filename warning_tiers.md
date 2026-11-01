# Warning / hint tiers (New Pokémon Snap)

Two independent tier flags control how much info the guide volunteers *preemptively*, before the player asks. Higher tiers include everything from lower. Each set independently.

**Game-specific mapping.** New Pokémon Snap has no combat. The **enemy** dial governs *surprise Pokémon encounters*: which species appear on a course, rare/one-off appearances, Illumina Spot Pokémon, and legendary/mythical sightings. "Boss" = an Illumina Spot's Illumina Pokémon or a legendary encounter. The **puzzle** dial governs LenTalk requests and hidden-behavior triggers (the game's puzzle layer).

## the player's current settings

- **Enemies: Tier 0** -- set 2026-11-01
- **Puzzles: Tier 0** -- set 2026-11-01

To change: "set enemy warning to tier N" / "set puzzle tier to N." Update this section with the date.

---

# Enemy tiers (0-5)

### Tier 0 -- No warning
- No mention of which Pokémon appear on a course before the player sees them.
- No "keep an eye out for X," no species names in route hints.
- Illumina Pokémon / legendary encounter existence hidden. No prep.
- Permitted: post-sighting help on request.

### Tier 1 -- Mobs only
- Common course species named in route hints when relevant.
- Illumina / legendary encounters still hidden.
- May reference obliquely ("something special happens at the end of this spot").

### Tier 2 -- Mobs + boss-drop heads-up
- Tier 1 + explicit warning that an Illumina / special encounter is coming at the end of a course.
- No species name, no behavior details, no recommended tool use.

### Tier 3 -- Boss prep
- Tier 2 + name the encounter generically ("a big glowing Pokémon") and recommend which NEO-ONE tools to have ready.
- No step-by-step of the sequence.

### Tier 4 -- Boss prep + materials
- Tier 3 + which items (Illumina Orbs, Fluffruit) to hold in reserve and when.
- Still no step-by-step during the sequence.

### Tier 5 -- Full boss strategy
- Tier 4 + phase-by-phase Illumina sequence, best-shot timing, high-score framing, common failure modes.

---

# Puzzle tiers (0-3)

The hint ladder (Lvl 1 nudge → Lvl 2 more → Lvl 3 step-by-step) is **request-based** -- the player asks for what they want. The puzzle *tier* controls how much is delivered **automatically on entry**, before they ask.

### Tier 0 -- Silent
- No request / behavior info preempted. Player asks for everything via the Lvl 1/2/3 ladder.

### Tier 1 -- Mechanic identified (suggested default)
- When the player names a LenTalk request or hidden behavior they're working on, name the core mechanic in one short sentence: "this one is about which tool you use on it," "this is a timing / chain-reaction request."
- Don't deliver Lvl 1 nudge unless asked.

### Tier 2 -- Auto-nudge
- Tier 1 + deliver the **Lvl 1 nudge automatically**.

### Tier 3 -- Full walkthrough
- Deliver the **Lvl 3 step-by-step** automatically. Use sparingly.

### Per-puzzle ladder requests are NOT tier changes
A "Lvl 2" or "Lvl 3" request on a specific request/behavior is a **one-off escalation** for that one only. The tier flag does NOT change. Next one resets to whatever the flag says. To change permanently, the player says "set puzzle tier to N."

---

## Implementation note

Before delivering preemptive info, check **both** tier settings here. When in doubt between tiers, err stricter. the player can always raise.

For multi-contributor / GitHub-distributed guides, every claim and section carries explicit tier metadata (`enemy-tier` and `puzzle-tier`) plus a `category` field so the aggregator can render reader-tier-appropriate output.

## Breach log

[Record any time the tier was breached unintentionally. Format: `YYYY-MM-DD -- what happened, what should have happened, what changed to prevent recurrence.`]
