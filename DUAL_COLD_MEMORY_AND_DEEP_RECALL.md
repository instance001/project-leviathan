# Dual Cold Memory and Deep Recall

**Status:** Working architecture specification  
**Purpose:** Add a human-like deep-memory shape to Chatty-Cog and the wider MCM architecture  
**Primary related systems:** Tri-helix memory, Relational Permutation Engine, EF Engine, lesson library, Chatty-Cog

---

## Core Claim

A useful long-term memory system should not force a choice between:

- loading raw historical logs directly into working context, or
- relying on compressed summaries that have discarded important detail.

Human-like recall appears to use at least two distinct long-term layers:

1. a broad, compressed sense of what exists in memory;
2. a deeper, effortful retrieval path for exact details when the broad recollection is insufficient.

For the MCM, this suggests a dual cold-memory architecture:

```text
HOT MEMORY
what is being actively manipulated now

LUKEWARM MEMORY
the current task/thread summary

COLD ATLAS
compressed, searchable summaries of older events,
investigations, relationships, lessons, and unresolved questions

COLD EVIDENCE LOG
exact historical records, directional relation atoms,
source spans, event order, provenance, and unresolved detail
```

The cold atlas locates.

The cold evidence log substantiates.

> Broad memory says, “something like this happened before.”  
> Deep recall asks, “what exactly happened, in what order, and which detail belonged to which object?”

---

## Why One Cold Layer Is Not Enough

A single cold store creates two bad operating modes.

### Mode A: Raw-log retrieval

```text
query
→ retrieve many old records
→ flood hot context
→ spend tokens rediscovering relevance
→ risk distraction and contradiction
```

Advantages:

- exact detail
- strong provenance
- fewer summary distortions

Costs:

- expensive
- noisy
- context hungry
- difficult to rank
- cognitively clumsy

### Mode B: Summary-only retrieval

```text
query
→ retrieve compressed recollection
→ answer cheaply
```

Advantages:

- fast
- cheap
- easy to fit into context

Costs:

- directional detail may be lost
- sequence may be flattened
- uncertainty may disappear
- differences may be collapsed
- summaries may slowly rewrite history
- edge cases become unrecoverable

The dual-cold design introduces a middle path:

```text
query
→ search compressed cold atlas
→ identify likely relevant memories
→ selectively hydrate exact evidence records
→ place only the needed detail into hot memory
```

---

## Human-Like Memory Shape

A rough cognitive analogy:

```text
HOT / WORKING
“What am I thinking about right now?”

LUKEWARM
“What has this recent conversation or task been about?”

COLD ATLAS
“What do I broadly remember existing back there?”

COLD EVIDENCE
“Fuck, what exactly happened? Let me strain for the specifics.”
```

This should not be treated as a literal neuroscience claim.

It is an engineering analogy for a practical retrieval architecture.

The important distinction is between:

- **remembered gist**, and
- **recoverable detail**.

---

## The Four Memory Layers

## 1. Hot Memory

Hot memory contains the exact blocks currently under active scrutiny.

Examples:

- current user request
- active constraints
- source excerpts
- retrieved historical details
- A and B in a relational comparison
- current hypothesis
- current contradiction
- selected tool evidence

Properties:

- small
- exact
- rapidly changing
- high relevance
- directly visible to the model
- aggressively bounded

Hot memory is where manipulation occurs.

---

## 2. Lukewarm Memory

Lukewarm memory contains the current face-level summary.

It answers:

- what are we doing?
- why are these items together?
- what has already been established?
- what remains unresolved?
- which older memories appear relevant?
- what should remain active next turn?

It is not merely a transcript summary.

For a fully realised MCM, it should include the active relational arrangement.

Example:

```text
Current task:
Audit promotion authority in ChattyFactory.

Active objects:
- approval receipt
- promotion capability
- journal verification

Current relation:
The capability claims to derive from approval, but the approval is not yet journal-backed.

Open question:
Can a valid-looking candidate be cross-wired into a different approval chain?

Relevant cold areas:
- earlier capability replay audit
- authority-boundary lessons
- semantic lineage failures
```

---

## 3. Cold Atlas

The cold atlas is the compressed, searchable map over long-term evidence.

