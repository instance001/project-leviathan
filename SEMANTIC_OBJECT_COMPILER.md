# Semantic Object Compiler

## Project Leviathan: From Linear Vectors to Manipulable Semantic Objects

**Status:** Concept / research direction  
**Project:** Leviathan  
**Purpose:** Define a host-governed mechanism that compiles granular semantic material into persistent, modular, inspectable objects that can be compared, connected, rotated, decomposed, and recursively abstracted.

---

## 1. Core idea

Project Leviathan already attempts to reason across large piles of semantically related material. Its current form can retrieve, compare, cluster, and permute granular snippets, but this still leaves the system repeatedly reconstructing the same higher-level meaning from many small fragments.

The proposed **Semantic Object Compiler** changes the working medium.

Instead of treating snippets, vectors, and fragments as the final reasoning surface, the compiler inspects them and produces a higher-order semantic object with a stable external shape:

- ports;
- gear teeth;
- latch points;
- blockers;
- tolerances;
- internal components;
- invariants;
- uncertainty markers;
- provenance back to the source material.

The underlying snippets remain preserved, but the system normally reasons over the compiled object as a whole. It descends back into the granular evidence only when a fit fails, uncertainty is localised, a contradiction appears, or recompilation is required.

This is the proposed jump from **2D semantic proximity** to **3D structural reasoning**.

---

## 2. The problem with the current reasoning surface

Vector search and semantic retrieval are useful for locating related material, but they do not automatically create a persistent, manipulable representation of the thing those fragments collectively describe.

A conventional reasoning loop often looks like this:

1. Retrieve many related snippets.
2. Compare them inside a temporary context window.
3. Form a provisional interpretation.
4. Use that interpretation for one task.
5. Lose most of the assembled structure when the context moves on.
6. Reconstruct it again during the next reasoning pass.

This produces several costs:

- repeated compute spent rebuilding already established structures;
- excessive granular comparison;
- weak preservation of solved relationships;
- poor localisation of uncertainty;
- difficulty comparing whole mechanisms across different domains;
- abstraction that collapses into loose summarisation rather than structural deduction;
- large Rubik's-cube search spaces driven by blind permutation rather than informed manipulation.

The system repeatedly works with the quarry instead of building with bricks.

---

## 3. Proposed transformation

The compiler should transform a bounded pile of semantic material through the following stages:

```text
semantic proximity
        ↓
relation induction
        ↓
boundary detection
        ↓
functional role assignment
        ↓
interface extraction
        ↓
invariant discovery
        ↓
counterfactual verification
        ↓
persistent typed semantic object
```

Embeddings and vectors remain useful, but only as a retrieval and candidate-discovery substrate. They are the forklift that brings material into the yard. They are not the finished structure.

The compiled object becomes the unit of higher-order reasoning.

---

## 4. The semantic object

A semantic object is not merely a summary. It is an operational, inspectable contract.

A compiled object should expose at least the following fields.

### Identity

What kind of thing does this material collectively instantiate?

### Function

What role does the object perform inside a larger mechanism?

### Input ports

What kinds of state, evidence, constraints, signals, or objects can it accept?

### Output ports

What does it produce, expose, mutate, or guarantee?

### Latch conditions

What must be true before a connection is considered stable or admissible?

### Gear teeth / affordances

Which external functions, interfaces, or object classes can align with it?

### Blockers

Which conditions, assumptions, or incompatibilities prevent a fit?

### Tolerances

Where can the object flex without losing its identity or function?

### Internal components

Which smaller compiled parts or granular structures make up the object?

### Invariants

What remains true across examples, wording changes, contexts, and permissible mutations?

### Uncertainty

Which properties are observed, inferred, provisional, disputed, or unsupported?

### Provenance hatch

Which exact snippets, files, observations, tests, and compilation decisions support each property?

---

## 5. Example object envelope

```yaml
object_id: governed_retrieval_mechanism_v1
identity: Governed Retrieval Mechanism
status: provisional

function:
  description: Recover relevant stored material for an active task under explicit retrieval constraints.

input_ports:
  - type: query_or_intent
    required: true
  - type: current_task_state
    required: true
  - type: retrieval_constraint_set
    required: false

output_ports:
  - type: ranked_evidence_bundle
  - type: provenance_references
  - type: unresolved_ambiguity_report

latch_conditions:
  - searchable_store_exists
  - source_identity_is_stable
  - retrieval_policy_is_declared

gear_teeth:
  - planner_input
  - verifier_input
  - abstraction_compiler_input

blockers:
  - untraceable_generated_material
  - conflicting_identity_systems
  - missing_freshness_metadata

invariants:
  - returned_claims_remain_traceable
  - retrieval_does_not_silently_rewrite_source_evidence

uncertainty:
  - property: ranking_policy
    state: incomplete

provenance:
  - property: returned_claims_remain_traceable
    evidence_refs:
      - source_17
      - source_22
    derivation: observed_across_examples
```

