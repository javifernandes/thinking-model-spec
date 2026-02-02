# Probe #001 — Author → Learner Flow (HOF / Delegation)

## Probe Type
End-to-end learning experience simulation

## Purpose
This probe explores the full flow from:
- an author-written chapter fragment
- through system interpretation
- into a learner-facing reading + exercise experience
- and back into author-facing feedback signals

The goal is **not** to validate correctness of content, but to stress:
- concept extraction
- learning dynamics
- feedback generation
- author feedback loops

## Scope
- One concept: Higher-Order Functions
- One sub-concept: Delegation via `map`
- One chapter excerpt
- Simulated learner behavior

No tooling, persistence, or UI is assumed.

## Why This Probe Exists
This probe validates whether:
- prose can be transformed into structured learning objects
- learner misconceptions emerge naturally
- feedback can be framed in conceptual (not rule-based) terms
- author insights can be generated post hoc

This probe is an **instance** of the probing methodology described in `/vision/methodology`.

## Status
Completed (manual simulation)

## Outcomes
 See `reflection/insights.md`.

## Folder structure (probe layers)

- `source/` — author inputs
- `evidence/` — raw learner evidence
- `derived/` — structured outputs (YAML)
- `reflection/` — human synthesis and promotion notes

> Note: The legacy `generated/` folder was removed.
> The probe contract is now fully expressed by `source/`, `evidence/`, `derived/`, and `reflection/`.