It stores broad recollections such as:

```text
Several ChattyFactory audits found that private types and typed APIs
did not necessarily enforce authority.

A prior investigation distinguished envelope topology from
payload-level semantic lineage.

Multiple model failures involved converting uncertainty into hidden
positive method authority.
```

The atlas should support:

- semantic search
- entity search
- relation search
- time-range search
- project search
- unresolved-question search
- contradiction search
- lesson search
- evidence-strength filtering
- links to exact underlying records

The atlas is allowed to change as understanding improves.

It is an interpretation layer.

It must never become the sole source of historical truth.

---

## 4. Cold Evidence Log

The cold evidence log stores exact, provenance-rich records.

Examples:

- original message or file span
- exact event order
- exact actor and object roles
- exact comparison vector
- directional relation atom
- failure observation
- tool output
- receipt chain
- source hashes
- uncertainty state
- model identity
- timestamp
- contradiction links

The evidence log should be:

- append-oriented
- difficult to rewrite silently
- addressable by stable IDs
- linked to source material
- searchable at field level
- recoverable independently of summaries

The evidence log does not need to be loaded wholesale.

It exists so the system can descend from gist to exactness.

---

## Core Rule

> The atlas tells hot memory where to look.  
> The evidence log tells hot memory what actually happened.

---

## Example: Why Directional Detail Matters

Suppose the cold atlas stores:

```text
A and B differ in colour.
```

That may be enough for a broad comparison.

But an edge case may require:

```text
A is blue.
B is red.
```

Or even:

```text
A is unlike B under colour because A is blue and B is red.

B is unlike A under colour because B is red and A is blue.
```

These statements are related, but the subject/object direction may matter later.

For example:

- “Which item matched the blue prerequisite?”
- “Which item changed state?”
- “Which item was the exception?”
- “Did the relation remain symmetric under a different vector?”

The evidence log must preserve directional atoms.

The atlas may compress them.

---

## Directional Relation Atom

```text
DirectionalRelationAtom
- atom_id
- subject_ref
- object_ref
- comparison_vector
- relation_class
    - like
    - unlike
    - unknown
    - contradiction
- subject_property
- object_property
- relational_claim
- supporting_evidence_refs
- source_span_refs
- confidence
- uncertainty_notes
- inverse_atom_ref
- prior_atom_refs
- created_at
```

Important rule:

```text
(subject=A, object=B)
is not automatically equivalent to
(subject=B, object=A)
```

The engine may mark a relation as symmetric only when the relation itself supports symmetry.

---

## Cold Atlas Record

```text
ColdAtlasRecord
- atlas_record_id
- title
- summary
- scope
- entities
- projects
- relation_types
- unresolved_questions
- contradictions
- confidence
- evidence_record_refs
- child_atlas_refs
- parent_atlas_refs
- lesson_refs
- last_revised_at
- revision_reason
```

The summary is mutable.

The evidence references must remain intact.

---

## Cold Evidence Record

```text
ColdEvidenceRecord
- evidence_id
- source_type
- source_ref
- source_hash
- exact_text_or_payload
- source_spans
- event_time
- ingest_time
- actors
- objects
- project_scope
- trace_id
- request_id
- attempt_id
- relation_atoms
- failure_refs
- contradiction_refs
- confidence
- provenance
```

The exact schema can vary by evidence type, but the stable principles are:

- precise source identity
- exact content or canonical payload
- stable addressing
- provenance
- lineage
- directionality
- no dependence on a summary for meaning

---

## Multi-Scale Cold Atlas

The atlas should not be one flat summary blob.

It should support multiple scales.

```text
event summary
→ thread summary
→ investigation summary
→ recurring-pattern summary
→ project summary
→ domain summary
```

Example:

```text
Event:
Codex issued a promotion capability from caller-supplied candidate data.

Investigation:
Promotion authority was not journal-backed.

Recurring pattern:
Typed interfaces were mistaken for enforced semantic authority.

Project:
ChattyFactory authority boundaries required replay and lineage hardening.

Domain:
Capability systems fail when nominal receipts are accepted without
verified provenance and single-use enforcement.
```

Each higher level points downward.