The exact schema can evolve. The important requirement is that the exterior shape is machine-comparable while every emitted property remains inspectable and reversible.

---

## 6. Whole-part comparison

Once snippets have been compiled into objects, Leviathan can compare complete structures instead of running broad pairwise checks across thousands of granular entries.

The default reasoning ladder becomes:

```text
whole-object comparison
        ↓
interface inspection
        ↓
local internal inspection
        ↓
raw snippet retrieval
```

The system starts at the highest useful surface level.

- If two ports clearly fit, connect them without reopening the internals.
- If they clearly do not fit, reject the connection without expensive granular analysis.
- If the fit is ambiguous, descend only into the relevant interface region.
- If the object was compiled incorrectly, revise only that object or interface.
- If a missing intermediary is implied, propose and test an adapter object.

This creates **adaptive resolution** rather than permanent maximum granularity.

---

## 7. Novel deduction through interface mismatch

A central benefit is the ability to deduce a missing mechanism from the geometry of two parts.

Example:

```text
Part A
Produces: ranked evidence
Guarantees: source traceability

Part B
Consumes: verified evidence
Requires: confidence threshold
Produces: authorised work order
```

No source may explicitly name the missing component. However, whole-object comparison reveals:

```text
ranked evidence ≠ verified evidence
```

Leviathan can then generate a bounded set of hypotheses:

1. Part A is missing a verification stage.
2. Part B's requirement is overstated.
3. The parts are incompatible.
4. An intermediary evidence-verification adapter must exist.

The proposed adapter can itself be compiled:

```text
Input: ranked evidence
Operation: validate claims, source identity, and confidence
Output: verified evidence
Failure: unresolved contradiction or insufficient support
```

The system then tests whether inserting that object makes the larger assembly coherent.

This is a concrete form of novel structural deduction:

```text
observe structures
        ↓
compare interfaces and invariants
        ↓
detect missing relation
        ↓
hypothesise new object
        ↓
test composition
        ↓
compile accepted result
```

---

## 8. The Rubik's-cube process at the object layer

Leviathan currently uses permutation and comparison in a relatively granular form. The Semantic Object Compiler allows the same process to operate at a different dimension.

Instead of rotating individual snippets against one another, Leviathan can rotate whole semantic objects:

- change perspective;
- alter orientation;
- compare input and output geometry;
- expose hidden symmetry;
- detect inverse relationships;
- identify duplicated function under different vocabulary;
- locate a missing connector;
- test alternative object boundaries;
- compare several candidate assemblies;
- preserve solved regions while manipulating only uncertain ones.

This reduces the need to repeatedly spin the entire cube.

A solved face should remain solved unless new evidence directly invalidates it.

---

## 9. Abstraction at the whole-object dimension

The most important consequence is recursive abstraction.

Once Part A and Part B exist as whole objects, Leviathan can run the Rubik's-cube process against the objects themselves and ask:

> What structural invariant remains when these two complete mechanisms are rotated, compared, and stripped of incidental domain-specific differences?

For example, a memory retrieval mechanism and a supply-chain inventory mechanism may use completely different vocabulary. At the snippet layer, they may appear only weakly related. At the object layer, they may reveal the same geometry:

```text
stored units
        ↓
indexed location
        ↓
demand signal
        ↓
selective retrieval
        ↓
availability validation
        ↓
delivery
        ↓
state update
```

Leviathan can then compile a new higher-order object such as:

```text
Governed Retrieval Pipeline
```

That new abstraction is not a vague sentence summarising both domains. It is a reusable structural object with its own ports, invariants, blockers, and possible applications.

The abstraction can then participate in further assembly and comparison.

---

## 10. Recursive semantic solidification

The process should operate recursively across several levels:

```text
snippets
  → evidence objects
  → functional parts
  → mechanisms
  → subsystems
  → architectures
  → cross-architecture invariants
  → new abstract parts
```

At each level:

- internal complexity is packaged behind a verified external shape;
- provenance remains available;
- uncertainty is localised;
- solved structure is preserved;
- comparison occurs at the highest stable resolution;
- descent happens only when needed.

This is structural compression rather than lossy summarisation.

A summary becomes smaller by discarding detail. A semantic object becomes usable by placing detail behind an inspectable interface.

