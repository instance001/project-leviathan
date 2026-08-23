# Leviathan Cognitive Gears and Tuning-Fork Calibration

**Status:** Working architecture and experimental specification  
**Project context:** Project Leviathan / Cognitive Economy Governor / pressure-driven thread hopping / controlled novelty calibration / blind-stage reasoning  
**Purpose:** Define the hypothesis that Leviathan may require multiple validated operating regimes rather than one universal configuration, and describe how controlled calibration models can be used to discover, compare, and tune those regimes.

---

# 1. Core Claim

Leviathan should not assume that one configuration is optimal for all reasoning tasks.

The same underlying system may need to operate in materially different regimes depending on:

- task type;
- ambiguity;
- stakes;
- available time;
- available compute;
- memory demand;
- novelty;
- contradiction level;
- number of active threads;
- pressure;
- reversibility;
- required confidence.

The useful abstraction is therefore not:

> **one perfect reasoning configuration**

but:

> **a gearbox of validated cognitive operating modes.**

Each gear may use the same underlying organs and connective tissue while changing:

- activation gain;
- thread concurrency;
- hop thresholds;
- memory hydration depth;
- EF depth;
- mutation diversity;
- negative-space farming intensity;
- C-composition budget;
- Pub Test hostility;
- stopping thresholds;
- uncertainty tolerance.

The model remains the same.

The host machinery remains the same.

The operating regime changes.

---

# 2. Observation That Motivated the Hypothesis

A useful human analogy appeared under two very different operating conditions.

## Richer concurrent mode

Under better conditions, several tasks may remain substantially active at once:

```text
task A: hot
task B: hot
task C: warm-hot
task D: warm
peripheral information: semantically available
```

Properties:

- richer concurrency;
- easier cross-thread movement;
- cheaper re-entry;
- more spontaneous context interaction;
- broader awareness;
- less explicit scheduling.

## Constraint mode

Under severe pressure or fatigue, the same underlying cognitive system may shift toward:

```text
task A: extremely hot
task B: low
task C: low
task D: near-idle
peripheral information: weak / fogged
```

Properties:

- narrower focal cone;
- stronger serialisation;
- more aggressive damping;
- greater re-entry cost;
- explicit thread hopping;
- stronger economy;
- reduced peripheral richness.

The important observation is:

> **These are not necessarily "good mode" and "bad mode."**

They may be different operating regimes suited to different constraints.

---

# 3. Same Machinery, Different Regime

Leviathan may not need different architectures for every task.

A cleaner model is:

```text
same memory
same EF Engine
same Negative-Space Farmer
same C Applicator
same Pub Test
same host authority
same blind-stage rules

+
different gain / timing / depth / resource settings

=
different cognitive gear
```

This preserves inspectability.

The system changes **how it runs**, not **what it is**.

---

# 4. Cognitive Gear

A cognitive gear is a validated cluster of operating parameters.

Example:

```text
CognitiveGear
- gear_id
- intended_task_shape
- activation_profile
- concurrency_limit
- pressure_thresholds
- thread_hop_policy
- memory_hydration_depth
- EF_budget
- mutation_diversity_requirement
- negative_space_threshold
- C_application_budget
- composition_policy
- ablation_policy
- pub_test_profile
- uncertainty_tolerance
- stop_condition
- resource_ceiling
- calibration_results
- known_failure_modes
```

A gear is not a personality.

It is a mechanical operating profile.

---

# 5. Candidate Gear Family

These are working hypotheses, not fixed categories.

Implementation may reveal that some should merge, split, or disappear.

---

## 5.1 Surface Gear

Purpose:

- ordinary;
- low-risk;
- reversible;
- low-ambiguity work.

Possible profile:

```text
concurrency: low
memory depth: shallow
EF depth: minimal
mutation count: very low
negative-space farming: only if non-closure appears
Pub Test: light
uncertainty tolerance: moderate
resource budget: low
```

Target behaviour:

> Solve ordinary problems without waking the entire cognitive factory.

---

## 5.2 Relational Gear

Purpose:

- compare multiple objects;
- detect hidden structure;
- test analogy;
- explore A/B relationships.

Possible profile:

```text
concurrency: medium-high
co-presence: high
relational permutation: active
memory hydration: medium
EF: bounded
negative-space farming: active
Pub Test: medium
```