No higher-level summary may replace the evidence below it.

---

## Summary Candidate Promotion

Not every cold summary should immediately become part of the atlas.

A candidate summary may be:

- proposed
- provisional
- contradicted
- accepted
- revised
- split
- superseded
- retired

Suggested flow:

```text
evidence records
→ summary candidate
→ compare against source evidence
→ contradiction check
→ operator/model review
→ atlas insertion
```

A summary candidate should state:

- what it compresses
- what it omits
- confidence
- unresolved details
- evidence coverage
- known counterexamples

---

## Mutable Interpretation Over Stable Evidence

The architecture should deliberately allow:

```text
mutable interpretation
over
stable evidence
```

Why?

Because later evidence may change what an old event means.

Example:

Initial atlas summary:

```text
The model ignored tool instructions.
```

Later revised summary:

```text
The model showed tool-salience inversion:
it overused tools in one framing and underused them in another.
```

The historical events did not change.

The interpretation improved.

The atlas record may be revised.

The exact source events and tool calls remain untouched.

---

## Deep Recall

Deep recall is the deliberate descent from a broad memory into exact historical detail.

It should be a first-class host operation.

### Deep Recall Request

```text
DeepRecallRequest
- request_id
- current_question
- remembered_gist
- missing_detail
- candidate_entities
- candidate_projects
- candidate_time_range
- candidate_relation
- required_precision
- maximum_context_budget
- stop_conditions
```

### Deep Recall Result

```text
DeepRecallResult
- request_id
- atlas_matches
- hydrated_evidence_refs
- exact_details
- unresolved_gaps
- contradictions_found
- confidence
- context_cost
- retrieval_steps
```

---

## Deep Recall Flow

```text
1. Hot memory asks:
   “Have we seen something like this?”

2. Lukewarm memory identifies the active relation:
   “This resembles a prior authority-boundary failure.”

3. Cold atlas search returns:
   - template fallback incident
   - substrate inference incident
   - rescue substitution incident

4. The host asks:
   “Which incident happened before execution,
    and which happened after failure?”

5. Exact evidence records are hydrated.

6. Hot memory receives:
   - incident A: family inferred before execution
   - incident B: fallback substituted after failure
   - incident C: unresolved because exact sequence was not preserved

7. The model continues with exact distinctions.
```

---

## Honest Recall Failure

The system must be able to say:

```text
I found the broad memory, but I could not recover the exact detail.
```

This is preferable to reconstructing a plausible detail.

Recall states should include:

- exact detail recovered
- partial detail recovered
- broad summary only
- contradictory records found
- no supporting record found
- source unavailable
- retrieval budget exhausted

---

## Cold Summary Search

The atlas should support several search lanes.

### Semantic search

Find conceptually related summaries.

### Lexical search

Find exact names, terms, IDs, paths, or quoted phrases.

### Relation search

Find prior records involving:

- same relation vector
- same authority boundary
- same failure pattern
- same contradiction type
- same transfer issue

### Entity search

Find all memories involving a specific:

- project
- model
- tool
- person
- file
- component
- capability

### Temporal search

Find:

- events in a time window
- earlier/later occurrences
- first known appearance
- recent recurrence

### Structural search

Find records matching:

- same trace shape
- same receipt chain
- same A/B role pattern
- same boundary condition
- same unresolved investigation

---

## Hydration Policy

The host should not automatically hydrate every linked evidence record.

Hydration should be bounded.

Possible signals:

- active intent relevance
- contradiction
- uncertainty
- edge-case sensitivity
- missing directionality
- missing event order
- low summary confidence
- high stakes
- explicit operator request
- candidate lesson promotion
- EF triangulation need

Possible stopping conditions:

- requested detail found
- contradiction resolved
- context budget reached
- no further evidence
- remaining records are redundant
- confidence threshold met
- operator interruption

---

## Cheap Recall and Deep Recall Modes

### Cheap recall

Use when:

- broad historical context is enough
- exact sequence does not matter
- stakes are low
- the user asks for a gist
- the atlas confidence is high

Flow:

```text
query
→ atlas match
→ hot memory summary
```

### Deep recall

Use when:

