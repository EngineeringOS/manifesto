# Kernel v0

`Kernel v0` is the minimal executable proof of the manifesto. Its purpose is not to launch a broad product surface, but to demonstrate that EngineeringOS can carry one project through a disciplined semantic pipeline and produce a compiled output from that pipeline.

## Objective

The objective of `Kernel v0` is to prove the architecture through the smallest useful slice of execution. That slice must begin with authored engineering intent, lower that intent into canonical structure, apply explicit rule logic, and produce a concrete export. The kernel is successful if it demonstrates the compiler-first path clearly enough that the manifesto becomes operational rather than rhetorical.

```text
DSL -> IR -> Rule -> Export
```

This objective prioritizes the semantic core and execution boundary over any GUI surface. `Kernel v0` exists to show that language, ontology-aligned structure, and compiler logic can already do real work before broader product layers are introduced.

## Scope

The scope is intentionally narrow. `Kernel v0` includes a minimal authoring DSL, a canonical IR model, one canonical rule evaluation step, and one canonical export path. The implementation should be small enough to inspect end to end, but complete enough to prove that the architecture can carry engineering meaning through compilation.

The authoring example remains intentionally simple:

```kotlin
system("DemoCabinet") {
    device("PLC1") {
        type = "PLC"
        model = "S7-1200"
    }
}
```

The IR example remains equally minimal and explicit:

```kotlin
data class Node(
    val id: String,
    val type: String,
    val props: Map<String, Any>
)
```

Within this scope, the kernel may use a minimal ontology-aligned vocabulary for systems, devices, relationships, and properties, but it should not attempt to encode the full long-term domain model. The goal is a narrow executable slice, not a premature platform expansion.

## Non-Goals

`Kernel v0` is not a roadmap for the whole platform. It does not include EPLAN UI or KiCad UI work, because the kernel must prove semantic execution before any application-like surface is allowed to dominate the architecture.

It does not include 3D or OpenCascade integration. Geometry and layout systems may matter later, but they are not required to prove the first compiler path and would distract from the semantic core.

It does not include plugin ecosystems, full standards coverage, broad domain packs, or enterprise surfaces. Those require a stable core to attach to and should arrive only after the kernel has demonstrated a disciplined execution model.

## MVP Pipeline

The MVP pipeline is deliberately linear and inspectable. A small authored DSL is lowered into canonical IR, the IR is evaluated by an explicit rule step, and the resulting state is exported into a downstream artifact. For `v0`, the canonical rule is `Every connection endpoint must resolve to an existing device`, and the canonical export artifact is a JSON serialization of the validated IR. Each stage must be visible enough that a reviewer can understand what changed between stages and why.

The DSL stage proves that engineering intent can be written in a constrained author-facing form. The IR stage proves that meaning can be represented canonically. The rule stage proves that execution belongs in explicit compiler logic rather than hidden application state. The export stage proves that outputs can be generated as compiled consequences of the same source model.

## Deliverables

The first deliverable is a minimal DSL authoring path that can represent a small system with at least one device definition and stable properties. The second is an IR model that preserves identity, type, and properties in a form suitable for rule evaluation and export. The third is a rule step that evaluates the canonical `Every connection endpoint must resolve to an existing device` condition over the IR and emits a deterministic pass or failure result.

The final deliverable is a JSON export produced from that same pipeline. The export is intentionally narrow, but it must be concrete enough to show that downstream artifacts can be derived from the compiled model rather than authored separately.

## Milestones

The first milestone is `DSL -> IR`: authored input lowers into a canonical representation without losing the meaning required for later steps. The second milestone is `IR -> Rule`: explicit rule logic operates over that representation and verifies that every connection endpoint resolves to an existing device in the model. The third milestone is `Rule -> Export`: the pipeline emits the canonical JSON artifact derived from the evaluated model.

Completion of these milestones is more important than surface breadth. `Kernel v0` should remain small, readable, and architecturally disciplined even if that means leaving many future concerns unimplemented.

## Acceptance Criteria

`Kernel v0` is accepted when a reviewer can trace one example end to end through the full pipeline and see that each stage performs a distinct architectural role. The example must begin in the DSL, lower into the IR, pass through the canonical `Every connection endpoint must resolve to an existing device` rule, and produce the canonical JSON export without relying on hidden UI behavior.

The DSL and IR artifacts in this document must remain intact as canonical examples of the kernel boundary. The kernel must demonstrate that compiler execution is real, inspectable, and downstream-oriented, and that the first executable slice stays centered on semantic structure rather than on product breadth.
