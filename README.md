# EngineeringOS Manifesto

> The founding architecture and doctrine for semantic engineering infrastructure.

EngineeringOS is a proposal for a new layer of engineering infrastructure: an open semantic foundation where engineering intent is represented as language, ontology, intermediate representation, and compiler logic rather than as isolated CAD or schematic files. In this model, existing tools such as EPLAN, KiCad, QElectroTech, OpenSCAD, FreeCAD, PDF, SVG, MES, and ERP systems become targets and integrations, not the source of truth. The purpose of this repository is to define that architecture clearly enough that it can become a long-lived open standard rather than a vague product idea.

## What EngineeringOS Is

EngineeringOS is an architecture for treating engineering intent as a durable semantic system rather than as a collection of application-specific files. It proposes a shared layer made of engineering language, ontology, intermediate representation, compiler logic, and rules that can generate or synchronize many downstream formats, views, and tool integrations.

## The Core Thesis

The central claim of EngineeringOS is that the source of truth in engineering should move from drawings to semantics. Schematics, layouts, reports, exports, and enterprise records remain necessary, but they become compiled projections of a deeper model that captures devices, functions, relationships, constraints, and standards in a form that both humans and machines can reason about.

## Why Now

The file-centric model of engineering software is increasingly brittle in a world of automation, cross-tool workflows, and machine-assisted reasoning. AI makes the limits of drawing-first systems more visible, while modern language tooling, graph-based representations, open-source infrastructure, and standards work make it realistic to define a shared semantic layer that did not previously exist.

## What EngineeringOS Is Not

EngineeringOS is not a replacement campaign against every existing engineering tool. It is not a wrapper around one vendor format, a drawing editor with new branding, or an automation layer that removes engineering judgment. It is also not a conventional product README; it is the public entry point to a doctrine about how engineering systems should be structured.

## Repository Structure

- `docs/` contains the manifesto chapters and foundational architecture narrative.
- `docs/architecture/` contains the core system design layers.
- `docs/technologies/` records the third-party platforms, standards references, and reuse boundaries the draft depends on.
- `docs/prd/` holds product-facing documents that emerge from the doctrine, not the other way around.
- `docs/rfc/` is the place for durable technical decisions and evolving formal specifications.
- `docs/references/` collects standards, ecosystem context, and supporting material.
- `examples/` is reserved for illustrative cases, patterns, and sample artifacts.
- `assets/` contains diagrams and shared visual material for the written corpus.

## Recommended Reading Order

1. `README.md`
2. `docs/00-vision.md`
3. The doctrine and architecture chapters in `docs/`
4. The leverage and methods layer in `docs/technologies/`
5. `docs/prd/`, `docs/rfc/`, and `docs/references/` as the architecture becomes more formal

## Status

This repository is the first edition of the EngineeringOS manifesto. Its current purpose is to establish the doctrine, vocabulary, and architectural direction of the project before the more detailed RFC and implementation layers are expanded.
