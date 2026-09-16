# SWARM Agent Architecture

A reusable architecture for building human-directed recursive AI agents.

## Status

This repository is documentation-first.

It records the SWARM Agent Architecture as a public, versioned architectural
foundation. The architecture emerged through a real private reference
implementation, Grant Scout, and is published here so future agents can build on
the reusable structure without inheriting Grant Scout's domain logic.

Current status:

- v0.1 architecture statement.
- Validated through one private reference implementation: Grant Scout.
- Public reference implementations are intentionally deferred.
- Additional implementations will refine the architecture over time.

## What v0.1 Means

SWARM Agent Architecture v0.1 is the first public versioned statement of the
architecture validated through Grant Scout.

It records:

- Six-layer architecture
- SWARM recursive protocol
- Human authority model
- Architectural governance laws
- Governed Adaptation
- Runtime-mode distinction
- Entity Surface pattern
- Artifact and historical-evidence principles

It does not yet provide:

- Generic Agent Template
- Reusable runtime
- Public reference implementation
- SWARM Design System
- Mature reusable implementation tooling

v0.1 describes architecture maturity, not ecosystem maturity. It establishes a
durable public record of the architecture while leaving templates, runtimes,
design systems, and public agents for later validation.

## Purpose

This repository captures the reusable foundation shared by SWARM-style agents.

It is not another agent. It is not a framework, product, design system, or
autonomous-agent runtime. It is the architecture future agents can use without
reinventing the same responsibilities, contracts, workflows, and governance
rules.

A human-directed recursive agent is a system in which machine execution
repeatedly gathers, evaluates, organizes, remembers, and proposes while human
judgment remains responsible for consequential decisions and future-facing
change.

The purpose of this repository is to preserve the smallest reusable foundation
for that kind of system.

The reusable foundation may include:

- Architecture
- Runtime concepts
- Contracts
- Governance
- Validators
- Artifact model
- Headless workflows
- Adaptation model
- Entity Surface pattern
- Documentation conventions

Domain-specific logic belongs in individual agent repositories. A grant agent, a
hockey agent, a research agent, and a planning agent may share architecture, but
they should not share business rules, prompts, data, sample records, or
assumptions that only make sense in one domain.

## Architecture at a Glance

The SWARM Agent Architecture has six durable layers.

These layers define where responsibility, truth, artifacts, and evidence live.
They are architectural responsibilities, not UI screens, services, packages, or
execution steps.

### Identity

Current durable truth about who the system serves: goals, constraints,
preferences, context, and relevant signals.

### Discovery

Current external facts gathered without applying downstream judgment.

### Evaluation

Current reasoning applied to Discovery using Identity as context.

### Guidance

Explicit human judgment, correction, acceptance, rejection, prioritization, and
redirection.

### Memory

Historical evidence of what happened, what was decided, and what resulted.

### Adaptation

Evidence-backed proposals and governed application of changes that may improve
future runs.

## SWARM Protocol

SWARM is the recursive protocol that moves work through the architecture. It is
not a seventh layer.

The six layers define where durable responsibility, truth, and artifacts live.
SWARM describes recursive activity through them:

- Spot
- Weigh
- Arrange
- Refine
- Make

These terms describe the pattern of work, not a strict one-to-one mapping to the
architectural layers. A run may move through the same responsibility more than
once as new evidence, evaluation, guidance, memory, or adaptation changes the
state of the work.

## Core Architectural Laws

**Human judgment remains authoritative.**

AI proposes. Humans decide.

**Layers contribute. They do not rewrite.**

Later layers may reference earlier artifacts, but they should not silently
mutate historical reasoning, evidence, or decisions.

**Adaptation proposes. Humans decide.**

Adaptation may identify and propose changes, but those changes require explicit
human approval and governed application.

Supporting principles:

- Historical artifacts remain immutable.
- Current truth and historical evidence remain separate.
- Accepted and Applied are different states.
- Validation gates Applied state.
- Execution host is not architecture.
- Human judgment remains structural rather than incidental.

## Adaptation Lifecycle

Adaptation changes future behavior, not historical artifacts.

