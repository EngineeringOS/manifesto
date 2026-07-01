# LSP

LSP is the direct route into a serious editor ecosystem. It gives EngineeringOS a path to diagnostics, completion, navigation, and tooling across VS Code, Cursor, IntelliJ, and similar environments without inventing a private IDE stack.

## How EngineeringOS Uses It

EngineeringOS should implement language-server support for its authoring surfaces so the engineering language behaves like a real programmable system from the start. That includes completion, diagnostics, go-to-definition, references, and semantic inspection.

## Boundary

LSP should be used directly rather than reimagined. The value is interoperability with existing editors, not invention of a proprietary tooling protocol.