---

## 11. Proposed object operations

The object layer should eventually support an explicit semantic object algebra.

Candidate operations include:

### Composition

Can Object A connect to Object B while satisfying both objects' latch conditions and invariants?

### Rotation / perspective shift

Does the same object expose a different meaningful interface when viewed from another role, timescale, abstraction level, or causal direction?

### Substitution

Can one object replace another without breaking the surrounding assembly?

### Intersection

Which structure is shared by two or more objects?

### Difference

Which properties, interfaces, or invariants distinguish them?

### Contradiction

Do the objects make mutually incompatible claims or require incompatible world states?

### Decomposition

Can the object be split into smaller stable objects with clearer boundaries?

### Adapter inference

What missing object would reconcile two nearly compatible interfaces?

### Counterfactual mutation

Which changes preserve the object's identity, and which changes cause it to become a different object?

### Abstraction

What invariant relational geometry survives after incidental details are removed?

### Recursive recompilation

When new evidence arrives, which local object, interface, or invariant must be rebuilt?

---

## 12. Compiler pipeline

A first implementation could use an existing LLM for candidate generation while the host governs state, evidence, admissibility, and verification.

### Stage 1: Candidate gathering

Retrieve a bounded pile of potentially relevant material using vectors, metadata, explicit references, and existing Leviathan structures.

### Stage 2: Relation induction

Propose typed relationships between fragments:

- supplies;
- consumes;
- constrains;
- verifies;
- transforms;
- depends on;
- conflicts with;
- instantiates;
- causes;
- updates;
- replaces;
- contains.

### Stage 3: Boundary detection

Determine which material belongs inside the candidate object, which belongs to its environment, and where the object stops.

This is likely one of the hardest stages.

### Stage 4: Functional role assignment

Infer what the object does rather than merely what topic it discusses.

### Stage 5: Interface extraction

Generate candidate ports, latch conditions, gear teeth, blockers, tolerances, and guarantees.

### Stage 6: Invariant discovery

Identify properties that survive wording changes, example substitution, context changes, and permissible internal mutation.

### Stage 7: Adversarial testing

Attempt to break the proposed object:

- remove supporting fragments;
- introduce contradictory evidence;
- swap examples;
- test unseen cases;
- generate alternative boundaries;
- compare competing compilations;
- inspect whether inferred ports are actually supported;
- detect circular justification.

### Stage 8: Object emission

Emit a versioned semantic object with property-level provenance and uncertainty.

### Stage 9: Object registry

Store the object, its history, its dependencies, and the assemblies that currently use it.

### Stage 10: Incremental revalidation

When an object changes, revalidate only directly affected interfaces and assemblies.

---

## 13. Competing object hypotheses

The compiler should not force one authoritative shape when evidence is ambiguous.

A single pile may plausibly compile as:

- one mechanism with three internal stages;
- three cooperating objects;
- one mechanism plus an adapter and verifier;
- two competing implementations of the same function.

Leviathan should retain multiple candidate compilations with:

- support scores;
- contradiction scores;
- unresolved assumptions;
- discriminating tests;
- affected downstream assemblies.

The next reasoning action should favour the probe that eliminates the most uncertainty for the least cost.

This turns Rubik spinning into information-seeking manipulation.

---

## 14. Evidence and trust requirements

The primary danger is producing impressive-looking but unsupported Lego bricks.

Every important object property should retain a receipt:

```text
property
  → supporting evidence
  → observed or inferred status
  → compilation rule or transformation
  → tests survived
  → known counterevidence
```

Required trust principles:

1. **No unsupported hard ports.** A port may be proposed, but it must remain provisional until supported.
2. **No hidden boundary decisions.** Inclusion and exclusion should be inspectable.
3. **No silent provenance loss.** Higher-level abstraction must retain ancestry.
4. **No single-shape coercion.** Competing compilations remain available when uncertainty is real.
5. **No global rebuild by default.** New evidence should trigger the smallest justified recompilation.
6. **No mystical understanding claim.** Understanding is operational: the system can state what the object does, why it has its shape, how it connects, what would break it, and which evidence supports it.

---

## 15. Relationship to existing FMI work

The Semantic Object Compiler does not replace Leviathan's existing organs. It gives them a shared centre of gravity.

Potential relationships include:

