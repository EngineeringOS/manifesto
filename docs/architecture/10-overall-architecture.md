# Overall Architecture

The architecture of EngineeringOS is built around a semantic core that sits between engineering intent and engineering outputs. Its role is to transform natural language, structured language, and standards-derived knowledge into a canonical representation that can be validated, compiled, extended, and rendered into many downstream targets. This chapter provides the end-to-end system model and names the major layers that all later architecture chapters refine.

## End-To-End Pipeline

EngineeringOS begins with a project-compilation path that accepts inputs expressing design intent rather than finished drawings. Those inputs include natural language prompts, authored `Engineering Language`, and imported structured data. The system lowers those project inputs into explicit semantic constructs, aligns them against the `Engineering Ontology`, normalizes them into `Engineering IR`, and then submits that IR to the `Engineering Compiler` for validation, derivation, and target preparation.

Alongside that project path, EngineeringOS maintains a separate knowledge-compilation path for standards-derived material. Public standards, manufacturer references, and reviewed extractions are compiled through the `Knowledge Compiler` into governed ontology additions, rules, and `Standards Mapping` artifacts. Those governed knowledge assets inform project compilation, but they are not authoring inputs compiled directly into project IR.

The outbound side of the pipeline is deliberately plural. A single semantic source can produce schematic views, tabular reports, machine-readable exports, enterprise integrations, and domain-specific files through a `Renderer` or other target adapter. This is why EngineeringOS is not a replacement for every downstream tool. It is the layer that makes many outputs possible without making any one output authoritative.

## Core Layers

The architecture is organized into a small number of layers with distinct responsibilities. The authoring layer accepts natural language and `Engineering Language` as human-facing inputs. The knowledge layer maintains `Engineering Ontology`, rules, and `Standards Mapping` through the governed `Knowledge Compiler` path. The representation layer defines `Engineering IR` as the canonical model of project and design semantics. The execution layer runs the `Engineering Compiler` over that IR using governed knowledge as input. The extension layer exposes `Plugin` interfaces for domains, integrations, and targets.

These layers are ordered intentionally. Language is allowed to be expressive, ontology is allowed to be conceptual, and targets are allowed to be heterogeneous because the center is stabilized by the IR and compiler boundary. Later chapters refine each layer separately, but the system only remains coherent if their contracts stay explicit.

## The Semantic Core

The `Semantic Core` is the combination of `Engineering Language`, `Engineering Ontology`, and `Engineering IR`. It is the part of the architecture that preserves engineering meaning independent of any one editor, document, or vendor file. `Engineering Language` makes intent writable, `Engineering Ontology` makes meaning explicit, and `Engineering IR` makes that meaning computationally stable.

This core is what allows EngineeringOS to be compiler-first rather than drawing-first. When identity, relationships, constraints, behavior, and standards references exist inside the `Semantic Core`, downstream systems no longer have to infer meaning from coordinates, symbols, and page structure. That shift is what makes validation, regeneration, automation, and AI assistance dependable instead of heuristic.

## Compiler And Pass Model

The `Engineering Compiler` operates on the `Semantic Core` through explicit passes rather than hidden application behavior. Typical operational passes include lowering, normalization, type and relationship validation, rule evaluation, derivation of numbering and cross-references, report construction, and preparation for target-specific rendering. Each pass should consume declared inputs, produce declared outputs, and remain inspectable as part of a reproducible pipeline.

EngineeringOS also needs a second compiler-shaped process for knowledge acquisition. The `Knowledge Compiler` is responsible for turning standards documents, manufacturer references, and reviewed AI extractions into governed ontology additions, rules, and `Standards Mapping` artifacts that the operational compiler can trust. The two compilers serve different purposes: one compiles engineering projects from authoring inputs into `Engineering IR` and downstream outputs, and the other compiles engineering knowledge into governed assets consumed during project compilation.

## Plugin Boundary

Variation belongs outside the core wherever possible. A `Plugin` may introduce a domain extension, import or export adapter, standards pack, AI integration, or `Renderer`, but it should do so through published extension points rather than by redefining the contracts of the `Semantic Core`. This boundary keeps the center small and allows the ecosystem to grow without dissolving architectural coherence.

The plugin boundary is also the adoption boundary. Existing electrical, mechanical, and enterprise systems can be integrated incrementally when they are treated as targets or sources at the edge. EngineeringOS does not need every external tool to share its internals. It needs them to connect to a stable semantic and compiler contract.

## Outputs And Targets

Outputs are compiled consequences of a semantic source of truth. They include diagrams, layouts, BOMs, wiring tables, compliance reports, PDFs, SVG views, machine-readable exports, and synchronized tool-specific project artifacts. A `Renderer` is therefore a target-facing component, not the place where engineering intent is defined.

This target model is the practical expression of the overall architecture. EngineeringOS can coexist with current workflows because it treats downstream artifacts as projections of the same underlying meaning. When the `Semantic Core` and `Engineering Compiler` are correct, new targets become additive rather than destabilizing, and external tools become outputs, companions, or integration surfaces instead of the deepest authority.