```text
Evidence
   |
   v
Proposal
   |
   v
Human decision
   |
   v
Approved / action required
   |
   v
Bounded application
   |
   v
Validation
   |
   v
Applied
   |
   v
Future run
```

Proposed is not Accepted.

Accepted is not Applied.

Approval authorizes a change. Application makes the change real. Applied should
only be reached after validation succeeds.

Adaptation application should be bounded, traceable, explicit, and owned by the
receiving layer. The architecture favors constrained translators or similarly
bounded mechanisms over universal self-modification.

## Runtime Modes

Execution host is not architecture.

The architecture currently recognizes two validated runtime modes.

### Headless Agent

AI execution occurs inside an AI coding or agent environment. A standalone
product runtime is not required.

Headless does not mean "CLI version of the interactive application." It means
the same architecture can operate without a dedicated user-facing app runtime.

### Interactive Agent

The agent is packaged as a user-facing application with its own runtime and
interaction surface.

Both runtime modes preserve the same architectural core:

- Six layers
- Artifacts
- Contracts
- Provenance
- Validators
- Persistence semantics
- Governance
- Human authority

## Entity Surfaces

Entity Surface is the reusable human-review pattern for SWARM agents.

```text
Entity List
   |
   v
Entity Selection
   |
   v
Focused Detail
   |
   v
Human Review
   |
   v
Explicit Human Action
   |
   v
Return to List
```

Entity Surfaces make recursive machine activity legible, reviewable,
actionable, and governable.

They are an interaction pattern, not a mandate that every screen or agent use
the same UI. Different agents may express Entity Surfaces differently while
preserving the same review logic.

## Relationship to Other Projects

```text
Creative Operating System
          |
          v
SWARM Protocol
          |
          v
SWARM Agent Architecture
          |
          v
Grant Scout
(private reference implementation)
          |
          v
SWARM Agent Architecture v0.1
(public architecture statement)
          |
          v
Future Agents
```

The Creative Operating System is the broader operating model for human-directed
creative and analytical work.

The SWARM Protocol defines the recursive collaboration pattern used by
human-directed AI systems.

The SWARM Agent Architecture defines the reusable six-layer architecture through
which SWARM work becomes durable, reviewable, and governable.

Grant Scout was the private reference implementation through which the SWARM
Agent Architecture was first validated. It proved the six-layer architecture,
recursive SWARM protocol, governed Adaptation workflow, artifact contracts,
validators, and Entity Surface pattern in a working domain agent.

Grant Scout itself is not included in this repository and is not required to use
the public architecture. Public reference implementations may be added
separately as new agents are built.

Future Agents will build from the extracted architecture, then validate,
challenge, and simplify it beyond its first implementation.

## Repository Scope

This repository is expected to become the canonical reference for the shared
architecture used by SWARM agents. Its scope is architectural rather than
domain-specific: responsibilities, boundaries, contracts, workflows, governance
laws, and vocabulary that can be reused across agents.

What belongs here:

- Conceptual model for human-directed recursive agents
- Layer responsibilities
- SWARM protocol vocabulary
- Artifact boundaries
- Human review points
- Runtime-mode principles
- Validation expectations
- Adaptation governance
- Entity Surface pattern
- Documentation standards
- Criteria for extracting reusable patterns

What does not belong here:

- Domain logic
- Business rules unique to one agent
- Project-specific prompts
- Application data
- Sample opportunities
- Agent-specific configuration
- Generic Agent Template implementation
- Reusable runtime implementation
- SWARM Design System implementation
- Public demo agent solely for release optics

If a concept only applies to one implementation, it should remain in that
implementation until proven reusable.

## Architecture, Protocol, Implementation

Architecture defines durable responsibilities and boundaries.

Protocol defines recursive movement through those responsibilities.

Implementation expresses the architecture in a specific runtime, domain, and
interaction model.

Template work should remain deferred until additional implementations validate
which structures are truly reusable. The SWARM Design System is a separate
project and dependency; it should not be implemented inside this architecture
repository.

## Governance

Governance is part of the architecture, not an afterthought.

SWARM agents should make clear:

- Who has authority
- Where decisions are made
- What AI is allowed to propose
- What requires human approval
- What artifacts must be preserved
- What validations must pass
- What can be adapted over time

