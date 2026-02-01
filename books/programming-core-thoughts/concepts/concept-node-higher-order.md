# Concept Node: Higher-Order Functions

> **Concept ID:** hof.core
> **Domain:** Programming abstractions
> **Status:** Instantiated (draft, feedback-open)

---

## 1. Identity

* **Canonical Name:** Higher-Order Functions
* **Short Label:** HOF
* **Aliases / Pre-names:**

  * functions as values
  * passing behavior
  * verbs as data

---

## 2. Preconditions (Conceptual Dependencies)

A learner encountering this node is expected to already have experiential familiarity with:

* Functions as named transformations
* Basic composition (output feeds input)
* Collections / sequences (implicit or explicit)
* Control flow (conditionals, loops)

> ⚠️ These are *experience-level*, not formal knowledge prerequisites.

---

## 3. Core Insight

> **Behavior can be treated as data.**

A function is not only something you *do* — it is something you can:

* pass
* return
* store
* combine

This allows *structure* to be separated from *variation*.

---

## 4. Recognizable Moments (Before Naming)

The learner has *already used* Higher-Order Functions if they have:

* Written duplicated logic differing only by a small rule
* Parameterized behavior with conditionals or flags
* Chosen between multiple strategies at runtime

These moments are candidates for **retroactive naming**.

---

## 5. Canonical Examples

### 5.1 Chess Player Strategy

```pseudo
player_random = moves => any(moves)
player_defensive = moves => find(moves, is_defensive?) or any(moves)

play(player_strategy)
```

> The game engine is stable. Strategy varies.

---

### 5.2 Collection Processing

```pseudo
map(items, transform)
filter(items, predicate)
reduce(items, combine)
```

> Shape is fixed. Meaning is injected.

---

## 6. Typical Anti-Patterns (Signals)

### A1. Branching on Type / Mode

```pseudo
if player_type == "random" then ...
if player_type == "defensive" then ...
```

**Signal:** behavior encoded as data instead of behavior-as-value.

---

### A2. Flag Explosion

Functions that accept booleans or enums to alter behavior.

---

### A3. Premature Naming

Naming a function parameter before the learner understands what *varies*.

---

## 7. Exercise Archetypes

### E1. Refactor Duplication

* Given multiple similar functions
* Extract the varying behavior

### E2. Strategy Injection

* Same engine
* Multiple behaviors plugged in

### E3. Behavior Discovery

* Learner writes a solution
* System detects latent HOF usage
* Concept is revealed *after the fact*

---

## 8. Levels of Concept Acquisition

> Higher-Order Functions are not acquired in a single leap.

The system recognizes **graded ownership**.

### L0 — Unseen

* Learner has not encountered situations requiring behavior abstraction

### L1 — Structural Separation

* Learner separates stable process from variable decision
* Variation encoded as data (flags, modes, enums)
* Typical form: interpreted strategies

### L2 — Behavior as Value (Core HOF)

* Learner passes functions as arguments
* Engine becomes agnostic to strategy
* Canonical recognition point

### L3 — Fluent Composition

* Learner combines behaviors
* Uses map / filter / reduce naturally
* Abstracts over multiple axes

### L4 — Reflective Use

* Learner recognizes HOFs in unfamiliar domains
* Can explain *why* the abstraction works

---

## 9. Partial Understanding Representation

The system may record **partial ownership** without naming the concept.

```yaml
partial_understanding:
  concept: hof.core
  level: L1
  missing: behavior-as-value
```

Partial understanding:

* is not an error
* is not surfaced to the learner as failure
* may later trigger retroactive recognition

---

## 10. Evaluation Signals (Non-Binary)

* Level reached (L0–L4)
* Time spent per level
* Number of domain transfers
* Anti-pattern frequency over time

> ❌ Not correctness-based
> ✅ Trajectory-based

---

## 9. Cross-Concept Links

* Delegation
* Immutability (pure HOFs)
* Polymorphism
* Strategy Pattern
* Partial Application

---

## 10. Promotion Candidates (Feedback-driven)

* New anti-patterns discovered via dialogue
* Domain-specific metaphors (e.g. sci-fi strategies)
* Emergent naming conflicts

---

## 11. Visualization Hints

* Flow diagram: stable pipeline + injected node
* Highlight unchanged structure across examples

---

## 12. System Hooks

* Exercise generator must track seen abstractions
* Feedback Space listens for branching-on-type signals
* Reader Assistant may retroactively name the concept

---

## 13. Status Notes

This node is expected to **expand significantly** as learner interaction accumulates.
It is intentionally incomplete.
