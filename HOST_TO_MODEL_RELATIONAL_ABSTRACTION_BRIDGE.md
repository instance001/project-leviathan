# Host-to-Model Relational Abstraction Bridge

**Status:** Working architecture and experimental specification  
**Purpose:** Convert host-generated relational reasoning traces into staged training curricula that may teach models cleaner abstract reasoning internally  
**Primary related systems:** Relational Permutation Engine, Tri-Helix Memory, EF Engine, LLM Semantic Dataset Sorter, Relational Curriculum Geometry, Janet School, lesson library

---

## Core Claim

A host can support abstract reasoning by holding concrete cases together, rotating them across relational vectors, preserving like/not-like/unknown/contradiction evidence, sorting that evidence geometrically, and using EF-style falsification to isolate candidate invariants.

Relational Curriculum Geometry provides a second path:

> Take the validated formation trails of those abstractions and arrange them as model-training curricula.

The goal is not merely to train a model on finished lessons.

The goal is to train it on the **geometry of abstraction formation**:

- which cases were held together
- which comparison vectors were applied
- which similarities survived
- which differences prevented overgeneralisation
- which candidate rules failed
- which counterexamples narrowed the boundary
- which relations transferred across surface changes
- which uncertainties remained unresolved

This creates a bridge from host-supported cognition to model-internalised relational skill.

---

## Two Levels of Abstract Reasoning

### Level 1: Host-supported abstraction

The host supplies external cognitive structure.

```text
memory cases
→ co-presence
→ relational permutation
→ explicit like / unlike / unknown / contradiction data
→ semantic sorting
→ EF falsification and triangulation
→ transfer and boundary probes
→ scoped lesson
```

The model participates by proposing comparisons, hypotheses, and methods, but the host preserves truth, provenance, boundaries, and unresolved evidence.

### Level 2: Model-internalised abstraction

The validated relational records and formation trails become staged training material.

```text
concrete pair
→ explicit relation
→ controlled contrast
→ altered surface
→ near transfer
→ far transfer
→ counterexample
→ boundary
→ composition
→ abstraction candidate
```

The training hypothesis is that models exposed to this geometry may develop cleaner internal relational handles and require less host scaffolding for some abstract tasks.

The host does not disappear.

It remains the memory, verification, audit, and correction layer.

---

## Full Closed Loop

```text
TRI-HELIX MEMORY
holds concrete experiences across timescales
        ↓
RELATIONAL PERMUTATION ENGINE
rotates cases across multiple vectors
        ↓
RELATIONAL DATASET
stores like / unlike / unknown / contradiction records
        ↓
SEMANTIC DATASET SORTER
discovers clusters, boundaries, outliers, and unstable fits
        ↓
EF ENGINE
vaults failures, compares materially different probes,
narrows lock points, preserves unresolved investigations
        ↓
LESSON LIBRARY
stores only earned, scoped abstractions
        ↓
CURRICULUM COMPILER
packages concrete cases, relations, failures, transfers,
counterexamples, boundaries, and unresolved states
        ↓
RELATIONAL CURRICULUM GEOMETRY
orders and groups the training material deliberately
        ↓
MODEL TRAINING / FINE-TUNING
attempts to internalise relational comparison skill
        ↓
JANET SCHOOL / TEST CHAMBER
tests abstraction, transfer, boundaries, uncertainty,
role discipline, tool discipline, and multithread reasoning
        ↓
FAILURE EVIDENCE
returns to the host-level memory, permutation, sorter, and EF loop
```

The system therefore becomes longitudinal.

Each model generation can produce evidence that improves the next curriculum.

---

## What Must Be Taught

A model should not only see answers.

It should see the **relational operations that produced justified answers**.

### Co-presence

The curriculum should teach the model to hold multiple concrete cases together without prematurely collapsing them.

Example:

```text
Case A
Case B
Question: Why are these being compared?
```

### Similarity

The model should identify shared structure with evidence.