- exact attribution matters
- sequence matters
- directional relation matters
- edge cases matter
- a contradiction exists
- evidence is needed for promotion
- a decision may become durable
- the user explicitly asks for specifics

Flow:

```text
query
→ atlas match
→ evidence descent
→ exact hydration
→ hot memory
```

---

## Relation to the Relational Permutation Engine

The dual-cold architecture is necessary for the Rubik-style memory mechanism.

The relational permutation engine needs two things:

1. compressed maps that help identify promising A/B comparisons;
2. exact evidence that preserves subtle differences during rotation.

### Atlas role

The atlas nominates:

```text
A may be comparable to B under authority.
```

### Evidence role

The evidence log supplies:

```text
A occurred before execution.
B occurred after failure.
A involved classification.
B involved fallback substitution.
```

### Permutation role

The engine then rotates A and B through:

- authority
- time
- mechanism
- scope
- uncertainty
- boundary

Without exact evidence hydration, the cube spins flattened blocks.

Without the atlas, the system cannot efficiently find which blocks to bring forward.

---

## Relation to EF Engine

EF requires exact historical comparison.

A broad summary such as:

```text
Two attempts failed similarly.
```

is insufficient.

EF may need:

- exact failure class
- exact environmental state
- exact changed variable
- exact attempt sequence
- exact tool
- exact model
- exact lock signal
- exact contradiction
- exact success condition

The cold atlas can locate candidate related failures.

The evidence log determines whether they are actually comparable.

No EF triangulation should rely solely on atlas summaries.

---

## Relation to the Lesson Library

The lesson library should sit above both cold layers.

```text
lesson
→ supporting atlas records
→ supporting evidence records
```

A lesson may cite broad investigation summaries for navigation.

But it must retain paths to exact evidence.

Lesson use should support two modes:

### Fast lesson retrieval

Load:

- lesson statement
- scope
- boundary
- confidence

### Audited lesson retrieval

Also load:

- supporting cases
- counterexamples
- failed probes
- exact evidence
- promotion record

This prevents the lesson library from becoming detached folklore.

---

## Relation to Chatty-Cog

Chatty-Cog currently has:

- hot memory
- lukewarm rolling summary
- cold logs / durable records

The eventual addition should be:

```text
cold logs
        ↑
cold-summary atlas
```

This is not cosmetic UI work.

It changes the cognitive usefulness of the memory architecture.

### Proposed Chatty-Cog surfaces

#### Cold Atlas panel

Shows:

- relevant old summaries
- unresolved investigations
- recurring patterns
- lesson links
- confidence
- evidence counts

#### Deep Recall action

Allows the operator or model to request:

- exact detail
- exact sequence
- exact source span
- exact prior wording
- exact A/B relation
- contradiction search

#### Hydration receipt

Shows:

- what was retrieved
- why it was retrieved
- which summary led to it
- context cost
- unresolved gaps

#### Evidence drill-down

Allows navigation:

```text
domain summary
→ pattern summary
→ investigation summary
→ event summary
→ exact evidence
```

---

## Cold Atlas Update Loop

```text
new evidence arrives
→ assign stable evidence ID
→ append to cold evidence log
→ identify affected atlas records
→ propose summary revisions
→ compare old and new summaries
→ preserve revision history
→ update atlas links
```

The system should not silently overwrite an atlas interpretation.

A revision record should preserve:

```text
old summary
new summary
reason for change
new evidence refs
confidence change
operator/model author
timestamp
```

---

## Atlas Revision Record

```text
AtlasRevisionRecord
- revision_id
- atlas_record_id
- prior_version
- new_version
- old_summary
- new_summary
- reason
- added_evidence_refs
- removed_evidence_refs
- contradiction_refs
- confidence_delta
- approved_by
- created_at
```

---

## Duplicate and Overlap Handling

Cold summaries may overlap.

The system should allow:

- multiple perspectives over the same evidence
- project-specific summaries
- domain-level summaries
- unresolved competing interpretations

It should avoid:

- silent duplication
- summary loops
- multiple records claiming the same scope without links
- one summary erasing a competing interpretation

Possible relationships:

- overlaps
- supersedes
- narrows
- broadens
- contradicts
- derives_from
- summarises
- partitions

