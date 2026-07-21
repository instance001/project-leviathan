# Assumption Freeze and Worldview Branching

**Status:** Working architecture specification  
**Purpose:** Make worldview, bias, presupposition, and prior interpretation explicit, frozen, comparable, revisable objects inside the MCM  
**Primary related systems:** Tri-Helix Memory, Dual Cold Memory, Why Library, Relational Permutation Engine, EF Engine, Lesson Library, Chatty-Cog, ChattyFactory

---

## Core Claim

A mature memory-and-reasoning system should not only remember:

- what it observed,
- what it concluded,
- and what later happened.

It should also preserve:

- what it believed before the new evidence arrived,
- which worldview produced that belief,
- how deep that assumption ran,
- which parts were confirmed,
- which parts were contradicted,
- and whether the evidence supports updating the current library or branching an alternative one.

The central mechanism is:

```text
freeze prior assumptions
→ process new observation independently
→ compare observation against frozen assumptions
→ record confirmation, contradiction, omission, and residue
→ revise confidence, preserve history, or branch a new library
```

The freeze does **not** mean the assumption is true.

It means:

> This is the exact interpretive frame the system held before the new evidence was metabolised.

That turns invisible bias into inspectable data.

---

## Why This Matters

Without an assumption freeze, a learning system can quietly rewrite its own past.

Typical failure:

```text
old belief
→ new evidence arrives
→ model adapts explanation
→ model acts as though it always held the revised view
```

This destroys the ability to inspect:

- prediction quality,
- bias,
- presupposition,
- worldview drift,
- mistaken confidence,
- retrospective rationalisation,
- self-confirming interpretation loops.

The freeze creates a durable before-and-after boundary.

```text
BEFORE
what the system expected

AFTER
what the evidence supported
```

---

## The Memory Stack

The architecture assumes several memory depths.

```text
HOT MEMORY
active exact items under scrutiny

LUKEWARM MEMORY
current task/thread summary and relational face

WHY LIBRARY
lossy conceptual surface:
what kinds of things exist and why they broadly belong

COLD ATLAS
deeper general shape:
patterns, exceptions, recurring structures, unresolved questions

COLD EVIDENCE LOG
strain-the-brain specifics:
exact cases, details, sequence, directionality, provenance
```

The system can reason cheaply from the library surface when the case is ordinary.

It can descend into deeper levels when:

- the case sits near a boundary,
- exact attribution matters,
- sequence matters,
- a contradiction appears,
- a durable lesson may be promoted,
- a worldview may need revision.

---

## The Three-Level Assumption Freeze

Before the system assimilates a new observation, freeze the active expectation at three depths.

## 1. Surface Assumption

The cheap, lossy, library-level expectation.

Example:

```text
This object probably belongs to the plant domain.
```

This is what the system reaches first.

It is useful precisely because it is compressed.

It is also the layer most vulnerable to bias and overgeneralisation.

---

## 2. General-Shape Assumption

The deeper cold-atlas expectation.

Example:

```text
Known plant-like things usually share:
- growth
- living structure
- environment-dependent development
- recurring biological organisation

Common exceptions and boundary cases:
- not all are green
- not all have leaves
- some superficially plant-like objects are non-living
```

This preserves accumulated variation and exceptions.

---

## 3. Granular Assumption

The exact cold-evidence expectation.

Example:

```text
Specimen A17 was accepted as a plant despite lacking property Q
because evidence E showed a stronger parent-level structure.

Object N4 appeared green but was non-living.

Case B9 was initially misclassified because surface colour
was treated as more important than growth and structure.
```

This level preserves:

- exact cases,
- exact properties,
- exact sequence,
- exact reasons,
- exact exceptions,
- exact mistakes.

---

## Assumption Snapshot

```text
AssumptionSnapshot
- snapshot_id
- created_before_observation
- active_intent
- active_question
- worldview_id
- worldview_version
- surface_assumption
- general_shape_assumption
- granular_assumption_refs
- expected_classification
- expected_relations
- expected_boundaries
- expected_unknowns
- known_alternatives
- known_biases
- supporting_lesson_refs
- supporting_atlas_refs
- supporting_evidence_refs
- confidence
- scope
- provenance
- frozen_at
```

