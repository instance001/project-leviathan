# Semantic Assimilation and Why Library

**Status:** Working architecture specification  
**Purpose:** Define how repeated observations become accumulated, multilevel, evidence-backed conceptual knowledge inside the MCM  
**Primary related systems:** Tri-Helix Memory, Dual Cold Memory, Relational Permutation Engine, LLM Semantic Dataset Sorter, EF Engine, Assumption Freeze, Worldview Branching, Cognitive Economy Governor, Lesson Library, Chatty-Cog, ChattyFactory

---

## Core Claim

A reasoning system does not gain useful abstract knowledge merely by storing observations.

It needs a mechanism that can:

- characterise each new observation;
- compare it against accumulated knowledge;
- sort the resulting explanations into semantic “why” structures;
- inherit only the parent-level properties supported by evidence;
- exclude unsupported child-level classifications;
- preserve unresolved differences;
- and allow repeated residual patterns to become candidate new concepts over time.

The central mechanism is:

```text
observe
→ characterise
→ compare
→ group reasons
→ sort by why
→ inherit supported structure
→ exclude unsupported structure
→ place provisionally
→ preserve residue
→ accumulate
→ propose new concept only when earned
```

The Why Library is the lossy conceptual surface produced by this process.

It is not a dictionary of labels.

It is an accumulated, semantically organised map of:

- what kinds of things have been encountered;
- why they appear related;
- why they differ;
- what usually defines a domain;
- what only defines a subtype;
- which cues are misleading;
- where boundaries remain uncertain;
- and which exact observations support those claims.

---

## The Human Analogy

Human knowledge develops with few reference points at first.

A child may learn:

```text
grass is a plant
```

Later they encounter something unfamiliar.

They may reason:

```text
this is not grass
but it shares several properties with grass
those shared properties are the ones that made grass a plant
therefore this may also be a plant
```

The inference is not based on one direct memorised rule.

It depends on accumulated knowledge at several depths:

- a fast conceptual surface;
- a broader general-shape memory;
- exact remembered examples and edge cases.

The system proposed here aims to reproduce that engineering shape.

---

## The Multilevel Knowledge Stack

```text
HOT MEMORY
the current observation and active comparisons

LUKEWARM MEMORY
the current grouped face:
properties, relations, unknowns, contradictions, candidate domains

WHY LIBRARY
lossy, fast conceptual knowledge:
what broadly belongs where and why

COLD ATLAS
deeper general-shape history:
patterns, exceptions, recurring structures, unresolved clusters

COLD EVIDENCE LOG
strain-the-brain specifics:
exact cases, source spans, event order, directional details, provenance
```

The system should normally reason from the shallowest sufficient level.

It descends only when:

- the case is near a boundary;
- the surface classification is unstable;
- exact detail matters;
- a contradiction appears;
- an assumption may need revision;
- a durable concept or lesson may be promoted.

---

## What the Why Library Stores

The library stores explanatory structures.

Example:

```text
PLANT

Broad why:
- living biological organisation
- growth and development
- environment-dependent processes
- recurring internal structure

Known subtypes:
- grass
- tree
- moss
- flowering plant

Subtype why:
- grass has plant-level properties plus grass-specific structure
- trees have plant-level properties plus tree-specific structure

Known false cues:
- green colour alone
- rooted appearance alone
- stationary position alone

Known boundaries:
- fungi
- artificial imitations
- non-living green objects
- unresolved biological edge cases
```

The label `plant` is only a retrieval handle.

The useful knowledge is the evidence-backed “why” structure beneath it.

---

## First Encounter: Processing A

A new observation A enters hot memory.

The system should not require B immediately.

A first-pass permutation process examines A across bounded vectors.

Possible vectors:

- physical properties;
- functional properties;
- causal role;
- temporal behaviour;
- environmental dependence;
- authority;
- scope;
- uncertainty;
- success conditions;
- failure conditions;
- boundaries;
- resemblance;
- exclusion;
- reversibility;
- transferability;
- composition.

The output should be explicit relational atoms.

Example:

