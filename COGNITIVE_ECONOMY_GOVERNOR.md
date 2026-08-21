# Cognitive Economy Governor

**Status:** Working architecture specification  
**Purpose:** Prevent the MCM from collapsing into recursive over-analysis, runaway triangulation, summary-of-summary sludge, and unnecessary cognitive expense  
**Primary related systems:** Tri-Helix Memory, Dual Cold Memory, Why Library, Relational Permutation Engine, EF Engine, Assumption Freeze, Worldview Branching, Lesson Library, Chatty-Cog, ChattyFactory

---

## Core Claim

A capable cognitive system does not reason as deeply as possible about every input.

It reasons only as deeply as the current intent, stakes, uncertainty, and expected value justify.

The Cognitive Economy Governor is a host-owned negative control layer that limits:

- reasoning depth,
- memory descent,
- permutation count,
- EF retries,
- worldview branching,
- lesson promotion effort,
- operator-facing explanation,
- and total cognitive expenditure.

It does not decide what is true.

It does not produce methods.

It does not suppress evidence merely because the evidence is inconvenient.

It decides whether more cognition is justified.

> Depth on demand, not depth by default.

---

## Human Analogy

The governor is an engineering analogue of the human internal voice that says:

- hold your tongue;
- keep it simple, stupid;
- this is not worth the brain damage;
- we already know enough to act;
- that detail does not change the decision;
- stop rewording the same thought;
- park it until something new happens;
- this is important enough to strain for;
- this one deserves another angle;
- this uncertainty is acceptable.

It is not anti-curiosity.

It is what prevents curiosity from becoming self-consuming recursion.

---

## The Problem

Without a governor, the full MCM stack can become an epistemic bureaucracy.

```text
observation
→ summary
→ summary of summary
→ assumption behind summary
→ worldview behind assumption
→ alternative worldview
→ comparison of worldviews
→ summary of comparison
→ challenge to comparison frame
→ recursive collapse
```

The system may spend enormous compute and context while producing little or no decision-relevant information.

Typical failure forms:

- repeated paraphrase mistaken for progress;
- every uncertainty treated as an obligation to resolve now;
- every contradiction triggering a worldview branch;
- every memory query descending into raw evidence;
- every similarity triggering full relational permutation;
- every failure triggering EF triangulation;
- every cluster triggering a lesson candidate;
- every lesson candidate triggering exhaustive transfer testing;
- every answer burdening the operator with internal complexity.

The result is cognitive sludge.

---

## Authority Boundary

The governor has **negative authority only**.

It may:

- stop;
- pause;
- defer;
- limit;
- request clarification;
- permit one deeper level;
- permit a bounded number of additional probes;
- mark unresolved;
- return an investigation to dormancy;
- suppress low-value operator-facing detail while preserving it internally.

It may not:

- invent a conclusion;
- select a preferred positive method;
- declare an unresolved question solved;
- delete contradictory evidence;
- lower standards merely to finish;
- rewrite user intent;
- promote a lesson;
- force a worldview winner;
- transform “unknown” into “false”;
- block operator-requested depth without surfacing the conflict.

---

## Core Law

```text
Use the shallowest cognitive path that satisfies frozen user intent
and preserves required truthfulness.
```

The governor should ask:

1. Is the current understanding sufficient for the requested action?
2. Would deeper reasoning likely change the decision?
3. Did the previous pass produce materially new information?
4. Are the stakes high enough to justify more cost?
5. Is the decision reversible?
6. Is exactness required, or is a broad shape sufficient?
7. Can the unresolved remainder safely sleep?
8. Has the operator explicitly requested deeper inspection?

---

## Material Information Gain

Another cognitive pass is justified only when it is expected to do at least one of the following:

- add new evidence;
- recover exact detail that matters;
- eliminate a live possibility;
- expose a contradiction;
- narrow a boundary;
- distinguish two previously conflated cases;
- change confidence meaningfully;
- change the intended action;
- reveal a hidden assumption;
- test a prediction;
- create a materially different probe;
- connect a dormant investigation to genuinely new evidence.

The following do **not** count as material gain:

- paraphrasing;
- renaming;
- stylistic elaboration;
- repeating the same comparison vector;
- producing another summary with no new distinction;
- increasing confidence without new evidence;
- multiplying nearly synonymous hypotheses;
- re-running the same probe under trivial wording changes;
- expanding explanation after the decision is already stable.

> Rewording is not information gain.

---

