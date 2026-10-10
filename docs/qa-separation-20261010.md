# Separation QA — 2026-10-10

**Scope:** Migration from public `mcataloe/music_composition` to private `mcataloe/music_campaign`, reusable-framework refactor and open-source readiness. This is QA evidence, **not an independent governing ruleset**. See [Project Directions](project-directions.md) and [Separation Runbook](separation-runbook.md).

## Verified repository facts

- Campaign visibility confirmed **private** prior to writing personal material, and reconfirmed before merging.
- The private campaign import [PR #1](https://github.com/mcataloe/music_campaign/pull/1) **merged** (commit `e31ec03001547afaf29dd871b817c8d11c97e420`).
- All **eight** song dossiers and the original song backlog match source commit `37e7838a535f00b57782bec6462d9e092c1bbbcb` by **both content equality and Git blob SHA**. The original full `docs/music-song-framework.md` was also copied, with matching blob SHA, to the private archival path.
- The special-purpose application song *Before the First Note* was correctly kept outside the family-song backlog, as originally decided.
- The public refactor branch contains **no active song dossiers or song catalog**; deletion was performed only after the private destination was successfully copied and verified.
- The public draft contains separate CC BY 4.0 documentation and MIT software license notices, scoped to current files and explicitly excluding original campaign creative work.
- Public framework working-tree links were validated with **38 relative links, zero broken** in the initial final refactor audit. The private import has active links resolving; **seven historical links** in the exact archived framework snapshot are intentionally stale due to its relocated directory and are explicitly documented in `archive/README.md`. The archive itself is not edited to preserve its original Git blob SHA.

## Ruleset synchronization and de-duplication

| Rule or artifact | Canonical active owner | QA |
| --- | --- | --- |
| Discovery rounds, option-before-recommendation, Materiality Gate | `docs/project-directions.md` | Preserved; only this file defines behavior |
| Explicit instruction precedence and conflict/override handling | `docs/project-directions.md` | Confirmed shared protocol versus campaign decisions; boundaries/profile reference this rule |
| Formal QA invocation/status and synchronization | `docs/project-directions.md` | Preserved; framework adds music-specific criteria only |
| Musical creative dimensions, meaning architecture, creative briefs and music QA | `docs/music-song-framework.md` | Generalized; examples do not create additional gates |
| Tool-specific Suno values and channels | `docs/adapters/suno.md` | Optional, version-dependent; campaign references without duplicating numeric limits |
| Family audience, 4–7 age access, roughly 50/50 catalog balance, artistic taste | Private `docs/creative-profile.md` | Campaign-only; no longer universal |
| Concept priorities and actual song status | Private `docs/potential-songs.md` | Source content matched |
| Approved revisions, provenance, lyrics, generator packages and listening notes | Private song dossiers | All eight copied verbatim |
| Historical Discovery record | Private `archive/legacy-music-song-framework-20261010.md` | Exact copy, explicitly archival/not active |
| Creative examples | `docs/meaning-architecture-examples.md` | Removed personal song touchstones/broken catalog link |
| Versioning, ownership and dependency policy | `docs/framework-boundaries.md` | Framework never needs private campaign data |

## Portability pressure tests

**Case A: family-life campaign with lyrics and Suno.** The private campaign profile supplies age/access gates, balance aspirations, explicit style preferences and concept scoring priorities; the public framework supplies Discovery/meaning dimensions/QA; optional Suno adapter supplies UI-specific controls. **Design-level PASS.**

**Case B: unrelated instrumental experimental campaign with no vocalist, lyrics, family topic, semantic story or Suno.** The public core expressly accepts instrumental/experimental works; its Lite/Full briefs do not require lyrics, singer or a message; audience access and hard gates must be chosen by that campaign; the optional Suno adapter is not invoked. **Design-level PASS.**

These are **document/semantics tests**, not claims that external audio generation, software integration or real music listening occurred.

## Risks and release condition

- **Existing public Git history still exposes previous campaign content.** Removing files from the latest branch does not erase prior commits, clones or cached copies. History rewriting was not authorized.
- Documentation attribution and software license scopes are stated, but no independent legal review was performed. Do not interpret licensing as granting rights in third-party materials.
- No tagged release currently exists. Do **not** label the refactor as a tagged version until a tag/release is actually created. Campaign dependency should be pinned to an immutable merged commit in the meantime.
- Tool UIs can change. Recheck Suno limits before relying on an adapter's dated observations.

**Outcome:** **PASS** for migrated file integrity and staged architecture/document-link/ruleset synchronization checks; **CONDITIONAL PASS** for full release readiness pending public PR merge, subsequent immutable dependency pin and any separately desired history remediation. A tagged release remains outstanding and is not falsely claimed.