Target behaviour:

> Keep enough structures simultaneously available for relational differences and similarities to become visible.

---

## 5.3 Deep Gear

Purpose:

- hard ambiguity;
- durable conclusions;
- complex hidden relations;
- difficult counterexamples.

Possible profile:

```text
memory depth: deep
exact recall: enabled
EF: high
mutation diversity: high
independent probes: high
C composition: permitted where earned
Pub Test: strong
resource budget: high
```

Target behaviour:

> Spend heavily only when deeper cognition is justified.

---

## 5.4 Constrained Gear

Purpose:

- scarce compute;
- scarce time;
- overloaded context;
- too many simultaneous obligations.

Possible profile:

```text
foreground gain: very high
background gain: low
concurrency: low
thread hopping: explicit
pressure sensitivity: high
memory hydration: targeted
EF depth: narrow
stop thresholds: aggressive
```

Target behaviour:

> Preserve focal competence by sacrificing concurrent richness.

---

## 5.5 Exploratory Gear

Purpose:

- imagination;
- novelty;
- weakly structured problems;
- broad search.

Possible profile:

```text
candidate breadth: high
mutation diversity: high
residue tolerance: high
closure pressure: low
composition: permissive but bounded
memory breadth: medium-high
Pub Test: delayed but strong
```

Target behaviour:

> Permit more possible structure before pruning.

The strong final gate matters because exploratory breadth increases nonsense risk.

---

## 5.6 Critical Gear

Purpose:

- safety-sensitive;
- high-stakes;
- irreversible;
- evidence-sensitive decisions.

Possible profile:

```text
independent probes: high
memory provenance: exact
EF: deep
blind-stage separation: strict
candidate redundancy: allowed
Pub Test: hostile
uncertainty tolerance: low
external validation requirement: strong
resource budget: high
```

Target behaviour:

> Prefer slower, more redundant reasoning over fast closure.

---

# 6. Gears Are Task-Fit, Not Rankings

The system should not assume:

```text
DEEP > SURFACE
CRITICAL > RELATIONAL
EXPLORATORY > CONSTRAINED
```

A gear is good only relative to the task.

Example:

```text
Surface Gear
excellent for ordinary lookup
terrible for hidden multi-C abstraction

Deep Gear
excellent for durable ambiguity
wasteful for simple reversible work

Constrained Gear
excellent under scarce resources
poor for broad simultaneous comparison

Exploratory Gear
excellent for novelty
dangerous for premature acceptance
```

The correct question is:

> **Which operating regime best fits this task and constraint envelope?**

---

# 7. Gear Selection Must Be Host-Owned

A model should not freely decide:

```text
"I feel like entering maximum cognition mode."
```

Gear selection should remain host-mediated.

Possible inputs:

- user intent;
- task reversibility;
- declared stakes;
- uncertainty;
- pressure;
- prior gear performance;
- available compute;
- time budget;
- memory requirement;
- failure history.

The host may propose or select among **already validated gears**.

It should not permit arbitrary self-invented configurations during a controlled run.

---

# 8. No Live Self-Rewriting

The system should prefer:

```text
switch validated gear
```

over:

```text
rewrite own reasoning architecture
```

This matters for:

- safety;
- reproducibility;
- debugging;
- calibration;
- provenance.

A surprising task should not trigger uncontrolled self-modification.

It may justify changing operating regime.

---

# 9. Gear Shift

A gear shift is a host-controlled state transition.

Example:

```text
GearShiftRecord
- shift_id
- from_gear
- to_gear
- trigger
- pressure_state
- task_state
- evidence
- expected_gain
- resource_delta
- approved_by_host
- created_at
```

Possible triggers:

```text
non-closure persists
contradiction rises
memory insufficiency detected
time budget falls
resource pressure rises
novelty demand increases
stakes increase
null-world suspicion rises
user explicitly requests deeper analysis
```

---

# 10. Gear Shifts May Be Part of Reasoning

A thread hop changes which local process is foregrounded.

A gear shift changes the broader operating regime.

They are related but distinct.

```text
THREAD HOP
local activation change

GEAR SHIFT
system-wide operating-profile change
```

Example:

```text
Relational Gear
↓
persistent contradiction
↓
Deep Gear
```

or:

```text
Deep Gear
↓
time pressure
↓
Constrained Gear
```

The gear shift itself may become a meaningful part of the reasoning trace.

---

# 11. The Tuning Fork

The controlled ground-up calibration model becomes essential here.

Its purpose expands.

It is not only a novelty test subject.

It becomes the **reference pitch** for discovering useful operating modes.

A tuning-fork experiment holds constant:

```text
same controlled model
same frozen weights
same world
same A/B problem
same hidden C
same visible evidence
```

Then varies:

```text
gear configuration
```

This isolates the effect of operating regime.

---

# 12. Gear Discovery Through Controlled Worlds

Suppose the same hidden-C world is tested under several configurations.

Example:

```text
Gear candidate A
- high concurrency
- medium EF
- broad memory

result:
recovers C

Gear candidate B
- narrow focus
- low EF
- fast hops

result:
misses C

Gear candidate C
- broad mutation
- strong farming
- high Pub Test

result:
recovers C but costs 4x compute
```

Now the question is no longer:

> Which gear is best?

It becomes:

> Which gear is efficient for which class of problem?

---

# 13. Gear Mapping

Over many controlled worlds, create a map.

Example:

```text
               Surface  Relational  Deep  Constrained  Exploratory  Critical

Simple lookup      ✓        -        -        ✓             -          -

Single hidden C    ✗        ✓        ✓        △             ✓          ✓

Multi-C            ✗        △        ✓        ✗             ✓          ✓

Null world         ✓        ✓        ✓        ✓             △          ✓

Far transfer       ✗        ✓        ✓        ✗             ✓          ✓

Time pressure      ✓        △        ✗        ✓             ✗          △
```

This is illustrative only.

The real map must be earned experimentally.

---

# 14. Gear Envelope

Each gear should acquire a documented performance envelope.

Example:

```text
GearEnvelope
- gear_id
- strong_task_classes
- weak_task_classes
- known_failure_modes
- null_world_performance
- rare_C_performance
- multi_C_performance
- transfer_performance
- compute_profile
- memory_profile
- latency_profile
- seed_stability
- confidence_calibration
```

The system should know not only:

> what this gear is good at

but:

> where this gear should not be trusted.

---

# 15. Gear Boundary Testing

The interesting region may be where one gear stops being adequate.

Example:

```text
Relational Gear works
until:
- C depth > 3 transforms
- contradiction count > threshold
- memory hydration demand > threshold
```

Then Deep Gear becomes justified.

The boundary itself should be measured.

This creates a practical routing policy.

---

# 16. Pressure and Gear Selection

Pressure may influence both:

```text
which thread wakes
```

and:

```text
which gear becomes appropriate
```

Example:

```text
mild contradiction
→ hop to relational comparison thread

persistent contradiction
→ shift Relational Gear → Deep Gear
```

or:

```text
resource pressure rises
→ shift Deep Gear → Constrained Gear
```

This creates two control scales:

```text
micro:
thread activation

macro:
operating regime
```

---

# 17. Human Analogy Without Literalism

The human analogy is useful only as an engineering prompt.

Humans appear capable of materially different cognitive regimes:

- broad concurrent awareness;
- narrow concentration;
- rapid serial task switching;
- exploratory association;
- cautious checking;
- crisis prioritisation.

Leviathan should not assume these correspond to literal biological modules.

The useful lesson is:

> one underlying system can exhibit different useful operating patterns under different demands.

---

# 18. Why One Universal Setting Is Likely Bad

A universal maximum-depth configuration risks:

- runaway compute;
- unnecessary EF loops;
- over-farming negative space;
- combinatorial C sludge;
- repeated memory descent;
- excessive Pub Test overhead;
- slow ordinary tasks;
- analysis paralysis.

A universal shallow configuration risks:

- missing hidden relations;
- poor transfer;
- weak boundary detection;
- premature closure;
- failure to wake necessary threads.

Therefore:

> **uniformity is not necessarily robustness.**

Task-fit may matter more.

---

# 19. Gear Calibration Variables

Candidate variables include:

