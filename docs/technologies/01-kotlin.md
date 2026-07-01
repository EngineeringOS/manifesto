# Kotlin

Kotlin is the preferred implementation language for EngineeringOS because it can host a readable DSL, support compiler-style back-end code, and span JVM, desktop, and web-adjacent product surfaces through one language family. The draft treats Kotlin as a strategic fit, not a convenience choice.

## How EngineeringOS Uses It

EngineeringOS should use Kotlin for the language front end, IR structures, compiler passes, plugin contracts, and the shared implementation substrate behind Studio. A Kotlin-hosted DSL is especially attractive in early stages because it gives typed authoring, testing, and tooling quickly.

## Boundary

EngineeringOS should borrow Kotlin's language platform, not mirror JetBrains product scope. The point is to gain a strong implementation base and DSL host, not to turn EngineeringOS into a Kotlin branding exercise.
