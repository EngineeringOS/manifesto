# Compiler v1

`Compiler v1` is the first product-facing release of the Engineering Compiler as a dependable service boundary. Its job is to make semantic compilation inspectable, deterministic, and useful across multiple downstream targets.

## Objectives

- Normalize authored input into canonical IR.
- Execute explicit passes for validation, derivation, numbering, and rule evaluation.
- Emit diagnostics with provenance.
- Prepare target-ready outputs for renderers and integrations.

## Product Shape

`Compiler v1` should be usable from command-line and service contexts, with plugin-aware rule packs and exporter targets. The emphasis is reliability, reproducibility, and traceability rather than optimization sophistication.

## Success Metric

The release is successful when one semantic model can generate multiple synchronized downstream artifacts while preserving one source of truth and one diagnostic trail.
