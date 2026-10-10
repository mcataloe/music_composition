# Contributing to Music Composition

This project welcomes proposals that make music creation and review more useful to **different kinds of musicians and campaigns**, not only one artistic style.

## What belongs here

- Reusable Discovery, music design, brief, QA, and review methods;
- optional adapter improvements for a supported generator or workflow;
- clearly hypothetical examples, tutorials, and documentation;
- tests or tooling that help creators use the framework independently.

**Do not submit private song dossiers, unpublished lyrics, personal family details, proprietary recordings, copyrighted third-party material, or one songwriter's subjective profile as core requirements.** Keep campaign-specific preferences in campaign repositories.

## Proposing a change

1. Describe the problem and whom it affects. For a rule change, identify its current canonical owner.
2. Show the smallest coherent modification; link to existing rules rather than copying detailed procedures into several files.
3. Explain the material tradeoff and whether the rule applies universally or only to an adapter/example.
4. Test on two very different campaigns (e.g. lyric-based family catalog and instrumental/experimental work) to catch accidental universal constraints.
5. Run the applicable QA and inspect links, override semantics, stopping conditions and de-duplication before proposing to merge.
6. Clearly identify which claims need generation, performance, listening or external evidence and mark them conditional rather than inventing proof.

See [Project Directions](docs/project-directions.md), [Framework Boundaries](docs/framework-boundaries.md), and the [Music & Song Framework](docs/music-song-framework.md) for canonical behavior.

## Licenses and attribution

Contributions to reusable documentation and Markdown creative templates are submitted under [CC BY 4.0](LICENSE-DOCS.md); covered software/scripts are submitted under [MIT](LICENSE). Only contribute material that you have authority to license accordingly. Document attribution and changes; do not include third-party works without suitable authorization.

For reports about generator UIs, include the tested service/mode/version and date. User-facing values can change, so avoid presenting observations as permanent universal facts.

Maintainers may request tests or revisions when a proposal introduces ruleset drift, accidentally includes campaign-private material, or changes Discovery/QA behavior without documenting it.