```text
foreground_gain
background_gain
activation_decay
concurrency_limit
pressure_threshold
thread_hop_threshold
rehydration_threshold
memory_depth
EF_attempt_budget
mutation_diversity
independent_probe_minimum
negative_space_threshold
candidate_limit
composition_threshold
ablation_depth
Pub_Test_hostility
uncertainty_threshold
closure_threshold
resource_ceiling
```

The tuning fork lets these be measured rather than guessed.

---

# 20. Parameter Cluster, Not Single Knob

A useful gear may not correspond to one parameter.

It may be a stable cluster.

Example:

```text
Relational Gear

foreground_gain: medium-high
background_gain: medium
concurrency: 4
memory_depth: medium
EF_budget: 3
mutation_diversity: 4
Pub_Test: medium
closure_threshold: medium
```

Changing one knob may destabilise the whole profile.

Therefore calibration should search for **regimes**, not isolated magic values.

---

# 21. Stable Regime

A gear should only be considered real if it produces stable behaviour across:

- multiple worlds;
- multiple seeds;
- multiple surface forms;
- small parameter perturbations.

A profile that only works at:

```text
pressure_threshold = 0.4317
```

and collapses at:

```text
0.4316
```

is probably not a useful gear.

A useful gear should occupy a stable parameter region.

---

# 22. Gear Robustness Test

```text
candidate gear
↓
run baseline world suite
↓
perturb each parameter slightly
↓
rerun
↓
compare
```

Measure:

- target recovery;
- false closure;
- cost;
- transfer;
- stability.

This helps distinguish genuine operating regimes from accidental tuning artefacts.

---

# 23. Gear Specialisation May Be Granular

The eventual gearbox may be more detailed than the first six candidate gears.

Possible later specialisations:

```text
causal reasoning gear
temporal reasoning gear
role-boundary gear
multi-C composition gear
counterexample-heavy gear
memory-reconstruction gear
creative synthesis gear
low-resource gear
fast-decision gear
deep-audit gear
```

These should emerge from repeated calibration evidence.

Do not invent dozens in advance.

---

# 24. Gear Discovery Rule

> **Do not create a gear because it sounds conceptually neat.**

Create a gear only when:

```text
a recurring task class
+
a recurring parameter cluster
+
a reproducible performance advantage
```

appears.

The tuning fork should discover gears.

Architecture prose should not legislate them into existence.

---

# 25. Gear Promotion Gate

A candidate gear should be promoted only after:

- repeatable benefit;
- multiple controlled worlds;
- multiple seeds;
- known failure envelope;
- cost profile;
- comparison against neighbouring gears;
- ablation of major parameters;
- stable parameter region.

Possible states:

```text
CANDIDATE
EXPERIMENTAL
VALIDATED
RESTRICTED
RETIRED
```

---

# 26. Gear Receipt

```text
GearValidationRecord
- gear_id
- configuration_hash
- model_hashes
- world_suite_refs
- seed_refs
- target_recovery
- false_closure_rate
- rare_C_rate
- multi_C_rate
- transfer_rate
- cost_profile
- latency_profile
- robustness_results
- known_failures
- promotion_status
- created_at
```

---

# 27. The Gearbox Is Host Infrastructure

The gearbox should live at the host level.

The model does not own it.

The model may participate locally inside whichever gear is active.

The host owns:

- selection;
- switching;
- enforcement;
- receipts;
- rollback;
- bounds.

This preserves role discipline.

---

# 28. Gear Switching Should Be Observable

Every shift should be visible in the trace.

Example:

```text
RUN 028

00:00
Surface Gear

00:03
non-closure pressure > threshold

00:04
shift → Relational Gear

00:09
persistent contradiction

00:10
shift → Deep Gear

00:21
candidate C produced

00:23
shift → Critical evaluation profile

00:31
Pub Test complete
```

This makes operating dynamics inspectable.

---

# 29. Gear Switching Costs Matter

A gear shift is not free.

Possible costs:

- rehydration;
- state transformation;
- additional memory;
- lost cache locality;
- extra model calls;
- scheduling overhead;
- increased latency.

Therefore the host should not thrash between gears.

A gear-shift policy may need:

```text
minimum dwell time
cooldown
hysteresis
confidence requirement
pressure persistence
```

---

# 30. Hysteresis

Without hysteresis:

```text
pressure 0.49 → Gear A
pressure 0.51 → Gear B
pressure 0.49 → Gear A
pressure 0.51 → Gear B
```

The system thrashes.

A better policy:

```text
enter Deep Gear at pressure >= 0.70
leave Deep Gear only when pressure <= 0.45
```

The exact values are experimental.

The principle is:

> **enter and exit thresholds may differ.**

---

# 31. Cognitive Economy Governs Gear Cost

The Cognitive Economy Governor should treat gear depth as a cost decision.

Questions:

```text
Would a deeper gear likely change the outcome?

Are stakes high enough to justify the cost?

Did the previous gear produce new information?

Can the unresolved remainder safely remain unresolved?

Is the current decision reversible?

Is the current gear failing repeatedly?
```

The governor should not automatically escalate.

---

# 32. Gear Escalation and De-Escalation

Possible escalation ladder:

```text
Surface
↓
Relational
↓
Deep
↓
Critical
```

But this must not become the only routing pattern.

Possible lateral shifts:

```text
Relational → Exploratory
Deep → Constrained
Exploratory → Critical
Constrained → Relational
```

Task shape determines routing.

---

# 33. Gear Selection Is Itself Testable

Create controlled worlds where the correct challenge is not only recovering C.

It is selecting an efficient regime.

Example:

```text
World X:
Surface Gear sufficient

failure:
system escalates to Deep Gear unnecessarily
```

or:

```text
World Y:
Deep Gear required

failure:
system remains in Surface Gear and falsely closes
```

Measure routing quality.

---

# 34. Gear-Routing Metrics

Possible metrics:

```text
correct_gear_selection
unnecessary_escalation_rate
missed_escalation_rate
gear_thrash_rate
average_shift_count
cost_per_valid_C
latency_per_task_class
false_closure_by_gear
transfer_by_gear
```

---

# 35. Calibration Model as a Gearbox Tuning Fork

The controlled tiny model is especially valuable because:

- its weights remain fixed;
- its training history is known;
- hidden C is known to experimenters;
- task worlds can be regenerated;
- the model is cheap enough for many repeats.

This allows:

```text
same pilot
same aircraft
different transmission settings
```

The performance difference becomes attributable to host operation more cleanly.

---

# 36. Multiple Calibration Models

Eventually one tuning fork may not be enough.

Use multiple controlled base models:

```text
Model A:
very weak

Model B:
moderate

Model C:
different curriculum geometry

Model D:
different architecture

Model E:
same architecture, different seed
```

Then ask:

> Are gears model-specific or host-general?

A gear that only works on one model may still be useful.

But it should be labelled accordingly.

---

# 37. Gear Portability

Test:

```text
validated gear on Model A
↓
apply to Model B
↓
compare
```

Possible outcomes:

```text
portable
partially portable
model-family specific
seed sensitive
not portable
```

This helps distinguish:

- general host dynamics;
- model-specific tuning;
- accidental coupling.

---

# 38. Gear/Model Compatibility Matrix

Eventually:

```text
                Model A   Model B   Model C

Surface            ✓         ✓         ✓
Relational         ✓         △         ✓
Deep               ✓         ✓         △
Constrained        △         ✓         ✓
Exploratory        ✓         ✗         △
Critical           ✓         ✓         ✓
```

Again, this must be measured.

---

# 39. Role-Fit Extends to Cognitive Gear

A broader doctrine appears:

> **Fit the work not only to the model, but also to the model-plus-host operating regime.**

The same model may be:

- good in one gear;
- poor in another;
- unstable under another;
- surprisingly strong under a fourth.

This aligns with the wider host philosophy:

> do not force every pilot to fly every mission the same way.

---

# 40. Gear Failure Evidence

A failed gear run should be preserved.

Example:

```text
GearFailureRecord
- gear_id
- task_class
- world_ref
- failure_type
- pressure_state
- missed_C
- false_C
- resource_overrun
- thread_thrash
- memory_failure
- Pub_Test_failure
- boundary_failure
- replay_refs
```

Failure becomes calibration data.

---

# 41. Gears Can Be Retired

A gear that appears useful early may later prove redundant.

Example:

```text
Gear X
looked useful on 3 worlds
↓
larger suite shows no benefit over Relational Gear
↓
retire Gear X
```

Do not preserve gears for historical pride.