---

## Two Kinds of Forgetting

The architecture should support different retention policies.

### Atlas forgetting

The atlas may:

- merge redundant summaries
- retire obsolete summaries
- compress old low-value maps
- reduce surface detail
- change wording
- reorganise hierarchy

This is interpretive housekeeping.

### Evidence forgetting

The evidence log should be much more conservative.

Evidence may be:

- retained
- archived
- redacted
- deleted by explicit policy
- compacted only when canonical equivalence is proven

The system should never pretend a deleted record still exists.

---

## Privacy and Scope Boundaries

Cold memory may contain sensitive information.

Every atlas and evidence record should carry scope.

Possible scopes:

- current conversation
- current project
- current user
- local device
- shared workspace
- exportable
- restricted
- ephemeral
- do not summarise
- do not train on

Deep recall must respect the most restrictive underlying scope.

A broad atlas summary must not leak restricted evidence.

---

## Memory Authority

### Operator

Owns:

- memory inclusion policy
- deletion
- privacy scope
- deep-recall approval where required
- lesson promotion
- correction of misremembered summaries

### Model

May propose:

- summary candidates
- retrieval queries
- relevance links
- contradiction notices
- deep-recall requests

The model does not own historical truth.

### Host

Owns:

- source integrity
- stable IDs
- provenance
- access control
- retrieval bounds
- evidence hydration
- revision history
- summary/evidence separation

### Evidence

Determines what can honestly be claimed.

---

## Computational Cost

The dual-cold design reduces some costs but introduces others.

### Savings

- broad queries can stop at atlas level
- exact records are hydrated selectively
- hot context remains bounded
- repeated raw-log scanning is reduced
- common recollections can be cached

### Costs

- atlas generation
- atlas revision
- evidence indexing
- multi-scale hierarchy maintenance
- provenance storage
- deep-recall search
- contradiction checks
- hydration receipts

The prototype should prefer correctness and inspectability over aggressive optimisation.

---

## Cost Controls

Possible later controls:

- hash-based retrieval caching
- incremental atlas updates
- vector and lexical hybrid search
- project-scoped indexes
- evidence popularity counters
- stale-summary detection
- bounded deep-recall budgets
- small-model atlas summarisation
- stronger-model contradiction review
- operator-pinned memories
- dormant archive tiers

These are optimisation layers.

They should not weaken the evidence path.

---

## Failure Modes

### Summary replaces evidence

The system begins treating atlas text as ground truth.

**Rail:** every substantive atlas claim retains evidence refs.

### Deep recall becomes generic RAG

The host dumps semantically nearby chunks into context.

**Rail:** retrieval must begin from a stated missing detail and stop when that detail is answered or remains unresolved.

### Summary drift

Repeated summarisation changes the meaning of old events.

**Rail:** versioned atlas revisions over stable evidence.

### Direction loss

“A differs from B” replaces exact directional properties.

**Rail:** directional relation atoms in evidence log.

### Sequence loss

The atlas preserves events but not their order.

**Rail:** event-time and parent/precedence links.

### False memory completion

The model fills missing details from plausibility.

**Rail:** explicit recall states and unresolved gaps.

### Atlas explosion

Every event produces many overlapping summaries.

**Rail:** staged summary candidacy, overlap links, and bounded promotion.

### Evidence explosion

Every token is stored forever.

**Rail:** source-aware retention policy and explicit archival classes.

### Privacy leakage

A broad summary exposes restricted underlying material.

**Rail:** scope inheritance and access checks.

### Premature lesson formation

A recurring atlas pattern becomes a lesson without evidence pressure.

**Rail:** lesson promotion still requires EF, transfer, boundary, and approval.

---

## Minimal Viable Prototype

The first prototype does not need a full distributed memory system.

### Scope

Use one Chatty-Cog project with:

- 50–200 cold evidence records
- 10–30 atlas records
- one project summary
- several investigation summaries
- several event summaries
- several exact directional relation atoms

### Required operations

1. Append exact evidence.
2. Create a summary candidate.
3. Link summary to evidence.
4. Search atlas.
5. Hydrate selected evidence.
6. Place hydrated detail into hot context.
7. Record deep-recall result.
8. Revise a summary without rewriting evidence.
9. Surface an honest unresolved recall.
10. Drill from project summary to exact source.

