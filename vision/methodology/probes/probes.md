# Probes: Instrumented Discovery

This project deliberately distinguishes between **specification** and **discovery**.

Before building systems, UIs, or tools, we use **probes**:
minimal, constrained artifacts whose purpose is to stress the model and surface mismatches between theory and experience.

Probes are not implementations.
They are *epistemic instruments*.

---

## What Is a Probe?

A probe is a deliberately incomplete artifact that:

- exercises a specific learning or authoring experience
- forces abstract models to confront concrete behavior
- generates insight, not correctness
- may be thrown away without regret

A probe is successful if it teaches us something we did not know before.

---

## What Probes Are *Not*

A probe is **not**:

- a production system
- a reusable subsystem
- an architectural commitment
- a polished UX
- a complete representation of the vision

Probes optimize for **friction**, not smoothness.

---

## Why Probes Are Necessary

Pure specification has a failure mode:
it can become internally coherent while drifting away from lived experience.

Probes counteract this by introducing:
- resistance
- time pressure
- ambiguity
- partial information

They help answer questions such as:
- What signals actually matter?
- Where does the model feel too abstract?
- What assumptions break when someone tries to use it?
- Which distinctions matter in practice, and which do not?

---

## Relationship to the Rest of the Repository

Probes occupy a distinct role:

- **Vision** defines intent, values, and meta-process
- **System** defines the formal model and subsystems
- **Books / Domains** instantiate the system
- **Probes** stress-test all of the above

Insights from probes may:
- refine system schemas
- add or remove learning signals
- invalidate parts of the vision
- reveal missing subsystems

However, **nothing in a probe is authoritative** by default.

---

## Lifecycle of a Probe

1. A question or discomfort emerges  
   (e.g. “This feels too abstract”)

2. A probe is designed with:
   - a narrow scope
   - explicit anti-goals
   - minimal tooling

3. The probe is run (often manually or semi-manually)

4. Observations are captured:
   - surprises
   - breakdowns
   - missing concepts
   - misleading abstractions

5. Insights are back-propagated into:
   - system specs
   - vision synthesis
   - future probes

6. The probe is either:
   - discarded
   - archived
   - or partially promoted (with caution)

---

## Example: AI-Assisted Simulation as a Probe (Instance)

One early probe instance consisted of:
- simulating a learner solving exercises
- using an AI agent to interpret attempts
- detecting anti-patterns, delays, and misapplications
- reflecting on what signals emerged naturally

This probe revealed:
- over-application as a frequent failure mode
- time-to-resolution as a meaningful metric
- that many anti-patterns cannot be foreseen by authors

These insights informed:
- the feedback-space model
- acquisition motifs
- concept-family distinctions

### Why this is an instance (not part of the definition)

The definition of what a probe *is* lives in this document.

Concrete probe instances are tracked separately as manifests:

- [`vision/methodology/probe.schema.yaml`](probe.schema.yaml)
- [`vision/methodology/probes/instances/ai-simulation.yaml`](probes/instances/ai-simulation.yaml)

The AI-assisted simulation is not defined in a separate prose document; its explanation lives in the instance manifest.

---

## Design Principles for Probes

- Prefer small over general
- Prefer ugly over polished
- Prefer insight over reuse
- Prefer disposability over permanence

If a probe starts to feel “too correct”, it is probably no longer a probe.