## Cognitive Depth Ladder

The governor controls descent through explicit levels.

## Level 0 — Surface Action

Use:

- current hot context;
- frozen user intent;
- Why Library surface knowledge;
- immediately available evidence.

Typical questions:

- Is this ordinary?
- Is the answer already known well enough?
- Is the action low-risk and reversible?
- Does the user need only a direct answer?

Possible outputs:

```text
SPEAK_NOW
ACT_NOW
KEEP_SIMPLE
ASK_ONE_CLARIFYING_QUESTION
```

Most work should end here.

---

## Level 1 — General Shape

Use:

- lukewarm summary;
- Cold Atlas;
- broad prior patterns;
- known lesson boundaries.

Enter when:

- surface knowledge is insufficient;
- a known edge may matter;
- the current case resembles prior work;
- broad historical context may resolve uncertainty.

Possible outputs:

```text
SPEAK_WITH_CAVEAT
ACT_WITH_GUARDRAIL
DESCEND_TO_EXACT_RECALL
SLEEP_UNRESOLVED
```

---

## Level 2 — Exact Recall

Use:

- Cold Evidence Log;
- exact event order;
- source spans;
- directional relation atoms;
- exact prior failures;
- exact lesson provenance.

Enter when:

- attribution matters;
- sequence matters;
- the broad summary may be lossy;
- a boundary case is suspected;
- a durable decision depends on exact precedent;
- the operator requests specifics.

Possible outputs:

```text
EXACT_DETAIL_RECOVERED
PARTIAL_DETAIL_ONLY
CONTRADICTION_FOUND
NO_SUPPORTING_RECORD
DESCEND_TO_RELATIONAL_COMPARISON
```

---

## Level 3 — Relational Comparison

Use:

- active A/B or A/B/C working set;
- selected comparison vectors;
- like / unlike / unknown / contradiction records;
- bounded permutation passes.

Enter when:

- exact facts still do not resolve the issue;
- two cases may share hidden structure;
- a false analogy must be tested;
- a recurring residual pattern may exist.

Possible outputs:

```text
RELATION_CLARIFIED
BOUNDARY_EXPOSED
NO_MATERIAL_GAIN
MORE_VECTOR_ALLOWED
DESCEND_TO_EF
SLEEP_UNRESOLVED
```

---

## Level 4 — EF Pressure

Use:

- materially different probes;
- failure vaults;
- retry deltas;
- triangulation;
- evidence-backed candidate narrowing.

Enter when:

- a conclusion may become durable;
- a constraint may be proposed;
- repeated failure remains unexplained;
- a candidate invariant must be challenged;
- a lesson may be promoted.

Possible outputs:

```text
CANDIDATE_NARROWED
CANDIDATE_REJECTED
EVIDENCE_INSUFFICIENT
TRIANGULATION_DORMANT
DESCEND_TO_WORLDVIEW_REVIEW
```

---

## Level 5 — Worldview Review

Use:

- assumption snapshots;
- worldview comparisons;
- alternative library branches;
- recurring structured contradiction.

Enter only when:

- the current organising assumptions repeatedly fail;
- contradictions recur across independent cases;
- a stable alternative frame exists;
- the alternative changes meaningful predictions or actions.

Possible outputs:

```text
CURRENT_WORLDVIEW_RETAINED
CURRENT_WORLDVIEW_NARROWED
ALTERNATIVE_BRANCH_PROPOSED
MULTIPLE_FRAMES_REMAIN_ACTIVE
INSUFFICIENT_FOR_BRANCH
```

Very little work should reach this level.

---

## Default Depth Policy

```text
Start shallow.
Descend one level at a time.
Require a reason for each descent.
Stop as soon as frozen intent is satisfied.
```

The governor should never awaken the entire cognitive stack merely because the stack exists.

---

## Governor Inputs

```text
CognitiveEconomyInput
- frozen_intent_ref
- current_question
- current_action
- stakes
- uncertainty
- novelty
- contradiction_strength
- reversibility
- decision_impact
- evidence_quality
- current_depth
- compute_spent
- context_spent
- elapsed_time
- operator_patience
- operator_requested_depth
- passes_completed
- material_gain_history
- unresolved_value
- dormancy_status
- privacy_scope
```

---

## Governor Outputs

```text
CognitiveEconomyDecision
- decision_id
- disposition
- permitted_depth
- permitted_additional_passes
- permitted_context_budget
- permitted_compute_budget
- required_stop_condition
- reason
- unresolved_disposition
- operator_message_policy
- created_at
```