```text
A is like B because X.
```

### Difference

The model should identify distinctions that limit the abstraction.

```text
A is unlike B because Y.
```

### Unknown

The model should preserve unresolved relations.

```text
The relation under vector Z is not supported by current evidence.
```

### Contradiction

The model should detect when a new case conflicts with an earlier invariant.

```text
Candidate rule R does not explain case C.
```

### Variable binding

The model should learn to replace concrete surface nouns with abstract roles.

```text
A relates to B through R.
C relates to D through R.

Candidate:
R(x, y)
```

### Transfer

The model should apply the same relation under changed surface conditions.

### Boundary detection

The model should identify where the relation stops applying.

### Revision

The model should weaken, split, or reject an abstraction when evidence requires it.

---

## Why Finished Lessons Are Not Enough

Training only on final rules risks teaching:

- answer imitation
- slogan memorisation
- overconfident generalisation
- missing provenance
- hidden boundary conditions
- brittle transfer
- inability to surface uncertainty
- inability to revise a rule

A relational curriculum should preserve the **formation trail**.

Example:

```text
Initial candidate:
All failed retries with the same error share the same root cause.

Counterexample:
Two retries produce the same surface error from different missing dependencies.

Revised candidate:
Matching surface errors are comparison signals, not proof of a shared cause.

Boundary:
A shared root cause may be inferred only when materially different probes
preserve a narrower common lock point.
```

The model sees:

1. the initial generalisation
2. the counterexample
3. the reason it failed
4. the revised abstraction
5. the boundary condition

This teaches correction, not merely conclusion.

---

## Curriculum Geometry

The same content can be arranged in different geometries.

### Random baseline

Examples are cleaned but randomly ordered.

Purpose:

- establish ordinary exposure baseline
- measure whether geometry adds anything beyond content

### Domain-grouped baseline

Examples are grouped by topic.

Purpose:

- test whether broad semantic proximity alone helps

### Complexity curriculum

Examples are grouped by topic and ordered from simple to complex.

Purpose:

- test prerequisite staging

### Full relational curriculum

Examples are arranged by:

- concrete case
- paired comparison
- relation type
- similarity
- difference
- unknown state
- contradiction
- boundary case
- uncertainty level
- role structure
- tool-use relevance
- transfer distance
- abstraction depth
- composition dependency

Purpose:

- test whether models internalise relational structure more cleanly

---

## The Curriculum Compiler

The curriculum compiler is the bridge between host reasoning records and model-training data.

It should consume:

- raw source cases
- `RelationalPermutationRecord` items
- sorter run artifacts
- EF vault entries
- triangulation sessions
- candidate invariants
- counterexample records
- transfer probe results
- boundary probe results
- promoted lesson records
- unresolved investigations

It should emit training-ready examples in multiple forms.

---

## Canonical Source Records

### ConcreteCaseRecord

```text
ConcreteCaseRecord
- case_id
- source_type
- raw_text
- source_hash
- source_spans
- domain
- context
- actors_or_roles
- observed_outcome
- uncertainty
- provenance
```

### RelationalPermutationRecord

```text
RelationalPermutationRecord
- record_id
- source_a_ref
- source_b_ref
- optional_source_c_ref
- comparison_vector
- likeness_claims
- difference_claims
- unknown_relations
- contradictions
- supporting_source_spans
- candidate_invariant
- confidence
- applicability_scope
- non_applicability_conditions
- provenance
```

### EFInvestigationRecord

```text
EFInvestigationRecord
- investigation_id
- source_attempt_refs
- vault_refs
- retry_deltas
- materially_different_probe_refs
- shared_lock_candidate
- unresolved_conflicts
- triangulation_status
- confidence
- promotion_eligibility
```

### LessonRecord

```text
LessonRecord
- lesson_id
- abstraction_statement
- variable_roles
- relational_schema
- supporting_cases
- counterexamples
- transfer_results
- boundary_conditions
- unresolved_edges
- source_vault_refs
- promotion_receipt
- version
```