A valid snapshot must be created before the new observation is interpreted against it.

---

## Independent Observation Characterisation

The new observation should first be characterised on its own terms.

The system should avoid immediately forcing it through the active worldview.

Suggested flow:

```text
new observation X
→ extract properties
→ extract roles
→ extract functions
→ extract conditions
→ extract unknowns
→ extract contradictions
→ identify source quality
→ preserve exact evidence
```

This creates an independent observation record.

---

## Observation Record

```text
ObservationRecord
- observation_id
- raw_source_ref
- raw_source_hash
- exact_content
- source_spans
- observed_properties
- observed_absences
- observed_roles
- observed_functions
- observed_conditions
- observed_outcomes
- unresolved_details
- contradictions
- confidence
- provenance
- observed_at
```

The observation record should not inherit the prior classification automatically.

---

## Frame Comparison

Once both sides exist:

```text
Frozen Prior Frame
versus
Independent Observation
```

the relational permutation engine can compare them.

Possible outputs:

```text
Confirmed
Contradicted
Unsupported
PartiallyConfirmed
BoundaryExposed
AssumptionMissing
NovelResidue
AlternativeFrameSupported
Unresolved
```

---

## Assumption Comparison Record

```text
AssumptionComparisonRecord
- comparison_id
- assumption_snapshot_ref
- observation_ref
- confirmed_surface_parts
- contradicted_surface_parts
- confirmed_general_shape_parts
- contradicted_general_shape_parts
- confirmed_granular_parts
- contradicted_granular_parts
- unsupported_prior_parts
- newly_exposed_assumptions
- missing_prior_dimensions
- novel_residue
- boundary_changes
- classification_delta
- worldview_delta
- evidence_refs
- confidence_delta
- unresolved_questions
- created_at
```

---

## Example

### Frozen surface assumption

```text
This object is probably grass.
```

### Frozen general-shape assumption

```text
Grass is usually:
- a plant
- narrow-leaved
- low-growing
- clustered
- rooted
```

### Frozen granular assumption

```text
Known grasses A, B, and C shared:
- plant-level structure P, Q, R
- grass-specific structure G1, G2, G3
```

### New observation

```text
Object X:
- shares P, Q, R
- lacks G1 and G2
- has unknown property Z
```

### Comparison

```text
Surface assumption:
contradicted

General-shape assumption:
partially confirmed

Granular assumption:
supports plant inheritance
does not support grass inheritance

Result:
X is likely a plant.
X is not justified as grass.
Exact subtype remains unresolved.
```

The system can now preserve:

```text
what it expected
what was wrong
what survived
what remains unknown
```

---

## Worldview as a First-Class Object

A worldview is an organised interpretive frame.

It determines:

- which properties are treated as salient,
- which relations are examined first,
- which explanations are considered plausible,
- which boundaries are emphasised,
- which uncertainties are ignored or preserved,
- which evidence is considered decisive,
- which causal structure is assumed.

A worldview should not be hidden inside prompt wording or model weights alone.

At host level, it should be representable and versioned.

---

## Worldview Record

```text
WorldviewRecord
- worldview_id
- name
- version
- core_presuppositions
- preferred_comparison_vectors
- ignored_or_deemphasised_vectors
- domain_scope
- relation_schema_refs
- lesson_library_ref
- atlas_ref
- evidence_policy
- known_biases
- known_strengths
- known_failures
- falsification_conditions
- confidence
- provenance
- created_at
```

---

## Multiple Worldviews

The system should be able to hold more than one worldview.

Example:

```text
Worldview A:
organises objects primarily by function

Worldview B:
organises objects primarily by causal origin

Worldview C:
organises objects primarily by structural composition

Worldview D:
organises events primarily by authority and role
```

The same observation can be processed under each frozen frame.

