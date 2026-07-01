# EngineeringOS Manifesto Design

Date: 2026-07-01
Repo: `engineeringos-manifesto`
Status: Approved design baseline

## Purpose

This document captures the approved design for a docs-only repository that defines the founding doctrine, architecture, and execution path of EngineeringOS. The repository is not the future codebase. It is the canonical manifesto and handbook from which later code, RFCs, and implementation plans can be derived.

The goal of this design is to convert the current `draft/` conversation artifacts into a coherent manifesto repository with a stable structure, stable vocabulary, and a minimum publishable first edition.

## Repository Role

The repository is a manifesto repository, not a product repository and not a monorepo. Its job is to define:

- the public thesis of EngineeringOS
- the architectural doctrine of the platform
- the strategic boundary of what the platform owns and what it reuses
- the first implementation slice that proves the thesis
- the future governance mechanism for changes

The repository should read like a handbook first, evolve like an RFC repository second, and support implementation through PRDs third.

## Repository Structure

The approved structure is:

```text
engineeringos-manifesto/
|-- README.md
|-- LICENSE
|-- ROADMAP.md
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- book.toml
|-- SUMMARY.md
|-- docs/
|   |-- 00-preface.md
|   |-- 01-vision.md
|   |-- 02-industry-analysis.md
|   |-- 03-platform-shift.md
|   |-- 04-design-principles.md
|   |-- 05-open-source-strategy.md
|   |-- 06-ecosystem-analysis.md
|   |-- 07-business-strategy.md
|   |-- 08-foundation-governance.md
|   |-- 09-roadmap.md
|   |-- architecture/
|   |   |-- 10-overall-architecture.md
|   |   |-- 11-language.md
|   |   |-- 12-ontology.md
|   |   |-- 13-ir.md
|   |   |-- 14-graph.md
|   |   |-- 15-compiler.md
|   |   |-- 16-plugin.md
|   |   |-- 17-ai.md
|   |   |-- 18-studio.md
|   |   `-- 19-cloud.md
|   `-- technologies/
|-- rfcs/
|-- prd/
|-- references/
|-- examples/
`-- assets/
```

## Document Classes

The repository is organized around distinct document classes:

- `README.md`: the shortest public statement of the manifesto
- `docs/`: the stable handbook
- `rfcs/`: proposals and change-control documents
- `prd/`: execution-facing product requirements for implementation slices
- `references/`: factual source-oriented material
- `examples/`: compact artifacts that make the architecture concrete

These classes should not be collapsed into one another. Handbook chapters define doctrine. RFCs define proposed or ratified changes. PRDs define build slices. References stay factual. Examples stay minimal.

## Core Thesis

EngineeringOS is an open semantic engineering platform in which the source of truth shifts from drawings and siloed project files to a semantic pipeline:

```text
Natural Language
-> Engineering Language
-> Engineering Ontology
-> Engineering IR
-> Engineering Compiler
-> Renderers / Integrations / Targets
```

In this model, existing tools such as EPLAN, KiCad, QElectroTech, OpenSCAD, FreeCAD, PDF, SVG, MES, and ERP systems become downstream targets, integrations, or projections. EngineeringOS is therefore not an open-source EPLAN clone and not a CAD replacement strategy. It is a semantic layer strategy.

## Approved Design Principles

The approved principles are:

- semantic-first
- compiler-first
- plugin-first
- open-standards-first
- borrow solved infrastructure
- human-governed knowledge

These principles are intended to remain stable even as implementation technologies evolve.

## Open Source Boundary

The approved boundary is:

EngineeringOS must own:

- Engineering Language
- Engineering Ontology
- Engineering IR
- Engineering Compiler
- rule and validation logic
- knowledge compiler concepts
- plugin boundaries for the semantic core

EngineeringOS should reuse:

- geometry kernels such as OCCT
- electrical and PCB ecosystem assets where useful
- parser, editor, rendering, and storage infrastructure
- existing open-source tools as targets or integration layers

The strategic rule is: never rebuild solved problems when the real missing layer is semantic coordination.

## First Edition Scope

The minimum serious first edition of the manifesto consists of these files:

1. `README.md`
2. `docs/00-preface.md`
3. `docs/01-vision.md`
4. `docs/03-platform-shift.md`
5. `docs/04-design-principles.md`
6. `docs/05-open-source-strategy.md`
7. `docs/architecture/10-overall-architecture.md`
8. `docs/architecture/12-ontology.md`
9. `docs/architecture/13-ir.md`
10. `docs/architecture/15-compiler.md`
11. `docs/architecture/17-ai.md`
12. `docs/09-roadmap.md`
13. `prd/00-kernel-v0.md`

This set is sufficient to publish a coherent first edition without forcing the entire long-term document tree to be complete.

## Draft Conversion Strategy

The current `draft/` directory should not be preserved 1:1. The approved migration method is merge-and-split.

Source priority:

1. `EngineeringOS_Founding_Architecture_v0.1.md`
2. `0008.md`
3. `0009.md`
4. `0002.md`
5. `0006.md`
6. `0007.md`
7. `0005.md`
8. `0004.md`
9. `0003.md`
10. `0010.md`
11. `0001.md`

Rules:

- choose one spine draft per target file
- pull only missing arguments from supporting drafts
- rewrite into one declarative voice
- remove Q&A framing entirely
- remove repeated analogies and repeated claims
- keep each target file single-purpose

## Chapter Order

The approved handbook order is:

1. Preface
2. Vision
3. Industry Analysis
4. Platform Shift
5. Design Principles
6. Open Source Strategy
7. Ecosystem Analysis
8. Business Strategy
9. Foundation Governance
10. Roadmap
11. Overall Architecture
12. Language
13. Ontology
14. Engineering IR
15. Graph
16. Compiler
17. Plugin
18. AI
19. Studio
20. Cloud

The initial production sequence is narrower and optimized for the first edition only.

## Production Sequence

The approved writing order for the first edition is:

1. `README.md`
2. `docs/00-preface.md`
3. `docs/01-vision.md`
4. `docs/03-platform-shift.md`
5. `docs/04-design-principles.md`
6. `docs/05-open-source-strategy.md`
7. `docs/architecture/10-overall-architecture.md`
8. `docs/architecture/12-ontology.md`
9. `docs/architecture/13-ir.md`
10. `docs/architecture/15-compiler.md`
11. `docs/architecture/17-ai.md`
12. `docs/09-roadmap.md`
13. `prd/00-kernel-v0.md`

## File Templates

The first edition files use a consistent structure:

- thesis paragraph
- 4 to 6 focused sections
- short closing paragraph that points to the next unresolved layer

Each document should read like a chapter, not like stitched chat logs.

## Canonical Vocabulary

The following terms are approved as canonical and should be used consistently:

- Engineering Language
- Engineering Ontology
- Engineering IR
- Semantic Core
- Engineering Compiler
- Knowledge Compiler
- Renderer
- Plugin
- Standards Mapping
- Human Review Loop

Avoid reframing the project as:

- AI CAD
- Open EPLAN
- converter platform
- drawing generator

## Quality Gates

A chapter is complete only when:

- it has one clear thesis
- section order is coherent
- vocabulary is consistent with the manifesto
- it belongs clearly to the correct document class
- conversational repetition from the drafts is removed
- it ends with a clean boundary paragraph

The first edition is complete when:

- all 13 first-edition files exist
- the files read cleanly in order
- the semantic core is understandable from the handbook alone
- `prd/00-kernel-v0.md` provides a believable first implementation slice

## Boundary

This design document defines the repository, structure, migration strategy, and first-edition production path. It does not itself author the final manifesto chapters. Those chapters are the next step.

Implementation planning for the first edition is complete. The next stage is direct chapter production following the approved first-edition sequence and consistency gates.