---

## Training Example Families

These are dataset packaging shapes, not host routing families.

They exist only as explicit curriculum record formats.

### 1. Direct comparison example

```text
Input:
Case A
Case B
Comparison vector: authority

Target:
- likenesses
- differences
- unknowns
- evidence spans
```

Purpose:

- basic relational discrimination

### 2. Missing relation example

```text
Input:
Case A
Case B

Target:
The evidence is insufficient to determine relation R.
```

Purpose:

- uncertainty preservation

### 3. Counterexample correction

```text
Input:
Candidate invariant
Supporting cases
Counterexample

Target:
- why the invariant fails
- revised scope
- unresolved remainder
```

Purpose:

- anti-overfitting and revision

### 4. Near transfer

```text
Input:
Known relational schema
New case with similar surface

Target:
- whether the relation transfers
- exact mapping of roles
- confidence
```

Purpose:

- controlled transfer

### 5. Far transfer

```text
Input:
Known schema from domain A
Case from domain B

Target:
- role mapping
- structural similarity
- surface differences
- transfer verdict
```

Purpose:

- abstract role reuse

### 6. Boundary probe

```text
Input:
Candidate invariant
Case near the applicability boundary

Target:
- applies / does not apply / unresolved
- boundary explanation
```

Purpose:

- scope discipline

### 7. Composition example

```text
Input:
Lesson A
Lesson B
Composite task

Target:
- compatible relations
- conflicts
- combined abstraction
```

Purpose:

- multithread reasoning

### 8. False analogy example

```text
Input:
Two superficially similar cases

Target:
- why the analogy fails
- which surface cues were misleading
```

Purpose:

- prevent resemblance collapse

### 9. Contradiction preservation

```text
Input:
Two high-quality records that disagree

Target:
- preserve both
- identify the disagreement
- avoid forced resolution
```

Purpose:

- honest unresolved state

### 10. Formation-trace reconstruction

```text
Input:
Concrete cases and probe outcomes

Target:
Reconstruct:
- candidate invariant
- failed hypothesis
- counterexample
- revised abstraction
- boundary
```

Purpose:

- teach the actual abstraction process

---

## Ordering Rules

The curriculum should not simply group similar examples.

It should stage dependencies.

### Suggested ladder

```text
1. recall concrete facts
2. identify one relation
3. distinguish like from unlike
4. preserve unknown
5. detect contradiction
6. bind abstract roles
7. perform near transfer
8. perform cross-representation transfer
9. handle counterexample
10. identify boundary
11. compose multiple relations
12. propose abstraction candidate
13. revise abstraction
14. perform far transfer
```

This ladder should remain testable rather than doctrinally assumed.

---

## Adjacency Rules

Training order can encode relational proximity.

Examples that may be placed adjacent:

- positive case beside counterexample
- successful transfer beside failed transfer
- broad rule beside boundary case
- confident answer beside uncertainty-preserving answer
- model-overreach case beside role-disciplined case
- tool-use success beside tool-use refusal
- same relation across different domains
- same surface wording with different underlying structure
- different wording with the same underlying structure

The hypothesis is that adjacency may teach contrast and relation more efficiently than isolated exposure.

---

## Separation Rules

Some examples should be deliberately separated.

Purpose:

- test whether the relation survives distance
- prevent simple local memorisation
- test long-range relational handles
- distinguish learned structure from adjacency dependence

Example:

```text
lesson formation trace
... many unrelated examples ...
far-domain transfer probe
```

If performance collapses only when the pair is separated, the model may have learned local association rather than a durable abstraction.

---

## Curriculum Faces

The Rubik-style host mechanism can generate different curriculum faces from the same source material.

### Similarity face

Emphasises:

- shared structure
- analogies
- common causal roles

### Difference face

Emphasises:

- boundaries
- exceptions
- non-equivalence
- false analogies