- **Semantic Sorter:** candidate gathering, relation discovery, and evidence bucketing;
- **Leviathan retrieval and memory:** granular source substrate and object persistence;
- **Venom Shell:** holding, rotating, and comparing multiple objects simultaneously;
- **Chatty-Cog:** persistent orientation, task state, and host-level coordination;
- **ChattyFactory:** admissibility gates, constraint checking, failure receipts, and verified object promotion;
- **RD Engine / EF Engine:** probe generation, iterative testing, and refinement;
- **Relational Curriculum Geometry:** investigation of how structured relations become internal capabilities;
- **Semantic Signal Alphabet:** possible compact representation of object interfaces and relational forms;
- **Cognition Mesh Test Chamber:** suitability, role-fit, and containment testing for object-producing models;
- **Tool Context Plugs:** declared module identity and affordance surfaces that may serve as manually authored object envelopes.

Much of the required support machinery may already exist in partial form across the FMI ecosystem.

---

## 16. Minimal viable experiment

A first experiment should be small, inspectable, and falsifiable.

### Dataset

Select 30–100 snippets describing one known FMI mechanism. Remove the repo name and expected architecture where practical.

### Compiler output

Require the system to emit:

1. a candidate internal relation graph;
2. proposed object boundaries;
3. typed input and output ports;
4. latch conditions and blockers;
5. invariants;
6. property-level source receipts;
7. at least two competing compilations;
8. a probe that would distinguish those compilations.

### Evaluation tasks

#### Fit detection

Given several other compiled FMI parts, which can connect directly and why?

#### Rejection

Which apparent connections should be rejected without granular descent?

#### Adapter discovery

What missing intermediary would make two near-fitting objects connect?

#### Cross-domain abstraction

Which apparently unrelated mechanism shares the same structural geometry?

#### Incremental update

When one new fragment changes an interface, can the system recompile only the affected region?

#### Provenance audit

Can every emitted property be traced back to supporting evidence and transformation steps?

### Baselines

Compare against:

- plain vector retrieval;
- vector retrieval plus free-form summarisation;
- conventional knowledge-graph extraction;
- full-context LLM reasoning without persistent objects.

---

## 17. Success criteria

The concept should be considered useful only if it produces measurable gains.

Candidate success metrics:

- fewer granular retrieval calls per completed reasoning task;
- fewer total pairwise comparisons;
- lower token and compute cost;
- improved compatibility prediction;
- improved adapter or missing-part discovery;
- better preservation of solved structure;
- stronger cross-domain abstraction;
- higher consistency across repeated runs;
- lower hallucination rate for interfaces and invariants;
- reliable local recompilation after new evidence;
- complete provenance for accepted objects and deductions.

The system should not be judged by whether the objects sound intelligent. It should be judged by whether they reduce work, survive testing, predict fit, support novel deduction, and remain auditable.

---

## 18. Major open problems

### Boundary detection

How does the compiler determine where one semantic object ends and its environment begins?

### Essential versus incidental properties

Which features define the object, and which are merely examples or implementation details?

### Interface canonicalisation

How can domain-specific ports be mapped onto reusable functional types without forcing a rigid ontology too early?

### False solidification

How do we detect a thematic cluster that has been incorrectly rendered as a coherent mechanism?

### Object identity across revisions

At what point does a modified object remain the same object, become a new version, or become a different class entirely?

### Recursive error amplification

How do we prevent a weak first-level compilation from contaminating higher abstractions?

### Scale management

How many active objects and candidate assemblies can Leviathan manipulate before the object layer becomes another combinatorial swamp?

### Discovery of genuinely new abstractions

How do we distinguish a useful structural invariant from a vague generalisation that applies to nearly everything?

### Verification cost

How much adversarial testing is enough before an object can be promoted from provisional to trusted?

---

## 19. Working hypothesis

> The jump from linear semantic vectors to higher-order abstract reasoning occurs when distributed evidence is compiled into persistent, falsifiable relational objects whose boundaries, interfaces, invariants, uncertainty, and provenance are explicitly represented.

The resulting system would not merely retrieve nearby ideas or generate plausible summaries. It would create semantic machinery that can be:

- picked up;
- rotated;
- connected;
- rejected;
- opened;
- tested;
- decomposed;
- abstracted;
- recompiled;
- reused.

Once a novel deduction can itself be compiled into a new persistent object, Leviathan gains the ability to accumulate reusable reasoning structure rather than repeatedly imitating abstract thought inside temporary context windows.

---

## 20. Condensed model

```text
linear vectors
    ↓ locate
related fragments
    ↓ organise
relational graph
    ↓ solidify
semantic object
    ↓ manipulate
object interaction
    ↓ compare
structural deduction
    ↓ verify
novel object
    ↓ persist
expanded reasoning world
```

The quarry remains available beneath the surface.

Leviathan simply stops rebuilding every wall from loose stones each time it needs to enter the room.

