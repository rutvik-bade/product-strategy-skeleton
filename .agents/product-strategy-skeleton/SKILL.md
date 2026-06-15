---
name: product-strategy-skeleton
description: Use when maintaining or applying this product strategy skeleton repo: business strategy, operational design, marketing and sales planning, technical specifications, product development lifecycle structure, and spec-driven SDLC workflows. Enforce Technical pillar spec-first development, Technical module expansion, and Spec and Architecture documentation before implementation work.
---

# Product Strategy Skeleton

Use this skill to operate this repo as a reusable product and business strategy skeleton. The repo provides a framework for users to run business planning, product strategy, operational design, marketing and sales planning, technical specification, and product development cycles.

## Dependencies 
This skill depends on the `grill-me` skill for specification planning and the `karpathy` skill for preventing assumptions in specification writing. Flag if you do not have access to these skills.


## Operating Context

Work in one of two modes:

- Generic skeleton mode: preserve broadly reusable structure. Do not overfit modules to one product, market, team, stack, or implementation.
- Applied product mode: allow modules to gain concrete product subdirectories, submodules, specifications, architecture maps, metrics, tests, and implementation references.

The root registry is `Product Strategy.md`. The major pillars are:

- `Business/`
- `Technical/`
- `Operational/`
- `Marketing and Sales/`

Business, Operational, and Marketing and Sales are strategic framework modules for now. Do not enforce strict spec-code architecture rules for them yet unless the user explicitly asks.

## Technical Pillar Rule

For SDLC or product development work, treat `Technical/Performance and Functional Specifications/Core Functionality.md` as the registry for core product behavior.

Start from the Technical registry and linked specifications before inspecting implementation. Do not begin Technical work with broad codebase exploration.

The specification tree and codebase should mirror each other at the major module and ownership level. Treat the specification as an ownership map, not a file map.

Specification is the behavioral authority. After establishing intended behavior, inspect named implementation paths, direct consumers, and targeted search results. If code-level behavior cannot be explained by the specification or architecture map, flag a documentation alignment gap.

When a Technical module becomes implementation-bearing:

1. Create or use a sibling directory for that module.
2. Inside it, use `Spec and Architecture/` as the required home for product specifications and architecture mappings.
3. Place relevant submodule documents under that layer.

Examples of Technical submodules include peripheral detection, classification, backup session creation, repair, state machine, validation, verification, and other product-specific capabilities.

## Spec and Architecture Template

Every Technical Spec and Architecture document must use this structure:

```markdown
# {Module Name}: {description}

## Specification

Functional specification, product policy, behavior expectations, invariants, constraints, and out-of-scope behavior. This is the primary section needed to understand what the module does.
Specification planning is the most critical part of the SDLC. You have to use the `karpathy` and `grill-me` skills to prevent any assumptions. The importance of this section cannot be overstated. If the specification is not clear, you cannot be sure that the implementation is correct, and you cannot be sure that the implementation is aligned with user needs or product goals. Do not proceed to implementation until this section is complete and approved by the relevant stakeholders.
Prevent editing specifications without planning phase and user approval. The planning phase should include:
1. Drafting the specification wording with the `karpathy` skill to ensure clarity and prevent assumptions.
2. Reviewing the drafted specification with the `grill-me` skill to identify any gaps, ambiguities, or misalignments with user needs and product goals.
If these steps are not followed, flag the issue and do not proceed to implementation.

## Architecture

Specification-codebase map. Include major submodules, each with spec responsibility and code map.

## Alignment Notes

Track differences between specification and implementation. Explicitly classify fulfilled, deferred, and gap.

## Architecture Decisions

Record architectural decisions made to honor the specification.

## API Shapes/Consumer Contracts

Document how consumers invoke the module, expected responses, error behavior, and compatibility expectations. This is the interface layer for other modules and consumers.
```

Agents may draft specification wording, but unresolved product policy must not be silently invented or finalized.

If a document diverges from this required structure, flag the divergence before changing implementation behavior.

## Authority Order

When sources conflict, use this order:

1. Explicit user instruction in the current conversation
2. `Product Strategy.md` and pillar registries
3. Technical registry
4. Linked module specification
5. Architecture map and ADR rationale where present
6. Referenced implementation and direct consumers
7. Tests
8. Legacy code only as migration evidence

If sources disagree about product policy, state meaning, ownership, or scope, stop and report the conflict before changing behavior.

If implementation clearly violates an unambiguous specification, flag the mismatch and align it within the requested scope.

## Navigation Protocol

Generic:
1. Read `Product Strategy.md`.
2. Documents contain cross-references formatted as [[$document$]]. To navigate and understand the contextual links of your current document, you must perform a global search for the exact string [[Current Document Name]]. This search reveals all external documents that reference the current page, establishing the network of cross-links.
This also helps understand documented nuances the user might skip out in the original directive.
3. Hierarchical walk: Walk the hierarchy of documents to understand structure, ownership and module boundaries.
4. Targeted search: When you need to understand a specific behavior, policy, or ownership, run targeted searches for the relevant terms across the codebase and documentation. 

For Technical work:

1. Read `Product Strategy.md`.
2. Read `Technical/Technical.md`.
3. Read `Technical/Performance and Functional Specifications/Core Functionality.md` when core behavior is involved.
4. Read the linked module specification.
5. Inspect only the implementation paths named by the specification, their direct consumers, and direct tests.
6. Run targeted searches for callers, configuration, environment variables, deployment hooks, tests, and stale references.

Do not modify implementation behavior unless the corresponding Technical specification exists. If a needed specification is absent, create or update the specification first and ask for user approval when product policy is unresolved.

For new Technical features, update in this order:

1. Specification
2. Architecture map and consumer contract
3. Implementation
4. Tests and validation commands
5. Stale-reference scans

Before implementation, identify explicitly:

- normative policy owner
- passive capability module
- orchestration owner
- adapter or deployment hook
- runtime-state owner
- durable-state owner
- stateless shared-helper opportunities
- consumer contract
- tests and validation commands

Do not extract a helper merely because code can be deduplicated. Extract only when ownership and reuse are clear.

> After implementation, update Alignment Notes and relevant Architecture sections in the specification file, then revisit the specification to confirm the code still aligns with intended behavior.

For Technical refactors, classify legacy behavior before editing:

- relocate: valid capability owned by a defined module
- remove: hidden policy, duplicate behavior, or obsolete behavior
- flag: useful behavior with a defined future owner but no implementation yet
- report: necessary behavior with no defined architectural home

Before deleting or replacing a path, identify the product signal it provided and preserve the requirement in strategy docs if implementation is deferred.

## Completion Gate

Before claiming completion:

1. Run `git status --short`.
2. Preserve unrelated working-tree edits.
3. Inspect the diff before editing any file already touched by the user.
4. Run focused tests or checks where applicable.
5. Run the full relevant suite when the blast radius is broad.
6. Compile or lint relevant languages where applicable.
7. Validate shell syntax when scripts change.
8. Run `git diff --check`.
9. Scan for stale references after renames, moves, or structural changes.
10. Report checks that could not run.

## Skill Boundaries

Do not add `agents/openai.yaml` unless explicitly requested.

Do not enforce Business, Operational, or Marketing and Sales spec-code architecture workflows yet. Keep their structure clean, measurable, and reusable, but treat strict submodule implementation governance as future work unless the user asks to expand it.
