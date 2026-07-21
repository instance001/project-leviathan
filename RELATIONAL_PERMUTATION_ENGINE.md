# Relational Permutation Engine

**Status:** Working architecture hypothesis  
**Purpose:** Host-level mechanism for earned abstract reasoning in a fully realised MCM  
**Related systems:** Tri-helix memory, EF Engine, LLM Semantic Dataset Sorter, lesson library, Janet School, relational curriculum geometry

---

## Core Claim

Abstract reasoning may be achievable at the host level by repeatedly rearranging concrete memories into explicit relational comparisons, preserving the resulting like/not-like evidence as a derived dataset, geometrically sorting that dataset, attacking candidate invariants through the EF loop, and promoting only the structures that survive transfer and boundary testing.

The mechanism does not require the model to produce a complete abstraction in one leap.

It creates the conditions in which abstraction can be earned.

> Memory supplies the blocks.  
> Relational permutation changes their arrangement.  
> Comparison manufactures new relational data.  
> Semantic sorting reveals geometry in that data.  
> EF removes unsupported explanations.  
> The lesson library preserves what survives.

---

## The Rubik's Cube Model

Tri-helix memory becomes an active computational geometry rather than three passive storage temperatures.

### Hot context: movable small blocks

Hot context contains the concrete items currently under scrutiny:

- events
- claims
- methods
- failures
- objects
- examples
- counterexamples
- source spans
- active hypotheses

These are the small cubes being moved.

The system should normally hold only a bounded working set at once: A, B, and possibly C where a third case is required to break a false binary comparison.

### Lukewarm memory: the current cube face

Lukewarm memory is the compressed face-level map of the active comparison.

It records:

- why A and B are being held together
- which comparison vectors have already been applied
- the strongest current likenesses
- the strongest current differences
- contradictions and unresolved questions
- which rotations remain useful
- which cold records should be retrieved next

It is not merely a summary of content. It is a summary of the current relational arrangement.

### Cold memory: the relational ledger

Cold memory stores the outputs of prior rotations:

- A is like B because X
- A is unlike B because Y
- the relation is unknown under vector Z
- the comparison contradicted an earlier claim
- a later case weakened or strengthened the relation
- a proposed invariant remains unresolved
- a prior investigation can be resumed when a comparable case appears

Cold memory is therefore both a vault and a growing derived dataset.

### Lesson library: promoted abstractions

The lesson library stores only abstractions that have survived:

- multiple materially different cases
- relational permutation
- semantic clustering
- EF falsification
- counterexamples
- transfer probes
- boundary tests
- explicit promotion review

A lesson is not a preferred answer or recipe. It is a scoped relational structure with provenance, limits, and unresolved edges.

---

## System Shape

```text
Concrete memories
    |
    v
Hot working set: A + B (+ optional C)
    |
    v
Lukewarm face: current relational map
    |
    v
Relational permutation across multiple vectors
    |
    v
Like / unlike / unknown / contradiction records
    |
    v
Cold relational dataset
    |
    v
Semantic Dataset Sorter
    |
    v
Candidate clusters, separations, outliers, unstable fits
    |
    v
EF Engine: perturb, retry differently, vault, compare, triangulate
    |
    v
Candidate invariant
    |
    v
Transfer + counterexample + boundary probes
    |
    +---- insufficient / contradictory ----> remain unresolved in cold vault
    |
    v
Explicit lesson-promotion gate
    |
    v
Scoped abstraction in lesson library
```

---

## What the Engine Produces

The engine does not primarily produce answers.

It produces **relational observations**.

Example source items:

```text
A: A coding model inferred a product family from an ambiguous request.
B: A coding model substituted a template after the first method failed.
```

Possible derived records:

```text
A is like B under authority ownership because:
- both converted uncertainty into hidden positive authority
- both replaced open search with a familiar implementation shape

A is unlike B under temporal position because:
- A occurred before execution
- B occurred after failure

A is unlike B under mechanism because:
- A used classification
- B used fallback substitution

Candidate invariant:
- unresolved uncertainty creates pressure for a proposing component to seize method authority
```

The external facts were already known.

The explicit relation between them was not previously represented.

That relational product is new internally grounded data.

---

## Relational Permutation

A permutation is a deliberate change in how two or more memories are aligned.

The engine should not compare A and B only once. It should rotate them across multiple vectors.

Possible vectors include:

- role
- function
- cause
- effect
- dependency
- authority
- sequence
- time scale
- abstraction level
- boundary
- failure mode
- success condition
- resource constraint
- uncertainty
- reversibility
- transferability
- scope
- structure
- surface form
- contradiction

These vectors must not become a host-owned ontology of correct conclusions.

They are comparison operators or prompts. They may be:

- proposed by the operator
- proposed by the model
- retrieved from prior successful investigations
- generated through a neutral permutation policy
- rejected when irrelevant

The host schedules, records, deduplicates, and bounds rotations. It does not dictate the substantive conclusion.

