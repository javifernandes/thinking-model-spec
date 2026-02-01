# Concept Node Specification

> This document defines the **Concept Node**: the atomic unit of meaning in the system.
> A concept node is *not* a lesson, a chapter, or an exercise.
> It is a **cognitive construct**, designed to be recognized, exercised, misused, and refined over time.

---

## 1. Purpose

A Concept Node exists to:

* Represent a **single conceptual abstraction** (e.g. Higher-Order Functions)
* Act as a **junction point** between reading, exercising, and feedback
* Support **non-linear learning paths**
* Enable system-level reasoning (prerequisites, emergence, misuse, transfer)

A Concept Node must survive:

* partial understanding
* misuse
* delayed naming
* retroactive formalization

---

## 2. Core Identity

Each Concept Node has a stable identity independent of:

* chapter structure
* narrative order
* UI projection

### Required Fields

* `id`

  * Stable, unique identifier
  * Example: `hof.core`

* `name`

  * Canonical human-readable name
  * May be introduced *after* recognition

* `short_description`

  * One-paragraph essence
  * Not a full explanation

---

## 3. Conceptual Role

Describes **what kind of abstraction this is**.

### Fields

* `concept_type`

  * Examples:

    * abstraction
    * pattern
    * anti-pattern
    * boundary
    * invariant

* `domain_tags`

  * Programming, Math, Language, etc.
  * Multiple allowed

* `level`

  * Relative conceptual depth (ordinal, not absolute)
  * Used for progression and mixing

---

## 4. Recognition Signals

Recognition precedes explanation.

### Fields

* `recognition_signals`

  * Observable behaviors indicating implicit understanding
  * Examples:

    * passing a function as data
    * abstracting over behavior instead of values

* `pre_name_usage_patterns`

  * Ways learners use the concept *before knowing its name*

---

## 5. Dependencies & Relations

Concepts live in a graph, not a tree.

### Fields

* `prerequisites`

  * Other concept node IDs
  * Soft constraints, not gates

* `enables`

  * Concepts this one unlocks or simplifies

* `related_concepts`

  * Lateral connections

---

## 6. Exercises as Probes

Exercises are **instruments**, not tests.

### Fields

* `exercise_templates`

  * Parameterized forms
  * Can be instantiated across domains

* `difficulty_gradient`

  * Simple → complex → emergent

* `domain_variants`

  * Sci-fi, math, games, etc.

---

## 7. Anti-Patterns & Tensions

Misuse is data.

### Fields

* `anti_patterns`

  * Common incorrect or limiting uses
  * Example:

    * branching on type instead of delegating behavior

* `tension_signals`

  * Situations where learners *feel* friction

---

## 8. Feedback Hooks

Concept nodes evolve through use.

### Fields

* `feedback_channels`

  * What signals can be emitted

    * confusion
    * overgeneralization
    * premature abstraction

* `promotion_candidates`

  * Signals that may justify:

    * new anti-patterns
    * new exercises
    * new conceptual links

---

## 9. Narrative Bindings (Optional)

Books are projections.

### Fields

* `chapter_references`

  * Where the concept appears in authored material

* `author_notes`

  * Intent, caveats, historical context

---

## 10. Evolution & Regeneration

Concept Nodes are **versioned**, not static.

### Fields

* `version`
* `change_log`
* `source_of_change`

  * author
  * system feedback
  * learner behavior

---

## 11. Non-Goals

A Concept Node is **not**:

* a lesson plan
* a UI component
* a syllabus unit
* an implementation detail

---

## 12. Design Principle

> A learner should be able to *use* a concept
> before they can *name* it —
> and the system should notice.