The shared architecture should define reusable governance expectations while
leaving domain-specific policies to the agents that need them.

## Artifacts, Validation, and Memory

Artifacts are durable outputs of SWARM agents. They may include plans, reports,
evaluations, structured records, decisions, validation results, or other
domain-specific deliverables.

Historical artifacts remain immutable. New truth belongs in current layer state,
new artifacts, explicit corrections, or governed Adaptation; it should not be
silently written back into historical evidence.

Validation protects trust. The shared architecture should define where
validation belongs, how validators relate to artifacts, and how validation
results influence the workflow. Domain validators belong in the agent
repositories that own those domains.

## Roadmap

- Record v0.1 as the first public versioned architecture statement.
- Identify and extract reusable runtime patterns as additional implementations
  provide evidence.
- Identify and extract reusable contract patterns as additional implementations
  provide evidence.
- Identify and extract reusable validator patterns as additional implementations
  provide evidence.
- Define the relationship between this architecture and the separate SWARM
  Design System.
- Defer the generic Agent Template until multiple implementations clarify what
  is truly reusable.
- Validate, challenge, and simplify the architecture through future public
  agent implementations.

## Initial Extraction Checklist

### Repository Foundation

- [x] Create repository
- [x] Initialize Git repository
- [x] Connect GitHub remote
- [x] Define repository purpose and scope
- [x] Create AGENTS.md
- [x] Add LICENSE
- [ ] Define release/versioning strategy

### Canon

- [ ] Create architecture canon
- [ ] Define canonical terminology
- [ ] Record architectural governance principles
- [ ] Identify stable architectural vocabulary
- [ ] Separate canonical architecture from implementation guidance

### Architecture Documentation

- [x] Document the six-layer architecture
- [x] Document "Layers contribute rather than rewrite"
- [x] Document human authority model
- [x] Define architecture vs protocol vs implementation
- [ ] Document detailed responsibilities of each layer
- [ ] Document layer boundaries
- [ ] Identify proven vs provisional patterns

### Grant Scout Extraction Audit

- [x] Identify Grant Scout as private reference implementation
- [x] Preserve Grant Scout's role without requiring source access
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

- [x] Define Headless and Interactive runtime modes
- [x] Document that execution host is not architecture
- [ ] Document runtime lifecycle
- [ ] Define runtime states
- [ ] Define runtime orchestration
- [ ] Define runtime validation
- [ ] Document recovery behavior

### Contracts & Artifacts

- [ ] Define generic artifact model
- [ ] Define artifact identity
- [ ] Define provenance rules
- [x] Define historical artifact immutability
- [ ] Define mutable current-layer state
- [ ] Define cross-layer references
- [ ] Define extension strategy for domain schemas

### Adaptation

- [x] Document proposal vs application
- [x] Document human approval
- [x] Document bounded, validated, traceable application
- [x] Document future-run adaptation behavior
- [x] Preserve adaptation traceability
- [ ] Document receiving-layer translators

### Validators

- [ ] Separate structural validators from domain validators
- [ ] Define minimum validator set
- [ ] Document runtime validation
- [ ] Document architecture validation
- [ ] Create unified validation workflow

### Entity Surfaces

- [x] Define Entity Surface as human-review pattern
- [ ] Document Entity Surface responsibilities
- [ ] Document implementation-neutral examples
- [ ] Validate Entity Surface across public implementations

### Agent Template

- [ ] Create minimal repository structure
- [ ] Create placeholder layer interfaces
- [ ] Create generic CLI
- [ ] Create documentation templates
- [ ] Validate against a second implementation

### SWARM Design System

- [ ] Create SWARM Design System repository
- [x] Define relationship between architecture and design system
- [x] Delay UI extraction until design system exists
- [ ] Identify architecture-level UI states
- [ ] Apply the design system to the template after it exists

### Cross-Domain Validation

- [ ] Build public Agent #2
- [ ] Record architectural friction
- [ ] Simplify architecture
- [ ] Promote only cross-domain patterns to canonical

## Documentation Conventions

Documentation is part of the architecture.

The repository should help future agents stay understandable through:

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