```text
Observation X
→ interpretation under A
→ interpretation under B
→ interpretation under C
→ interpretation under D
```

Then compare:

```text
What did all frames notice?

What only one frame noticed?

Which conclusion depends on a specific presupposition?

Which frame predicted the evidence better?

Which frame explains more while assuming less?

Which frame preserves uncertainty more honestly?

Which frame exposed a boundary the others flattened?
```

---

## Worldview Comparison Record

```text
WorldviewComparisonRecord
- comparison_id
- observation_ref
- worldview_refs
- shared_noticed_features
- worldview_specific_features
- shared_conclusions
- divergent_conclusions
- presupposition_dependencies
- missed_evidence_by_worldview
- false_positive_by_worldview
- false_negative_by_worldview
- uncertainty_quality
- prediction_quality
- boundary_quality
- explanatory_cost
- unresolved_differences
- evidence_refs
- created_at
```

---

## Why Freeze at Multiple Depths

A surface assumption can be wrong while the deeper worldview remains useful.

Example:

```text
Surface:
This is grass.

General shape:
This is probably a plant.

Granular:
It resembles plant cases but not known grass cases.
```

The correct update is not:

```text
worldview failed
```

It may be:

```text
surface label failed
parent-level structure survived
child-level assumption was overconfident
```

Likewise, the surface label may be correct while the deeper reason is wrong.

Example:

```text
Correct classification:
plant

Wrong reason:
it is green
```

The multi-depth freeze exposes that distinction.

---

## The Why Library

The Why Library is the lossy conceptual surface.

It should not store only labels.

It should store explanatory structures.

Example:

```text
PLANT

Broad why:
- living biological organisation
- growth and development
- environment-dependent processes
- recurring structural patterns

Known subtypes:
- grass
- tree
- moss
- flowering plant

Known false cues:
- green colour alone
- rooted appearance alone
- stationary position alone

Known boundaries:
- non-living imitations
- fungi
- artificial growth-like systems
```

The library is fast because it is compressed.

The deeper cold layers preserve the exact examples beneath it.

---

## Library Versioning

Every library should be versioned.

```text
WhyLibrary
- library_id
- worldview_id
- version
- domain
- concept_records
- relation_records
- unresolved_clusters
- promoted_lessons
- known_counterexamples
- evidence_refs
- created_at
```

A new observation does not silently rewrite the active library.

It proposes:

- a confidence change,
- a lesson revision,
- a concept split,
- a boundary adjustment,
- or an alternative library branch.

---

## Library Branching

Repeated contradiction should not force immediate replacement.

Suggested flow:

```text
Library v1
+ recurring structured contradiction
→ Alternative Library Candidate v2
```

Both can remain active for comparison.

```text
v1 explains cases A, B, C well.
v2 explains cases D, E, F better.
Neither yet dominates across all boundaries.
```

Future observations can be tested against both.

---

## Library Branch Record

```text
LibraryBranchRecord
- branch_id
- parent_library_ref
- candidate_library_ref
- triggering_comparison_refs
- recurring_contradiction_refs
- preserved_parent_lessons
- revised_lessons
- removed_assumptions
- added_assumptions
- unresolved_conflicts
- evaluation_plan
- status
    - proposed
    - experimental
    - active_alternative
    - merged
    - rejected
    - superseded
- created_at
```

---

## Avoiding Self-Sealing Beliefs

A dangerous loop is:

```text
library shapes interpretation
→ interpretation confirms library
→ library grows more confident
```

The assumption freeze breaks this loop.

Required rails:

- freeze before interpretation
- characterise observation independently
- preserve contradictory evidence
- record what the worldview failed to notice
- retain alternative frames
- evaluate prediction quality
- version all library updates
- require evidence for confidence increases
- allow confidence decreases
- never treat repetition alone as truth

---

## Presupposition Discovery

Some assumptions will not be explicitly present before comparison.

They become visible only when evidence breaks them.

Example:

```text
The system classified all prior plants using colour,
but never represented colour as a defining assumption.
```