Preserve the receipts.

Retire the mechanism.

---

# 42. Gear Composition

Eventually some tasks may require phases rather than one persistent gear.

Example:

```text
Surface Gear
for initial framing

→ Exploratory Gear
for candidate generation

→ Relational Gear
for comparison

→ Deep Gear
for negative-space closure

→ Critical Gear
for final evaluation
```

This is not simultaneous gear stacking.

It is a **gear trajectory**.

---

# 43. Gear Trajectory

A run may therefore be described by:

```text
GearTrajectory
- run_id
- ordered_gear_refs
- shift_triggers
- shift_times
- state_handoff_refs
- cost_per_phase
- output_per_phase
- final_result
```

The trajectory itself may become a reasoning feature.

---

# 44. Gear Trajectory as a Learned Pattern

Over many runs, the host may observe recurring useful trajectories.

Example:

```text
hidden relational task
often benefits from:

Surface
→ Relational
→ Deep
→ Critical
```

But this should remain an empirically validated routing pattern.

It must not become a rigid recipe that overrides evidence.

---

# 45. No One-Shoe-Fits-All Doctrine

The system should explicitly reject:

> **one shoe fits all**

A better doctrine:

> **Use the shallowest and simplest validated gear that fits the current task. Shift only when evidence says the current gear is insufficient.**

This preserves cognitive economy.

---

# 46. Calibration Ladder

Suggested development order:

## Stage 1

One gear.

Make end-to-end Leviathan work at all.

## Stage 2

Tune that gear against a small controlled world suite.

## Stage 3

Create one deliberately different gear.

Example:

```text
Relational
versus
Constrained
```

## Stage 4

Show that each wins on a different task class.

## Stage 5

Add host-controlled switching.

## Stage 6

Measure shift cost and thrashing.

## Stage 7

Expand gear family only where evidence justifies it.

---

# 47. Minimal Gear Experiment

A clean first experiment:

```text
same tiny controlled GGUF
same world
same hidden C

Run A:
high-concurrency relational configuration

Run B:
low-concurrency constrained configuration
```

Compare:

- C recovery;
- thread hops;
- negative-space quality;
- cost;
- latency;
- held-out transfer.

Then repeat on a time-pressure world.

Expected possibility:

```text
Relational wins hidden-C world.
Constrained wins time-pressure world.
```

If that happens reliably, the gearbox hypothesis has empirical support.

---

# 48. Null Gear Experiment

Also test:

```text
different gears
same null world
```

A good gear should not force closure merely because it has more cognition available.

Deep gear must be able to say:

```text
NO VALID C SUPPORTED
```

More compute must not mean more hallucinated structure.

---

# 49. Pub Test Can Also Have Gears

The Pub Test itself may eventually require calibrated profiles.

Examples:

```text
LIGHT
ordinary coherence check

STANDARD
default adversarial critique

HOSTILE
high-stakes challenge

DOMAIN-SPECIALISED
when evaluator expertise differs
```

But the same caution applies:

Do not invent these prematurely.

First establish whether one evaluator profile is insufficient across task classes.

---

# 50. Gear-Specific Pub-Test Bias

A harsh Pub Test may be valuable for critical tasks but harmful in exploratory tasks.

Example:

```text
exploratory candidate:
weak but useful hypothesis

HOSTILE Pub Test:
kills it too early
```

Therefore evaluation severity may need to match lifecycle stage.

Possible rule:

```text
exploration:
preserve plausible unresolved candidate

promotion:
apply hostile Pub Test
```

---

# 51. External Validation Still Wins

No gear, no matter how well calibrated, becomes truth authority.

The final chain remains:

```text
mechanical reasoning
↓
internal adversarial evaluation
↓
user-visible evidence package
↓
external validation where required
```

Gear tuning improves the process.

It does not replace reality.

---

# 52. Inspectability Requirement

Every gear must remain inspectable.

The user should be able to answer:

```text
Which gear was active?

Why was it selected?

What triggered the shift?

What did the shift cost?

What changed in behaviour?

Which candidate appeared under which regime?

Would the result survive under another gear?
```

Opaque automatic mode switching would undermine the research value.

---

# 53. Replay Across Gears

One of the strongest debugging tools:

