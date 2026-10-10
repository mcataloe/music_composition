# Music Composition Project Directions

This file is the canonical operating ruleset for the **reusable Music Composition framework**, not for any particular songwriter's campaign. Keep project behavior here; creative songwriting and music-specific QA live in `docs/music-song-framework.md`; optional Suno execution lives in `docs/adapters/suno.md`; boundaries in `docs/framework-boundaries.md`; and each campaign's creative profile, actual song catalog, dossiers and provenance in its own repository. Navigation belongs in `README.md`.

## 1. Source of truth and authority

The GitHub repository `mcataloe/music_composition` is the source of truth for **framework methodology and operating rules**. For a specific campaign's preferences, catalog or songs, consult that campaign's canonical repository too. Prefer current repository files to conversational memory when state matters.

Use this precedence order:

1. current explicit user instruction;
2. current repository source of truth;
3. project-level defaults and inferred conventions.

**Scope resolution:** “current repository source of truth” means the canonical owner for the decision at issue: this framework governs **shared process** and a campaign repository governs its own **creative profile, catalog, and individual works**. A campaign's approved artistic/content criteria take priority over a *generic creative default*; they do not silently change this framework's Discovery, override or QA semantics. For ownership references, see [Framework Boundaries](framework-boundaries.md).

A current explicit instruction may override repository convention, but conflicts must not be silently ignored.

- If the user explicitly acknowledges the override, proceed.
- If the instruction clearly conflicts with repository guidance and the user has not acknowledged the conflict, surface it and request confirmation.
- If the repository convention is plainly inapplicable and the new instruction is the natural fit, inform the user of the deviation and proceed.
- If an approved override is durable rather than a one-off exception, update the appropriate canonical repository artifact.

## 2. Semantic project commands

Project commands are semantic, not lexical. Interpret intent rather than requiring exact wording, capitalization, or syntax.

### QA

**QA** invokes a bounded, artifact-appropriate quality-assurance loop before an artifact is returned or declared ready.

A baseline quality check applies to substantive work even when QA is not explicitly invoked. Explicit QA activates the formal loop.

For music, lyrics, generation packages, and listening review, use the canonical QA criteria, finding classes, and stopping rules in `docs/music-song-framework.md`. Do not restate those rules here.

For other artifacts, apply the same defect-driven principle using criteria appropriate to that artifact.

Formal QA returns one of:

- **PASS** — applicable checks pass and no material known defect remains.
- **CONDITIONAL PASS** — currently testable checks pass, but material questions require generation, listening, execution, or other unavailable evidence.
- **FAIL** — a material correctable defect remains.
- **BLOCKED** — QA cannot be meaningfully completed because required information, access, input, or dependency is unavailable.

Summarize material findings and decisions rather than every low-level iteration.

### Discovery

**Discovery** is a structured session for defining the boundaries, constraints, goals, and decision space of a subject before committing to a direction.

At the start:
- state the estimated number of question rounds;
- apply the Materiality Gate before asking questions;
- ask no more than five questions per round;
- ask fewer when additional questions are not material;
- continue only while material unknowns remain.

The round estimate is guidance, not a quota. End early when the Materiality Gate closes. If answers materially expand the domain, revise the estimate.

Between rounds, use the user's answers to eliminate questions that no longer matter.

#### Recommendation-after-options presentation

For each material Discovery question that presents alternatives, preserve the songwriter's independent first impression:

1. State the question and show the materially distinct options **before** revealing a recommendation. Describe alternatives neutrally; do not flag a preferred option in the choices.
2. **After the options**, give a clear recommendation and explain the creative or practical reason for it, including the relevant tradeoff when useful. If the evidence does not support a preference, say so rather than manufacturing one.
3. **After the recommendation**, invite the songwriter's decision. Keep the answer initially unselected in interactive controls; do not automatically select the recommended choice. Allow another choice, a combination, or a freeform answer when materially appropriate.

The purpose is to let the songwriter form an instinct, contrast it with an argued recommendation, and make an informed choice. Do not replace the songwriter's decision with the assistant's default. Apply this order independently to each material question and preserve the existing Materiality Gate and five-questions-per-round ceiling.

### Materiality Gate

The **Materiality Gate** determines whether a question is worth asking.

A question is material only when its answer could reasonably change the scope, creative direction, audience, constraints, acceptance criteria, implementation approach, QA criteria, repository lifecycle, recommendation, or another decision the user would act on.

Do not ask questions merely because the answers are interesting or would only refine an already-stable result. When a non-material unknown can be handled safely with an assumption, make the assumption and continue.

Close the gate when remaining unknowns would refine rather than materially change the course of action.

## 3. Repository lifecycle

Place durable information in its canonical owner:

- project operating behavior → this file;
- reusable music methodology, brief templates and music QA checks → `docs/music-song-framework.md`;
- optional generator-specific execution rules → relevant `docs/adapters/` file;
- repository boundaries and dependency policy → `docs/framework-boundaries.md`;
- project scope and navigation → `README.md`;
- campaign identity, catalog, candidate prioritization/status and song-specific decisions, lyrics, directions and review → owning campaign repository.

When work concerns a specific song, consult its canonical dossier **in the owning campaign** and the governing framework when relevant. Do not recreate private song records in this public repository.

When the user approves a durable decision, that approval is sufficient authority to update the appropriate repository artifact without asking for a second “proceed.” Ask again only if the repository change is destructive, unusually broad, materially ambiguous, or goes beyond what was approved.

Keep durable project knowledge in the repository rather than only in conversational context.

## 4. Ruleset synchronization and de-duplication

Whenever a durable rule, convention, trigger, exception, precedence rule, workflow, or implementation behavior changes, perform a ruleset synchronization check before considering the change complete.

The check must:

1. identify the canonical owner of the changed rule;
2. inspect this file, `docs/music-song-framework.md`, `docs/framework-boundaries.md`, optional adapters, `README.md`, and materially affected campaign profile/catalog/dossiers in their owning repository as accessible;
3. detect duplicated, overlapping, or near-duplicated instructions;
4. consolidate implementation detail into one canonical location whenever practical, replacing duplicates with concise references or scope-specific extensions;
5. verify that references agree on activation semantics, precedence, exceptions, stopping conditions, and implementation behavior;
6. verify that override handling agrees with the authority hierarchy above;
7. update stale cross-references or summaries; and
8. QA the changed rule and all materially affected references.

Do not preserve duplicate instructions merely because they currently agree; duplication creates drift risk.

A short summary may exist in more than one place when operationally necessary, but only one location should own the full implementation rule. Secondary locations should defer to that canonical rule.

If repository instructions disagree about how an action should be triggered, overridden, stopped, or implemented, treat that as a ruleset defect and resolve it before returning **PASS**.

## 5. Operating principle

Use the repository to preserve continuity, Discovery to determine what matters, the Materiality Gate to control questioning, and QA to prevent avoidable defects.

The goal is not process for its own sake. The goal is sound creative decisions, durable project knowledge, and checked work.