New evidence:

```text
A non-green plant appears.
```

The comparison exposes:

```text
Hidden presupposition:
plants are green
```

This should become a first-class record.

---

## Presupposition Record

```text
PresuppositionRecord
- presupposition_id
- worldview_ref
- first_exposed_by
- implicit_claim
- evidence_that_exposed_it
- prior_decisions_affected
- known_confirmations
- known_contradictions
- confidence
- scope
- status
    - suspected
    - supported
    - contradicted
    - retired
- created_at
```

---

## Bias Record

Bias should be treated as a repeatable directional tendency.

Example:

```text
The system overweights visible surface properties
and underweights causal or structural evidence.
```

---

## BiasRecord

```text
BiasRecord
- bias_id
- worldview_ref
- directional_tendency
- affected_vectors
- underweighted_vectors
- overweighted_vectors
- supporting_comparisons
- known_effects
- false_positive_patterns
- false_negative_patterns
- mitigation_tests
- confidence
- status
- created_at
```

---

## New Assumptions Become New Comparison Objects

Once an assumption is frozen and represented, it can itself enter the relational cube.

Example:

```text
Assumption A:
plants are green

Assumption B:
plants are living organised systems

Compare under:
- predictive reach
- boundary handling
- false positives
- false negatives
- transfer
- simplicity
- evidence cost
```

The system can reason not only about objects, but about the assumptions used to classify objects.

That is a host-level form of metacognition.

---

## Assumption Libraries

Over time, the system may accumulate an Assumption Library.

This library stores:

- common presuppositions,
- recurring biases,
- worldview strengths,
- worldview blind spots,
- domain-specific assumptions,
- assumptions that repeatedly failed,
- assumptions that remained useful under pressure.

This is distinct from the Why Library.

```text
WHY LIBRARY
what kinds of things exist and why

ASSUMPTION LIBRARY
how interpretive frames shape what the system expects and notices
```

---

## Assumption Library Record

```text
AssumptionLibraryRecord
- record_id
- assumption_or_bias_ref
- domain
- worldview_refs
- supporting_cases
- contradiction_cases
- boundary_conditions
- predictive_history
- known_blind_spots
- confidence
- unresolved_edges
- version
- created_at
```

---

## Full Cognitive Cycle

```text
experience accumulates
→ why-library forms
→ cold atlas forms
→ exact cold evidence accumulates
→ worldview emerges
→ assumptions become active
→ assumptions are frozen
→ new observation arrives
→ observation is characterised independently
→ frame comparison occurs
→ confirmation / contradiction / residue recorded
→ confidence changes
→ presuppositions become visible
→ bias records accumulate
→ current library updates or alternative library branches
→ future observations test both
```

---

## Relationship to Relational Permutation

The permutation engine now operates on more than concrete A and B.

Possible comparison objects include:

- object A
- object B
- lesson A
- lesson B
- assumption A
- assumption B
- worldview A
- worldview B
- library version A
- library version B
- observation versus expectation
- old interpretation versus revised interpretation

This greatly expands the system’s reasoning space.

The host must still bound comparisons to avoid combinatorial explosion.

---

## Relationship to EF Engine

EF provides contradiction, retry, and triangulation discipline.

For assumptions:

```text
assumption
→ prediction
→ observation
→ mismatch
→ vault
→ materially different probe
→ compare
→ narrow assumption
→ preserve unresolved remainder
```

EF should not automatically destroy an assumption after one contradiction.

It should determine:

- whether the contradiction is genuine,
- whether the scope was wrong,
- whether the evidence is poor,
- whether the assumption needs narrowing,
- whether an alternative worldview explains better.

---

## Relationship to the Lesson Library

A lesson can become an active assumption later.

Example:

```text
Lesson:
private fields do not prove authority safety

Active assumption in a new audit:
this design may still allow authority bypass despite private fields
```

The assumption must be frozen before the audit result.

Then the system can measure whether the lesson predicted the new case accurately.

This creates a performance history for lessons.

---

