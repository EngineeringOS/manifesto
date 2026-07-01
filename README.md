# EngineeringOS Manifesto

> Build the open semantic infrastructure for engineering.

Engineering is about to undergo its biggest architectural shift since CAD replaced paper. The next era of engineering software will not be organized around drawings first, file formats first, or vendor applications first. It will be organized around explicit engineering meaning.

**Engineering software is still drawing-centric. AI requires semantic engineering.**

That is the problem. Everything in this repository exists to respond to it.

## The Shift

```text
Paper Era
        ->
CAD Era
        ->
Semantic Engineering Era
```

For decades, engineering software has treated the drawing or project file as the practical source of truth. That model was good enough when the primary task was document production. It is no longer good enough for machine reasoning, cross-tool continuity, reusable engineering knowledge, or trustworthy AI.

The next shift is from representation to meaning.

```text
Drawing
        ->
Model
        ->
Meaning
```

## What EngineeringOS Is

**EngineeringOS is an open semantic engineering platform that separates engineering intent from engineering representation.**

Its role is to define a shared layer of `Engineering Language`, `Engineering IR`, compiler logic, ontology, rules, and governed knowledge so that engineering meaning can survive outside any one CAD, schematic, or enterprise tool.

```text
Natural Language
        ->
Engineering Language
        ->
Engineering IR
        ->
Compiler
        ->
EPLAN / KiCad / QElectroTech / OpenSCAD / FreeCAD
```

In this model, downstream tools remain important, but they stop being the deepest source of truth. They become renderers, compatibility targets, and integration surfaces around a more durable semantic core.

## What EngineeringOS Is Not

EngineeringOS is **not**:

- another CAD
- another EPLAN clone
- another electrical editor
- another AI wrapper

EngineeringOS **is**:

- an Engineering Language
- an Engineering Compiler
- an Engineering Knowledge Platform
- an open semantic infrastructure

## Core Principles

1. Semantics before drawings.
2. Open standards before vendor lock-in.
3. AI augments engineering judgment, not replaces it.
4. Never reinvent solved problems.
5. Own the semantic layer.
6. Everything is pluggable.
7. Every engineering decision should be traceable.
8. Human-readable, machine-executable.

## Leverage, Don't Replace

EngineeringOS is differentiated not by trying to replace every existing engineering tool, but by standing on top of the strongest ecosystems that already exist.

- Geometry: `OCCT`
- PCB: `KiCad`
- Electrical: `QElectroTech`
- Mechanical: `FreeCAD`
- Visualization: `OpenUSD`
- Compiler method: `LLVM` philosophy

This is a pragmatic architecture, not a purity project. The goal is not to rebuild the whole stack. The goal is to own the missing semantic layer that can coordinate it.

## Why This Matters

If engineering meaning can be represented semantically, then rules, standards mappings, ontology packs, templates, validation logic, and domain workflows can become reusable public infrastructure. Engineering knowledge no longer has to die inside isolated projects, PDFs, or proprietary toolchains. It can be versioned, shared, audited, improved, and reused at global scale.

That is why EngineeringOS has the potential to become more than a product. It can become the open infrastructure layer on which future engineering systems are built.

## Repository Structure

- `docs/` contains the manifesto chapters and doctrine.
- `docs/architecture/` contains the core system design layers.
- `docs/technologies/` contains reuse strategy and technology decisions.
- `docs/prd/` contains product-facing documents.
- `docs/rfc/` contains evolving technical proposals.
- `docs/references/` contains standards, research, and ecosystem references.

## Recommended Reading Order

1. `README.md`
2. `docs/00-vision.md`
3. The doctrine and architecture chapters in `docs/`
4. The leverage and methods layer in `docs/technologies/`
5. `docs/prd/`, `docs/rfc/`, and `docs/references/`

## Call To Action

**Help build the open semantic infrastructure for engineering.**
