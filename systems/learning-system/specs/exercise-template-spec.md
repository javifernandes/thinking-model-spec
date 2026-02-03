# Exercise Template Specification

<!-- (v0.1 scaffold) Moved under `system/specs/` -->

> **Subsystem:** Exercise Engine
> **Purpose:** Define exercises as *cognitive provocations*, not questions.

---

## 1. Core Idea

An exercise is not primarily designed to elicit a correct answer.
It is designed to **provoke specific acquisition motifs**.

Exercises are therefore specified by:

* what they *intend* to surface
* what they *risk* surfacing instead

---

## 2. Exercise Template Structure

```yaml
exercise_template:
  id: <string>
  target_concepts:
    - concept_id
  target_levels:
    - L1
    - L2
  expected_motifs:
    - M1
    - M2
  bypass_motifs:
    - M6
  anti_goals:
    - "solvable without passing behavior"
```

---

## 3. Motifs at the Exercise Level

### Expected Motifs

Motifs the exercise *intentionally allows*.

Examples:

* Allow M2 (interpretation) early
* Encourage M1 (structural separation)

These indicate **productive struggle**.

---

### Bypass Motifs

Motifs that indicate the exercise failed to constrain interpretation.

Examples:

* M6 (lateral substitution)
* M3 (overfitting the prompt)

High frequency → redesign prompt or constraints.

---

## 4. Concept–Motif Alignment

Exercises must be aware that **concept families share motifs**.

Examples:

| Concept   | Common Confusion    | Motif |
| --------- | ------------------- | ----- |
| Strategy  | behavior injection  | M2    |
| Command   | encapsulated action | M2    |
| Predicate | boolean abstraction | M5    |

Misapplication often comes from **correct motif, wrong intention**.

---

## 5. Intention Gradient (GoF Insight)

Closely related concepts differ by **intended axis of variation**:

* Strategy → *how* something is done
* Command → *when* something is done
* Predicate → *whether* something applies

Exercises must make the **axis of variation unavoidable**.

Failure to do so results in concept substitution.

---

## 6. Anti-Goals

Each exercise declares what it must *not* allow.

Examples:

* Solving via conditionals
* Hardcoding outcomes
* Collapsing variation into state

Anti-goals are more important than goals.

---

## 7. Author Feedback Signals

The system reports:

* motif distribution per exercise
* concept substitution frequency
* time-to-resolution per motif

This allows authors to:

* refine prompts
* distinguish confusion from misalignment

---

## 8. Design Constraint

> An exercise that allows the wrong motif too easily is a *bug*, not a learner failure.