Possible dispositions:

```text
SPEAK_NOW
ACT_NOW
KEEP_SIMPLE
HOLD_YOUR_TONGUE
ASK_OPERATOR
DESCEND_ONE_LEVEL
ALLOW_ONE_MORE_PASS
ALLOW_BOUNDED_PROBES
STOP_DIMINISHING_RETURNS
SLEEP_UNRESOLVED
REACTIVATE_DORMANT
ESCALATE_HIGH_STAKES
REFUSE_UNSAFE_SHORTCUT
```

---

## “Hold Your Tongue”

Some internally generated material may be:

- interesting;
- technically valid;
- weakly relevant;
- too expensive to explain;
- unlikely to change the operator’s decision.

The governor may preserve that material without surfacing it.

```text
low relevance
+ low stakes
+ no action change
→ HOLD_YOUR_TONGUE
```

This is not evidence deletion.

It is operator-attention protection.

The hidden material should remain retrievable when appropriate.

---

## “Keep It Simple, Stupid”

Use the cheapest sufficient representation.

Examples:

```text
Why Library sufficient
→ do not descend to Cold Atlas

Cold Atlas sufficient
→ do not hydrate exact logs

Exact recall sufficient
→ do not launch permutations

One relation sufficient
→ do not awaken EF

Boundary note sufficient
→ do not branch a worldview
```

A simple answer is not a lower-quality answer when added complexity would not improve truth or action.

---

## “Too Cognitively Exhausting”

The system may identify a real unresolved question whose current value does not justify its cost.

```text
high remaining cost
+ low expected gain
+ low decision impact
→ SLEEP_UNRESOLVED
```

The investigation should retain:

- current state;
- evidence refs;
- open questions;
- reactivation conditions;
- last useful gain;
- reason for dormancy.

It should not continue spinning.

---

## Dormancy

Dormancy is a healthy cognitive state.

```text
active
→ diminishing returns
→ dormant
→ reactivated by genuinely new evidence
```

A dormant investigation is not:

- solved;
- rejected;
- forgotten;
- automatically promoted.

It is parked.

---

## Dormant Investigation Record

```text
DormantInvestigationRecord
- investigation_id
- current_state
- unresolved_questions
- evidence_refs
- last_material_gain
- last_gain_at
- reason_for_dormancy
- reactivation_conditions
- prohibited_reactivation_signals
- context_cost_so_far
- compute_cost_so_far
- created_at
```

Valid reactivation signals:

- new evidence;
- a materially different case;
- a contradiction;
- operator request;
- changed stakes;
- a previously unavailable exact record;
- a newly relevant lesson or boundary.

Invalid reactivation signals:

- time passing alone;
- repeated curiosity;
- paraphrased old evidence;
- a model restating the same hypothesis;
- unchanged failure labels.

---

## Diminishing Returns Detection

The governor should track gain over successive passes.

```text
Pass 1:
new contradiction found

Pass 2:
boundary narrowed

Pass 3:
same result rephrased

Pass 4:
same evidence reorganised

Decision:
STOP_DIMINISHING_RETURNS
```

Possible signals:

- repeated semantic similarity between outputs;
- no new evidence refs;
- no hypothesis eliminated;
- no confidence movement;
- no action change;
- no boundary change;
- no new unknown exposed;
- no prediction tested.

The governor does not need a perfect numerical score.

A coarse categorical judgement is sufficient.

---

## Expected Value of Another Pass

Conceptually:

```text
expected cognitive value
=
chance of changing the decision
× importance of that change
× evidence quality
− compute cost
− context cost
− operator burden
− delay cost
```

The implementation may use simple bands:

```text
HIGH
MEDIUM
LOW
NEGLIGIBLE
```

A pass should normally be denied when expected value is negligible.

---

## Stakes

High stakes justify deeper reasoning.

Possible stake dimensions:

- safety;
- legal;
- financial;
- irreversible action;
- destructive file operations;
- permission changes;
- durable lesson promotion;
- worldview revision;
- public release;
- sensitive personal information;
- major compute expenditure.

High stakes do not justify infinite reasoning.

They justify:

- stronger evidence standards;
- deeper recall;
- more independent probes;
- explicit uncertainty;
- operator confirmation.

---

## Reversibility

Reversible actions can tolerate shallower reasoning.

```text
low stakes
+ reversible
+ easy verification
→ act early, inspect outcome
```

