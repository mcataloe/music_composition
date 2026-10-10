# Music Composition

**An open, reusable music-composition framework for use with an AI assistant.** Start with a song idea, feeling, observation, story or musical possibility. The framework helps turn it into an intentional creative brief through **Discovery**, asks only questions that materially affect the result, and uses **QA** to refine the work before and after generation or performance. It supports songs, instrumental music and experimental work without imposing a genre, audience, artistic formula or AI music tool.

## Quick start: AI assistant → Discovery → Suno

1. **Share the repository URL with your AI assistant.** In a new conversation, give it [https://github.com/mcataloe/music_composition](https://github.com/mcataloe/music_composition) and ask it to follow [Project Directions](docs/project-directions.md), consulting the [Music & Song Framework](docs/music-song-framework.md) and [Suno Adapter](docs/adapters/suno.md) when relevant. The assistant needs access to these files; if it cannot open GitHub links, paste the relevant documents into your conversation.
2. **Start a Discovery session around a song theme.** Describe what you already know: your central idea, story, imagery, emotions, audience, musical preferences or other constraints. Provide as much or as little as you have. Ask the assistant to **start Discovery**; the framework will help identify the material decisions that remain rather than require every detail upfront.
3. **Answer the questions, then create with Suno.** Once the material decisions are settled and the song is ready for an initial lyric-based generation, ask for the **Suno package**: separate copy blocks for **Lyrics**, **Style / production instructions** and **Song caption**, plus a **Configuration** table. Paste lyrics and style into Suno, set the controls from the table, and use the caption for the published/shared song description. Listen to the result and revise as needed.

### Example prompt

```text
Use https://github.com/mcataloe/music_composition as our composition framework.
Read docs/project-directions.md first, and consult the music framework
and Suno adapter when relevant.

Start Discovery for a song about [central theme].
Here's what I already have in mind: [ideas, feelings, audience, sounds, or constraints].

Help me resolve the important decisions and create a song brief. When we're
ready for lyrics, give me the Suno package: Lyrics, Style, Configuration,
and a separate Song Caption. Run the framework's QA process.
```

Suno is an **optional** execution path. Instrumental pieces, manual composition, and other tools can use the same Discovery, brief and QA method without forcing a lyric-based Suno package.

## Explore the framework

- [Project Directions](docs/project-directions.md) — the canonical Discovery, Materiality Gate, QA, authority and synchronization rules.
- [Music & Song Framework](docs/music-song-framework.md) — architecture of meaning, musical dimensions, briefs, composition craft and review.
- [Architecture of Meaning — Idea Bank](docs/meaning-architecture-examples.md) — optional inspiration for different ways a piece can mean or simply *be*.
- [Suno Adapter](docs/adapters/suno.md) — optional generation fields, output channels and tool-specific QA.
- [Campaign Profile Template](templates/campaign-profile.md) — a starting point for an independent artist or project.
- [Contributing](CONTRIBUTING.md) — how to improve the reusable framework.

## Framework vs. your campaign

**This public repository** owns reusable methods, templates, QA and optional generator adapters. **Your own campaign** owns its artistic identity, song concepts, lyrics, compositions, original recordings, personal provenance, generation settings, review notes and publication decisions. It should reference an explicit framework version or immutable commit, rather than silently follow `main`.

See [Framework & Campaign Boundaries](docs/framework-boundaries.md) for the canonical ownership and upgrade contract. The [Separation Runbook](docs/separation-runbook.md) documents the original migration and QA evidence.

## Licensing

- Reusable **documentation and templates**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE-DOCS.md).
- **Software and scripts**, if added: [MIT License](LICENSE).
- Original campaign lyrics, audio, artwork, creative works and personal song dossiers are **not** included or licensed by this framework.

The original Git history contained personal song material before repository separation. Removing files from the current tree does not erase historical commits or copies.

## Project status

The framework has been separated from the private `music_campaign`. See [Separation QA](docs/qa-separation-20261010.md) for migration evidence. **No tagged framework release has yet been created**; campaigns may pin a reviewed immutable commit until a release exists.
