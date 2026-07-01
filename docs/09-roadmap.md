# Roadmap

The roadmap follows the manifesto architecture in sequence. EngineeringOS starts with the semantic core, then adds executable compilation, then AI-native workflows, then Studio as a projection layer, and only after that opens cloud and enterprise surfaces. This ordering is deliberate because the project's authority must be established in language, ontology, IR, and compiler logic before it is expressed in any richer interface or commercial surface.

## Phase 1: Language, Ontology, IR

Phase 1 establishes the semantic core. The first responsibility of EngineeringOS is to define `Engineering Language`, `Engineering Ontology`, and `Engineering IR` clearly enough that engineering intent can exist as a governed source of truth independent of any downstream tool. This phase covers the language surface, ontology vocabulary, canonical IR model, parser boundary, and the public specifications that make those layers stable and reviewable.

Phase 1 is not a GUI phase. It is the period in which the architecture proves that meaning can be authored, normalized, and preserved before any rich visual shell is allowed to define system behavior. If this layer is weak, every later phase collapses back into drawing-centric software.

## Phase 2: Compiler, Rules, Exporters

Phase 2 turns the semantic core into an executable system. The priority here is the `Engineering Compiler`: explicit passes for lowering, normalization, validation, rule execution, derivation, and target preparation. The point is not to add surface complexity, but to make the semantic core operational and testable.

This phase also introduces rule packs and exporters. Reports, structured exports, renderer inputs, and compatibility targets should all be compiled consequences of the same IR rather than separate sources of logic. Exporters belong after the compiler boundary because they depend on validated meaning, not on ad hoc file conversion.

## Phase 3: AI-Native Workflows

Phase 3 introduces AI-native workflows only after the semantic and compiler contracts exist. At this stage, natural-language authoring, transformation assistance, review flows, and model-aware automation can operate over stable language and IR interfaces instead of over drawings or prompts alone.

This phase also introduces standards knowledge extraction through the `Knowledge Compiler` path. Standards documents, manufacturer references, and reviewed AI extractions are turned into governed ontology additions, mappings, and rules that can inform project compilation. AI is useful here because it can accelerate extraction and proposal, but the accepted knowledge remains reviewable infrastructure rather than opaque model behavior.

## Phase 4: Studio

Phase 4 introduces `Studio` as a projection layer over the semantic core and compiler pipeline. By the time Studio appears, the architecture should already be able to author, validate, and export meaning without relying on a rich interface to hide system logic. Studio therefore exists to make the platform more usable, inspectable, and adoptable, not to become the deepest authority in the stack.

This distinction matters because Studio should consume and expose the same semantic and compiler contracts already established in earlier phases. It can provide authoring surfaces, visual projections, inspections, and workflow composition, but it should remain downstream of the core rather than redefining it.

## Phase 5: Cloud And Enterprise

Phase 5 adds cloud and enterprise surfaces only after the core has stabilized. By this point, the semantic model, compiler boundary, rules, exporters, and Studio projection model should already be coherent enough that collaboration, governance, deployment, and organizational integrations can build on a durable substrate.

This phase includes hosted workflows, multi-user coordination, managed knowledge distribution, policy surfaces, and enterprise-facing integration layers. These belong last because they amplify the platform's core assumptions; they should not be used to discover what those assumptions are.

## Adoption Milestones

The first adoption milestone is semantic credibility: users can see that language, ontology, and IR preserve engineering meaning more faithfully than file-centric workflows. The second is executable credibility: compiler passes, rules, and exporters produce repeatable outputs from one source of truth. The third is workflow credibility: AI-native authoring and standards knowledge extraction improve engineering practice without replacing governance.

The fourth milestone is interface credibility: Studio proves that a rich surface can remain subordinate to the semantic core rather than becoming another hidden application center. The fifth is organizational credibility: cloud and enterprise surfaces are adopted because the core is already stable enough to support collaboration, compliance, and integration at scale.
