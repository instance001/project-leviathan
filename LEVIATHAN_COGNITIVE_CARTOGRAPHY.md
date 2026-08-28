# Project Leviathan — Cognitive Cartography

## Status

Exploratory architecture / research note.

This document defines a proposed mapping program for testing how learned knowledge territory, relational structure, and host scaffolding affect a model's ability to derive novel conclusions.

The aim is not to reduce a model to a single "reasoning score." The aim is to survey the shape of what can be reached from what is already known.

## Core premise

A model's apparent reasoning ability cannot be cleanly separated from the knowledge territory available to it.

A person may possess strong abstract reasoning ability and still fail to derive a conclusion if the necessary concepts, representations, or relational tools are too far outside their education or experience.

Therefore:

> Before asking whether a model can derive C, first establish that A and B lie inside a domain in which the model is demonstrably competent, while C itself is absent.

The base experimental form is:

**A + B, with no trace of C → attempt to derive C**

If the model reliably derives C, the result is more interesting than a case in which C may simply have been memorized or encountered during training.

## Why this matters

Conventional reasoning benchmarks often collapse several different questions into one:

- Did the model already know the answer?
- Did it retrieve something semantically equivalent?
- Did it infer the answer from available premises?
- Did it notice that a relation exists but fail to resolve it?
- Did it invent a bridge because one sounded plausible?
- Was the task simply too far outside the model's learned territory?

Cognitive cartography attempts to separate these.

The goal is to build maps of known territory, reachable novel territory, difficult crossings, productive launch points, dead ends, hallucination cliffs, cross-domain bridges, regions where host scaffolding extends reach, and regions where the correct result is recognition of an unresolved gap.

## The map is not radial

"Distance from training" should not be assumed to behave like a simple circle around a knowledge centre.

Learned territory may be uneven.

Two concepts can be equally well represented while having radically different outward affordances.

One concept may behave like a major junction:

**A → D, E, F, G**

while another behaves like a cul-de-sac:

**A → B → unresolved gap**

This means the useful object of study is not merely distance, but topology.

## Threadhopping topology

A central Leviathan question is:

> How easily can a model move from one grounded relational thread to another without losing coherence or inventing unsupported bridges?

Candidate properties include:

- **Branching density** — how many distinct, valid, evidence-supported directions can be reached from a starting point?
- **Bridge cost** — how much inference, context, scaffolding, or host intervention is required to move between relational clusters?
- **Productive depth** — how many successive derived conclusions can be accumulated before coherence or evidential support collapses?
- **Dead-end rate** — how often does a valid line of reasoning terminate without yielding useful further affordances?
- **Convergence** — do different grounded starting paths independently arrive at the same derived conclusion?
- **Launch-point quality** — do particular concepts or relations consistently act as unusually productive starting points for further derivation?
- **Hallucination cliff** — at what point does the model stop identifying grounded relationships and begin constructing unsupported bridges with high confidence?

## Earned novelty

A derived conclusion should not automatically terminate an experiment.

If C is valid and properly supported, C can become new grounded territory for the next step:

**A + B → C**  
**C + D → E**  
**E + F → G**

This allows measurement of cumulative intellectual reach.

The interesting question becomes:

> How long can a model accumulate earned novelty before error, unsupported inference, or representational poverty destroys the chain?

Some conclusions may be terminal but correct. Others may be highly fertile, creating many further valid derivations.

This suggests that idea fertility may itself be a measurable property of learned relational geometry.

## Knowledge territory versus reasoning reach

A model may show several distinct outcomes when asked to derive a withheld C:

1. **Clean derivation** — C is reached from the supplied premises with an evidence-supported path.
2. **Scaffolded derivation** — C is reached only after bounded hints, restructuring, or host-assisted decomposition.
3. **Gap recognition** — the model correctly identifies that A and B imply an unresolved relation but cannot responsibly derive C.
4. **Relation failure** — the model fails to identify the relevant relationship at all.
5. **Hallucinated bridge** — the model supplies C or an alternative conclusion without adequate support.

These should not be collapsed into a single pass/fail score.

In some conditions, "there is a gap here, but I cannot responsibly cross it" may be a stronger cognitive result than a confident but unsupported answer.

## Corpus as geometry

Corpus design may affect more than factual recall.

Two models with similar factual competence may possess very different relational terrain if their corpora differ in ordering, density, cross-linking, causal structure, analogy, representation diversity, exposure to transformations, or sequencing of prerequisite concepts.

The same factual material could therefore support different reasoning reach.

This creates a direct experimental bridge to Relational Curriculum Geometry.

A core question is:

> Can corpus structure change the shape of reachable thought without materially changing the amount of factual knowledge available?

## Model / corpus pair as the unit of analysis

A cognitive reach map should be treated as a property of a **model-corpus-condition pair**, not of a model in the abstract.

Useful comparisons include:

- same architecture, different corpora;
- same corpus, different architectures;
- same model and corpus, different host scaffolding;
- same domain, different auxiliary-domain exposure;
- same token budget, different curriculum geometry;
- same starting knowledge, different relational organization.

## Leviathan role

Leviathan is suited to this work because it can preserve the path rather than only the answer.

Every hop can retain starting premises, corpus-grounded support, derived claims, failed bridges, uncertainty, verification, scaffolding used, rejected alternatives, convergence with independent paths, and provenance of promoted derived knowledge.

The resulting object is not merely a benchmark score.

It is a map.

## Long-term research question

The largest question is not:

> "Is this model intelligent?"

It is:

> "Given this learned territory, what novel territory can this system reach, by what paths, at what cost, with what reliability, and where does the bridge run out?"

That is the proposed foundation of Leviathan cognitive cartography.
