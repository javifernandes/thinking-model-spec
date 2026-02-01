# Subsystems Overview (Generic)

> **Layer:** Core System
>
> This document enumerates the major subsystems that together produce the learning / thinking experience.
> Each subsystem is specified independently and connected via explicit contracts.

---

## 1. Concept Model Subsystem

**Responsibility:** Represent structured knowledge.

* Concept nodes
* Concept graph (edges: prerequisite, reinforces, contrasts)
* Versioned, inspectable

Inputs:

* Author-curated concepts
* Promoted feedback signals

Outputs:

* Graph queries
* Tutor rules
* Exercise constraints

---

## 2. Exercise Engine

**Responsibility:** Generate situations that expose structure.

* Exercise archetypes
* Domain skins
* Difficulty modulation

Inputs:

* Concept model
* Reader model

Outputs:

* Concrete exercises
* Interaction traces

---

## 3. Reader Model

**Responsibility:** Track what the reader has *experienced*, not just read.

* Seen concepts
* Used patterns
* Struggles / fluency signals

Inputs:

* Interaction traces

Outputs:

* Tutor context
* Exercise constraints

---

## 4. Tutor / Companion AI

**Responsibility:** Mediate experience through dialogue.

* Hint timing
* Recognition moments
* Socratic prompts

Inputs:

* Reader model
* Concept model

Outputs:

* Dialogue
* Feedback signals

---

## 5. Feedback Space

**Responsibility:** Capture emergent understanding.

* Append-only event log
* Aggregation and ranking

Inputs:

* Exercises
* Dialogue
* Navigation patterns

Outputs:

* Reviewable signals for authors

---

## 6. Regeneration / Compiler

**Responsibility:** Keep representations consistent.

* Re-extract concepts
* Rebuild derived artifacts

Inputs:

* Book source
* Concept model changes

Outputs:

* Updated models
* Updated experiences

---

## 7. UI Projections (Plural)

**Responsibility:** Make the system perceivable.

* Interactive reader
* Graph explorer
* Author dashboard

All UIs consume the same underlying models.
