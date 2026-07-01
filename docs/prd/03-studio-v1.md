# Studio v1

`Studio v1` is the first serious user-facing shell of EngineeringOS. It should make the semantic platform inspectable and operable without relocating authority from the compiler and IR into hidden UI state.

## Objectives

- Provide language and graph-oriented project inspection.
- Expose diagnostics, compiler results, and generated outputs.
- Support projection views such as schematic, BOM, or report-oriented surfaces.
- Stay aligned with Kotlin Multiplatform, Compose Multiplatform, and WASM delivery goals.

## Product Boundary

`Studio v1` is not a drawing-first CAD clone. It is a semantic workstation for authoring, inspection, compilation, and projection.

## Success Metric

The release is successful when users can understand and operate the semantic pipeline through Studio without losing the ability to explain every action at the language, IR, and compiler boundary.