```text
A has property X.
A lacks property Y.
A performs function Z.
A changes under condition Q.
A resembles known item M under vector V.
A differs from known item N under vector W.
The relation under vector R is unknown.
Observation E contradicts prior claim C.
```

---

## Lukewarm Grouping

The first-pass atoms should be grouped into a temporary face.

Example:

```text
Physical properties
Functional properties
Causal properties
Temporal properties
Boundary properties
Known similarities
Known differences
Unknowns
Contradictions
Candidate parent domains
Candidate subtype exclusions
```

This grouping is provisional.

It exists to help the system see shape before committing to durable structure.

---

## Semantic Sorting by “Why”

The grouped observation data should then be semantically sorted.

The important shift is from:

```text
what properties were observed?
```

to:

```text
why might this property matter?
```

Possible Why buckets:

```text
Why A may belong to domain D
Why A may not belong to domain D
Why A resembles known item M
Why the resemblance may be superficial
Why A fits a parent category but not a child category
Why the classification remains unresolved
Why prior assumptions may have been wrong
Why an exact precedent should be retrieved
```

The sorter is not certifying truth.

It is proposing a stable semantic geometry for further inspection.

---

## Why Bucket Record

```text
WhyBucketRecord
- bucket_id
- run_id
- sort_intent
- bucket_label
- bucket_definition
- included_atom_refs
- excluded_atom_refs
- weak_fit_refs
- junk_refs
- explanation
- confidence
- known_biases
- evidence_refs
- created_at
```

A Why bucket may be:

- provisional;
- stable;
- contradicted;
- split;
- merged;
- retired;
- promoted into the library.

---

## Parent Inheritance

The system should identify the deepest parent-level structure supported by evidence.

Example:

```text
Known:
grass belongs to plant because of P, Q, R

New observation X:
shares P, Q, R
does not share grass-specific G1, G2
```

Supported inheritance:

```text
X may inherit plant
```

Unsupported inheritance:

```text
X may not inherit grass
```

The governing rule is:

> Place the new thing at the deepest level justified by accumulated why-evidence, never deeper.

Valid output:

```text
likely plant
not justified as grass
exact subtype unresolved
```

---

## Child Exclusion

Classification requires more than finding similarity.

The system must also represent why a narrower concept does not apply.

Example:

```text
X shares plant-level why:
P, Q, R

X fails grass-level why:
G1, G2

Therefore:
parent inheritance supported
child inheritance unsupported
```

This prevents resemblance from becoming overclassification.

---

## Classification Depth

Possible placement depths:

```text
KnownInstance
KnownSubtype
KnownParentOnly
PossibleAnalogue
BoundaryCase
UnresolvedMember
ConflictingMember
ResidualClusterMember
NovelConceptCandidate
RejectedClassification
```

The system should prefer an honest broad placement over a false narrow one.

---

## Observation Assimilation Record

```text
ObservationAssimilationRecord
- assimilation_id
- observation_ref
- active_library_ref
- active_worldview_ref
- candidate_parent_refs
- inherited_parent_properties
- rejected_parent_properties
- candidate_child_refs
- inherited_child_properties
- rejected_child_properties
- unresolved_properties
- misleading_surface_cues
- retrieved_atlas_refs
- retrieved_evidence_refs
- why_bucket_refs
- provisional_placement
- confidence
- residue_refs
- created_at
```

---

## The Role of B

When observation B arrives, it should first be characterised independently.

The system should not immediately force B through A’s frame.

Process:

```text
B
→ characterise
→ group
→ sort by why
→ provisional placement
```

Then A and B may be held together.

```text
A is like B because...
A is unlike B because...
B is like A because...
B is unlike A because...
A and B share parent why P.
A satisfies child why Q; B does not.
B introduces property R not represented in A.
```

This produces a richer dataset than treating one item as the unquestioned reference.

---

## Directionality

Some relations are symmetric.

Some are not.

Example:

```text
A resembles B under colour
```

may be symmetric.

But:

```text
A depends on B
```

is directional.

The system should preserve ordered relation atoms.

```text
(subject=A, object=B)
is not automatically equivalent to
(subject=B, object=A)
```

