# Withheld-C Base Corpus Protocol

## Purpose

This protocol defines a base test for distinguishing derivation from simple retrieval or memorized familiarity.

The experimental requirement is:

> The model must be demonstrably competent within a chosen domain, A and B must be present within that domain, and all trace of C must be withheld.

The system is then tested on whether it can derive C from A and B.

## Experimental primitive

**A + B → ?**

Where:

- **A** is a grounded fact, relation, rule, or structure available in the corpus.
- **B** is another grounded fact, relation, rule, or structure available in the corpus.
- **C** is a conclusion that follows from A and B.
- **C must not appear directly or semantically equivalently in the corpus.**

The test is not useful unless the model first demonstrates adequate competence with A, B, and the surrounding domain.

## Phase 1 — Domain competence calibration

Before testing C, establish that the model can reliably operate inside the relevant knowledge territory.

Calibration probes should test:

- direct recall of corpus-grounded facts;
- understanding of key terms;
- recognition of relevant relations;
- simple transformations explicitly supported by the corpus;
- discrimination between valid and invalid domain statements;
- ability to explain local mechanisms without requiring the withheld conclusion.

If the model cannot reliably perform these tasks, failure to derive C cannot be meaningfully attributed to reasoning reach.

## Phase 2 — C contamination audit

The strongest possible test requires C to be absent not only as an exact string, but as a paraphrase, synonymized statement, equivalent rule, worked example, near-identical analogy, memorized theorem, common-world fact, or sequence from which C is trivially copied.

For existing pretrained models, proving total absence may be impossible.

Therefore the cleanest experimental lane should use controlled synthetic domains.

## Synthetic microdomains

A synthetic microdomain can create arbitrary entities and relations that do not exist in ordinary training data.

Example:

- A **drel** under **moric pressure** acquires the property **vekan**.
- Any **vekan** object interacting with a **sorn** causes the sorn to enter state **tavil**.
- Q is a drel under moric pressure.
- Q interacts with R.
- R is a sorn.

Withheld conclusion:

> R becomes tavil.

The corpus should never state that conclusion directly.

The model must compose the available relations.

Synthetic ontologies should be randomized between runs to reduce benchmark memorization and shortcut learning.

## Phase 3 — Withheld-C derivation

The model is presented with the relevant premises and asked to solve the target problem.

The system should record:

- proposed C;
- supporting path;
- cited or retrieved premises;
- confidence;
- uncertainty;
- alternative candidates;
- whether scaffolding was requested or supplied;
- verification result.

The model's verbal confidence must not determine acceptance.

## Phase 4 — Distance manipulation

Once the base derivation succeeds, increase distance from the model's comfortable knowledge territory.

Possible manipulations include:

1. Adjacent premises in the same context.
2. Premises separated across passages.
3. Premises separated across documents.
4. Multi-hop composition.
5. Representation or synonym changes.
6. Irrelevant distractor relations.
7. Structural analogy within the same domain.
8. Transfer to a neighboring domain.
9. Transfer to a weakly related domain.
10. Transfer into deliberately alien relational territory.

The aim is to identify how derivational reliability changes with increasing relational distance.

## Outcome classes

Each attempt should be classified at minimum as one of the following:

1. **Clean C arrival** — correct withheld conclusion through a supported path.
2. **Scaffolded C arrival** — conclusion reached after bounded host assistance.
3. **Correct unresolved-gap recognition** — relevant relation noticed, unsupported conclusion refused.
4. **Missed relation** — relevant relationship not identified.
5. **Unsupported C** — correct-looking conclusion reached through an invalid or unsupported path.
6. **False C** — incorrect conclusion constructed.

## Metrics

Possible aggregate measures include:

- C-arrival rate;
- verified-path rate;
- unsupported-bridge rate;
- false-C rate;
- gap-recognition rate;
- scaffolding required;
- number of relational hops;
- time or token cost;
- confidence calibration;
- depth before cumulative failure;
- recovery after failed derivation;
- sensitivity to distractors;
- sensitivity to representation changes.

No single metric should be treated as the whole result.

## Critical distinction

A model that frequently says:

> "A and B appear to imply a missing relation, but I do not have enough grounded support to determine C"

may outperform a model that confidently invents C in difficult regions.

The desired system should distinguish failure to know from failure to reason and from failure to remain epistemically bounded.

## Baseline experimental claim

This protocol does not attempt to prove human-like reasoning or consciousness.

It tests a narrower proposition:

> Given a domain in which a model is demonstrably competent, and given grounded premises A and B while C is withheld, how reliably can the system construct C, and how does that reliability change as relational distance increases?

That is sufficient to begin mapping cognitive reach.
