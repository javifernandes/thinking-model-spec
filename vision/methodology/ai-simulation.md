### A note on the experimental method used so far

The work in this repository has already been shaped by a **recursive, low-fidelity experiment** that mirrors the system being specified.

In practice, we have been:
- Using a draft book chapter as the **source of truth**
- Simulating a learner attempting to solve exercises
- Using an AI agent to:
  - interpret the learner’s attempt
  - detect patterns, misapplications, and missing concepts
  - generate feedback and name what just happened
- Observing which signals emerge naturally (errors, timing, over-generalization, premature abstraction)
- Feeding those signals back into the **system specification itself**

This is analogous to:
- paper prototypes in product design
- storyboards and role-playing before UI exists
- “Wizard of Oz” experiments

No tooling exists yet — but the *thinking loop already does*.

The system is therefore not designed top-down.
It is being **discovered by running its future behavior manually**.

This recursion is intentional:
the system used to teach thinking
is itself being designed by thinking through its use.