---

## Relational Assimilation Record

```text
RelationalAssimilationRecord
- record_id
- source_a_ref
- source_b_ref
- optional_source_c_ref
- comparison_vector
- directional_relation
- likeness_claims
- difference_claims
- unknown_relations
- contradictions
- shared_parent_whys
- distinct_child_whys
- candidate_inheritance
- candidate_exclusions
- supporting_evidence_refs
- prior_relation_refs
- confidence
- created_at
```

---

## The Why Library as Lossy Working Knowledge

The Why Library should be fast and compressed.

It should support statements such as:

```text
Grass is a plant because it shares plant-level properties P, Q, R.

Trees are plants because they share P, Q, R but differ from grass
through T1, T2, T3.

Green colour alone is not sufficient evidence for plant membership.
```

This is intentionally lossy.

The Cold Atlas preserves broader historical shape.

The Cold Evidence Log preserves exact examples.

---

## Three Depths of Concept Retrieval

### Library Surface

Fast retrieval:

```text
plants share broad living and developmental structure
```

Use when:

- the case is ordinary;
- exact attribution is unnecessary;
- the action is reversible;
- the boundary is not contested.

### Cold Atlas

General-shape retrieval:

```text
most prior plant-like cases shared P, Q, R
several misleading green objects failed Q and R
property Q was common but not universal
```

Use when:

- broad variation matters;
- an exception may be relevant;
- the surface library may be too compressed.

### Cold Evidence

Exact retrieval:

```text
Specimen A17 lacked Q but was accepted because E showed...
Object N4 was green but non-living...
Case B9 was misclassified due to colour bias...
```

Use when:

- sequence matters;
- directionality matters;
- exact precedent matters;
- a durable revision is being considered.

---

## Deep Recall and Assimilation

Deep recall should be goal-directed.

Example:

```text
Current question:
Does X qualify as plant despite lacking Q?

Library:
Plants usually have Q.

Atlas:
Some prior plants lacked Q.

Exact retrieval:
Case A17 lacked Q but had stronger evidence E.
```

The exact case then enters hot memory for comparison.

The system should not dump all plant-related records into context.

---

## Residue

After inheritance and exclusion, some properties remain unexplained.

Example:

```text
X is likely a plant.
X is not grass.
X is not tree.
X is not moss.
X repeatedly exhibits V, W, Z.
```

The bundle V, W, Z is residual structure.

Residue should not be treated as junk.

It may be:

- noise;
- measurement error;
- one-off variation;
- an edge case;
- a hidden known subtype;
- a genuinely novel concept candidate.

The system must preserve it without premature classification.

---

## Residue Record

```text
SemanticResidueRecord
- residue_id
- source_assimilation_ref
- unexplained_properties
- failed_parent_refs
- failed_child_refs
- partially_matching_concepts
- contradiction_refs
- confidence
- suspected_noise
- recurrence_count
- related_residue_refs
- status
    - isolated
    - recurring
    - clustered
    - contradicted
    - explained
    - candidate_concept
- created_at
```

---

## Accumulation Over Time

A single residue rarely justifies a new concept.

The system should accumulate comparable residuals.

Example:

```text
X1:
plant-level properties supported
known subtypes unsupported
residue V, W, Z

X2:
plant-level properties supported
known subtypes unsupported
residue V, W, Z

X3:
plant-level properties supported
known subtypes unsupported
residue V, W, Z
```

Now the system has a recurring unexplained pattern.

This may support a candidate new subtype.

---

## Residual Cluster

```text
ResidualCluster
- cluster_id
- member_residue_refs
- shared_parent_ref
- shared_unexplained_properties
- non_shared_properties
- known_counterexamples
- boundary_candidates
- sorter_run_refs
- EF_investigation_refs
- status
    - open
    - dormant
    - unresolved
    - contradictory
    - candidate_concept
- confidence
- created_at
```

Attempt count alone does not justify promotion.

The cluster may remain unresolved indefinitely.

---

## Candidate New Concept

A new concept candidate emerges when:

- existing parent structure is supported;
- existing child concepts repeatedly fail;
- a stable residual bundle recurs;
- independent cases support the bundle;
- misleading surface similarities have been ruled out;
- counterexamples have been considered;
- the candidate improves classification or prediction;
- EF pressure does not immediately destroy it.

Example:

```text
Candidate C:
a plant subtype characterised by V, W, Z
```

This remains a candidate.

It is not yet a library truth.

---

## Concept Candidate Record

```text
ConceptCandidateRecord
- candidate_id
- proposed_name
- parent_concept_ref
- defining_why_properties
- supporting_case_refs
- supporting_residue_refs
- rejected_existing_child_refs
- counterexample_refs
- boundary_conditions
- non_applicability_conditions
- unresolved_edges
- predictive_claims
- transfer_results
- EF_refs
- confidence
- status
    - proposed
    - under_test
    - dormant
    - rejected
    - promoted
- created_at
```

---

## Concept Promotion

Promotion should require:

- exact evidence;
- recurring structured support;
- boundary testing;
- counterexamples;
- transfer where relevant;
- operator or explicit host approval;
- preserved unresolved edges;
- versioned library update.

Suggested flow:

```text
residual cluster
→ concept candidate
→ independent probes
→ EF pressure
→ boundary tests
→ approval
→ library insertion
```

No automatic promotion from:

- repetition alone;
- one interesting cluster;
- model confidence;
- semantic neatness;
- naming convenience.

---

## Why Library Concept Record

```text
WhyLibraryConceptRecord
- concept_id
- name
- parent_refs
- child_refs
- broad_why
- defining_properties
- optional_properties
- misleading_cues
- known_nonmembers
- known_boundary_cases
- supporting_atlas_refs
- supporting_evidence_refs
- counterexample_refs
- unresolved_edges
- confidence
- version
- promotion_receipt
- created_at
```

---

## Library Revision

New evidence may:

- strengthen a concept;
- narrow a concept;
- split a concept;
- merge concepts;
- expose a false cue;
- reveal a hidden assumption;
- create a new boundary;
- return a concept to unresolved status.

The library should be versioned.

No silent rewriting.

---

## Why Library Revision Record

```text
WhyLibraryRevisionRecord
- revision_id
- concept_ref
- prior_version
- new_version
- old_broad_why
- new_broad_why
- added_properties
- removed_properties
- added_boundaries
- removed_boundaries
- added_counterexamples
- added_evidence_refs
- contradiction_refs
- confidence_delta
- reason
- approved_by
- created_at
```

---

## Relation to the Semantic Dataset Sorter

The sorter can organise:

- property atoms;
- relation atoms;
- Why buckets;
- residuals;
- candidate concepts;
- boundary cases;
- contradiction types;
- transfer distances;
- uncertainty states.

Possible sort intents:

- parent-domain support;
- child-domain exclusion;
- causal role;
- functional role;
- authority relation;
- boundary type;
- false-cue pattern;
- unresolved residue;
- concept depth;
- transferability;
- contradiction strength.

The sorter proposes geometry.

It does not decide truth.

---

## Data-Skim and Blind-Label Modes

### Data Skim

Ask:

```text
What semantic structure does the accumulated evidence suggest?
```

### Blind Label

Ask:

```text
What ontology does the model impose before seeing the evidence?
```

Comparing the two can expose:

- model bias;
- imposed categories;
- unstable geometry;
- missing domains;
- overfitted labels;
- evidence-emergent structure.

---

## Relation to Relational Permutation

Permutation produces the comparison records that feed assimilation.

The engine may compare:

- observation to known concept;
- observation to exemplar;
- observation to counterexample;
- observation to prior residue;
- concept to concept;
- assumption to observation;
- library version to library version.

Assimilation decides where the result belongs in accumulated knowledge.

---

## Relation to Dual Cold Memory

The Why Library cannot replace cold memory.

```text
Why Library:
fast conceptual surface

Cold Atlas:
broader historical shape

Cold Evidence:
exact precedent
```

The library should always retain links downward.

No orphan concept.

No unsupported “everyone knows” entry.

---

## Relation to EF Engine

EF challenges:

- candidate inheritance;
- child exclusion;
- residual recurrence;
- concept boundaries;
- promoted Why structures.

Possible EF loop:

```text
candidate classification
→ probe
→ failure or contradiction
→ vault
→ materially different probe
→ compare
→ narrow / reject / preserve unresolved
```

EF should prevent conceptual folklore.

---

## Relation to Assumption Freeze

Before a new observation is assimilated, the active library expectation may be frozen.

Example:

```text
Surface:
X is probably grass.

General:
X is probably plant-like.

Granular:
X resembles plant cases A17 and B4.
```

After independent characterisation, compare expectation to evidence.

This exposes:

- correct parent inheritance;
- wrong child assumption;
- hidden false cues;
- worldview bias;
- retrospective rationalisation.

---

## Relation to Worldview Branching

Different worldviews may organise the same observations differently.

Example:

```text
Worldview A:
classifies by function

Worldview B:
classifies by structure

Worldview C:
classifies by causal origin
```

Each may produce a different Why Library.

The system should preserve:

- shared concepts;
- worldview-specific concepts;
- divergent boundaries;
- different predictive histories.

A new library branch should require recurring structured contradiction.

---

## Relation to the Cognitive Economy Governor

Assimilation can become computationally explosive.

The governor should control:

- number of vectors;
- number of candidate parents;
- cold-memory depth;
- number of pairwise comparisons;
- sorter runs;
- EF probes;
- concept-candidate creation;
- library-branch review.

Default policy:

```text
Use the shallowest sufficient concept.
Descend only when classification or action depends on it.
Preserve unresolved residue without endlessly analysing it.
```

---

## Routine Assimilation

For an ordinary familiar case:

```text
observation
→ library surface match
→ parent and child supported
→ provisional placement
→ stop
```

No deep recall.

No full permutation.

No EF.

---

## Boundary Assimilation

For an ambiguous case:

```text
observation
→ library surface uncertain
→ cold atlas retrieval
→ exact exemplar hydration
→ bounded comparison
→ parent-only placement
→ residue preserved
→ stop
```

---

## Novelty Assimilation

For recurring unexplained cases:

```text
observation
→ existing children fail
→ residue stored
→ later comparable residues accumulate
→ sorter groups them
→ EF pressure
→ concept candidate
```

---

## Honest Outputs

The system should be able to say:

```text
Known grass.
Likely plant, subtype unknown.
Possible analogue, insufficient evidence.
Boundary case.
Conflicting evidence.
Unresolved member.
Recurring residual cluster.
Novel concept candidate.
Rejected classification.
```

Forced precision is not intelligence.

---

## The Why Library and Lesson Library

These may overlap but should remain conceptually distinct.

```text
WHY LIBRARY
what kinds of things exist and why they belong

LESSON LIBRARY
what has been learned about actions, failures, constraints,
predictions, and reusable relational rules
```

A Why concept may support a lesson.

A lesson may revise a Why concept.

Neither should silently overwrite the other.

---

## The Why Library and Assumption Library

```text
WHY LIBRARY
what the system believes about domains and concepts

ASSUMPTION LIBRARY
how prior interpretive frames influence what the system expects
```

Example:

```text
Why Library:
plants are living organised systems

Assumption Library:
the system historically overweights green colour
```

Both may be active during classification.

---

## Computational Cost

Naive assimilation may scale badly.

Potential cost drivers:

```text
observations
× candidate parents
× candidate children
× comparison vectors
× exact precedent retrieval
× residual comparisons
× sorter runs
```

The first prototype should remain small and inspectable.

Later controls may include:

- candidate-parent preflight;
- vector caps;
- cached comparisons;
- semantic duplicate detection;
- bounded residual matching;
- dormant unresolved clusters;
- small-model first pass;
- stronger-model disputed cases;
- operator-approved deep dives;
- batch atlas updates.

---

## Avoiding Combinatorial Sludge

Hard rails:

- do not compare every observation to every concept;
- do not run every vector by default;
- do not descend into exact evidence unless needed;
- do not turn every residue into a candidate;
- do not promote from repetition alone;
- do not branch a library from one contradiction;
- do not repeatedly sort unchanged data;
- do not treat paraphrase as information gain;
- allow unresolved residue to sleep;
- require operator intent and cognitive budget.