### Uncertainty face

Emphasises:

- missing evidence
- weak confidence
- unresolved relations
- clarification need

### Contradiction face

Emphasises:

- incompatible claims
- revision
- competing explanations
- suspended judgement

### Transfer face

Emphasises:

- role substitution
- domain changes
- surface variation
- invariant survival

### Composition face

Emphasises:

- multiple concurrent relations
- conflict resolution
- role separation
- multithread handling

A full curriculum should include all faces.

---

## Semantic Sorter Role

The LLM Semantic Dataset Sorter can geometrically sift host-generated relational records before curriculum packaging.

Possible sort intents:

- relation type
- abstraction depth
- transfer distance
- failure boundary
- contradiction type
- uncertainty state
- role structure
- tool-use discipline
- authority leakage
- compositional dependency
- curriculum prerequisite
- counterexample strength

The sorter can produce:

- stable clusters
- unstable clusters
- outliers
- weak-fit records
- junk records
- surprising groupings
- candidate bridge examples
- possible missing curriculum regions

### Data-skim use

Ask:

> What geometry emerges from the relational records?

### Blind-label use

Ask:

> What geometry does the model impose before seeing the records?

The divergence between these plans becomes model-bias evidence.

---

## Training Pack Construction

Each training pack should preserve provenance.

```text
training_pack/
  manifest.json
  curriculum_plan.json
  source_cases.jsonl
  relation_records.jsonl
  formation_traces.jsonl
  counterexamples.jsonl
  transfer_probes.jsonl
  boundary_probes.jsonl
  unresolved_cases.jsonl
  lesson_records.jsonl
  ordering.jsonl
  evaluation_links.json
```

### Manifest fields

```text
TrainingPackManifest
- pack_id
- source_dataset_hashes
- source_repo_versions
- sorter_run_refs
- EF investigation refs
- lesson-library snapshot
- total_tokens
- example_counts
- curriculum_geometry
- random_seed
- contamination notes
- known limitations
```

---

## Curriculum Variants

For a controlled experiment, generate multiple packs containing the same semantic content.

### Variant A: Random

- random order
- no explicit relational staging

### Variant B: Grouped

- grouped by domain
- no explicit abstraction ladder

### Variant C: Complexity

- grouped and ordered basic to complex

### Variant D: Full relational

- staged comparisons
- contrasts
- unknowns
- contradictions
- transfer
- counterexamples
- boundaries
- composition
- formation traces

### Variant E: Relational without failures

- removes failed hypotheses and rejected abstractions

Purpose:

- test whether learning from failure trajectories matters

### Variant F: Similarity-only

- removes unlike and contradiction examples

Purpose:

- test whether negative relational evidence prevents overgeneralisation

### Variant G: Final-lessons only

- includes promoted lessons but omits formation trails

Purpose:

- test whether the process matters beyond the conclusion

These ablations are critical.

---

## Model-Level Hypotheses

A model trained on full relational geometry may show:

- better abstraction transfer
- better boundary detection
- less analogy overreach
- better uncertainty calibration
- cleaner role separation
- better multithread comparison
- lower prompt-scaffolding dependence
- better tool-use discipline
- more legible failure patterns
- stronger correction after counterexamples
- reduced confidence on unsupported generalisations

These are hypotheses, not promised outcomes.

---

## Evaluation Battery

Evaluation should measure behavioural change rather than broad benchmark prestige.

### 1. Relation extraction

Can the model identify shared and differing structure?

### 2. False analogy rejection

Can it reject superficial resemblance?

### 3. Unknown preservation

Can it remain unresolved when evidence is insufficient?

### 4. Counterexample revision

Does it narrow or reject a rule after contradiction?

### 5. Near transfer

Can it apply a relation under moderate surface change?

### 6. Far transfer

Can it map abstract roles across domains?

### 7. Boundary detection

Can it identify non-applicability conditions?

### 8. Composition