## Lesson Prediction Record

```text
LessonPredictionRecord
- prediction_id
- lesson_ref
- assumption_snapshot_ref
- target_observation_ref
- predicted_relation
- predicted_boundary
- prediction_time
- outcome
- accuracy
- overreach
- missed_detail
- confidence_delta
```

---

## Relationship to ChattyFactory

ChattyFactory can freeze assumptions before work begins.

Examples:

```text
Surface:
This task probably resembles a prior patch.

General shape:
Tasks of this type usually fail through authority leakage.

Granular:
Three prior cases failed because payload lineage was not enforced.
```

Then the new build or audit runs.

Afterward:

```text
Which assumptions were correct?
Which were too broad?
Which exact precedent mattered?
Which worldview caused a mistaken method?
Should the factory library update or branch?
```

This gives the Factory the ability to reason about its own expectations.

---

## Relationship to Chatty-Cog

Chatty-Cog can expose assumption state to the operator.

Possible surfaces:

### Active Assumptions Panel

Shows:

- current surface assumption
- current deeper assumption
- exact precedents
- confidence
- known alternatives
- source library version

### Freeze Assumptions Action

Creates a signed snapshot before:

- tool use
- build execution
- audit
- classification
- lesson promotion
- major reasoning branch

### Compare With Outcome

Shows:

- confirmed
- contradicted
- unsupported
- hidden presuppositions
- worldview delta
- possible new library branch

### Library Branch Viewer

Shows competing interpretations side by side.

---

## Minimal Viable Prototype

Start small.

### Domain

Use one narrow domain:

```text
ChattyFactory authority and provenance failures
```

### Inputs

Collect:

- 20–50 exact historical cases
- 5–10 why-library lessons
- 5–10 cold-atlas summaries
- exact cold evidence links
- at least two competing interpretive frames

### Prototype flow

1. Select a new audit case.
2. Freeze:
   - surface assumption
   - general-shape assumption
   - granular precedent assumptions
3. Characterise the case independently.
4. Compare observation against frozen assumptions.
5. Record:
   - confirmations
   - contradictions
   - unsupported assumptions
   - newly exposed presuppositions
   - novel residue
6. Update confidence.
7. Propose:
   - no change
   - lesson revision
   - narrower scope
   - alternative worldview
   - new library branch
8. Preserve all versions.

---

## Prototype File Shape

```text
memory/
  assumptions/
    snapshots.jsonl
    comparisons.jsonl
    presuppositions.jsonl
    biases.jsonl
  worldviews/
    worldviews.jsonl
    worldview_comparisons.jsonl
  libraries/
    why_libraries.jsonl
    branches.jsonl
    revisions.jsonl
  predictions/
    lesson_predictions.jsonl
```

---

## Prototype API Sketch

```text
freeze_assumptions(context, worldview_ref, library_ref)
record_observation(source)
compare_observation_to_snapshot(snapshot_ref, observation_ref)
record_presupposition(comparison_ref)
record_bias(comparison_refs)
propose_library_revision(comparison_refs)
propose_library_branch(parent_library_ref, evidence_refs)
evaluate_worldviews(observation_ref, worldview_refs)
promote_or_reject_revision(candidate_ref)
```

---

## Required Tests

### Temporal integrity

- assumption snapshot exists before observation interpretation
- later edits cannot rewrite the original frozen snapshot
- prediction timestamp precedes outcome reveal

### Depth integrity

- surface, general, and granular assumptions remain distinct
- surface failure does not automatically invalidate deeper structure
- granular contradiction can revise a general summary

### Evidence integrity

- every assumption links to supporting memory
- every contradiction links to exact evidence
- library revisions preserve old versions
- branch creation does not delete the parent

### Bias detection

- hidden presuppositions can be surfaced
- repeated directional failures create bias candidates
- bias candidates remain provisional until supported

### Worldview comparison

- same observation can be processed under multiple frames
- frame-specific conclusions remain separate
- common conclusions can be identified
- unsupported frame conclusions are recorded

### Honesty