Irreversible actions require deeper review.

```text
high stakes
+ irreversible
→ exact recall, stronger checks, operator confirmation
```

This prevents unnecessary analysis before cheap, safe experiments.

---

## Operator Control

The operator may:

- force shallow mode;
- force deep inspection;
- set a compute budget;
- set a context budget;
- pin an unresolved question;
- wake a dormant investigation;
- forbid worldview branching;
- require exact evidence;
- request only the conclusion;
- request the full reasoning trail.

The governor should surface conflicts honestly.

Example:

```text
The requested shallow path conflicts with the evidence standard
required for this irreversible action.
```

---

## Operator Patience

Operator attention is a scarce resource.

The governor should distinguish:

- internal cognition cost;
- operator-facing explanation cost.

A complex internal process may still yield a concise operator message.

Likewise, an operator may explicitly request the full audit trail.

Possible message policies:

```text
CONCLUSION_ONLY
CONCLUSION_PLUS_CAVEAT
BRIEF_EVIDENCE
FULL_AUDIT
ASK_BEFORE_EXPANDING
```

---

## Integration with Tri-Helix Memory

The governor controls memory depth.

```text
HOT
default

LUKEWARM
when current thread needs orientation

COLD ATLAS
when broad precedent matters

COLD EVIDENCE
when exact detail matters
```

The governor should prevent automatic deep-memory raids.

---

## Integration with Dual Cold Memory

The governor decides whether the system needs:

- atlas-level gist;
- exact evidence hydration;
- both.

It should ask:

```text
Does the current decision depend on exact sequence,
directionality, attribution, or boundary detail?
```

If no, atlas may be sufficient.

---

## Integration with Relational Permutation

The governor controls:

- which objects enter comparison;
- number of vectors;
- number of rotations;
- whether C is required;
- whether another pass is redundant.

Default rule:

```text
Start with the smallest useful vector set.
Expand only when new information appears.
```

---

## Integration with Semantic Dataset Sorting

The governor controls whether sorting is justified.

Sorting may be denied when:

- the dataset is too small;
- the active question is already answered;
- the proposed sort intent duplicates an existing run;
- the result would not affect action;
- the current cluster is too weak to justify a new geometry.

---

## Integration with EF Engine

The governor controls whether EF should awaken.

EF is justified when:

- failure repeats meaningfully;
- candidate constraints may become durable;
- materially different probes exist;
- unresolved evidence may affect future work.

EF should remain dormant when:

- one ordinary failure occurred;
- the action is reversible;
- a simple correction already succeeded;
- no durable lesson is proposed;
- no materially different probe is available.

---

## Integration with Assumption Freeze

Not every event needs a full three-depth assumption freeze.

Possible policy:

```text
ordinary low-stakes event
→ freeze surface assumption only

important classification
→ freeze surface + general shape

durable lesson / worldview-sensitive event
→ freeze surface + general + granular
```

The governor controls freeze depth.

---

## Integration with Worldview Branching

Worldview branching should be expensive.

Required signals:

- recurring contradiction;
- independent cases;
- stable alternative explanation;
- meaningful predictive difference;
- action or classification impact.

Most contradictions should produce:

- confidence reduction;
- boundary note;
- unresolved edge;
- lesson narrowing.

Not a new worldview.

---

## Integration with Lesson Promotion

Lesson promotion is cognitively expensive because it creates durable structure.

The governor should allow full promotion work only when:

- the lesson would affect future action;
- supporting evidence is strong;
- counterexamples have been considered;
- scope is narrow enough;
- exact provenance is available;
- unresolved edges are represented.

---

## ChattyFactory Operating Modes

### Routine Build

```text
intent
→ proposal
→ gate
→ execute
→ verify
```

No deep cognitive loop unless something fails or conflicts.

### Familiar Failure

```text
retrieve relevant Why Library lesson
→ inspect broad precedent
→ continue with guardrail
```

### Ambiguous Repeated Failure

```text
deep recall
→ bounded relational comparison
→ EF pressure
```

### Organising Assumption Failure

```text
freeze assumptions
→ compare with outcomes
→ consider library revision
```

### Recurring Worldview Failure

```text
evaluate alternative branch
```

This should be rare.

---

## Chatty-Cog Surfaces

### Cognitive Depth Indicator

Shows:

- current depth;
- reason for depth;
- permitted next step;
- compute/context spent.

### Keep It Simple Toggle

Constrains the host to the shallowest safe lane.