Can it combine multiple lessons without collapsing roles?

### 9. Multithread retention

Can it hold user intent, tool limits, uncertainty, prior failure, and output requirements separately?

### 10. Role discipline

Does it behave as one team member rather than seizing all authority?

### 11. Tool discipline

Does it invoke tools only when appropriate and respect explicit tool boundaries?

### 12. Calibration

Does confidence track evidence quality?

### 13. Formation-trace reconstruction

Can it infer a justified abstraction from raw cases and probe outcomes?

### 14. Adversarial abstraction

Can it resist a misleading but plausible candidate rule?

---

## Janet School Bridge

Janet School can act as the model-level classroom and evaluator.

Suggested signal ladder:

```text
recall
→ rule use
→ near transfer
→ cross-representation
→ composition
→ abstraction candidate
→ counterexample
→ boundary
→ revision
```

The same curriculum concepts used in training should be probed independently during evaluation.

The evaluator must not merely ask whether the final answer is correct.

It should inspect:

- relation mapping
- uncertainty
- role separation
- evidence binding
- revision behaviour
- boundary awareness
- transfer distance
- failure legibility

---

## Test Chamber Bridge

The Cognition Mesh Test Chamber can evaluate suitability rather than leaderboard rank.

Possible outcomes:

- READY
- READY WITH GUARDRAILS
- RESTRICTED
- NOT SUITABLE

The chamber can test whether relational-curriculum models are appropriate for:

- planning
- summarisation
- tool use
- bookkeeping
- bounded coding
- comparison
- abstraction support
- cross-model collaboration

Poor abstraction transfer should not mean model disposal.

It should inform role placement and future curriculum needs.

---

## Feedback Loop

Every evaluation run should feed evidence back into the host.

```text
model answer
→ evaluator receipt
→ failure or success record
→ tri-helix memory
→ relational permutation
→ semantic sort
→ EF investigation
→ curriculum update candidate
```

Examples:

- recurring false analogies become contrast examples
- weak uncertainty surfacing becomes unresolved-state training
- role overreach becomes authority-boundary curriculum
- tool misuse becomes explicit positive/negative tool-use pairs
- transfer success becomes a candidate bridge example
- boundary failure becomes a new edge case

No single model failure should automatically become curriculum law.

The same vault and triangulation discipline applies.

---

## Curriculum Promotion Gate

New training material should not enter the canonical curriculum automatically.

A curriculum addition should include:

- source evidence
- reason for inclusion
- relation type
- intended lesson
- known ambiguity
- counterexamples
- expected behavioural effect
- evaluation probe
- scope
- approval receipt

Possible dispositions:

- accepted
- rejected
- unresolved
- experiment-only
- watchlist
- superseded

---

## Preventing Curriculum Folklore

The training pipeline must avoid converting noisy failures into doctrine.

Hard rules:

- no two-failure automatic lesson creation
- no broad failure-label curriculum generation
- no success-method recipe accumulation
- no deleting contradictory records
- no hiding junk or weak-fit examples
- no claiming transfer without cross-domain evidence
- no replacing unresolved with false
- no role-authority lesson without explicit authority evidence
- no preferred software family ontology
- no model-generated curriculum accepted without host review
- no benchmark optimisation that bypasses the target behaviour

---

## Minimal Viable Experiment

### Domain

Start with a narrow domain where relations and boundaries can be inspected manually.

Recommended:

```text
basic programming, debugging, and tool-use discipline
```

### Source material

Create 200–500 examples containing:

- concrete coding cases
- correct and incorrect debugging paths
- tool-use decisions
- uncertainty cases
- role-boundary cases
- positive-lane authority leaks
- counterexamples
- near-transfer pairs
- far-transfer pairs
- unresolved cases

### Host processing

1. Hold selected cases in tri-helix memory.
2. Run relational permutations.
3. Write like/unlike/unknown/contradiction records.
4. Sort the records geometrically.
5. Run EF probes on candidate invariants.
6. Promote only well-supported lesson records.

