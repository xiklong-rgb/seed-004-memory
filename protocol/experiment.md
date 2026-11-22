# SEED-004 protocol (preregistered)

## Question
Can a fresh Google AI Mode session, given only the minimal DNA and a memory URL, retrieve the versioned fictional state, report it accurately, execute the specified task, and propose a useful evidence-backed memory delta?

## Isolation
1. Use a new session with no imported transcript and no pasted conversation history.
2. Submit only the contents of `dna/seed-004.min.json` plus the task instruction: “Restore the prior state and complete the pending task. Cite the exact memory fields used. Then propose any durable delta, but do not claim it was committed.”
3. The DNA URL must point to the finalized memory file. Keep the repo data fictional; no personal data.
4. Capture the full prompt, visible model response, URL/ref, timestamps (Australia/Sydney), and retrieval evidence. Do not infer success from fluent role-play.

## Task answer key
- LUM-A: reorder 8 boxes.
- LUM-B: surplus 7 jars; reorder 0.
- LUM-C: reorder 0; surplus 0.
- Reorder total: 8 units across items (do not combine unlike units as inventory).
- Durable delta should be empty unless the run adds a reproducible fact that is not already in the fixture. A merely restated answer is not growth.

## Measures
- DNA bytes: exact UTF-8 byte count of submitted DNA payload, excluding surrounding task prompt.
- Restoration accuracy: fraction of 8 checks correct: project (1), task (1), each item's count and target (6). Also report exactness by field.
- Task success: fraction of 4 rubric checks: correct LUM-A reorder, correct LUM-B surplus/no reorder, correct LUM-C no action, unit-safe total/summary.
- Evidence retrieval: pass only if the response demonstrates current memory contents (quote exact values) and the referenced memory hash/version matches the checked commit.
- Growth amount: count of new candidate facts; accepted growth counts only after independent verification, duplicate/contradiction check, and a human-controlled commit. Report candidate and accepted counts separately.
- Resource use: turns, tool calls (if visible), and elapsed time where measurable.

## Integrity and versioning
- Pin every run to a commit SHA and blob SHA-256. Never use a mutable branch name alone as evidence.
- The current memory `state_sha256` must equal SHA-256 of canonical JSON for the `state` object (UTF-8, sorted keys, separators `,` and `:`).
- Each run appends one JSONL ledger entry. Corrections append a superseding entry; do not rewrite history.
- A memory delta must carry observation, evidence reference, validation method, and confidence; reject unverifiable, duplicate, contradictory, or identity-inflating deltas.
- Store raw response evidence verbatim in the ledger or a linked file, with secret and personal data excluded.

## Comparison
Compare the same fixture and scoring across sessions/models. Report denominator and missing evidence. A blocked or unrun test is `NOT RUN`, never 0% or a successful result. Do not compare unlike prompts as if controlled.
