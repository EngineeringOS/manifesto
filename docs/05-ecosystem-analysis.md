# Ecosystem Analysis

EngineeringOS sits inside a dense ecosystem of software platforms, standards, protocols, and implementation frameworks. The project is viable only if that ecosystem is classified correctly. Some assets should be reused directly. Some should be integrated through adapters. Some should be studied as reference architecture. Others should be treated as standards boundaries rather than implementation dependencies.

## Four Reuse Modes

EngineeringOS should classify every external dependency by method, not by popularity.

- `Own`: language, ontology, IR, compiler, rules, standards mapping, and plugin contracts.
- `Use directly`: technologies such as Kotlin, Compose Multiplatform, WASM, LSP, ANTLR, Tree-sitter, SQLite, and DuckDB where direct leverage is stronger than reinvention.
- `Integrate`: platforms such as OCCT, FreeCAD, QElectroTech, KiCad, AutomationML, and OPC UA that provide external capability or compatibility surfaces.
- `Study`: systems such as OpenSCAD, LLVM, MLIR, SysML v2, OpenUSD, LibrePCB, Blender, IFC, and Kubernetes that contribute architectural lessons even when their code is not the main dependency.

## Platform Inventory

`OCCT` is the industrial geometry kernel. `FreeCAD` is the practical mechanical workbench and STEP-facing ecosystem reference around that geometry world. `QElectroTech` is the most relevant open electrical symbol and schematic reference. `KiCad` is the PCB compatibility and ecosystem anchor. `OpenSCAD` is a design-philosophy reference for programmable modeling. `LibrePCB` is worth studying for cleaner PCB architecture and UX patterns. `AutomationML`, `OPC UA`, `SysML v2`, `IFC`, and `IEC CIM` matter as semantic and exchange references. `LLVM`, `MLIR`, `LSP`, `ANTLR`, and `Tree-sitter` matter as compiler and language-tooling references. `SQLite`, `DuckDB`, `Neo4j`, `Skia`, `WebGPU`, `OpenUSD`, `Blender`, and `OpenBOM` fill out the storage, rendering, analytics, visualization, and future digital-twin perimeter.

## The Method Layer

The key lesson from the draft corpus is that EngineeringOS is not just an AI project and not just a CAD project. It is a method for orchestrating many mature systems through one semantic core. That method is compiler-first at the center, plugin-first at the edges, standards-aware in governance, and selective in reuse. It does not absorb external code indiscriminately. It gives each dependency a narrow, explicit role.

That method should remain visible in every future design document. When the project evaluates a dependency, it should always answer four questions: what capability does this system provide, at which boundary do we consume it, what do we refuse to inherit from it, and what strategic layer must remain under EngineeringOS control.

## Practical Implication

The ecosystem is not a background list. It is part of the architecture. Every serious chapter about compiler design, plugin boundaries, Studio, cloud distribution, standards mapping, or enterprise integration should be legible against this ecosystem map. If the map is missing, the project drifts either into reinvention or into dependency capture.