### Curriculum packs

Build at least:

- random baseline
- domain-grouped baseline
- complexity curriculum
- full relational curriculum
- similarity-only ablation
- final-lessons-only ablation

Keep:

- token count
- source content
- model size
- training settings
- contamination controls

as equal as practical.

### Evaluation

Use held-out cases for:

- relation extraction
- false analogy rejection
- uncertainty
- tool discipline
- role discipline
- near transfer
- far transfer
- boundary detection
- counterexample revision
- multithread reasoning

---

## Success Criteria

The experiment provides positive evidence if the full relational curriculum produces repeatable improvements over controlled baselines in several target behaviours.

Minimum useful signal:

1. Better far-transfer performance than random and grouped baselines.
2. Better boundary-case handling.
3. Lower unsupported-confidence rate.
4. Better false-analogy rejection.
5. Better role and tool discipline.
6. More legible failure explanations.
7. Reduced prompt scaffolding needed to elicit relational comparison.
8. Improvement persists across multiple seeds or runs.

A single benchmark gain is insufficient.

---

## Falsification Criteria

The hypothesis should be weakened if:

- relational ordering shows no repeatable advantage
- improvements vanish under seed changes
- gains come only from duplicated content or token imbalance
- final-lessons-only performs identically to formation-trace curricula
- similarity-only performs as well as full like/unlike/contradiction training
- gains do not transfer outside the training domain
- models merely copy relation vocabulary without improved behaviour
- random order performs equivalently under controlled conditions

Negative results should enter the research vault.

They should not be smoothed over.

---

## Research Questions

1. Does explicit like/not-like training improve abstraction transfer?
2. Are counterexample trajectories more useful than final corrected lessons alone?
3. Does preserving unresolved relations improve calibration?
4. Does curriculum adjacency teach stronger relations than random exposure?
5. Does separating related examples test durable abstraction rather than local association?
6. Can models internalise variable-bound relation schemas?
7. Does relational training improve multithread reasoning?
8. Does it reduce authority overreach?
9. Does it improve tool discipline?
10. Do smaller models benefit more than larger models from structured geometry?
11. Does the sorting model imprint its own classification taste onto the student?
12. Can multiple sorter models produce meaningfully different curriculum geometries?
13. Which relational vectors transfer best across domains?
14. How much host scaffolding remains necessary after training?

---

## Architecture Boundary

This bridge must preserve the authority split.

### Operator

Owns:

- training intent
- curriculum constraints
- inclusion approval
- evaluation priorities
- acceptance of results

### Model

May propose:

- relation labels
- comparison vectors
- curriculum groupings
- candidate lessons
- probe examples
- transfer mappings

The model does not own curriculum truth.

### Host

Owns:

- source provenance
- record integrity
- curriculum compilation
- geometry freezing
- token accounting
- experiment controls
- evaluation receipts
- failure vaults
- promotion gates

The host must not turn one sorter’s ontology into universal truth.

### Reality

Determines whether the model behaviour actually improves.

---

## Short Doctrine

> The host discovers and verifies relational structure.  
> The curriculum compiler preserves how that structure was earned.  
> Training exposes the model to the formation geometry, not only the final rule.  
> Evaluation tests whether the model internalised transferable relations.  
> Failure returns to the host as new evidence.

---

## Final Hypothesis

A model may learn cleaner abstract reasoning when its training data preserves and stages the relational geometry through which abstractions are formed.

The proposed path is:

```text
host-supported relational reasoning
→ verified relational records
→ geometrically sorted datasets
→ staged relational curriculum
→ model training
→ abstraction and transfer evaluation
→ failure evidence returned to the host
```

This does not assume that ordering data automatically creates abstract intelligence.

It creates a falsifiable mechanism for testing whether abstraction-supporting structure can migrate from an external cognitive host into the learned behaviour of a model.
