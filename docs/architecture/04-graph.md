# Graph

EngineeringOS needs a graph-oriented internal model because engineering meaning is defined as much by relationships as by objects. Devices, ports, functions, constraints, signals, and standards references form networks of dependency, not isolated records. The graph layer is therefore the operational shape of the IR, not an optional storage trick.

## Why Graph Matters

A graph model gives EngineeringOS first-class representation for connectivity, control relationships, topology, provenance, and derived dependencies. It makes it practical to ask compiler questions such as which devices are connected, which constraints apply along a path, what systems are affected by a change, and which outputs must be regenerated after a semantic edit.

This is one of the draft's most important method points: AI should edit the semantic graph, not draw symbols. Compiler passes should validate and transform the graph, not reverse-engineer it from pages.

## Identity And Edges

Every engineering node in the graph should carry stable identity. Every edge should carry explicit meaning, such as `connects`, `controls`, `contains`, `references`, or `violates`. That structure lets the compiler distinguish topology from containment, behavior from ownership, and semantic linkage from presentation linkage.

Stable identity plus typed edges is what makes diff, merge, traceability, and regeneration workable. Without that, the graph would collapse into another transient export structure instead of the computational center of the platform.

## Storage And Execution Boundary

The graph does not require one storage engine forever. Early versions can use typed in-memory models with SQLite-backed persistence and selective analytics in DuckDB. If later scale demands graph-native storage, a system such as Neo4j can be evaluated as an implementation option. The architectural contract, however, is the graph semantics, not the database brand.
