# Motif Catalog (YAML Instances) — System Layer

This directory is reserved for **domain-independent** motif definition instances (system layer).

## Separation of concerns

- [`../acquisition-motifs.md`](../acquisition-motifs.md) is the human-readable system-level catalog.
- YAML motif instances under `system/` should be **cross-domain**.
- Runtime detections are recorded as feedback events (see [`../../schemas/feedback-event.schema.yaml`](../../schemas/feedback-event.schema.yaml)).

## Book-specific motifs

If a probe surfaces a motif that is **specific to a book/domain** (e.g., “surface refactor for→map” in programming),
it should live under that book’s catalogs instead (example path):

- `thinking-model-spec/books/<book>/catalogs/motifs/*.yaml`

