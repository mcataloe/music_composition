# Campaign Separation Runbook

**Status:** Staged plan; migration **not complete**. Approved decisions: universal core with optional profiles; move all personal song materials to Campaign; make Campaign private; CC BY 4.0 documentation / MIT software; released-version dependency. [Framework Boundaries](framework-boundaries.md) is canonical for architectural ownership.

## Baseline observed on 2026-10-10

- Source: `mcataloe/music_composition`, **public**, `main` at `0fe49b6a04360b8fda2cec414010dd65baee907f` when first inventoried.
- Destination: `mcataloe/music_campaign`, **public**, empty (no branches or files observed).
- Source currently mixes reusable methods, family-life preferences, actual song dossiers, and personal provenance. Being public is not the same as having an explicit open-source license.
- This separation plan does not authorize forced Git-history rewriting, deleting the source repository, or publishing original lyrics under the framework license.

## Inventory and destination mapping

| Existing source path | Treatment |
| --- | --- |
| `README.md` | Change source README to public-framework scope once migration has passed; add a private campaign README |
| `docs/project-directions.md` | Keep; generalize source-of-truth lifecycle and repository references |
| `docs/music-song-framework.md` | **Refactor in place** into universal songwriting/craft rules; extract personal preferences and Suno execution constraints to their owners |
| `docs/meaning-architecture-examples.md` | Keep neutral/invented examples; move or replace song-specific touchstones |
| `docs/potential-songs.md` | Copy intact into private Campaign; after QA remove from *active* source branch |
| `docs/songs/before-the-first-note.md` | Copy intact into private Campaign; professional application song, **intentionally outside the family-song catalog** |
| `docs/songs/between-the-raindrops.md` | Copy intact into private Campaign |
| `docs/songs/dishes-come-back.md` | Copy intact into private Campaign |
| `docs/songs/feed-the-cats.md` | Copy intact into private Campaign |
| `docs/songs/five-more-minutes.md` | Copy intact into private Campaign |
| `docs/songs/the-long-way-home.md` | Copy intact into private Campaign |
| `docs/songs/woodpeckers-are-the-best.md` | Copy intact into private Campaign |
| `docs/songs/you-watched-it-without-me.md` | Copy intact into private Campaign; retain file-to-title history for **Friday Night** |

The current framework is long and includes prior Discovery decisions. Preserve every campaign-specific decision in a private archival/working artifact before deleting or rewriting those sections in the public framework. Do not treat the table above as proof of migration.

## Order of operations and stop conditions

1. **Stage safely** — create a dedicated framework branch and draft PR; do not change the source `main` yet. Establish exact migration inventory and QA expectations.
2. **Privacy prerequisite — BLOCKER** — owner changes `music_campaign` to **private** in GitHub Settings. Re-read visibility before placing personal lyrics, identifying provenance, or campaign material there. The connected GitHub actions do not offer a repository-visibility change.
3. **Copy before deleting** — copy the song catalog and all eight source dossiers without changing their words or history. Verify source/destination content equality, path presence, title and status, all lyrics, generation settings, decision history, and reference continuity. Copy legacy source-framework decisions that are personal before generalizing them.
4. **Extract campaign profile** — capture family-life/child-and-parent audience policy, ages 4–7, catalog-wide roughly 50/50 aspiration, stylistic preferences, personal creative goals, and any other campaign-only defaults. Record explicit override semantics and the framework dependency reference.
5. **Generalize framework** — retain architecture of meaning, musical dimensions, Discovery protocol, QA loop and reusable templates; move generator-specific details into optional adapters; remove campaign-owned catalog and dossiers from the working framework only after step 3 passes.
6. **Licensing / publication gate** — only after the license-covered paths are inspected and campaign material is removed from the proposed release tree, apply **CC BY 4.0 to reusable documentation** and **MIT to software/scripts**, with clear separate scopes. Do not blanket-license old song dossiers, melodies, media, audio, or private campaign assets. Include attribution instructions and third-party-content review. An explicit license on a current tree does not automatically settle licensing questions about earlier content/history.
7. **Sync and QA** — inspect `docs/project-directions.md`, framework, examples, README, adapter, catalog and dossiers in both repositories; detect duplicate/conflicting instructions, stale links, unqualified campaign assumptions, bad template references and changed semantics. Test both profile scenarios in [Framework Boundaries](framework-boundaries.md).
8. **Release deliberately** — review and merge both changes only once the destination is private and migration data QA passes; cut a tagged, documented framework release only after release QA; pin the campaign to that released version. Avoid claiming versioned integration before the release exists.

## History and privacy limitation

Deleting files in a new commit **does not delete their older Git history**. Existing public clones/forks, cached references, PR links, and direct historical commit access can remain. Do not imply that the source repo has been completely de-personalized simply because its newest tree no longer displays dossiers.

A destructive history rewrite, clean-room repository replacement, or removal request requires separate review and explicit approval. Such measures may be incomplete and affect links, forks, collaboration, and provenance; take an external backup first.

## Formal release QA checklist

- [ ] Destination private, independently reverified immediately before writing personal material.
- [ ] Each of eight source dossiers copied, with full content matching original SHA/content.
- [ ] Catalog copied, statuses and canonical song references reconciled (including title/filename history); verify *Before the First Note* intentionally remains outside the family-song catalog.
- [ ] Personal Discovery decisions extracted with provenance; no loss of approved creative constraints.
- [ ] Source public release tree contains no campaign-owned dossiers/catalog or unapproved private material.
- [ ] No duplicate/conflicting instructions between operating rules, framework, adapters, profiles and READMEs.
- [ ] Framework passes family and unrelated instrumental/experimental campaign tests.
- [ ] All cross-repository links point to their new owners; no broken relative links.
- [ ] Tool-specific constraints optional, current, correctly scoped; no unqualified Suno dependency.
- [ ] Copyright/third-party and licensing scope audited; LICENSE, attribution/contributor guidance correct.
- [ ] History/privacy limitations and any residual exposure are explicitly accepted, not concealed.
- [ ] An actual tagged framework release exists before a campaign references its version as released.
- [ ] Repository rule synchronization and affected-artifact QA pass.

## QA status of this document

This runbook is a reviewed **plan**, not a completed migration. Apply **CONDITIONAL PASS** to the current architecture/plan and **BLOCKED** to migration execution until repository privacy is confirmed. Do not mark execution **PASS** simply because the steps are documented.
