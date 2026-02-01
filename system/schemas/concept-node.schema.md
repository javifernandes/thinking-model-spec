# Concept Node Schema (Generic)

<!-- (v0.1 scaffold) Moved under `system/schemas/` (YAML schema to follow) -->

> **Layer:** System / Meta-model
>
> This schema defines the minimal and extensible structure of a *concept node*.
> It is intentionally incomplete: it must support evolution through use.

---

## 1. Identity

* `id`: stable identifier
* `name`: human-readable concept name
* `domain`: programming | math | physics | language | etc.

---

## 2. Intent

* `why_it_exists`: what cognitive leverage this concept provides
* `threshold`: why this concept changes how problems are seen

---

## 3. Prerequisites

* `explicit`: formally required prior concepts
* `experiential`: intuitions the learner should have *felt*

---

## 4. Core Meaning

* `definition`: concise, formal-enough statement
* `informal_frames`: metaphors / narratives used to introduce it

---

## 5. Recognition Signals

> Used by the system to detect *implicit mastery*.

* patterns in learner solutions
* phrases learners use before naming the concept
* structural shapes in code / reasoning

---

## 6. Common Misconceptions

> Author-identified misunderstandings.

* description
* why they arise

---

## 7. Anti-Patterns (Open World)

> **Not assumed complete.** May be discovered by the system.

Each anti-pattern has:

* `name`
* `description`
* `detection_signals`
* `provenance`: author | system | community
* `confidence`: provisional | validated | deprecated

---

## 8. Exercise Archetypes

> Shapes of problems, not instances.

* intent
* allowed variations
* forbidden concepts (not-yet-seen)

---

## 9. Visualization Hooks

* abstract shapes
* state transitions
* alternative views

---

## 10. System Hooks

* tutor triggers (when to speak)
* assessment signals
* graph edges (unlocks / reinforces)

---

## 11. Traceability

* source references (book sections, lectures, etc.)
* evolution notes
