# Concept Families and Axes of Variation

> **Purpose:** Explain why closely related concepts are confused, substituted, or over-applied — and make that confusion *useful*.

---

## 1. Core Insight

Many concepts are not isolated.
They belong to **families** that:

* share acquisition motifs
* share structural shape
* differ primarily by **axis of variation**

Learner confusion often arises not from ignorance, but from **correct abstraction applied to the wrong axis**.

---

## 2. What Is a Concept Family?

A concept family is a group of concepts that:

* solve related problems
* are structurally similar
* diverge by *what dimension they abstract over*

Families explain why learners substitute one concept for another.

---

## 3. Axis of Variation

An **axis of variation** answers:

> "What is allowed to change, and what must remain stable?"

Axes are:

* conceptual (not syntactic)
* often implicit in expert thinking
* rarely explicit in teaching materials

Making axes explicit dramatically reduces misapplication.

---

## 4. Example Family: Behavioral Abstraction (GoF-adjacent)

### Shared Motifs

* M1 — Structural Separation
* M2 — Interpretation vs Reification

### Family Members

| Concept   | Primary Axis               | Stable Part | Variable Part    |
| --------- | -------------------------- | ----------- | ---------------- |
| Strategy  | *How* behavior is chosen   | Context     | Selection logic  |
| Command   | *When* behavior runs       | Invoker     | Execution timing |
| Predicate | *Whether* behavior applies | Pipeline    | Condition        |
| Callback  | *Where* control returns    | Flow        | Continuation     |

Learners often pick the right *shape* but wrong *axis*.

---

## 5. Typical Misapplications (Teacher-Learned)

* Using Command when Strategy is needed
* Encoding Strategy as Predicate chains
* Overusing callbacks where dataflow suffices

These indicate:

* correct motif activation
* axis confusion

---

## 6. Acquisition-Level Interaction

At early levels (L1):

* family members are interchangeable in learner’s mind

At core ownership (L2):

* axis distinction becomes visible

At fluent use (L3+):

* learner selects concept *by axis*, not by name

---

## 7. Exercise Design Implications

Exercises must:

* isolate the intended axis
* make alternative axes fail visibly
* avoid prompts that allow axis collapse

Example:

* To teach Strategy, ensure *when* is fixed and *how* varies

---

## 8. System Representation

```yaml
concept_family:
  id: behavioral-abstraction
  shared_motifs:
    - M1
    - M2
  axes:
    - how
    - when
    - whether
  members:
    - strategy
    - command
    - predicate
```

---

## 9. Author-Facing Insight

High substitution rates inside a family indicate:

* unclear axis signaling
* premature naming
* exercise ambiguity

This is *diagnostic*, not failure.

---

## 10. Design Constraint

> Concepts should not be taught in isolation if they belong to a family.
> Axes must eventually be made explicit.

---

## 15. Time is an abstraction axis

Errors involving variable lifetime, scope, or unintended shared state are often not "bugs" but **temporal misalignment**.

Learners extend the lifetime of state because the *time axis* was never made explicit.

Concurrency failures frequently surface as delayed evidence of this misunderstanding.

---

## 16. Declarative vs imperative is semantic weight

"Too procedural" feedback usually signals **excess semantic weight placed on control flow**.

Declarative approaches shift meaning from *how* to *what*, reducing cognitive and temporal load.

This distinction must be modeled, not merely named.
