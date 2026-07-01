# RFC-0005: Compiler

- Status: Draft
- Area: Execution

## Proposal

Define the `Engineering Compiler` as an explicit pass pipeline over canonical IR, covering normalization, validation, rule execution, derivation, diagnostics, and target preparation.

## Open Questions

- Which passes are mandatory in the first public compiler contract?
- How should plugin-contributed passes declare ordering and compatibility?
