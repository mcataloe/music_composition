# Framework and Campaign Boundaries

**Status:** Approved architecture; implementation pending migration QA. This document owns the target repository boundaries. [Separation Runbook](separation-runbook.md) owns the execution sequence and release gates.

## Architecture decision (2026-10-10)

- **`mcataloe/music_composition`:** reusable, audience-neutral and genre-neutral composition methodology, meaning architectures, musical design dimensions, Discovery and Materiality Gate, QA criteria, templates, and optional generator adapters.
- **`mcataloe/music_campaign`:** the songwriter's private creative campaign, including creative profile, intended audience and catalog balance, song concepts, dossiers, personal inspiration/provenance, working lyrics, generation packages, listening feedback, and portfolio status.
- **Other campaigns:** independent consumers of the same composition framework. A new campaign must be usable without importing the author's family-life defaults or musical taste.
- **Dependency direction:** campaigns depend on a released framework; the framework never depends on a particular campaign or its private files.

This is the *approved target model*, not a claim that the present repository content has already been separated.

## Canonical ownership after migration

| Concern | Canonical owner |
| --- | --- |
| Discovery question protocol; Materiality Gate; artifact-appropriate QA outcomes and stopping criteria | Composition: `docs/project-directions.md` |
| Reusable songwriting craft, architecture of meaning, musical dimensions, song briefs, pre-/post-generation review | Composition: `docs/music-song-framework.md` |
| Generic or invented idea examples (not required personal song excerpts) | Composition: `docs/meaning-architecture-examples.md` |
| Tool-specific generator controls, limits, syntax, and export channels | Composition: optional adapter, e.g. `docs/adapters/suno.md` |
| Campaign objectives, personal artistic preferences, age and content boundaries, creative defaults, catalog balance | Campaign: creative profile |
| Actual concepts, song backlog/status, lyrics, arrangements, drafts, dossier decisions, family provenance, releases | Campaign: `docs/potential-songs.md`, `docs/songs/`, campaign-specific files |
| Campaign-specific application of a general scoring method | Campaign profile/configuration; general scoring methodology remains in Composition |
| Repository navigation | Each repository's own `README.md` |

**Extraction rule:** Place reusable *methods* in Composition and user/campaign *chosen values* in Campaign. A rule does not become universally valid merely because it was discovered while making a personal song. Conversely, a principle discovered during personal work can be promoted once generalized and checked.

## Portability requirements

1. No mandated audience, children's access rule, family-life topic, 50/50 catalog mix, default genre, vocalist, or particular generator in the **universal core**.
2. The current child-access and family-listening constraints are valid *campaign profile* choices. The core can teach how to establish and test audience constraints without choosing them for all users.
3. Meaning architecture remains independent of genre, musical form, topic, and audience. Layered metaphor is optional, not mandatory.
4. Creative intent governs critique. A pure observational, absurdist, impressionistic, or unresolved song is not marked defective merely for lacking subtext or a traditional arc.
5. Generator adapters translate an approved, generator-independent brief into tool-specific instructions, respecting limits and channel separation. A manual composition workflow must also work.
6. The framework may offer templates and example profiles but must not require any one profile. An empty campaign can supply its own constraints.
7. The migration must preserve the current project's Discovery, Materiality Gate, QA, song-review criteria, and exceptions unless an approved, documented rule change occurs.
8. Keep one canonical owner per governing rule; examples and READMEs reference rather than duplicate that owner.

## Dependency and version rules

- A campaign records an explicit released framework version or commit reference; **never silently track the latest `main`**.
- Upgrades are deliberate, reviewed, and tested against the campaign's active creative profile, song briefs and QA requirements.
- Framework upgrades do not overwrite campaign-owned decisions or retrospectively rewrite song dossiers.
- Until the first reviewed release exists, do not invent a `v1.0.0` tag or claim compatibility with an unreleased version.
- Current explicit songwriter instructions take precedence; approved campaign configuration selects domain-specific constraints; framework rules provide reusable defaults and governing protocol. Surface conflicts rather than silently applying incompatible rules. Changes to the protocol itself require a documented, approved override and synchronization QA under [Project Directions](project-directions.md).

## Portability acceptance tests

Test both profiles with the same Discovery and QA mechanics:

- **Family-song campaign:** child/adult listening; age-appropriate content; portfolio balance; Suno export where chosen.
- **Unrelated instrumental or experimental campaign:** no child-access gate, mandatory lyrics, family theme, singer, Suno account, or pressure toward meaning-by-metaphor.

A framework that forces the second campaign into the first campaign's rules has **failed** portability QA. Song-artifact QA and repository/migration QA are separate tests; neither substitutes for the other.
