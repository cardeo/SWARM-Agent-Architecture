# AGENTS.md

Governance for AI contributors to the SWARM Agent Architecture repository.

## Repository Mission

This repository defines the reusable architecture for SWARM agents.

It is documentation-first. Architectural work should begin by clarifying intent,
scope, vocabulary, boundaries, and evidence before adding machinery.

The architecture is extracted from successful implementations rather than
invented in isolation.

Its purpose is to preserve the smallest reusable foundation for
human-directed recursive AI agents.

This repository is not an agent implementation. It is the shared architectural
reference that future agents may use, test, challenge, and refine.

## Core Principles

Human judgment remains authoritative.

AI proposes.

Humans decide.

Layers contribute rather than rewrite.

Durable artifacts matter more than transient conversations.

Prefer reduction over expansion.

Extract patterns only after they prove reusable.

Canonical architecture requires validation across multiple implementations.

SWARM is the protocol moving work through the architecture, not a seventh
runtime layer.

Entity Surface is an architectural human-review pattern, not universal UI
doctrine.

## Repository Scope

The following belong in this repository:

- Architecture
- Runtime concepts
- Governance
- Contracts
- Validators
- Documentation
- Reusable patterns
- Architectural vocabulary

The following do not belong in this repository:

- Domain logic
- Business rules
- Project-specific prompts
- Sample data
- Implementation-specific code
- Application configuration
- Experimental ideas that have not yet been validated

If a concept only applies to one implementation, it should remain in that
implementation until proven reusable.

## Contribution Rules

Before introducing a new abstraction, contributors should ask:

Has this already been demonstrated in a working implementation?

If not, do not extract it.

Leave the concept inside the implementation until additional evidence exists.

Avoid speculative architecture.

Prefer documenting observed structure over designing theoretical structure.

When a contribution changes the architectural surface area, it should also make
the reason for that change clear.

## Documentation Expectations

Documentation is treated as architecture.

Whenever architectural decisions change:

- Update documentation
- Keep terminology consistent
- Avoid undocumented architectural drift
- Distinguish canonical patterns from provisional ones

Documentation should explain:

- What is proven
- What is provisional
- What still requires validation

Use consistent names for shared concepts. Do not introduce synonyms unless they
clarify a real distinction.

When a pattern is extracted from a reference implementation, name the evidence
for extraction and preserve the boundary between shared architecture and
implementation behavior.

## Decision Framework

When multiple solutions are possible, prefer the one that:

- Reduces complexity
- Improves clarity
- Increases reuse
- Preserves human authority
- Minimizes architectural surface area

Avoid adding abstractions solely for flexibility.

Every abstraction should solve a demonstrated problem.

Prefer small, stable concepts that can survive across domains over broad
concepts that only seem reusable in theory.

## Extraction Philosophy

The architecture is extracted from working implementations.

Grant Scout is currently the primary private reference implementation.

Future implementations should refine, challenge, or simplify the architecture.

They may change provisional guidance, but should not casually overwrite
established architectural law.

Architecture should evolve through evidence rather than speculation.

Extraction should separate reusable structure from domain-specific behavior
without erasing the history of where that structure was proven.

Provisional patterns may be documented, but they should not be presented as
canonical until they have stronger evidence.

## North Star

Every abstraction should exist because a working implementation proved it
valuable.

Every canonical abstraction should eventually be validated by more than one
implementation before becoming part of the long-term architecture.

Simplicity, clarity, and human-directed judgment define the SWARM Agent
Architecture.
