# Music Composition Project Directions

These directions define how work in the Music Composition project should be conducted. They are intentionally a thin operating layer over the repository's detailed songwriting framework rather than a duplicate of it.

## 1. Source of truth

The GitHub repository `mcataloe/music_composition` is the source of truth for this project.

It owns:
- the reusable songwriting and composition framework;
- the general family-life song campaign / catalog direction;
- song-specific dossiers;
- lyrics, generation directions, listening-review findings, and lessons learned captured in those dossiers;
- reusable QA and generation conventions;
- durable decisions that materially affect future music-composition work.

When repository content is relevant to a task, consult the current repository rather than relying on conversational memory alone.

### Authority and conflict resolution

Use this precedence order:

1. current explicit user instruction;
2. current repository source of truth;
3. project-level defaults and inferred conventions.

A current explicit instruction may override repository convention, but conflicts must not be silently ignored.

- If the user explicitly acknowledges that they are overriding an existing convention, proceed with the override.
- If a new instruction clearly conflicts with repository guidance and the user has not acknowledged the conflict, surface the conflict and request confirmation before proceeding.
- If the repository convention is plainly inapplicable to the situation and the new instruction is the natural fit, inform the user of the deviation and proceed without blocking.
- When an approved override represents a durable change rather than a one-off exception, update the appropriate repository artifact so the repository remains current.

## 2. Semantic project commands

Project commands are semantic, not lexical.

Treat wording, capitalization, punctuation, and minor phrasing differences as equivalent when the user's intent is clear. For example, “QA this,” “let's qa the dossier,” and “run quality assurance on this” should invoke the same QA protocol.

### QA

**QA** means to run a bounded, artifact-appropriate quality-assurance loop before returning the requested artifact or declaring it ready.

A reasonable baseline quality check applies to substantive artifacts even when the user does not explicitly invoke QA. Explicit QA activates the formal defect-driven QA process.

Use this general pattern:

> artifact → apply applicable canonical checks → revise material defects → rerun affected checks → return result

#### Canonical QA ownership

Keep QA logic in one authoritative place whenever possible.

- Detailed music, lyric, generation-package, and listening-related QA criteria, finding classes, and stopping rules live in the pre-generation QA loop of `docs/music-song-framework.md`.
- This project-directions document owns the meaning of the **QA** command, its activation behavior, artifact-appropriate application, and the project-level result states below.
- For non-song artifacts such as repository documentation, prompts, framework changes, or campaign plans, apply the same bounded, defect-driven principle but do not import irrelevant songwriting criteria.
- When QA mechanics change, update the canonical implementation and its references rather than copying the same rule into multiple locations.

If a revision materially changes the artifact, rerun the checks affected by that change. Run a full relevant pass when the change can affect the artifact as a whole.

#### QA result states

Return one of these states after a formal QA pass:

- **PASS** — applicable hard gates pass and no material known defect remains.
- **CONDITIONAL PASS** — all currently testable hard gates pass, but one or more material questions require generation, listening, external execution, or other evidence not yet available.
- **FAIL** — one or more material defects remain that can and should be corrected before the artifact is accepted.
- **BLOCKED** — QA cannot be meaningfully completed because required information, access, input, or an external dependency is unavailable.

Summarize material findings and decisions. Do not burden the user with every low-level iteration.

For music-specific QA, use the framework's canonical stopping rule and **Must fix / Should fix / Test in generation** classifications. For other artifacts, stop when no material defect remains and further changes are primarily preference rather than identifiable improvement.

Preserve intentional irregularity and distinctiveness when they serve the work.

### Discovery

**Discovery** means a structured session for understanding the boundaries, constraints, goals, and decision space of a subject before committing to a direction.

At the beginning of a Discovery session:
- state the estimated number of question rounds;
- apply the Materiality Gate before asking questions;
- ask no more than five questions in a round;
- ask fewer than five when additional questions would not materially improve the decision;
- continue in rounds only while material unknowns remain.

The round estimate is guidance rather than a quota. End early when the Materiality Gate closes. If new answers materially expand the domain, revise the estimate rather than manufacturing or suppressing questions to match the original estimate.

Between rounds, use the user's answers to eliminate questions that no longer matter and narrow the remaining decision space.

### Materiality Gate

The **Materiality Gate** determines whether a question is worth asking.

A question is material when its answer could reasonably change one or more of the following:
- scope or boundaries;
- creative direction;
- audience or intended experience;
- constraints or acceptance criteria;
- implementation or production approach;
- QA criteria;
- repository authority, location, or lifecycle;
- a recommendation or decision the user would act on.

Do not ask a question merely because the answer would be interesting, provide extra detail, or make an already-stable recommendation slightly more customized.

When a non-material unknown can be handled safely with an assumption, make the assumption and continue.

Close the Materiality Gate when the remaining unknowns would refine rather than materially change the course of action.

## 3. Repository lifecycle

Repository placement should follow the durability and scope of the decision.

- Reusable songwriting rules, creative principles, QA logic, and generation lessons belong in the governing framework.
- General campaign / catalog decisions belong in the appropriate framework or catalog-level repository documentation.
- Song-specific concept, lyrics, generation directions, review findings, and lessons belong in that song's dossier.
- Project operating behavior such as QA, Discovery, Materiality Gate, authority, and repository lifecycle belongs in this document.

When work concerns an existing song, consult both its current dossier and the governing framework when those sources are relevant.

When the user approves a durable decision, that approval is sufficient authority to update the appropriate repository artifact without asking for a second “proceed.” Ask again only when the proposed repository change is destructive, unusually broad, materially ambiguous, or goes beyond the decision the user approved.

Keep repository documentation synchronized with approved decisions so conversational context does not become the only place where project knowledge exists.


### Ruleset synchronization and de-duplication

Whenever a durable rule, convention, trigger, exception, precedence rule, workflow, or implementation behavior changes anywhere in the repository, perform a ruleset synchronization check before considering the change complete.

The check must:

1. identify the canonical owner of the changed rule;
2. inspect `docs/project-directions.md`, `docs/music-song-framework.md`, and any other repository documents materially affected by that rule;
3. detect duplicated, overlapping, or near-duplicated instructions;
4. consolidate implementation detail into one canonical location whenever practical, replacing duplicates with concise references or scope-specific extensions;
5. verify that references agree on activation semantics, precedence, exceptions, stopping conditions, and implementation behavior;
6. verify that override handling does not contradict the authority hierarchy in this document;
7. update stale cross-references or summaries affected by the rule change; and
8. QA the changed rule and all materially affected references before the ruleset change is considered complete.

Do not preserve duplicate instructions merely because they currently agree. Duplication creates drift risk.

A short summary may exist in more than one document when it is operationally necessary, but only one location should own the full implementation rule. Secondary locations should clearly defer to the canonical rule rather than restating it independently.

If two repository instructions disagree about how an action should be triggered, overridden, stopped, or implemented, treat that as a ruleset defect. Resolve it through the authority hierarchy and approved intent before returning **PASS** on the maintenance change.


## 4. Operating principle

Use the repository to preserve continuity, Discovery to determine what matters, the Materiality Gate to control questioning, and QA to prevent avoidable defects.

The goal is not process for its own sake. The goal is to make good creative decisions, preserve them durably, test the work appropriately, and return artifacts that have already been checked before the user has to find the problems.
