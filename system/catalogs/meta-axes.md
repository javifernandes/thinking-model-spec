# Meta-Axes (System Layer)

> **Layer:** System / Meta-model
>
> These are **meta-axes**: reusable lenses for describing *how* concepts differ and how learners misapply them.
> They are intentionally abstract so they can apply across many domains.

## Why meta-axes (hybrid model)

- Domains will have their own axes (e.g., music: voice-leading, harmonic function).
- The system keeps a small set of **meta-axes**.
- Domain axes may optionally declare `maps_to: <meta-axis>` when they are essentially a specialization or re-framing.

This prevents two failure modes:

1. Making the system catalog too domain-specific
2. Losing cross-domain comparability

## Current meta-axes (v0.1)

### intent
**Question:** Why does this abstraction exist? What future change does it anticipate?

### time
**Question:** When does something happen? What is the lifetime/scope of effects?

### ownership
**Question:** Who decides? Who owns invocation vs definition? Who holds responsibility for the choice?

### semantic-weight
**Question:** Where does meaning “live”? Control-flow mechanics vs declarative description.