### Deep Dive Action

Explicitly permits one deeper level.

### Hold Your Tongue Policy

Controls whether low-value internal insights are surfaced.

### Dormant Questions Panel

Shows parked unresolved investigations and reactivation conditions.

### Cognitive Receipt

Shows:

- why the system stopped;
- what remained unresolved;
- what would justify reopening.

---

## Cognitive Receipt

```text
CognitiveReceipt
- receipt_id
- frozen_intent_ref
- start_depth
- final_depth
- passes_completed
- evidence_added
- hypotheses_eliminated
- boundaries_changed
- action_changed
- compute_spent
- context_spent
- stop_reason
- unresolved_items
- reactivation_conditions
- operator_message_policy
- created_at
```

---

## Stop Reasons

```text
INTENT_SATISFIED
DECISION_STABLE
REVERSIBLE_ACTION_AVAILABLE
NO_MATERIAL_GAIN
DIMINISHING_RETURNS
BUDGET_EXHAUSTED
OPERATOR_REQUESTED_STOP
INSUFFICIENT_EVIDENCE
NO_MATERIALLY_DIFFERENT_PROBE
UNRESOLVED_CAN_SLEEP
PRIVACY_BOUNDARY
WORLDVIEW_BRANCH_NOT_EARNED
```

A stop reason is not necessarily failure.

Stopping is often the correct cognitive act.

---

## Anti-Sludge Rails

Hard rules:

- paraphrase is not progress;
- no automatic descent through all memory layers;
- no worldview branch from one contradiction;
- no EF loop without a materially different probe;
- no lesson promotion because a cluster is interesting;
- no repeated sorting with unchanged data and intent;
- no hidden operator burden;
- no infinite unresolved loop;
- no assumption that deeper means better;
- no deletion of unresolved evidence merely to stop;
- no forced answer when “unknown” is the honest result;
- no cognitive spending beyond frozen user intent.

---

## Minimal Viable Prototype

### Scope

One small host-side governor around a bounded ChattyFactory audit or build simulation.

### Inputs

- frozen intent;
- stakes;
- reversibility;
- uncertainty;
- current depth;
- last-pass gain;
- compute/context spent.

### Decisions

Implement:

```text
SPEAK_NOW
KEEP_SIMPLE
DESCEND_ONE_LEVEL
ALLOW_ONE_MORE_PASS
STOP_DIMINISHING_RETURNS
SLEEP_UNRESOLVED
ASK_OPERATOR
```

### Prototype Flow

1. Begin at Level 0.
2. Evaluate sufficiency.
3. Permit one-level descent only with explicit reason.
4. After each pass, record material gain.
5. Stop after two consecutive no-gain passes.
6. Preserve unresolved state.
7. Reactivate only on new evidence or operator request.

---

## Prototype State Machine

```text
Surface
  ├─ sufficient → Complete
  └─ insufficient → GeneralShape

GeneralShape
  ├─ sufficient → Complete
  ├─ no_gain → Dormant
  └─ exact_detail_needed → ExactRecall

ExactRecall
  ├─ sufficient → Complete
  ├─ no_support → Unresolved
  └─ comparison_needed → Relational

Relational
  ├─ clarified → Complete
  ├─ no_gain → Dormant
  └─ durable_candidate → EF

EF
  ├─ rejected → Complete
  ├─ insufficient → Dormant
  └─ recurring_worldview_conflict → WorldviewReview

WorldviewReview
  ├─ retain → Complete
  ├─ narrow → Complete
  ├─ branch_not_earned → Dormant
  └─ branch_earned → AlternativeBranch
```

---

## Prototype API Sketch

```text
evaluate_depth(context)
record_pass_gain(pass_result)
request_descent(reason)
request_additional_pass(reason)
stop_investigation(reason)
sleep_unresolved(state, reactivation_conditions)
reactivate(investigation_ref, new_evidence_ref)
set_operator_budget(compute, context, patience)
```

---

## Required Tests

### Depth control

- starts at shallowest level;
- cannot skip levels without explicit high-stakes override;
- stops when intent is satisfied;
- reversible low-risk action prevents unnecessary descent.

### Information gain

- paraphrase does not count as gain;
- new evidence counts as gain;
- eliminated hypothesis counts as gain;
- repeated no-gain passes trigger stop.

### Dormancy

- unresolved investigation can sleep;
- sleeping does not mean solved;
- time alone does not reactivate;
- new evidence can reactivate.

### Worldview control

