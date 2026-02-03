# Concept Acquisition Model (Domain-Independent)

<!-- (v0.1 scaffold) Moved under `system/specs/` -->

> This specification defines **how concepts are learned**, independent of domain.
> It is reusable across programming, math, physics, language, and beyond.

---

## 1. Core Premise

Concepts are not binary possessions.
They are **trajectories** through recognizable cognitive states.

However:

* Not all concepts require multiple levels
* Some concepts *appear* binary until usage reveals hidden gradients

The model must support **both**.

---

## 2. Acquisition Modes

Each concept node declares an **acquisition mode**.

### Mode A — Binary

Used for concepts that are:

* definitional
* atomic
* prerequisite vocabulary

Examples:

* what a function is
* variable naming
* basic arithmetic operators

Representation:

```yaml
acquisition:
  mode: binary
```

System behavior:

* detect presence / absence
* no partial states tracked
* errors are usually semantic, not structural

⚠️ Caveat:
Binary is a *default assumption*, not a truth claim.
The system may later discover gradients.

---

### Mode B — Graded (Levels)

Used for concepts that:

* restructure thinking
* appear across domains
* emerge before naming

Examples:

* higher-order functions
* immutability
* abstraction
* delegation
* conservation laws (physics)
* grammatical tense (language)

Representation:

```yaml
acquisition:
  mode: graded
  levels:
    - id: L0
      label: unseen
    - id: L1
      label: partial / workaround
    - id: L2
      label: core ownership
    - id: L3
      label: fluent use
    - id: L4
      label: transfer / reflection
```

Levels are **concept-specific**, not globally fixed.

---

## 3. Transitional States Are First-Class

The system explicitly models **in-between states**:

* workaround solutions
* brittle success
* interpreted abstractions
* overfitting to examples

These states:

* are not errors
* are not failures
* are *evidence of learning in motion*

---

## 4. Surprise Principle

> The system must assume that the author is wrong about learning shape.

Therefore:

* Binary concepts may be promoted to graded
* New intermediate levels may be discovered
* Unexpected paths are stored, not discarded

This preserves pedagogical humility.

---

## 5. Domain Generalization

The same acquisition patterns recur across domains:

| Pattern               | Programming  | Math             | Physics            | Language          |
| --------------------- | ------------ | ---------------- | ------------------ | ----------------- |
| Structural separation | HOF          | function vs rule | law vs instance    | syntax vs meaning |
| Invariance            | immutability | identity         | conservation       | grammar rules     |
| Delegation            | strategy     | operator         | frame of reference | tense/voice       |

Concept nodes reference **shared acquisition motifs**.

---

## 6. Time as Signal

For graded concepts, the system tracks:

* time per level
* regressions
* skips
* cross-domain transfer latency

Time is treated as **cognitive resistance**, not performance.

---

## 7. Author-Facing Implications

Authors can:

* inspect unexpected learning paths
* discover hidden complexity in "simple" concepts
* decide whether to formalize new levels

The model supports **retroactive theory refinement**.

---

## 8. Design Constraint

> The system does not enforce a learning theory.
> It allows one to *emerge from use*.