---

## Required Comparison Outputs

Every useful rotation should be allowed to emit all four result classes.

### Like

Shared structure supported by evidence.

```text
A is like B because X.
```

### Unlike

A bounded distinction that prevents overgeneralisation.

```text
A is unlike B because Y.
```

### Unknown

Evidence is insufficient.

```text
The relation between A and B under vector Z is unresolved.
```

### Contradiction

The new comparison conflicts with an earlier relation or candidate invariant.

```text
This result contradicts relation R because evidence E does not fit.
```

The unlike, unknown, and contradiction lanes are mandatory.

A system that stores only likeness will analogise everything to everything and mistake resemblance for abstraction.

---

## Canonical Record

```text
RelationalPermutationRecord
- record_id
- trace_id
- source_a_ref
- source_b_ref
- optional_source_c_ref
- source_hashes
- comparison_vector
- vector_provenance
- permutation_operation
- likeness_claims
- difference_claims
- unknown_relations
- contradictions
- supporting_source_spans
- counterexample_refs
- prior_rotation_refs
- ef_evidence_refs
- candidate_invariant
- confidence
- uncertainty_notes
- applicability_scope
- non_applicability_conditions
- created_at
```

Every claim should remain traceable to the original source records and exact spans where possible.

A record is evidence, not truth.

---

## The Semantic Sorter as Geometry Engine

The LLM Semantic Dataset Sorter already provides the machinery needed to sift the derived relational dataset.

For this use, the dataset is not raw documents. It is a collection of `RelationalPermutationRecord` items.

The sorter can run the same relational dataset through different intents:

- shared invariant
- causal dependency
- failure boundary
- authority relation
- temporal structure
- contradiction type
- transferability
- abstraction depth
- unresolved uncertainty
- scope of applicability

### Why frozen bucket plans matter

The sorter should preserve its existing separation:

1. preflight
2. bucket-plan generation
3. frozen plan
4. assignment
5. validation
6. artifact save

The model must not invent new categories halfway through assignment.

This gives the comparison geometry a stable face long enough to inspect it.

### Data-skim versus blind-label

Both genesis modes become useful epistemic probes.

**Data skim**

> What geometry does the accumulated relational evidence suggest?

**Blind label**

> What geometry does the model impose before inspecting the evidence?

The difference between those outputs is itself evidence.

It may expose:

- model-imposed ontology
- stable data-emergent structure
- bucket instability
- overfitting
- missing dimensions
- ambiguous records that repeatedly fall into junk

### Second-order relational data

The sorter can generate structure about the comparison records themselves:

- these likeness claims repeatedly cluster
- these claimed similarities consistently separate
- these unlike records form a stronger group than the original similarity
- this candidate invariant falls into junk under several geometries
- these records change buckets whenever the sorting ontology changes
- this boundary remains stable across multiple sort intents

This is second-order relational data produced from first-order relational data.

---

## EF Engine Role

EF Engine is the falsification and narrowing organ.

It should not promote a lesson after a fixed attempt count.

Its job is to:

- preserve failed comparisons
- require materially different probes
- record what changed
- compare outcomes
- reopen dormant investigations
- triangulate only when evidence supports a shared lock point
- preserve unresolved or contradictory sessions indefinitely
- produce scoped promotion candidates only when warranted

### Vault doctrine

A vault is unresolved evidence, not a waiting room with an automatic expiry.

A vault may remain open for months or years.

A later case can resume the investigation when it produces comparable evidence.

```text
failure
→ vault
→ different probe
    ├─ success: current task succeeds; prior vault remains unless clarified
    ├─ different failure: separate or branching evidence
    └─ comparable recurrence: resume triangulation
```

Attempt count is never sufficient evidence.

Two failures may be unrelated.

Twenty failures may still be too ambiguous.

A single precise deterministic contrast may be more informative than dozens of broad repetitions.

---

## Candidate Invariant

A candidate invariant is a relational schema that appears to survive surface variation.

Example:

```text
Concrete:
A relates to B through R.
C relates to D through R.

Candidate schema:
R(x, y)
```

A valid candidate should state:

- the shared relation
- the variables or roles being abstracted
- supporting cases
- differences already ruled incidental
- known counterexamples
- unresolved cases
- applicability conditions
- non-applicability conditions
- confidence
- provenance

It must not enter the lesson library yet.

---

## Abstraction Promotion Gate

Triangulation can identify a possible invariant.

Transfer determines whether it is an abstraction.

Before promotion, the candidate should face:

### Surface transfer

Does the relation survive when names, objects, wording, or domain surface changes?

### Role substitution

Can different concrete actors occupy the same abstract roles?

### Near transfer

Does the relation hold in a closely related case?

### Far transfer

Does the relation hold in a different domain with the same structure?

### Counterexample

Can the system find a case that appears to fit but breaks the rule?

### Boundary probe

Where does the rule stop applying?

### Composition

Can the candidate combine with another lesson without contradiction?