---

## Minimal Viable Prototype

### Domain

Use one narrow, manually inspectable domain.

Recommended:

```text
ChattyFactory authority, provenance, and failure cases
```

### Inputs

- 20–50 exact cases;
- 5–10 existing Why concepts;
- 5–10 atlas summaries;
- exact cold evidence links;
- several known boundary cases;
- several unresolved cases.

### Prototype flow

1. Ingest one observation.
2. Characterise it independently.
3. Generate bounded property and relation atoms.
4. Group them in lukewarm memory.
5. Sort them into Why buckets.
6. Retrieve candidate parent concepts.
7. Test supported inheritance.
8. Test child exclusion.
9. Produce provisional placement.
10. Preserve unexplained residue.
11. Accumulate comparable residues over later runs.
12. Allow concept candidacy only after recurring structured support.

---

## Prototype File Shape

```text
semantic_assimilation/
  observations/
    observation_records.jsonl
  atoms/
    property_atoms.jsonl
    relation_atoms.jsonl
  why_buckets/
    why_bucket_records.jsonl
  assimilation/
    assimilation_records.jsonl
  residue/
    residue_records.jsonl
    residual_clusters.jsonl
  concepts/
    candidates.jsonl
    library_concepts.jsonl
    revisions.jsonl
```

---

## Prototype API Sketch

```text
record_observation(source)
characterise_observation(observation_ref)
generate_relation_atoms(observation_ref, vector_budget)
group_lukewarm_face(atom_refs)
sort_why_buckets(group_ref, intent)
retrieve_candidate_parents(observation_ref, library_ref)
evaluate_parent_inheritance(observation_ref, parent_ref)
evaluate_child_exclusion(observation_ref, child_refs)
place_provisionally(assimilation_input)
record_residue(assimilation_ref)
cluster_residues(residue_refs)
propose_concept(cluster_ref)
review_concept_candidate(candidate_ref)
revise_why_library(concept_ref, evidence_refs)
```

---

## Required Tests

### Observation integrity

- observation is preserved before classification;
- source hashes remain stable;
- exact evidence remains retrievable;
- prior labels are not injected automatically.

### Why sorting

- atoms can be grouped into multiple Why buckets;
- weak-fit records remain visible;
- junk does not erase evidence;
- frozen bucket plans prevent drift.

### Inheritance

- supported parent properties can be inherited;
- unsupported child properties block narrow classification;
- parent-only placement is valid;
- one surface similarity cannot prove membership.

### Directionality

- A→B and B→A can differ;
- symmetric relations are explicit;
- summary compression does not erase exact directionality.

### Residue

- unexplained properties remain stored;
- one residue cannot create a concept automatically;
- recurring residues can form a cluster;
- contradictory residues can keep a cluster unresolved.

### Concept promotion

- repetition alone is insufficient;
- counterexamples can narrow or reject a candidate;
- promotion preserves evidence and boundaries;
- rejected candidates remain auditable.

### Memory integration

- library surface can answer ordinary cases;
- cold atlas can resolve broader ambiguity;
- cold evidence can recover exact precedent;
- missing exact detail remains unresolved.

### Governor integration

- routine cases stop shallow;
- vector budget is enforced;
- dormant residue does not spin;
- operator can request a deeper pass.

### Assumption integration

- prior library expectation can be frozen;
- independent observation can contradict it;
- library revision preserves the old version.

---

## Success Criteria

The prototype is useful if it demonstrates:

1. New observations produce explicit property and relation records.
2. Why buckets organise reasons rather than merely labels.
3. Parent inheritance and child exclusion remain distinct.
4. Broad classification can remain valid when narrow classification fails.
5. Unexplained residue is preserved rather than discarded.
6. Repeated residual patterns can become concept candidates.
7. Exact evidence remains available beneath lossy library knowledge.
8. The system can honestly remain unresolved.
9. Concept promotion is rare and evidence-backed.
10. The same mechanism can later support both host reasoning and curriculum generation.

