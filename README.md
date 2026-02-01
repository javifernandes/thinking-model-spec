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

# Repository structure

This repository is intentionally structured by **stability and intent**, not by implementation.

```
thinking-model-spec/
│
├── vision/        # Philosophy, guiding insights, long-term intent
│
├── system/        # Domain-agnostic meta-model (the core spec)
│
├── books/         # Concrete instantiations of the system (examples)
│
└── README.md
```

### vision/

The most exploratory part of the repo.
High-level framing and distilled insights that shape the system.
* Why this exists
* What problem it addresses
* How it differs from traditional “teaching systems”

This is _philosophy_ made operational.

- `synthesis.md`  
  A living snapshot of what is currently understood.  
  It is periodically rewritten, not appended to.

- `methodology/`  
  How insights in this repo are produced and validated  
  (e.g. AI-assisted simulation, low-fidelity prototyping).

- `plans/`  
  Possible futures, split by scope and certainty  
  (near-term, exploratory, long-term).  
  These are **not commitments**.

Expect high churn here.

## 2. system/ (domain-agnostic)

The core specification, reusable across domains (programming, math, physics, language, etc.).

Includes:

* Concept Nodes
  * schemas, bindings, lifecycle
* Concept Families & Axes
  * how similar abstractions differ by intent, time, ownership, semantics
* Acquisition Motifs
  * recurring ways humans grasp ideas
* Exercise Templates
  * how exercises surface understanding and misalignment
* Feedback Space
  * how learner behavior becomes signal for authors
* Subsystems Overview
  * how UI, analytics, and generation fit together (at a high level)

Nothing here is specific to programming.

## 3. books/ (system instances)

Concrete example instantiations of the system.

Currently included:
* programming-core-thoughts/
  * a first example book
  * used as a working laboratory to stress-test the model

This contains:
* concept nodes (e.g. Higher-Order Functions)
* chapter-level material
* early examples and exercises

These files are **not normative** — they are exploratory and expected to evolve.

---

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