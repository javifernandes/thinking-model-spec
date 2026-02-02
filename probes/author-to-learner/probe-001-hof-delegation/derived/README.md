# derived/ (Probe Outputs)

This directory contains **derived artifacts** produced during the probe run.

## Purpose

- Preserve *what the probe produced* (even if messy)
- Make it reviewable
- Allow explicit promotion into `books/` / `system/`

## Important note: candidates vs promoted artifacts

During Probe 001, a **new candidate concept** emerged: `hof.delegation`.

Per the current workflow decision, candidate concepts may be created directly in the book-domain concept set but marked `draft`.

- Candidate concept node (book domain, draft):
  - `thinking-model-spec/books/programming-core-thoughts/concepts/hof.delegation.yaml`

The file in this folder:

- `concept-node.hof.delegation.yaml`

should be treated as a *probe-derived draft* (non-authoritative), retained for provenance.

## Motifs can also be discovered via probes

This probe surfaced candidate motifs that are not yet part of the stable M1–M8 catalog.

- Candidate motif definitions (YAML, draft):
  - [`thinking-model-spec/books/programming-core-thoughts/catalogs/motifs/pct.substitution.yaml`](../../../../books/programming-core-thoughts/catalogs/motifs/pct.substitution.yaml)
  - [`thinking-model-spec/books/programming-core-thoughts/catalogs/motifs/pct.branching-workaround.yaml`](../../../../books/programming-core-thoughts/catalogs/motifs/pct.branching-workaround.yaml)

The probe’s exercise template currently references these draft motif ids.

## Feedback events (runtime detections)

The probe run can emit runtime detections as **feedback events**, which reference motif ids and include evidence:

- [`feedback-events.yaml`](feedback-events.yaml)
