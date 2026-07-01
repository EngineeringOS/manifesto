# Compose Multiplatform

Compose Multiplatform is the preferred UI shell for Studio because it supports desktop and web-facing surfaces from one architecture and aligns naturally with a Kotlin-based core.

## How EngineeringOS Uses It

Compose should be used for inspectors, project views, semantic editors, diagnostics, and projection-oriented interfaces. It is a product-shell technology, not the source of truth.

## Boundary

EngineeringOS should not confuse Compose with platform differentiation. Compose is a delivery mechanism for Studio. The semantic and compiler layers remain the real asset.
