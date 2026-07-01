# Preface

This repository exists because the idea it describes is too large, too foundational, and too consequential to live as a single manifesto essay or a scattered set of product notes. EngineeringOS is not being framed here as a feature, an app, or even a conventional startup plan, but as the founding doctrine for an open semantic engineering platform. The role of this preface is to explain how this repository should be read, how its documents relate to one another, and why a handbook-plus-RFC structure is necessary from the beginning.

## Why This Manifesto Exists

EngineeringOS addresses a structural gap in modern engineering software: the absence of an open semantic layer that can stand above individual tools, file formats, and drawing environments. That argument cannot be carried by a short pitch, because the claim is architectural rather than promotional. It requires explicit doctrine about source of truth, system boundaries, standards, compilers, knowledge, and the role of existing software ecosystems.

This manifesto therefore exists to define first principles before implementation details multiply. It establishes the vocabulary that later specifications, RFCs, examples, and products must inherit. Without that doctrinal base, the project would drift into feature accumulation or collapse back into the assumptions of the toolchain it is trying to transcend.

## What Problem This Repository Solves

Before there is a coherent repository, ideas of this kind tend to fragment. One part lives in visionary essays, another in technical notes, another in product documents, and another in ad hoc conversations about specific tools. The result is ambiguity about what is being built, what layer matters most, and what should remain outside scope.

This repository solves that fragmentation by giving EngineeringOS a stable public architecture. It provides a single place where the mission, model, principles, terminology, and document hierarchy can be read in sequence. That shared structure is necessary if contributors are expected to build toward an open standard rather than toward disconnected experiments.

## How To Read This Repository

The repository should be read from doctrine toward specification. The README is the public entry layer. The opening chapters in `docs/` explain the vision, platform shift, principles, and strategic posture. RFCs should eventually formalize the parts of the architecture that require precision, while references and examples support understanding without replacing the core argument.

This reading order matters. EngineeringOS should not be interpreted as a collection of integrations, a user interface plan, or a tooling wishlist. It should be understood first as a semantic and compiler-centered architecture, then as a repository of specifications that derive from that architecture, and only after that as a basis for concrete software systems.

## Document Types

This repository uses different document types for different levels of permanence and precision.

- Manifesto chapters establish doctrine, framing, and the durable architectural thesis.
- RFCs are for formal technical proposals that need stable interfaces, terminology, or decision records.
- PRDs describe product-facing slices that may be built on top of the doctrine once the architecture is clear.
- References collect standards, ecosystem research, and source material that inform the architecture without defining it.
- Examples demonstrate how the semantic model and surrounding ideas may be expressed in practice.

## Scope And Boundaries

The scope of this repository is the semantic foundation of EngineeringOS: the ideas, principles, and architectural structures needed to define an open engineering language, ontology, intermediate representation, compiler model, rule system, and integration surface. It also includes the public rationale for why those layers should exist as shared infrastructure rather than as proprietary product internals.

Its boundaries are equally important. This repository is not intended to be a complete implementation guide, a substitute for detailed standards mapping, or a collection of vendor-specific operational manuals. It does not attempt to settle every future product decision in advance. Its job is to make the foundational architecture legible enough that later work can be rigorous, compatible, and cumulative.
