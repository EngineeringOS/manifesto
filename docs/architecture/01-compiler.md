# Compiler

The compiler is where EngineeringOS stops being a theory of semantics and becomes an executable engineering system. Its job is to take structured engineering meaning, apply rules and validations, derive consistent outputs, and generate the artifacts required by tools, workflows, and organizations downstream. In this sense, the compiler is not a secondary component but the operational heart of the platform, and this chapter defines the responsibilities and boundaries of that heart.

## Compiler Purpose

The purpose of the `Engineering Compiler` is to convert semantic engineering intent into validated and reusable outputs. It does this by operating over `Engineering IR` with explicit passes that check correctness, derive implied structure, and prepare information for reports, integrations, and targets. The compiler is where the platform enforces that semantics are not merely described but made operational.

This purpose is broader than file generation. The compiler is responsible for preserving coherence across views, ensuring that derived artifacts agree with the same source model, and making rule execution visible and testable. Without a compiler, the platform would degrade into a collection of editors, scripts, and exporters with no dependable center.

## Input And Output Model

The compiler consumes normalized `Engineering IR` together with the contracts that give that IR meaning: the `Engineering Ontology`, rule packs, extension metadata, and `Standards Mapping` artifacts. `Engineering Language`, imported files, and AI-generated candidates are not compiler outputs in their raw form; they are inputs that must first be lowered into the canonical representation the compiler understands.

The compiler produces more than one class of output. It emits diagnostics, validated and enriched IR, numbering and cross-reference derivations, reports, machine-readable exports, and target-ready structures that a `Renderer` or integration adapter can consume. In other words, the compiler turns one semantic source into many coordinated consequences.

## Pass Structure

The `Engineering Compiler` should be structured as a sequence of explicit passes rather than hidden state transitions. Typical passes include normalization, identity resolution, ontology conformance checks, relationship validation, rule execution, derivation of references and numbering, report assembly, and target preparation. Each pass should be deterministic, inspectable, and scoped to a clear responsibility.

This pass model matters because engineering logic grows over time. When the compiler is organized into clear passes, new rule sets, domain extensions, and targets can be inserted without turning the entire system into one opaque procedure. A compiler-centered architecture is maintainable precisely because responsibilities are separated, ordered, and reviewable.

## Validation And Rules

Validation is the first operational duty of the compiler. It confirms that the IR is structurally sound, semantically well-typed, and consistent with domain and standards expectations. Some validations are universal, such as identity consistency or relationship cardinality. Others come from domain packs and `Standards Mapping`, where the platform must check requirements derived from governed engineering knowledge.

Rules should therefore be treated as executable knowledge rather than UI-side conveniences. The compiler should distinguish errors, warnings, and advisory findings, and it should preserve enough provenance that a result can be traced back to ontology definitions, rule sources, or mapped standards. This traceability is what makes the compiler credible in engineering settings rather than merely convenient.

## Reports And Render Targets

Reports and render targets are downstream products of compilation, not separate sources of truth. BOMs, wiring tables, cross-reference lists, compliance summaries, PDFs, SVGs, and external project exports should all be derived from the same compiled semantics. The compiler assembles the engineering content of those outputs, while the `Renderer` or target adapter handles presentation and format-specific emission.

This distinction keeps the architecture clean. A `Renderer` should not be responsible for recovering missing engineering meaning from incomplete data, and a report generator should not invent its own business logic in isolation. The compiler owns derivation and consistency; target-facing components own formatting and transport.

## Engineering Compiler Versus Knowledge Compiler

EngineeringOS needs two different compiler-shaped systems with different authorities. The `Engineering Compiler` compiles engineering projects: it takes instance-level intent and produces validated instance-level outputs. The `Knowledge Compiler` compiles engineering knowledge: it turns standards documents, manufacturer references, and reviewed AI extractions into governed ontology updates, rules, and mappings that the operational compiler can later use.

Keeping these responsibilities separate is essential. The operational compiler must be deterministic and project-focused, while the knowledge side is iterative, evidence-driven, and mediated by a `Human Review Loop`. If the two are collapsed, project compilation becomes unstable and standards interpretation becomes opaque. If they remain distinct, EngineeringOS can evolve its knowledge base without compromising the reliability of engineering execution.
