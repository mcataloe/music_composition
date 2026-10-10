# Campaign Separation Runbook

**Status:** Private campaign import and public framework refactor **both merged**. Campaign pinned to the public framework's immutable merge commit. Formal version tag not yet created; historical public song commits remain unchanged. Approved decisions: universal core with optional profiles; move all personal song materials to Campaign; make Campaign private; CC BY 4.0 documentation / MIT software; released-version dependency. [Framework Boundaries](framework-boundaries.md) is canonical for architectural ownership.

## Baseline observed on 2026-10-10

- Source: `mcataloe/music_composition`, **public**, `main` at `0fe49b6a04360b8fda2cec414010dd65baee907f` when first inventoried.
- Destination at initial inventory: `mcataloe/music_campaign`, **public**, empty. **Current:** visibility independently confirmed **private** before copying; catalog and archive imported through [private campaign PR #1](https://github.com/mcataloe/music_campaign/pull/1), squash-merged at `e31ec03001547afaf29dd871b817c8d11c97e420`.
- Source at initial inventory mixed reusable methods, family-life preferences, actual song dossiers and personal provenance. The framework PR now removes those active song files, generalizes the framework and supplies explicit documentation/software license notices. The **old public Git history** still exists.
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
2. **Privacy prerequisite — COMPLETE** — owner changes `music_campaign` to **private** in GitHub Settings. Re-read visibility before placing personal lyrics, identifying provenance, or campaign material there. The connected GitHub actions do not offer a repository-visibility change.
3. **Copy before deleting — COMPLETE** — copy the song catalog and all eight source dossiers without changing their words or history. Verify source/destination content equality, path presence, title and status, all lyrics, generation settings, decision history, and reference continuity. Copy legacy source-framework decisions that are personal before generalizing them.
4. **Extract campaign profile — COMPLETE** — capture family-life/child-and-parent audience policy, ages 4–7, catalog-wide roughly 50/50 aspiration, stylistic preferences, personal creative goals, and any other campaign-only defaults. Record explicit override semantics and the framework dependency reference.
5. **Generalize framework — COMPLETE** — retain architecture of meaning, musical dimensions, Discovery protocol, QA loop and reusable templates; move generator-specific details into optional adapters; remove campaign-owned catalog and dossiers from the working framework only after step 3 passes.
6. **Licensing / publication gate — COMPLETE for current working tree** — only after the license-covered paths are inspected and campaign material is removed from the proposed release tree, apply **CC BY 4.0 to reusable documentation** and **MIT to software/scripts**, with clear separate scopes. Do not blanket-license old song dossiers, melodies, media, audio, or private campaign assets. Include attribution instructions and third-party-content review. An explicit license on a current tree does not automatically settle licensing questions about earlier content/history.
7. **Sync and QA — PASSED at document/migration level** — inspect `docs/project-directions.md`, framework, examples, README, adapter, catalog and dossiers in both repositories; detect duplicate/conflicting instructions, stale links, unqualified campaign assumptions, bad template references and changed semantics. Test both profile scenarios in [Framework Boundaries](framework-boundaries.md).
8. **Release deliberately — PRs MERGED; version tag PENDING** — review and merge both changes only once the destination is private and migration data QA passes; cut a tagged, documented framework release only after release QA; pin the campaign to that released version. Avoid claiming versioned integration before the release exists.

## History and privacy limitation

Deleting files in a new commit **does not delete their older Git history**. Existing public clones/forks, cached references, PR links, and direct historical commit access can remain. Do not imply that the source repo has been completely de-personalized simply because its newest tree no longer displays dossiers.

A destructive history rewrite, clean-room repository replacement, or removal request requires separate review and explicit approval. Such measures may be incomplete and affect links, forks, collaboration, and provenance; take an external backup first.

## Formal release QA checklist

- [x] Destination private, independently reverified immediately before writing personal material.
- [x] Each of eight source dossiers copied, with full content matching original SHA/content.
- [x] Catalog copied, statuses and canonical song references reconciled (including title/filename history); verify *Before the First Note* intentionally remains outside the family-song catalog.
- [x] Personal Discovery decisions extracted into private creative profile, with the full prior framework also preserved unchanged in the archive for historical traceability.
- [x] Source public release tree contains no campaign-owned dossiers/catalog or unapproved private material.
- [x] No known duplicated canonical implementation or conflicting protocol across operating rules, creative framework, optional adapter and campaign profile. Additional edits require the ongoing synchronization check.
- [x] Framework passes family and unrelated instrumental/experimental **document-level portability** tests; no audio was generated as part of this QA.
- [x] All active cross-repository and relative documentation links point to owners; seven stale links inside the exact historical archive are acknowledged and intentionally preserved.
- [x] Tool-specific constraints optional, current, correctly scoped; no unqualified Suno dependency.
- [x] Current-tree documentation/software licensing scope and contributor attribution guidance reviewed; no independent legal opinion or third-party rights clearance has been claimed.
- [ ] History/privacy limitations and any residual exposure are explicitly accepted, not concealed.
- [ ] An actual tagged framework release exists before a campaign references its version as released.
- [x] Repository rule synchronization and affected-artifact document-level QA passed.

## QA status of this document

Private catalog migration is **PASS for content integrity**: the eight dossiers, catalog, and legacy framework archive match their original Git blob hashes, with private visibility independently verified. Active relative links in the campaign resolve; seven historical links inside the *verbatim archived snapshot* remain stale by design and are documented in its archive README. The public framework refactor and private import have both been merged, and the campaign has pinned immutable framework commit `8ad4b65359af7dc7af9e9c600122b7bb599ba47f`. Documentation portability, ownership and link QA have passed. Old public Git history remains accessible and was not rewritten. The full open-source **tagged-release** milestone remains **CONDITIONAL PASS** until a real tag is created and any desired historical-privacy action is separately considered.
