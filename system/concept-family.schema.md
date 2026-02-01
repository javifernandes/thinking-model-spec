# Concept Families & Axes of Variation (Schema)

> This schema generalizes **learning beyond individual concepts**.
> It models how related abstractions cluster, diverge, and compete.

---

## 1. Concept Family

A **Concept Family** is a group of abstractions that:

* share structural similarity
* differ primarily by **intent**, **axis selection**, or **contextual emphasis**

Examples:

* Strategy / Command / Predicate
* Map / Filter / Reduce
* Event / Message / Command

```yaml
concept_family:
  id: behavior-encapsulation
  description: Ways of treating behavior as an explicit, manipulable unit
  members:
    - strategy
    - command
    - predicate
```

---

## 2. Axes of Variation

An **Axis** is a dimension along which concepts in a family differ.

Typical axes:

### a) Intent Axis

* *Why* is this abstraction introduced?
* What future change does it anticipate?

### b) Temporal Axis

* Immediate execution vs deferred execution
* Single-use vs repeatable

### c) Ownership Axis

* Who decides the behavior?
* Who owns invocation vs definition?

### d) Semantic Weight Axis

* Is behavior descriptive, imperative, or interrogative?

```yaml
axis:
  id: intent
  values:
    - vary-algorithm
    - represent-action
    - test-condition
```

---

## 3. Learning Levels Across Families

Learning is **layered**, not binary.

### Level 1 — Tool Use

* Learner applies one concept to one problem
* No comparison with alternatives

### Level 2 — Pattern Awareness

* Learner recognizes multiple related patterns
* Can explain differences post hoc

### Level 3 — Axis Selection

* Learner faces ambiguous problem
* Multiple patterns viable
* Must choose axis based on context, values, constraints

```yaml
learning_level:
  level: 3
  description: Axis selection under uncertainty
```

---

## 4. Misapplication as Signal

When learners choose a "wrong" pattern:

* This is often **family-level success**
* And **axis-level misalignment**

The system records:

* which family was activated
* which axis was misinterpreted

```yaml
misapplication:
  family: behavior-encapsulation
  chosen: command
  expected: strategy
  axis_confused: intent
```

---

## 5. Exercise Design Implication

Exercises should:

* constrain some axes
* intentionally leave others ambiguous

This enables:

* observation of learner priorities
* emergence of design reasoning

> Poor exercises leak axes.
> Good exercises surface them.

---

## 6. Author Feedback Loop

Aggregated signals enable the author to:

* detect systematic axis confusion
* refine explanations or examples
* introduce meta-level content ("why this choice matters")

---

## 7. System Contract

* Concepts belong to families
* Families define axes
* Learning is movement across axes, not checklist completion

This schema applies across domains:

* programming
* mathematics
* physics
* language