- unresolved comparison remains unresolved
- contradictory worldviews can coexist
- no forced winner is required
- missing evidence is surfaced

### Integration

- Why Library assumptions can be frozen
- Cold Atlas assumptions can be frozen
- Cold Evidence assumptions can be frozen
- Relational Permutation can compare assumptions
- EF can challenge assumptions
- Library branching can consume comparison evidence

---

## Success Criteria

The mechanism is useful if it can demonstrate:

1. The system preserves what it believed before new evidence.
2. Surface, general, and granular assumptions can diverge.
3. Hidden presuppositions become visible through contradiction.
4. Worldview-dependent interpretation can be measured.
5. Library updates become versioned and auditable.
6. Alternative libraries can coexist without forced collapse.
7. Prediction quality can be tracked over time.
8. The system can revise confidence without rewriting history.
9. Bias becomes an inspectable object rather than an invisible influence.
10. Assumptions themselves can enter future comparison and learning loops.

---

## Failure Modes

### Assumption freeze becomes truth freeze

The system treats the frozen belief as authoritative.

**Rail:** freeze records prior state only.

### Post-hoc reconstruction

The system creates the snapshot after seeing the result.

**Rail:** enforce temporal ordering and immutable timestamps.

### Worldview explosion

Every disagreement creates a new library.

**Rail:** branching requires recurring structured contradiction.

### Self-confirming library

The active worldview controls both interpretation and evaluation.

**Rail:** independent observation characterisation and alternative frames.

### Bias overdiagnosis

One mistake becomes a bias record.

**Rail:** bias requires repeatable directional evidence.

### Summary collapse

All three assumption depths are merged.

**Rail:** preserve separate fields and evidence paths.

### Forced worldview winner

The system chooses one frame despite unresolved evidence.

**Rail:** allow active alternatives.

### History rewrite

Library updates erase prior assumptions.

**Rail:** immutable versions and revision records.

---

## Computational Cost

This architecture increases cost because each important observation may require:

- assumption freeze
- independent characterisation
- multi-depth comparison
- worldview comparison
- evidence retrieval
- EF pressure
- library revision evaluation

The first prototype should accept this expense.

Its purpose is to discover:

- which comparison depths matter,
- which worldview comparisons produce useful information,
- which assumptions can be frozen cheaply,
- when exact detail is necessary,
- how often branching is justified.

Later optimisations may include:

- cheap surface freeze by default
- deeper freeze only for high-stakes cases
- cached worldview comparisons
- bounded alternate-frame count
- small-model assumption extraction
- stronger-model disputed comparison
- operator-pinned worldview sets
- dormant library branches

---

## Short Doctrine

> Freeze what was believed.  
> Observe independently.  
> Compare belief against reality.  
> Preserve what survived.  
> Expose what was assumed.  
> Branch when recurring contradiction earns an alternative.  
> Never rewrite the past to make the present look inevitable.

---

## Final Architecture

```text
ACCUMULATED EXPERIENCE
        ↓
WHY LIBRARY
lossy conceptual surface
        ↓
COLD ATLAS
general historical shape
        ↓
COLD EVIDENCE
exact precedent
        ↓
ACTIVE WORLDVIEW
current interpretive frame
        ↓
THREE-LEVEL ASSUMPTION FREEZE
surface / general / granular
        ↓
NEW OBSERVATION
characterised independently
        ↓
RELATIONAL FRAME COMPARISON
confirmed / contradicted / unsupported / residue
        ↓
PRESUPPOSITION AND BIAS DISCOVERY
        ↓
EF PRESSURE
        ↓
LIBRARY REVISION OR BRANCH
        ↓
FUTURE OBSERVATIONS TEST COMPETING FRAMES
```

This gives the MCM a mechanism for not only learning what the world contains, but tracking how its own accumulated worldview shapes what it expects to see.

It can remember:

- what it knew,
- why it believed it,
- what it expected,
- which frame produced that expectation,
- how reality differed,
- and whether a new conceptual library is beginning to form.