### Compression

Can the candidate be stated more simply without losing explanatory power?

Promotion should occur only through explicit review.

A candidate may remain dormant, unresolved, contradictory, or insufficient indefinitely.

---

## Lesson Library Entry

```text
LessonRecord
- lesson_id
- abstraction_statement
- variable_roles
- relational_schema
- supporting_case_refs
- counterexample_refs
- failed_probe_refs
- transfer_probe_results
- boundary_conditions
- non_applicability_conditions
- confidence
- unresolved_edges
- source_vault_refs
- sorter_run_refs
- ef_triangulation_refs
- promotion_receipt
- version
- supersedes
- created_at
```

A lesson is not immutable truth.

Future evidence may:

- narrow it
- split it
- weaken it
- contradict it
- supersede it
- return it to unresolved status

---

## Host / Model Authority Split

### Operator

Owns:

- investigation intent
- acceptable scope
- hard constraints
- approval of promoted lessons
- ability to force, pause, reopen, or reject an investigation

### Model

May propose:

- comparison vectors
- permutation operations
- like/not-like claims
- candidate invariants
- counterexamples
- transfer probes
- lesson wording

The model does not own truth or promotion authority.

### Host

Owns:

- memory selection bounds
- provenance
- source integrity
- permutation scheduling
- duplicate-angle prevention
- receipt lineage
- vault persistence
- EF attempt comparison
- sorter-plan freezing
- verification
- promotion gating

The host must not manufacture the substantive abstraction.

### Reality

Determines whether the claimed relation survives evidence.

---

## Anti-Overfitting Rails

The engine must prevent these failure modes:

- similarity-only reasoning
- two-attempt promotion
- broad failure-class blocking
- model-authored success criteria
- lesson promotion without counterexamples
- treating repeated wording as repeated structure
- collapsing unknown into false
- collapsing contradiction into junk
- deleting vaults after a successful retry
- storing successful methods as preferred recipes
- host-owned semantic ontology
- cross-domain transfer claims without actual transfer probes
- abstraction wording that outruns its evidence

---

## Minimal Viable Experiment

The first experiment should be small enough to inspect manually.

### Inputs

Select three to six concrete records from a known FMI development history.

Example domain:

- positive-lane authority leaks in coding agents

### Phase 1: Working set

Place A and B in hot context.

Create a lukewarm face containing:

- exact source summaries
- why they may be comparable
- open questions
- selected comparison vectors

### Phase 2: Permutation

Run at least five materially different vectors:

- authority
- temporal sequence
- failure response
- scope
- uncertainty

Require like, unlike, unknown, and contradiction outputs.

### Phase 3: Derived dataset

Write each output as a `RelationalPermutationRecord`.

### Phase 4: Geometric sift

Feed the records into the semantic sorter.

Run at least:

- one `data_skim` plan
- one `blind_label` plan
- two different sort intents

Compare bucket stability, junk placement, and surprising groupings.

### Phase 5: EF pressure

Choose one candidate invariant.

Probe it using:

- a counterexample
- a materially different case
- a far-domain transfer attempt
- a boundary case

Vault unresolved results.

### Phase 6: Promotion decision

Do not promote automatically.

Produce either:

- a scoped lesson candidate
- an unresolved investigation
- a rejected candidate
- a split candidate requiring two abstractions

---

## Success Criteria

The experiment succeeds if it can demonstrate all of the following:

1. The system creates explicit relational records not present in the source material.
2. Like and unlike evidence both affect the candidate abstraction.
3. The sorter reveals at least one stable or unstable geometric pattern.
4. EF eliminates or narrows at least one candidate explanation.
5. A counterexample or boundary probe changes the abstraction.
6. Every derived claim remains traceable to source evidence.
7. The system can honestly remain unresolved.
8. No lesson is promoted merely because attempts repeated.
9. The final candidate transfers beyond the original surface form, or is rejected for failing to do so.

---

## Research Hypothesis

A fully realised MCM may achieve host-supported abstract reasoning through this cycle:

```text
co-presence
→ relational permutation
→ explicit comparison data
→ geometric semantic sorting
→ falsification and triangulation
→ transfer and boundary testing
→ scoped lesson promotion
→ future retrieval and refinement
```

The novelty is not any single component.

The novelty is the closed loop:

- tri-helix memory holds and revisits cases
- the permutation engine manufactures relational observations
- the sorter discovers geometry in those observations
- EF preserves failure and removes unsupported explanations
- the lesson library stores only earned abstractions
- later use produces new evidence that can refine the lesson

This is a mechanism for producing novel relational knowledge from already known data without pretending that recombination alone guarantees truth.

---

## Short Doctrine

> Hold the cases together.  
> Rotate them deliberately.  
> Record both likeness and difference.  
> Sort the relations, not merely the documents.  
> Attack every candidate invariant.  
> Keep unresolved evidence alive.  
> Promote only what survives transfer and boundaries.
