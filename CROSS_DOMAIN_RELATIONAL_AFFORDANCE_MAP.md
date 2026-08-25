# Cross-Domain Relational Affordance Map

## Purpose

Knowledge in one domain may make withheld conclusions easier to derive in another.

This file defines a proposed Leviathan research lane for mapping those effects.

The central question is:

> Which learned domains act as enabling machinery for reasoning in other domains?

## Core premise

Reasoning does not occur over an abstract vacuum.

A model may possess the same target-domain facts under two training conditions while differing dramatically in its ability to derive new conclusions because one condition supplies additional conceptual tools.

Example:

**Chemistry alone**

versus:

**Chemistry + algebra**

If the second condition reaches withheld chemistry conclusions more easily, algebra may be functioning as a reusable relational tool rather than merely an unrelated body of facts.

Possible enabling structures supplied by an auxiliary domain include proportionality, equivalence, transformation, conservation, unknown-variable manipulation, rates, spatial relationships, state transitions, recursion, causal decomposition, probability, hierarchy, sequence, and symmetry.

## Directed relationships

Cross-domain assistance should not be assumed to be symmetric.

For example:

**Algebra → Chemistry** may provide strong assistance.

**Chemistry → Algebra** may provide little assistance.

Therefore the map should be represented as a directed graph.

Each edge represents:

> Added competence in domain Y changes the ease or reliability of deriving withheld conclusions in target domain X.

## Base comparison

Hold the target-domain task constant.

Compare conditions such as:

- **X**
- **X + Y**
- **X + Z**
- **X + Y + Z**

Where X is the target domain, Y and Z are auxiliary domains, and C is a withheld conclusion inside X.

Example:

- chemistry only;
- chemistry + algebra;
- chemistry + geometry;
- chemistry + algebra + geometry.

Measure the change in C-arrival behavior.

## Domain-assistance matrix

A simple aggregate representation could record:

| Target domain | Added domain | Effect on C reach | Notes |
|---|---|---:|---|
| Chemistry | Algebra | TBD | Proportions, unknowns, conservation |
| Chemistry | Geometry | TBD | Spatial and structural relations |
| Mechanics | Algebra | TBD | Rates, transformations, equations |
| Biology | Statistics | TBD | Uncertainty, populations, distributions |
| Programming | Logic | TBD | State, branching, formal relation |
| History | Causal modelling | TBD | Multi-factor consequence chains |

The point is not to assume these relationships in advance.

The interesting data may be the relationships that violate expectation.

## Higher-order effects

Some enabling effects may emerge only through combinations.

Possible pattern:

- X + Y: little change;
- X + Z: little change;
- X + Y + Z: large improvement.

This means pairwise testing alone is insufficient.

The system should eventually test higher-order combinations and interactions.

## Enabling domains

One long-term objective is to identify domains whose relational machinery improves derivational reach across many otherwise unrelated subjects.

Such domains may act more like **cognitive tools** than isolated stores of knowledge.

Candidate examples might include algebra, logic, probability, geometry, programming, causal modelling, systems thinking, formal language, measurement, and analogy.

These are hypotheses only.

The map must be empirical.

## Token-efficiency question

A particularly important experiment is:

> Does adding a small amount of carefully chosen auxiliary-domain training expand target-domain reasoning reach more than adding a much larger amount of target-domain material?

For example:

- +50M target-domain tokens;
- versus +5M auxiliary relational-tool tokens.

If the smaller auxiliary addition creates a larger increase in derivational reach, corpus design becomes an optimization problem rather than a simple data-volume problem.

This could support the proposition that:

> Breadth can sometimes deepen competence.

## Threadhopping between domains

Cross-domain mapping should also measure how easily a grounded reasoning path can move between domains.

Possible outcomes include:

- **Easy bridge** — a concept or relation transfers naturally and continues producing valid derivations.
- **Expensive bridge** — transfer is possible but requires substantial scaffolding or representation changes.
- **One-way bridge** — Y strongly assists X, while X does not meaningfully assist Y.
- **Conditional bridge** — transfer appears only when a third domain or concept is also present.
- **False bridge** — surface similarity encourages unsupported analogy.
- **No bridge** — the domains remain largely independent for the tested task.

## Surprising relationships as high-value data

Expected relationships are useful for calibration.

Unexpected relationships may be more scientifically interesting.

Examples might include musical structure aiding sequence reasoning, programming improving decomposition in non-computing tasks, geometry improving biological reasoning, narrative structure improving temporal causal tracking, or statistics reducing hallucination in uncertain domains.

These should not be assumed.

They should be tested.

## Integration with cognitive cartography

The full Leviathan map may eventually contain:

- nodes = domains, concepts, or relational clusters;
- directed edges = measured assistance or reachability;
- edge weights = ease, reliability, or cost;
- higher-order structures = combinations producing emergent reach;
- local topology = productive launch points, dead ends, branching density;
- risk zones = hallucination cliffs and unsupported analogy;
- host effects = areas where scaffolding or verification extends reliable reach.

This produces a terrain-and-transport map rather than a leaderboard.

Some domains may behave like destinations.

Some may behave like roads.

Some may behave like bridges.

Some may behave like high-value junctions.

Some may be fucking roundabouts.

## Research question

The long-term question is:

> What learned structures make further thought easier?

This is broader than measuring what a model knows.

It asks how different knowledge territories alter the reachability of novel conclusions elsewhere.

That is the proposed basis for cross-domain relational affordance mapping in Project Leviathan.
