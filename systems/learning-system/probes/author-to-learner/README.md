# Probe 001 — Author → Content → Learner Loop

## Purpose

This probe explores the **end-to-end learning loop** for a single concept:

> an author writes → content is derived → a learner reads & practices → signals emerge → insights feed back to the model.

This probe exists to **stress the system model**, not to validate tooling or UX.

---

## Scope (Deliberately Narrow)

This probe is constrained to:

- One author
- One chapter or chapter fragment
- One primary concept (e.g. Higher-Order Functions)
- One learner
- One short learning session

No persistence, no UI, no generality.

---

## What This Probe Explicitly Includes

This probe **does include**:

1. **Authoring**
   - Writing prose
   - Writing examples
   - Implicit pedagogical intent

2. **Content Derivation**
   - Extracting concepts
   - Generating exercises
   - Generating examples
   - Deciding *how* content is presented to the learner

3. **Learner Experience**
   - Reading derived material
   - Playing with examples
   - Attempting exercises
   - Making mistakes, shortcuts, or over-generalizations

4. **Signals**
   - Errors and anti-patterns
   - Time to resolution
   - Misapplied abstractions
   - Concept leakage (using unseen concepts)

5. **Feedback**
   - System feedback to learner
   - Signals surfaced to the author
   - Questions raised about the model itself

---

## What This Probe Explicitly Excludes

This probe does **not** attempt to define:

- UI design
- Persistence
- APIs
- User accounts
- Adaptivity algorithms
- Reusability across domains

If any of those feel “necessary”, that friction is itself a signal.

---

## How the Probe Is Run (Manually or Semi-Manually)

1. **Author writes**
   - A short chapter or excerpt in markdown
   - Minimal annotations if needed

2. **Content is derived**
   - Concepts are identified
   - Exercises are generated (manually or with AI assistance)
   - Examples are prepared for learner consumption

3. **Learner engages**
   - Reads the material
   - Modifies examples
   - Attempts exercises
   - Thinks aloud or explains reasoning

4. **Observer records**
   - Time spent
   - Confusions
   - Misapplications
   - Surprising behaviors

5. **Reflection**
   - What concepts were actually used?
   - Which distinctions mattered?
   - Where did the model feel too abstract?
   - Where was content generation weak or repetitive?

---

## Questions This Probe Is Meant to Answer

- Is the concept model sufficient to derive useful exercises?
- Are generated exercises meaningfully diverse?
- Which learner behaviors were not anticipated?
- What signals are genuinely informative?
- Where does the author need support?
- Where does the system over-assume clarity?

---

## Expected Outcomes

This probe is successful if it produces:

- New anti-patterns
- Missing axes of variation
- Weaknesses in exercise generation
- Better understanding of author vs system responsibility

Failure to produce insight means the probe was too safe.

---

## Relationship to the System Spec

Nothing in this probe is authoritative.

However, insights may lead to:
- updates in `system/`
- refinements in `vision/synthesis.md`
- new probes

Promotion from probe → system must be **explicit and deliberate**.
