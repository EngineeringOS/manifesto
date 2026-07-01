# Layout And Geometry

EngineeringOS should distinguish clearly between engineering meaning, layout intent, and geometry. This is not a secondary implementation detail. It is one of the foundational architectural separations of the platform.

Most engineering tools collapse these layers into one file and one editing surface. As a result, engineering semantics, presentation choices, and rendering artifacts become tightly coupled. That coupling makes it difficult to support multiple synchronized views, reliable automation, renderer independence, and trustworthy AI. EngineeringOS should reject that structure explicitly.

## The Three-Layer Model

```text
Engineering Intent
        ->
Semantic Model
        ->
Presentation / Layout Model
        ->
Geometry Model
```

These layers answer different questions:

- `Engineering IR`: What the system is.
- `Layout IR`: How humans want to see it.
- `Geometry IR`: How that view is rendered precisely.

Treating them as one model makes every layer weaker. Separating them makes the system more durable.

## Engineering Meaning

The engineering layer is responsible for semantic truth: devices, functions, signals, constraints, relationships, identities, and governed references to standards or rules. This is the layer that should survive independent of any page, coordinate system, or rendering target.

An engineering authoring language should therefore describe engineering intent rather than drawing mechanics. It may express that a breaker protects a motor, that a relay controls a circuit, or that a safety function constrains operation. It should not need to encode x/y position, pixel distance, or arbitrary presentational alignment in order to remain valid.

## Layout Intent

The layout layer is responsible for view logic. It describes how humans want to arrange and inspect the semantic model in a particular context: cabinet views, wiring views, functional views, power views, safety views, and other presentation structures.

This layer may encode grouping, relative placement, alignment, flow direction, routing preferences, cabinet composition, and view-specific emphasis. Those choices matter operationally, but they do not redefine engineering meaning. Layout is a projection of semantic truth, not the source of it.

This distinction is especially important because the same engineering model may legitimately support many layouts at once. Different teams, tasks, or lifecycle phases may require different views over the same semantic project without creating separate engineering realities.

## Geometry

The geometry layer is responsible for exact renderable output. Coordinates, paths, line segments, splines, polygons, symbol placement, text boxes, and final drawing primitives belong here. Geometry is the realized output of layout and rendering decisions.

In this architecture, geometry should remain downstream of both semantic meaning and layout intent. It is necessary, but it is not authoritative. If geometry becomes the deepest source of truth again, the platform collapses back into the same structural weakness found in conventional CAD-centric systems.

## Compiler Consequence

This architectural separation suggests a compiler pipeline with multiple explicit intermediate forms:

```text
Engineering Language
        ->
Engineering IR
        ->
Layout IR
        ->
Geometry IR
        ->
SVG / QET / EPLAN / FreeCAD / Other Targets
```

Each intermediate representation should own one concern:

- `Engineering IR` preserves semantic truth.
- `Layout IR` preserves presentation intent.
- `Geometry IR` preserves exact renderable structure.

That separation gives the platform a cleaner contract at every stage and prevents one representation from becoming overloaded with responsibilities it cannot carry well.

## Why This Matters

Once meaning, layout, and geometry are separated, the same engineering project can support multiple synchronized views without duplicating the underlying design. Cabinet layout, wiring layout, functional layout, power layout, and safety layout can all derive from the same engineering model while remaining free to express different presentational logic.

This also makes AI more useful. AI should operate on semantic and layout intent rather than on brittle pixel-level manipulations. The right instruction is not "move this object twenty pixels." It is "group all safety devices together" or "place the motor to the right of its protective breaker." That kind of operation becomes more reliable only when the platform has explicit layers for meaning and layout.

## Architectural Principle

EngineeringOS should treat this separation as a governing principle:

- semantics define what the system is
- layout defines how humans choose to view it
- geometry defines how that view is rendered

The platform should own these abstractions explicitly and prevent them from collapsing back into a single drawing-centric model. That is one of the conditions that makes semantic engineering possible at all.
