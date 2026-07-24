# SWARM Agent Architecture

A reusable architecture for building human-directed recursive AI agents.

## Status

This repository is currently in its earliest stage.

It is intentionally documentation-first. The architecture will be extracted from
Grant Scout rather than invented from scratch.

Current status:

- Early foundation under extraction.
- Validated by one implementation: Grant Scout v0.1.0.
- Additional implementations will refine the architecture over time.

## Purpose

This repository captures the reusable foundation shared by all SWARM-style
agents.

It is not another agent. It is the architecture that future agents can build on
without reinventing the same structure, contracts, workflows, and governance
model each time.

Grant Scout v0.1.0 is the first reference implementation. The purpose of this
repository is to extract what Grant Scout proves to be reusable, then make that
foundation available to future agents in a clear, durable, implementation-ready
form.

The reusable foundation may include:

- Architecture
- Runtime orchestration
- Contracts
- Governance
- Validators
- Artifact model
- Headless workflows
- Adaptation model
- Documentation conventions

The repository should answer questions such as:

- What makes an agent a SWARM agent?
- What responsibilities belong in the shared architecture?
- What responsibilities belong in a domain-specific implementation?
- How should agents preserve human authority while using recursive AI systems?
- How should artifacts, decisions, validations, and adaptations be represented?
- How can future agents reuse proven structure without copying Grant Scout
  directly?

The goal is not to generalize prematurely. The goal is to identify the parts of
working agents that are stable enough to become shared infrastructure.

Domain-specific logic belongs in individual agent repositories. A grant agent, a
hockey agent, a research agent, and a planning agent may share architecture, but
they should not share business rules, prompts, data, or assumptions that only
make sense in one domain.

## Design Philosophy

Human judgment remains authoritative.

AI proposes. Humans decide.

The architecture should help layers contribute to a shared result rather than
overwrite each other. Each layer should add perspective, constraints, review, or
adaptation while preserving traceability.

Durable artifacts matter more than transient conversations. A useful agent
should produce outputs that can be reviewed, tested, revised, archived, and used
outside the chat where they were created.

Architecture should emerge from working systems. Patterns should be extracted
only after they prove reusable in practice.

## Relationship to Other Projects

```text
Creative Operating System
          │
          ▼
SWARM Protocol
          │
          ▼
SWARM Agent Architecture
          │
          ▼
Grant Scout v0.1.0
(first reference implementation)
          │
          ▼
SWARM Agent
(extracted foundation)
          │
          ▼
Future Agents
```

The Creative Operating System is the broader operating model for human-directed
creative and analytical work.

The SWARM Protocol defines the general recursive collaboration pattern used by
human-directed AI systems.

The SWARM Agent Architecture is the reusable structure being extracted from
working agents that implement the SWARM Protocol.

Grant Scout v0.1.0 is the first reference implementation that proved the
architecture in a real domain.

SWARM Agent is this repository: the extracted foundation separated from Grant
Scout's domain-specific behavior.

Future Agents will build from the extracted architecture, then validate,
challenge, and simplify it beyond its first implementation.

## Repository Scope

This repository is expected to become the canonical reference for the shared
architecture used by SWARM agents. Its scope is architectural rather than
domain-specific: structures, boundaries, contracts, workflows, and conventions
that can be reused across agents.

The repository may eventually contain reusable definitions for:

- Agent responsibilities
- Layer responsibilities
- Artifact boundaries
- Human review points
- Runtime coordination
- Validation expectations
- Adaptation patterns
- Documentation standards
- Implementation contracts
- Reference workflows

Those pieces should be added only when they have been extracted from working
implementations or are required to explain the architecture clearly. The
repository should remain careful about what it claims: patterns validated only
by Grant Scout should be described as extracted from Grant Scout, while patterns
validated across multiple agents can become part of the broader architecture.

## What Belongs Here

The shared architecture belongs here: concepts and reusable components expected
to apply across multiple SWARM agents, such as:

- The conceptual model for human-directed recursive agents
- Layering conventions
- Runtime orchestration patterns
- Shared contracts between layers
- Governance and review expectations
- Validator roles and responsibilities
- Artifact lifecycle conventions
- Headless workflow patterns
- Adaptation and refinement models
- Documentation conventions
- Criteria for extracting reusable patterns

The repository should help future builders distinguish stable architecture,
provisional patterns, and ideas that still need validation.

## What Does Not Belong Here

Domain-specific implementation details do not belong here.

Examples include:

- Grant-specific logic
- Hockey logic
- Project-specific prompts
- Application data
- Sample opportunities
- Business rules unique to one agent
- Domain scoring rules
- Domain-specific intake forms
- Domain-specific reporting language
- Agent-specific configuration
- Reference data for a single implementation

Those remain inside agent repositories.

An agent repository may depend on the SWARM Agent Architecture, conform to it,
or provide evidence that changes it. It should not move its domain assumptions
into this repository merely because they are useful to one implementation.

## Extraction Model

Extraction means identifying structures that are already useful in a working
agent, separating them from grant-specific behavior, and documenting them in a
form future agents can reuse.

The extraction process should preserve the distinction between:

- Proven architecture
- Reference implementation behavior
- Experimental patterns
- Domain-specific logic

Grant Scout should remain understandable as an implementation. SWARM Agent
should become understandable as the architecture.

## Reference Implementation

Grant Scout v0.1.0 is the first reference implementation. It demonstrates the
initial form of the architecture in a real domain with real constraints:

- Human-directed work
- Recursive AI contribution
- Structured artifacts
- Review and validation
- Domain adaptation
- Headless workflows
- Documentation discipline

Grant Scout is not the architecture itself. Future implementations should reuse
the architectural patterns Grant Scout proves useful while replacing the
grant-specific model with their own domain model.

## Roadmap

- Phase 1: Extract architecture from Grant Scout.
- Phase 2: Separate reusable runtime.
- Phase 3: Separate contracts.
- Phase 4: Separate validators.
- Phase 5: Integrate the SWARM Design System.
- Phase 6: Validate with multiple agent implementations.

## Initial Extraction Checklist

### Repository Foundation
- [x] Create repository
- [x] Define repository purpose and scope
- [ ] Initialize Git repository
- [ ] Connect GitHub remote
- [ ] Create AGENTS.md
- [ ] Add LICENSE
- [ ] Add CONTRIBUTING.md
- [ ] Define release/versioning strategy

### Canon
- [ ] Create architecture canon
- [ ] Define canonical terminology
- [ ] Record architectural governance principles
- [ ] Identify stable architectural vocabulary
- [ ] Separate canonical architecture from implementation guidance

### Architecture Documentation
- [ ] Document the six-layer architecture
- [ ] Document responsibilities of each layer
- [ ] Document layer boundaries
- [ ] Document "Layers contribute rather than rewrite"
- [ ] Document human authority model
- [ ] Define architecture vs template vs implementation
- [ ] Identify proven vs provisional patterns

### Grant Scout Extraction Audit
- [ ] Inventory reusable architecture
- [ ] Identify grant-specific concepts
- [ ] Identify reusable runtime pieces
- [ ] Identify reusable contracts
- [ ] Identify reusable validators
- [ ] Identify naming requiring generalization
- [ ] Record patterns that should NOT yet be extracted

### Skills
- [ ] Inventory reusable Codex skills
- [ ] Separate architecture skills from domain skills
- [ ] Define the minimum required skills for every SWARM agent
- [ ] Create architecture-level validation skills
- [ ] Identify skills that remain implementation-specific

### Runtime Foundation
- [ ] Document runtime lifecycle
- [ ] Define runtime states
- [ ] Define runtime orchestration
- [ ] Define headless workflow lifecycle
- [ ] Define runtime validation
- [ ] Document recovery behavior

