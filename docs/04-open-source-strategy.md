# Open Source Strategy

EngineeringOS should not attempt to rebuild the engineering software stack from first principles. The strategic opportunity is not to recreate geometry kernels, symbol libraries, schematic editors, or parser frameworks, but to own the missing semantic layer that can coordinate them. This chapter defines that boundary clearly: what EngineeringOS must build itself, what it should deliberately reuse from the open ecosystem, and why orchestration is a stronger strategy than replacement.

## Strategy Statement

The strategy is simple: own the semantic layer and reuse the rest wherever reuse is structurally sound. EngineeringOS should build the components that define semantic authority and platform leverage, and it should stand on existing open ecosystems for geometry, rendering, compatibility, parsing, storage, and surrounding tooling. The goal is not independence from the ecosystem. The goal is control over the layer the ecosystem currently lacks.

That boundary is what keeps the project technically credible. If EngineeringOS tries to replace every incumbent subsystem, it becomes a diffuse software stack with no strategic center. If it owns the semantic and compiler layer while reusing mature infrastructure below and around it, it becomes a focused platform with a realistic path to adoption.

## What EngineeringOS Must Own

EngineeringOS must own the language, ontology, intermediate representation, compiler pipeline, rule engine, and plugin SDK that define how engineering meaning is expressed and transformed. It must also own the governed knowledge layer that maps standards, constraints, and domain concepts into reviewable semantic structures. These components are the architectural core. If they are outsourced, the project loses its reason to exist.

Owning these layers does not mean building them as a closed monolith. It means that their design, contracts, and governance must remain intentional and coherent. The platform must be able to say what a device is, how relationships are represented, how rules execute, how outputs are derived, and how extensions plug into the system without deferring those decisions to external tools.

## What EngineeringOS Must Reuse

EngineeringOS should deliberately reuse open-source assets that solve adjacent but already-mature problems. Geometry should come from established kernels such as OCCT rather than custom solid-modeling code. Symbol libraries and electrical compatibility can draw from projects such as QElectroTech. PCB and mechanical interoperability can lean on ecosystems such as KiCad and FreeCAD, while OpenSCAD is better treated as a useful DSL reference than as the architectural center.

The same discipline applies to infrastructure. Parser frameworks such as ANTLR and Tree-sitter, language tooling such as LSP, embedded databases such as SQLite, analytics engines such as DuckDB, and modern UI foundations are examples of where differentiation is unnecessary. They are leverage points. EngineeringOS should combine them in service of the semantic platform instead of turning them into reinvention projects.

## Why Forking Is Usually The Wrong Move

Forking is usually the wrong move because it imports another project's maintenance burden, historical constraints, and roadmap into the center of this one. A fork can look faster at the start, but it often traps the team in upstream drift, legacy architecture, and compatibility work that does not increase control over the semantic layer. The result is local ownership of someone else's problem rather than strategic ownership of the missing platform.

The default posture should therefore be integration, adaptation, and contribution around stable boundaries. Forking should be reserved for narrow cases: when a dependency is abandoned, when a critical interface cannot be obtained any other way, or when the cost of maintaining a small targeted divergence is lower than the cost of waiting. Even then, the fork should remain peripheral rather than becoming the identity of EngineeringOS.

## Ecosystem Leverage Model

EngineeringOS should treat the open ecosystem as a set of specialized capabilities that can be orchestrated through a semantic core. Geometry engines provide shape and topology. Electrical tools provide symbols, conventions, and compatibility. PCB and mechanical systems provide domain workbenches and exchange formats. Standards bodies provide public reference models. Parsing and storage projects provide implementation infrastructure. EngineeringOS gains leverage by coordinating these assets through one semantic and compiler-centered pipeline.

That model compounds over time. Every importer, exporter, standards bridge, renderer, and domain plugin increases the usefulness of the same core representation instead of creating another silo. Community libraries, example projects, and external toolchains become accelerants rather than dependencies that define the architecture. Orchestration is stronger than replacement because it allows the platform to inherit decades of ecosystem investment while concentrating new effort on the missing layer.

## Shared Engineering Knowledge As Infrastructure

EngineeringOS is valuable not only because it provides a semantic layer for engineering design, but because it can turn engineering knowledge itself into reusable infrastructure. Rules, ontology packs, standards mappings, templates, validation logic, domain libraries, and workflow modules can be published, versioned, shared, and improved collectively rather than remaining trapped inside one company, one project archive, or one vendor file format.

In software, package ecosystems such as `npm` and Maven Central made accumulated knowledge reusable at global scale. Open infrastructure projects such as Apache and Linux created common foundations that the rest of the industry could build on. EngineeringOS should aim for the same structural effect in engineering: a shared semantic layer where domain knowledge compounds over time and where every serious contribution can strengthen the whole ecosystem rather than disappear into isolated project silos.

## Strategic Boundary

EngineeringOS is not a geometry kernel, not a schematic editor clone, not a symbol-library replacement, and not a thin AI shell over legacy files. It is the semantic, compiler, and governance layer that sits above those systems and makes them interoperable under a common source of truth. Its job is to make engineering meaning explicit, portable, and machine-operable across many downstream tools.

That boundary should remain strict. The project should build enough product surface to prove the platform and make it usable, but it should not confuse demonstrations of the platform with the platform itself. The long-term asset is the open semantic infrastructure. Everything else should either serve that infrastructure directly or stay outside the core.
