# Optional Suno Adapter

This adapter translates a **tool-independent, approved music brief** into Suno's current lyric, style, audio-input and generator-control fields. It is **optional**; manual composition, instrumental recording, notation, live performance and other generators must not depend on this file.

The canonical creative and music-QA rules are in [Music & Song Framework](../music-song-framework.md); exact QA invocation, status and override rules are in [Project Directions](../project-directions.md). This file owns **Suno-only implementation details**.

## Output for an initial lyrics generation

When a campaign chooses Suno and requests an initial **lyric-based** generation package, present:

1. **Lyrics** in a separate copy/edit block with clear bracketed section markers where supported.
2. **Style and production instructions** in a separate copy/edit block. Keep within the currently documented/applicable style-field size; the source project's observed ceiling is **under 1,000 characters**. Reverify after interface changes and include a character count when practical.
3. **Suno control configuration** in a table, with a concise rationale and any settings not available for the selected generation mode.

For an instrumental Suno generation, adapt the format rather than inventing lyrics or a singer. In later revision cycles, return only the parts necessary to implement the request unless the campaign asks for a complete package.

## Tool control inventory (Suno v6-era source workflow)

- **Exclude Styles:** None or a concise negative list.
- **Vocal Gender:** Male / Female / Unspecified (only when this control exists for the current mode).
- **Duration:** Auto or Custom and target duration.
- **Max Mode:** On / Off where present.
- **Weirdness:** Numeric recommended value when applicable.
- **Style Influence:** Numeric recommended value when applicable.
- **Audio Influence:** N/A without audio input; with a source audio clip, strength of conditioning toward that audio, not a universal musical factor.
- **Variety:** **Off, Normal, High, Very High, Max** — *the five named categories observed in the source workflow*. Do not invent an intermediate category.
- **Personalize:** On / Off as appropriate.

Some controls are conditional and tool versions change. Treat this list as a dated working adapter, **not** a claim about a guaranteed live UI. Check the available interface before presenting exact values that could have changed.

## Prompt translation

- Start from the independent Full/Lite Brief; prioritize its real artistic intent and genre behavior.
- Put a setting in the dedicated control when one exists. Use prose for *complementary* performance or production details: human feel, vocal intimacy, rhythm, orchestration, transitions, texture, emotional restraint.
- Do not echo gender, duration, Max Mode, Weirdness, Style Influence, Variety or Personalize in the style prose when those decisions are already in controls.
- If too long, remove low-priority repetition before discarding important musical identity.
- In lyric mode, use supported bracketed sections such as `[Verse]`, `[Chorus]`, `[Bridge]` and `[Outro]`. Do not assume every possible bracketed annotation is interpreted reliably.
- Test difficult structural changes (key modulation, atypical bridge harmony, unusual ensemble treatment) in generated audio; a written hint does **not** guarantee the audible result.

## Controlled exploration

For an initial baseline with an intentionally engineered style field, the source campaign has often used **Variety: Off**, relatively strong Style Influence and restrained Weirdness, seeking faithful initial generation. These are **starting hypotheses, not universal defaults**. If exploration is the objective, higher variety or other settings may be more suitable; change a small number of meaningful parameters per test to attribute effects.

Run the entire package through the shared framework's pre-generation QA, then reserve audio-dependent findings for listening review. Store actual chosen controls, final lyrics, style instructions, and what happened in the **campaign-owned song dossier**, not this general adapter.

## License and separation

Adapter content is reusable documentation subject to the public repository's documentation license when that license is published. Personal lyrics and generation settings recorded in a separate campaign are not automatically released by this adapter.
