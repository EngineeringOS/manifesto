# Design Principles

EngineeringOS should be guided by a small number of principles that remain stable even as its implementation evolves. These principles exist to prevent the project from collapsing into familiar but weaker patterns: another monolithic CAD, another file converter, another AI wrapper over legacy tools, or another technically elegant system detached from real engineering practice. What follows is the design constitution of the platform: the core rules that shape architecture, governance, and scope.

## Semantic-First

EngineeringOS must treat the semantic model as the source of truth. Every device, function, relationship, constraint, and behavior that matters to engineering should exist explicitly in that model before it is expressed in drawings, reports, or external files. If a feature only works by making a drawing authoritative again, it violates the architecture.

Semantic-first also means that interoperability is defined at the level of meaning, not merely at the level of syntax. The platform should preserve intent across tools and domains instead of moving opaque files from one application to another. Drawings remain essential outputs, but they are downstream artifacts, not the canonical record.

## Compiler-First

EngineeringOS should be a compiler-first system. Its core responsibility is to transform a semantic representation into validated outputs, derived views, standards mappings, and compatibility targets through explicit passes. The center of the architecture is therefore the language, intermediate representation, rule engine, and compilation pipeline, not a stateful editor UI.

This principle prevents the project from becoming an application with hidden logic scattered across front-end interactions. Validation, numbering, cross-reference generation, standards checks, report generation, and export behavior should be traceable to compiler logic that can be tested, versioned, and reused across interfaces.

## Plugin-First

EngineeringOS should be plugin-first wherever variation is expected. Domains, renderers, importers, exporters, standards packs, rule sets, and AI-assisted workflows will evolve at different speeds and should not all be fused into one core. The platform should stay small at the center and extensible at the edges.

Plugin-first is also a governance rule. It allows the platform to support electrical, mechanical, hydraulic, robotics, or future engineering domains without freezing them into one premature ontology or one vendor-owned roadmap. Extension should be a first-class path, not an afterthought added after the architecture hardens.

## Open Standards First

EngineeringOS should prefer open standards whenever they can define an interface, exchange boundary, or domain reference. Where relevant standards already exist, the platform should map to them, learn from them, and remain legible to the ecosystems that depend on them. Closed internal structures should not become the default merely because they are faster to invent.

Open standards first does not mean every existing standard is sufficient as-is. It means the platform should align with the public language of engineering where possible and create new structures only where the gap is real. The burden of invention belongs on the missing semantic layer, not on problems that standards communities have already stabilized.

## Borrow Solved Infrastructure

EngineeringOS should borrow solved infrastructure aggressively. Geometry kernels, parser frameworks, editor protocols, storage engines, rendering stacks, symbol assets, and compatibility libraries should be reused when they already exist in mature form. The project should not spend its strategic energy rebuilding commodity subsystems in order to feel complete.

This principle creates discipline around scope. The platform should own what defines architectural leverage and reuse what the broader ecosystem already maintains well. Rebuilding solved infrastructure is not technical ambition. In this context, it is misallocated effort that delays the semantic layer the project actually exists to build.

## Human-Governed Knowledge

EngineeringOS should treat engineering knowledge as reviewable public infrastructure, not as an opaque side effect of prompts or model weights. Ontology changes, standards mappings, rule definitions, and knowledge assertions should be inspectable, versioned, and governed by humans with domain accountability. AI can assist in proposing, extracting, and organizing knowledge, but it cannot be the final authority over it.

This principle matters because the platform aims to carry real engineering intent. When the system explains why a rule exists, how a concept is defined, or how a standard is interpreted, that answer should resolve to governed artifacts rather than hidden heuristics. Human-governed knowledge is what keeps an AI-native platform from becoming an unreviewable one.