```text
same frozen problem
same model
same seed where possible

replay under:
Gear A
Gear B
Gear C
```

Compare trajectories.

This can expose:

- hidden dependence on concurrency;
- pressure threshold sensitivity;
- memory effects;
- EF depth effects;
- evaluation bias.

---

# 54. Cross-Gear Consensus Is Not Automatic Truth

If multiple gears produce the same C, that is interesting.

It is not proof.

Record:

```text
C17 recovered by:
Relational
Deep
Critical
```

This may increase confidence.

But shared model biases or shared evidence can still produce shared error.

The Pub Test and external validation remain necessary.

---

# 55. Cross-Gear Divergence Is Valuable

If:

```text
Relational → C17
Deep → C04
Exploratory → C12+C19
```

do not immediately average them.

The divergence is evidence.

Ask:

- what different information paths occurred?
- what pressure caused different hops?
- which candidate transfers?
- which survives cold evaluation?
- which gear exposed which boundary?

Different gears may reveal different parts of the negative space.

---

# 56. The Gearbox as Research Instrument

The final goal is not simply a user-facing "mode selector."

The gearbox is an experimental instrument for studying:

- concurrency;
- serialisation;
- pressure;
- memory depth;
- abstraction;
- resource economy;
- evaluation severity;
- transfer.

It lets us vary the cognitive regime while holding other factors constant.

---

# 57. What Success Would Look Like

A strong result would be:

```text
same controlled model
same hidden-world family
same host organs

Gear A:
best on shallow reversible tasks

Gear B:
best on hidden relational C recovery

Gear C:
best under severe resource constraint

Gear D:
best on null-world caution

Gear E:
best on creative synthesis but needs stronger final filtering
```

with reproducible envelopes and costs.

At that point the gearbox is real.

---

# 58. What Would Falsify the Gearbox Hypothesis

The hypothesis should weaken if:

- one configuration dominates almost every task;
- gear differences vanish across seeds;
- task-specific gains are tiny;
- switching costs exceed benefits;
- gear selection cannot be predicted reliably;
- parameter clusters are unstable;
- apparent gears are just arbitrary thresholds;
- simpler adaptive scaling performs equally well.

In that case, simplify.

Do not preserve the gearbox because the metaphor is attractive.

---

# 59. Relationship to Existing Leviathan Work

This document extends:

```text
LEVIATHAN_CONNECTIVE_TISSUE_AND_MICRO_GOVERNANCE.md

LEVIATHAN_NEGATIVE_SPACE_FARMING_AND_PUB_TEST.md

LEVIATHAN_BLIND_STAGE_REASONING_AND_CONTROLLED_NOVELTY_CALIBRATION.md
```

The previous files establish:

- connective tissue;
- micro-governance;
- pressure-driven hopping;
- EF negative-space farming;
- cold C application;
- adversarial Pub Test;
- blind frozen stages;
- controlled novelty testing;
- tuning-fork models.

This file adds:

> **the hypothesis that the tuning fork may reveal multiple stable cognitive operating regimes, each suited to different task envelopes.**

---

# 60. Compressed Doctrine

> **There may be no single optimal Leviathan mode.**

> **Same organs, different operating regime.**

> **A gear is a validated parameter cluster, not a personality.**

> **Different gears should earn different task envelopes.**

> **The host owns gear selection and switching.**

> **Pressure may trigger both local thread hops and larger gear shifts.**

> **Use the tuning fork to discover gears rather than inventing them from prose.**

> **A good gear must be stable across worlds, seeds, and small parameter changes.**

> **A gear must document where it fails.**

> **The simplest sufficient gear should win.**

> **Shift only when evidence says the current gear is insufficient.**

> **The gearbox itself must remain inspectable.**

---

# 61. Closing Position

The controlled calibration model is not merely a way to prove that Leviathan can derive a hidden C.

It may become the instrument used to discover **how Leviathan should think under different conditions**.

The likely question is not:

> What is the correct global configuration?

It may be:

> Which stable operating regime is appropriate for this task, under these pressures, with these resources, at these stakes?

If repeated controlled experiments reveal distinct parameter clusters that reliably outperform one another on different task families, then Leviathan does not have one cognitive setting.

It has a gearbox.

And the tuning fork tells us where the gears actually are.
