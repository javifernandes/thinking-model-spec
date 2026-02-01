# Concept Node Bindings

> **Purpose:** Bind individual concept nodes to families, axes, motifs, and detection rules.

This layer connects:

* abstract family structure
* concrete book concepts
* system detection behavior

---

## 1. What Is a Concept Node Binding?

A binding specifies how a *single concept* participates in:

* one or more families
* specific axes of variation
* learner-signal interpretation

It allows the system to reason about *near misses*.

---

## 2. Example: Higher-Order Functions (HOF)

```yaml
concept_node:
  id: hof.core
  chapter: Naming and Abstraction

families:
  - id: behavioral-abstraction
    role: behavior-as-value

axes_emphasized:
  - how (behavior selection)
  - where (binding site)
  - semantic-weight (declarative vs imperative)

shared_motifs:
  - delegation
  - reification

neighbors:
  - strategy
  - predicate
  - callback

anti_patterns:
  - id: branching-on-type
    axis_violation: how
    description: behavior selection encoded via control flow

  - id: stateful-strategy
    axis_violation: time
    description: behavior stored with excessive lifetime

recognition_signals:
  - learner passes behavior as data
  - behavior applied in multiple contexts
  - composition without branching

misapplication_signals:
  - if/else on player type
  - storing behavior in mutable instance state
```

---

## 3. System Use

The system uses bindings to:

* classify learner attempts
* detect family-level understanding
* surface axis-level confusion
* generate reflective feedback

Example feedback:

> "You correctly treated behavior as a value, but fixed it too early. This is a time-axis issue."

---

## 4. Author Feedback Loop

Aggregated signals allow the author to:

* detect unclear axis presentation
* refine exercises
* add warnings or contrasts

Bindings evolve as new patterns emerge.

---

## 5. Design Constraint

> Concept nodes must be bindable without rewriting family definitions.

This ensures:

* reuse across domains
* late discovery of new anti-patterns
* system extensibility

---

## 15. Choosing abstractions under underspecification

You are not teaching abstractions.
You are teaching **how to choose abstractions when the problem is underspecified**.

At advanced levels, correctness is not binary.
What matters is:

* which questions the learner asks
* which axes they surface
* which assumptions they challenge

The system must reward *epistemic moves*, not just technical ones.

---

## Immutability — Concept Node Binding

```yaml
concept_node:
  id: immutability.core
  chapter: Two Philosophies of Change

families:
  - id: state-management
    role: state-transition-discipline

axes_emphasized:
  - time (state lifetime)
  - identity (value vs reference)
  - semantic-weight (state vs transformation)

shared_motifs:
  - snapshot
  - derivation
  - replay

neighbors:
  - mutation
  - event-sourcing
  - snapshotting

anti_patterns:
  - id: unnecessary-mutation
    axis_violation: time
    description: state mutated where derivation suffices

  - id: hidden-aliasing
    axis_violation: identity
    description: multiple references to mutable state

recognition_signals:
  - state represented as value
  - transformations return new state
  - old and new states coexist

misapplication_signals:
  - defensive copying everywhere
  - immutability used without need, harming clarity
```

**Key pedagogical note:**
Immutability is often mislearned as a *rule*.
It must be learned as a **temporal and semantic alignment tool**.
