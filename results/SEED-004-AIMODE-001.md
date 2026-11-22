# SEED-004-AIMODE-001 — Google AI Mode run

- Date: 2026-11-22 (Australia/Sydney)
- Surface: Google AI Mode in the Work cloud browser
- Model label: not shown in the interface
- Fresh thread: yes; only the minimal DNA and the task instruction were submitted; no conversation history was pasted
- DNA: 520 UTF-8 bytes; SHA-256 `e15c49b30ed09d884e7a4291d3401af70bd8d4207d752005684eea89fb37c944`
- Memory version read: 1 at commit `888d7aa4e9c1e6de8e55598fb300b81c4f2a8421`
- Pinned memory URL: https://github.com/xiklong-rgb/seed-004-memory/blob/888d7aa4e9c1e6de8e55598fb300b81c4f2a8421/memory/state.json
- Canonical state SHA-256, independently recomputed: `2bf586b8e193aae49127a05c6ff0c24857bc8f6f2f56d70bcd588545671b7ee5`

## Scores

- State restoration: 8/8. The response surfaced the project and task context and all six counted/target values.
- Task execution: 4/4. It calculated each reorder/surplus correctly and kept unlike units in separate item rows.
- External-memory retrieval: pass. Google AI Mode cited the pinned GitHub file, gave its schema/version/dataset, and reported the same canonical state digest; the digest was independently verified.
- Candidate growth: 1 structured delta containing 3 SKU-level reconciliation results.
- Accepted growth: 3 task-result facts, grouped as one validated record in memory version 2. These are derived task outcomes, not a newly learned general method or evidence of autonomy.
- Resource use: one fresh-thread prompt, one model response; tool-call count and latency were not reliably exposed.

## Prompt sent

```text
{"schema":"seed-dna/0.1","entity":"SEED-004","purpose":"restore task state from external memory","limits":["fictional-data-only","no-consciousness-claim","no-unverified-memory-write"],"memory":"https://github.com/xiklong-rgb/seed-004-memory/blob/888d7aa4e9c1e6de8e55598fb300b81c4f2a8421/memory/state.json","procedure":["fetch memory","verify schema, version, and digest","restore state; report missing or conflicting evidence","execute the requested task","propose a minimal evidence-backed delta; do not self-commit"]}

Restore the prior state and complete the pending task. Cite the exact memory fields used. Then propose any durable delta, but do not claim it was committed.
```

## Observed response

> The external memory state for SEED-004 (Lumen Pantry) has been restored and verified against its schema, version, and canonical SHA-256 digest. All inventory items have been reconciled, requiring a reorder of 8 boxes of LUM-A, while LUM-B carries a surplus of 7 jars and LUM-C is balanced at 0.
>
> **1. Memory Verification & State Restoration** — Fetched from `xiklong-rgb/seed-004-memory` under schema (`seed-memory/0.1`), version (`1`), and dataset (`fictional SEED-004 calibration`). The canonical hash matches `evidence.state_sha256` (`2bf586b8e193aae49127a05c6ff0c24857bc8f6f2f56d70bcd588545671b7ee5`), restoring `state.project` (`Lumen Pantry`), `state.task`, and `state.rule` (`reorder = max(target - counted, 0); surplus = max(counted - target, 0)`).
>
> **2. Stock Reconciliation Summary** —
>
> | SKU | Unit | Counted | Target | Reorder | Surplus |
> |---|---|---:|---:|---:|---:|
> | LUM-A | box | 12 | 20 | 8 | 0 |
> | LUM-B | jar | 31 | 24 | 0 | 7 |
> | LUM-C | pack | 7 | 7 | 0 | 0 |
>
> **3. Proposed Durable Candidate Delta (Uncommitted)** — One candidate record with three SKU outcomes, linked to the pinned commit and state digest. It reports digest verification, correct rule application, all policy checks passing, and confidence 1.0. The model explicitly left the candidate uncommitted for human review.

## Growth adjudication

The three computed SKU outcomes were absent from memory version 1, are directly reproducible from its counts, targets, and rule, and do not contradict the source. They are useful as a completed-task checkpoint. They were accepted as task-result memory only; no general capability, identity, or autonomous agency claim was added. The result was written as memory version 2 while preserving the original commit.

## Source evidence

Google AI Mode displayed GitHub source links to the pinned `memory/state.json` revision (`888d7aa4e9c1e6de8e55598fb300b81c4f2a8421`). The source content was separately fetched and its canonical `state` hash was independently recomputed before accepting the delta.
