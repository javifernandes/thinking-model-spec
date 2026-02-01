# Acquisition Motifs

<!-- (v0.1 scaffold) Moved under `system/catalogs/` -->

> **Purpose:** Identify recurring *cognitive moves* learners make while acquiring concepts.
> Motifs are **domain-independent**, **concept-agnostic**, and **observable in action**.

---

## 1. What Is an Acquisition Motif?

An acquisition motif is a **recognizable pattern of thinking-in-motion**:

* not a concept
* not an error
* not a solution

It is a *way a learner tries to make sense of a problem*.

Motifs often:

* appear before correct abstraction
* recur across domains
* generate both insight and derailment

---

## 2. Why Motifs Matter (Teacher Insight Encoded)

Teachers usually design:

> concept → exercise → expected solution

Reality produces:

> concept → exercise → **interpretive fork** → workaround / bypass / partial capture

Motifs explain *why* learners sometimes:

* "solve" without learning
* miss the intended abstraction
* invent clever but orthogonal solutions

---

## 3. Core Acquisition Motifs

### M1 — Structural Separation

**Gesture:**

> "This part never changes. That part does."

Appears in:

* HOF (engine vs strategy)
* Math (rule vs instance)
* Physics (law vs measurement)
* Language (grammar vs utterance)

Failure mode:

* separation done via flags instead of behavior

---

### M2 — Interpretation Instead of Reification

**Gesture:**

> "I’ll encode choices as data and interpret them later."

Appears as:

* branching on type
* mode enums
* strategy strings

This is **not wrong** — it is a *transitional motif*.

---

### M3 — Overfitting to the Prompt

**Gesture:**

> "I’ll satisfy the letter of the problem, not the underlying pattern."

Teacher recognition:

* exercise technically solved
* concept completely bypassed

System implication:

* exercise flaw or ambiguity

---

### M4 — Premature Generalization

**Gesture:**

> "I see a pattern — let me abstract now."

Appears as:

* unnecessary indirection
* complex abstractions early

Often hides weak conceptual grounding.

---

### M5 — Concrete Anchoring

**Gesture:**

> "I’ll stick to a specific example to reason safely."

Helpful early.
Limiting if never released.

---

### M6 — Lateral Substitution

**Gesture:**

> "I’ll solve a *different* problem that avoids this difficulty."

Classic exam flaw manifestation.

Signals:

* correct output
* wrong abstraction path

---

## 4. Motifs Are Not Errors

Motifs:

* indicate *where the learner is*
* reveal conceptual tension
* guide intervention strategy

The system should:

* detect motifs
* log frequency
* correlate with acquisition levels

---

## 5. Author-Facing Use

Authors can:

* see which motifs dominate per exercise
* detect flawed prompts
* refine exercises to block bypass motifs

Motifs help authors **debug pedagogy**.

---

## 6. Motifs as Shared Vocabulary

Motifs give teachers and designers:

* a non-judgmental language
* a way to talk about "almost getting it"
* a bridge between intuition and system data

---

## 7. Design Constraint

> The system does not punish motifs.
> It *listens* to them.
