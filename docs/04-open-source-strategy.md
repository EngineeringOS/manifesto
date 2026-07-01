# Open Source Strategy

EngineeringOS should not try to win by replacing the whole engineering software world. It should win by providing the missing semantic layer that lets the rest of that world interoperate more intelligently. The strategy is not replacement. The strategy is leverage.

## Leverage, Don't Replace

This is one of the defining choices of the project. EngineeringOS should stand on top of the strongest ecosystems that already exist instead of fighting them all at once.

- Geometry: `OCCT`
- PCB: `KiCad`
- Electrical: `QElectroTech`
- Mechanical: `FreeCAD`
- Visualization: `OpenUSD`
- Compiler method: `LLVM` philosophy

That decision signals technical maturity. It says the project understands where real leverage lives: not in rebuilding solved subsystems, but in owning the layer that coordinates them.

## What EngineeringOS Must Own

EngineeringOS must own the language, ontology, intermediate representation, compiler pipeline, rule engine, plugin contracts, and governed knowledge layer that define how engineering meaning is expressed and transformed. These components are the architectural core. If they are left to external tools, the platform loses its strategic center.

Owning the semantic layer does not mean building a monolith. It means being able to say, with precision, what a device is, how relationships are represented, how rules execute, how standards are mapped, and how outputs are derived without surrendering those questions to downstream vendors or legacy file formats.

## What EngineeringOS Must Reuse

EngineeringOS should deliberately reuse open-source assets that solve adjacent but already-mature problems. Geometry should come from established kernels such as `OCCT`. Electrical compatibility can draw from `QElectroTech`. PCB and mechanical interoperability can lean on `KiCad` and `FreeCAD`. Parsing, editor tooling, storage, analytics, and rendering foundations should be reused where they are already strong.

This is not compromise. It is strategic discipline. The project should not waste its best effort recreating systems whose value is already widely available.

## Shared Engineering Knowledge As Infrastructure

The semantic layer matters not only because it improves software architecture, but because it changes what can be shared. Once rules, ontology packs, standards mappings, templates, validation logic, domain libraries, and workflow modules become governed semantic artifacts, they can be published, versioned, improved, and reused collectively instead of dying inside one company archive or one vendor toolchain.

In software, ecosystems such as `npm` and Maven Central turned accumulated knowledge into reusable infrastructure. Open foundations such as Apache and Linux made shared public layers possible at global scale. EngineeringOS should aim for the same structural effect in engineering: a semantic infrastructure layer where knowledge compounds over time and every serious contribution can strengthen the whole ecosystem.

## Why Forking Is Usually The Wrong Move

Forking is usually the wrong move because it imports another project's maintenance burden, historical constraints, and architectural assumptions into the center of this one. The default posture should be integration, adaptation, and contribution around stable boundaries. Forking should be exceptional, narrow, and peripheral.

## Strategic Boundary

EngineeringOS is not a geometry kernel, not a schematic editor clone, not a symbol-library replacement, and not a thin AI wrapper over legacy files. It is the semantic, compiler, and governance layer that sits above those systems and makes them interoperable under a common source of truth.

That boundary should remain strict. The long-term asset is the open semantic infrastructure. Everything else should either serve that layer directly or remain outside the core.
