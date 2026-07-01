# Studio

Studio is the human-facing shell of EngineeringOS, not the source of truth. Its job is to expose the semantic core, compiler behavior, graph state, diagnostics, and downstream projections in a usable form without relocating authority back into UI state. That constraint is what separates Studio from a conventional CAD application.

## Product Role

Studio should provide authored language views, semantic inspectors, graph-oriented navigation, diagnostics, report previews, and target projections such as schematic, panel, BOM, or 3D-adjacent views. It should make the compiler pipeline visible and operable. It should not hide core logic behind one privileged editor surface.

## Technology Direction

The draft is clear about the preferred direction: Kotlin Multiplatform for the shared implementation base, Compose Multiplatform for the UI shell, and WASM for browser delivery and embeddable views. That stack is attractive because it keeps the language and product surfaces aligned while supporting desktop and web deployment from one architecture.

## Boundary

Studio should remain downstream of language, ontology, IR, graph, and compiler contracts. If a workflow only works in Studio and cannot be explained at the semantic or compiler boundary, that is a design failure. Studio exists to make the platform adoptable, not to become a second hidden architecture.