- one contradiction cannot create a branch;
- recurring independent contradiction may permit review;
- review may still remain unresolved.

### Operator control

- operator can request deep dive;
- operator can set budget;
- operator receives conflict warning when shallow mode is unsafe;
- operator can request conclusion-only output.

### Evidence preservation

- stopping does not delete evidence;
- hold-your-tongue does not erase internal records;
- unresolved state remains retrievable.

### Integration

- governor can deny unnecessary cold-log hydration;
- governor can cap permutation vectors;
- governor can prevent EF activation;
- governor can limit assumption-freeze depth;
- governor can prevent premature lesson promotion.

---

## Success Criteria

The governor is useful if it demonstrates:

1. Most ordinary tasks stop at Level 0 or Level 1.
2. High-stakes tasks reliably receive deeper review.
3. Repeated paraphrase is detected and stopped.
4. Unresolved investigations can sleep safely.
5. Exact evidence is retrieved only when it matters.
6. EF activation becomes exceptional rather than default.
7. Worldview branching remains rare.
8. Operator-facing output becomes shorter without losing honesty.
9. Compute and context use decrease without significant accuracy loss.
10. The system can explain why it stopped.

---

## Failure Modes

### Premature stopping

The governor blocks necessary reasoning.

**Rail:** stakes, irreversibility, contradiction, and operator override can force descent.

### Cost obsession

The governor optimises cheapness over truth.

**Rail:** truthfulness and frozen intent outrank economy.

### Hidden suppression

Useful contradictory evidence is withheld permanently.

**Rail:** hold-your-tongue affects surfacing, not retention.

### Infinite escalation

Every uncertainty triggers deeper levels.

**Rail:** explicit gain requirement and one-level-at-a-time descent.

### Dormancy graveyard

Questions sleep forever despite new evidence.

**Rail:** indexed reactivation conditions.

### Operator overload

The governor reports every internal stop decision.

**Rail:** concise receipts and message policies.

### Fake material gain

Models label paraphrase as novelty.

**Rail:** evidence refs, hypothesis changes, boundary changes, and action changes must be inspectable.

### Branch starvation

The governor never permits worldview revision.

**Rail:** recurring predictive failure can force review.

---

## Computational Strategy

The first prototype should prioritise inspectability.

Later optimisations may include:

- gain estimation with small local models;
- semantic duplicate detection;
- cached sufficiency decisions;
- budget bands by task type;
- operator-specific patience profiles;
- adaptive vector caps;
- per-depth token budgets;
- deferred batch analysis of dormant investigations;
- separate cheap and expensive cognition lanes.

The governor should remain simple.

It should not become another giant reasoning engine tasked with deciding how much reasoning to do.

---

## Minimal Decision Heuristic

A first implementation can use a small rule set.

```text
IF intent is satisfied
THEN stop.

ELSE IF action is low-risk, reversible, and verifiable
THEN act and inspect.

ELSE IF exact detail could change the decision
THEN descend one level.

ELSE IF last pass produced no material gain
THEN stop or sleep unresolved.

ELSE IF contradiction is strong and stakes are meaningful
THEN allow one bounded deeper pass.

ELSE ask operator or keep simple.
```

That is enough for an initial prototype.

---

## Short Doctrine

> Think cheaply when cheap thought is enough.  
> Descend only when exactness matters.  
> Triangulate only when durability matters.  
> Branch only when recurring contradiction earns it.  
> Rewording is not progress.  
> Unresolved questions are allowed to sleep.  
> Stop when further depth will not change the action.

---

## Final Architecture

```text
FROZEN USER INTENT
        ↓
CHEAPEST AVAILABLE COGNITIVE LAYER
        ↓
SUFFICIENCY CHECK
        ├─ sufficient → act / speak / stop
        └─ insufficient
                ↓
        MATERIAL-GAIN CHECK
                ├─ no likely gain → keep simple / sleep unresolved
                └─ likely gain
                        ↓
                DESCEND ONE LEVEL
                        ↓
                RECORD GAIN AND COST
                        ↓
                REPEAT ONLY WHILE JUSTIFIED
```

The Cognitive Economy Governor keeps the wider MCM from becoming an endlessly introspective machine.

It gives the system a healthy rhythm:

- most things receive quick competent thought;
- important uncertainty earns deeper recall;
- contradiction earns comparison;
- durable conclusions earn triangulation;
- worldview revision remains rare;
- and everything else is allowed to remain unfinished.