### Contracts & Artifacts
- [ ] Define generic artifact model
- [ ] Define artifact identity
- [ ] Define provenance rules
- [ ] Define append-only behavior
- [ ] Define mutable artifacts
- [ ] Define cross-layer references
- [ ] Define extension strategy for domain schemas

### Adaptation
- [ ] Document proposal vs application
- [ ] Document human approval
- [ ] Document receiving-layer translators
- [ ] Document future-run adaptation behavior
- [ ] Preserve adaptation traceability

### Validators
- [ ] Separate structural validators from domain validators
- [ ] Define minimum validator set
- [ ] Document runtime validation
- [ ] Document architecture validation
- [ ] Create unified validation workflow

### Agent Template
- [ ] Create minimal repository structure
- [ ] Create placeholder layer interfaces
- [ ] Create generic CLI
- [ ] Create documentation templates
- [ ] Validate against a second implementation

### SWARM Design System
- [ ] Create SWARM Design System repository
- [ ] Define relationship between architecture and design system
- [ ] Delay UI extraction until design system exists
- [ ] Identify architecture-level UI states
- [ ] Apply the design system to the template after it exists

### Cross-Domain Validation
- [ ] Build Agent #2
- [ ] Record architectural friction
- [ ] Simplify architecture
- [ ] Promote only cross-domain patterns to canonical

## Documentation-First Foundation

This repository begins with documentation because the first task is to define
scope before machinery. Documentation should make the architecture legible to
engineers and designers by clarifying intent, boundaries, responsibilities, and
vocabulary without pretending that every implementation detail is settled.

## Engineering Expectations

The architecture should be practical. It should help teams build agents that can
be inspected, tested, adapted, and maintained without requiring unnecessary
complexity.

Reusable pieces should have clear boundaries. Contracts should describe
responsibilities without leaking domain assumptions, and validators should
protect quality without encoding one agent's business rules. The architecture
should grow only when multiple implementations need the same structure.

## Design Expectations

The architecture should support human understanding. Designers should be able to
see where human judgment enters the system, where AI contribution is allowed,
where artifacts become durable, and where review happens.

The system should make decisions visible, preserve useful context, and help
humans direct the agent rather than merely observe it.

## Governance

Governance is part of the architecture, not an afterthought. SWARM agents should
make clear:

- Who has authority
- Where decisions are made
- What AI is allowed to propose
- What requires human approval
- What artifacts must be preserved
- What validations must pass
- What can be adapted over time

The shared architecture should define reusable governance expectations while
leaving domain-specific policies to the agents that need them.

## Artifacts, Validation, and Adaptation

Artifacts are the durable outputs of SWARM agents. They may include plans,
reports, evaluations, structured records, decisions, validation results, or
other domain-specific deliverables. The shared architecture should define how
artifacts are treated as durable, reviewable objects; agent repositories should
define the specific artifact types their domains require.

Validation should help protect trust. The shared architecture should define
where validation belongs, how validators relate to artifacts, and how validation
results influence the workflow. Domain validators belong in the agent
repositories that own those domains.

SWARM agents should improve through use without hiding the fact that they are
changing. Adaptation should remain visible, reviewable, and governed by human
judgment, with domain-specific adaptation rules kept inside the relevant agent
repositories.

## Headless Workflows

SWARM agents should be usable beyond an interactive chat surface. Headless
workflows should preserve human authority, artifact durability, review points,
and validation; headless execution should not mean invisible decision-making.

## Documentation Conventions

Documentation should be treated as part of the system. The architecture should
help future agents stay understandable through:

- Clear scope boundaries
- Explicit responsibilities
- Stable vocabulary
- Separation between architecture and implementation
- Notes on validation status
- Traceability from reference implementations

Documentation should explain what is known, what is provisional, and what still
needs evidence.

## Guiding Principle

The architecture is not designed in isolation.

It is extracted from successful implementations.

Every new agent should simplify the architecture rather than complicate it.

Every abstraction in this repository should exist because at least one working
implementation proved it valuable. Every canonical abstraction should eventually
be validated by more than one implementation before it becomes part of the
long-term architecture.
