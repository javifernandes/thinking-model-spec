# thinking-model-spec

A specification for modeling how concepts are learned, misapplied, refined, and evolved — not just taught.

This repository defines a meta-system for learning and thinking, grounded in real instructional practice and extended through interaction, feedback, and iteration.

It is not a curriculum, not a course, and not an AI tutor.
It is the thinking substrate that those experiences can be built on.

# What this is

thinking-model-spec describes:
* how concepts are represented (nodes, families, axes)
* how learning unfolds over time (acquisition motifs, levels, misapplications)
* how exercises expose understanding rather than test recall
* how feedback loops allow authors and systems to evolve content
* how ambiguity and choice are central to advanced learning

## The core idea:

Learning is not binary acquisition.
It is movement across dimensions, under uncertainty, with feedback.

## How This Repository Is Structured

This repository is organized by **conceptual role and stability**, not by implementation.

### vision/
Meta-level material:
- how we think about the problem
- how insights are generated
- reflective synthesis
- methodologies (including probes)
- future horizons

This folder is intentionally volatile.
This is the meta-level (and this README you are reading is the meta-meta level :P)

---

### system/
Domain-agnostic specifications:
- concept models
- learning dynamics
- feedback mechanisms
- subsystems and schemas

This is the formal core of the project.
This is the model of a learning/authoring experience. Describes it.

---

### books/
Concrete domain instances of the system:
- programming
- math
- other future domains

These contain instances of system concepts, not the system itself.

---

### probes/
Experimental, disposable artifacts used to **stress the model**.

Probes simulate real learning and authoring experiences without committing to:
- tooling
- UI
- persistence
- architecture

Probes exist to generate insight, not correctness.
They may be archived or deleted at any time.

---

> If you are new: start in `vision/synthesis.md`, then read `system/`, then look at one probe.


# What this repo is not (yet)

* ❌ Not a runnable tool
* ❌ Not an AI implementation
* ❌ Not a learning platform
* ❌ Not a finished book

Those are **downstream artifacts**.

This repo exists to ensure that when tools are built, they are built on a **coherent, explicit model of thinking and learning**.

---

# Design principles

* Misapplication is signal, not failure
* Ambiguity is essential at advanced levels
* Learning progresses across axes, not checklists
* Authors cannot foresee everything — systems must learn too
* Feedback must flow both ways: learner → system → author

---

# Status

* System spec: actively evolving
* Example book: exploratory
* Tooling: future work

Expect refactoring. Expect renaming. Expect insight-driven change.

That is the point.

# Why this exists

Traditional education optimizes for:
* coverage
* correctness
* evaluation

This system optimizes for:
* understanding
* judgment
* conceptual movement
* long-term transfer

Or, more simply:

> Not “did you get the right answer?”
>
> but “how did you think — and what does that tell us?”