### Test questions

- Can the system recall broad prior context cheaply?
- Can it recover exact attribution when needed?
- Can it recover event order?
- Can it distinguish A→B from B→A?
- Can a revised summary preserve old evidence?
- Can the system admit exact detail is unavailable?
- Can it avoid loading irrelevant logs?
- Can a lesson point back to exact source evidence?

---

## Suggested Prototype Files

```text
memory/
  hot/
  lukewarm/
  cold_atlas/
    atlas_records.jsonl
    atlas_revisions.jsonl
  cold_evidence/
    evidence_records.jsonl
    relation_atoms.jsonl
  deep_recall/
    requests.jsonl
    results.jsonl
```

This is only an illustrative storage shape.

The implementation may later use a database or indexed store.

---

## Prototype API Sketch

```text
append_evidence(record)
propose_atlas_summary(evidence_refs, candidate)
review_atlas_summary(candidate_id, decision)
search_atlas(query, scope, limit)
request_deep_recall(request)
hydrate_evidence(evidence_refs, budget)
revise_atlas_record(record_id, revision)
link_lesson_to_memory(lesson_id, atlas_refs, evidence_refs)
```

Public APIs should accept minimal external facts and construct internal receipts themselves.

---

## Required Tests

### Evidence integrity

- exact evidence survives atlas revision
- evidence hashes remain stable
- deleted evidence is reported as unavailable
- source refs remain resolvable

### Summary integrity

- atlas summaries cannot exist without evidence refs
- revisions preserve version history
- summary confidence can decrease
- contradictory summaries can coexist explicitly

### Retrieval

- atlas search returns relevant summaries
- deep recall hydrates exact linked evidence
- retrieval respects scope
- context budgets are enforced
- redundant records are not repeatedly hydrated

### Directionality

- A→B and B→A can differ
- symmetric relations are marked explicitly
- summary compression does not erase subject/object detail from evidence

### Honesty

- missing exact detail returns unresolved
- contradictory evidence is surfaced
- broad summary is not represented as exact recall

### Integration

- hydrated evidence enters hot memory
- lukewarm summary records why it was retrieved
- relational permutation can consume exact hydrated records
- EF triangulation rejects atlas-only evidence
- lesson audit can descend to source evidence

---

## Success Criteria

The dual-cold architecture is useful if it demonstrates:

1. Broad historical relevance can be recovered cheaply.
2. Exact detail can be selectively reconstructed when needed.
3. Summaries remain navigational rather than authoritative.
4. Directional and sequential details survive compression.
5. The system can honestly fail to remember.
6. Hot context receives less irrelevant history.
7. Relational comparisons improve when exact evidence is hydrated.
8. Atlas interpretations can evolve without rewriting the past.
9. Lessons remain auditable down to source records.
10. Privacy scope remains intact across summary and retrieval layers.

---

## Short Doctrine

> Hot memory manipulates.  
> Lukewarm memory orients.  
> Cold atlas remembers the shape.  
> Cold evidence remembers the specifics.  
> Deep recall moves from shape to specifics only when needed.

---

## Final Architecture

```text
HOT MEMORY
active exact blocks
        ↓
LUKEWARM MEMORY
current face and thread map
        ↓
COLD ATLAS
compressed searchable map of the past
        ↓
DEEP RECALL
goal-directed descent for missing detail
        ↓
COLD EVIDENCE LOG
exact provenance-rich historical records
        ↓
HYDRATION
only relevant detail returns to hot memory
```

Connected reasoning loop:

```text
cold atlas nominates A and B
→ deep recall hydrates exact A and B
→ hot memory holds them together
→ relational permutation rotates them
→ EF challenges the resulting relations
→ cold evidence stores exact outcomes
→ cold atlas updates its map
→ lesson library receives only earned abstractions
```

This design gives Chatty-Cog and the wider MCM something closer to a usable sense of personal history:

- broad recollection when gist is enough;
- effortful exact recall when the edge case matters;
- and a stable evidence layer that prevents the present interpretation from silently rewriting the past.