---

## Failure Modes

### Label-first classification

The system chooses a label and retrofits reasons.

**Rail:** characterise observation before classification.

### Similarity collapse

One resemblance causes overclassification.

**Rail:** require parent inheritance and child exclusion separately.

### Why Library becomes folklore

Concepts lose links to evidence.

**Rail:** every concept retains atlas and exact evidence refs.

### Residue treated as junk

Potential novelty is discarded.

**Rail:** separate weak-fit, junk, and unexplained residue states.

### Concept explosion

Every recurring difference becomes a new concept.

**Rail:** require stable structure, counterexamples, boundaries, and review.

### Memory flattening

Library surface replaces exact precedent.

**Rail:** mandatory downward links and deep recall.

### Worldview lock-in

One library geometry becomes universal truth.

**Rail:** assumption freeze, alternative frames, versioned branches.

### Endless assimilation

Every observation triggers maximum depth.

**Rail:** Cognitive Economy Governor and dormancy.

### Sorter authority

The sorter’s buckets are treated as certified ontology.

**Rail:** sorter output remains provisional geometry.

### Retrospective rewriting

The library changes and acts as though it always held the new view.

**Rail:** immutable revisions and version history.

---

## Host / Model Authority Split

### Operator

Owns:

- domain intent;
- acceptable scope;
- concept-promotion approval;
- memory and privacy policy;
- cognitive budget;
- worldview selection where relevant.

### Model

May propose:

- properties;
- comparison vectors;
- Why buckets;
- candidate parents;
- candidate exclusions;
- residual clusters;
- concept names;
- boundary probes.

The model does not own truth or promotion.

### Host

Owns:

- source preservation;
- provenance;
- memory depth;
- bucket freezing;
- record integrity;
- inheritance checks;
- residue persistence;
- revision history;
- promotion gates;
- compute limits.

### Evidence

Determines what can honestly be inherited, excluded, or promoted.

---

## Relation to Host-to-Model Training

The assimilation process produces training material.

Possible examples:

- observation → parent inheritance;
- observation → child exclusion;
- surface resemblance → false analogy rejection;
- residue → unresolved classification;
- repeated residue → concept candidate;
- counterexample → concept revision;
- frozen assumption → corrected classification.

These formation trails can feed Relational Curriculum Geometry.

The model can then be trained on:

- how concepts are formed;
- how boundaries are preserved;
- how unknowns remain unknown;
- how parent and child structure differ;
- how false cues are rejected;
- how new concepts emerge over time.

---

## Short Doctrine

> Characterise before classifying.  
> Sort reasons, not merely labels.  
> Inherit only what the evidence supports.  
> Exclude what the evidence does not support.  
> Preserve every unexplained remainder.  
> Let repeated residues accumulate.  
> Promote a new concept only when the why-structure earns it.

---

## Final Architecture

```text
NEW OBSERVATION
        ↓
INDEPENDENT CHARACTERISATION
        ↓
PROPERTY / RELATION ATOMS
        ↓
LUKEWARM GROUPING
        ↓
SEMANTIC WHY SORTING
        ↓
WHY LIBRARY RETRIEVAL
        ↓
PARENT INHERITANCE
        ↓
CHILD EXCLUSION
        ↓
PROVISIONAL PLACEMENT
        ↓
UNEXPLAINED RESIDUE
        ↓
COLD ATLAS + COLD EVIDENCE
        ↓
LATER COMPARABLE OBSERVATIONS
        ↓
RESIDUAL CLUSTER
        ↓
EF PRESSURE + BOUNDARY TESTS
        ↓
CANDIDATE NEW CONCEPT
        ↓
VERSIONED WHY LIBRARY UPDATE
```

This mechanism gives the MCM a path from sparse experience to accumulated conceptual knowledge.

Over time, the system can develop:

- fast lossy understanding;
- deeper general-shape memory;
- exact recoverable precedent;
- evidence-backed domain concepts;
- provisional classifications;
- persistent unresolved edges;
- and new concepts that emerge from repeated structure rather than one clever guess.
