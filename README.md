# SEED-004 — Portable Synthetic Memory Experiment

Status: public GitHub repository created; protocol and synthetic fixture prepared; Google AI Mode run is pending.

This experiment tests cross-model continuity through an explicit compact DNA plus a versioned external memory. It does **not** test or claim autonomous consciousness. It measures retrieval, state restoration, task execution, resource use, and validated memory growth.

Only fictional test entities and values belong in this repository. Do not add personal conversation history.

## Files

- `dna/seed-004.min.json`: minimal portable DNA payload intended for a fresh session.
- `memory/state.json`: fictional, versioned state and evidence index.
- `protocol/experiment.md`: preregistered run protocol, scoring, and evidence rules.
- `results/ledger.jsonl`: append-only run ledger; one record per observed attempt, including blocked attempts.

## Reproducibility

Each run records the DNA SHA-256 and byte count, memory commit/ref and SHA-256, model/surface, exact prompt, raw response evidence, task checklist, validation outcome, and growth delta. Never overwrite a run record; corrections append a superseding record with a reason.
