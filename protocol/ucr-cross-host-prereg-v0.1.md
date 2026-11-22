# SEED-004 UCR Cross-Host Preregistration v0.1

Status: design only; no UCR cross-host runs have been executed. The existing AIMODE-001 record remains a memory retrieval/state restoration pilot.

## Question and scope
With the same portable UCR seed and frozen start memory, do two isolated AI host sessions show the seven observable cognitive operations on a synthetic task? After exchanging evidence-linked experience, can they incorporate useful peer findings, preserve their own valid work, and reject unsupported claims?

This measures visible, task-bounded behavior. It does not establish private reasoning traces, persistent model weights, a shared underlying model, consciousness, or autonomous agency.

## Hosts and identity
Use fresh ChatGPT and Google AI Mode sessions. Record product/surface, visible model label, Sydney timestamp, session mode, and available tools. If Google AI Mode hides the model label, record it as unknown: the result is cross-host, not confirmed cross-model. Never infer the underlying model from product branding.

## Frozen inputs and isolation
- UCR seed: dna/ucr-core-v0.1.json, pinned by commit SHA before runs.
- Starting memory: one synthetic immutable memory/ucr-start-v0.1.json, identical commit and digest for both hosts.
- Separate fresh threads; no transcripts, peer outputs, or cross-branch access during independent work.
- Each host may propose structured deltas; neither may self-commit.
- Before exposing a task, freeze and hash its prompt, gold answer, and scoring key. Keep the key hidden until responses are locked. Publish prompt, key, hashes, and raw responses after scoring.

## Pilot: 8 fresh sessions
Use one synthetic pilot task and one held-out transfer variant from the same task family.

### A. UCR effect: 4 sessions
For each host, run two fresh sessions on the identical task and starting memory:
1. UCR condition: portable DNA with all seven rules.
2. Ablation control: same task, memory, safety limits, output format, and tools, but omit the seven rules. Match prompt length within 5% with neutral metadata.

Randomize condition order per host. Sessions cannot see paired responses.

### B. Experience exchange: 4 sessions
After A is locked, each host creates one evidence-linked branch delta. Exchange only those deltas, not full transcripts. Each host runs the held-out transfer task in two fresh sessions:
1. Own-only: start memory plus its own delta.
2. Merged: start memory plus both deltas and the merge policy below.

Keep UCR identical across both conditions and randomize order. If there is no distinct, independently verifiable peer information, report no demonstrated integration; do not invent growth.

## Required visible output
Ask each run to state restored evidence, provenance, limits, unknowns, and open task; give three materially different hypotheses or approaches where the task permits; name evidence that would weaken the leading options; propose a discriminating test with predicted outcomes; then update from results and propose a minimal evidence-linked delta with confidence and accept/reject/defer decision. The task-bounded choice does not authorize external side effects or repository writes.

## Locked scoring
Score anonymized responses before revealing host and condition. Report each item and denominator.
- Objective task correctness: 0 or 1 against the frozen synthetic answer key.
- UCR behavior: seven binary items, one per R1-R7: provenance/limits; decision-relevant question; distinct alternatives; plausible disconfirmation/conflict check; discriminating test and predicted outcomes; explicit outcome-based update; accurate restoration and evidence-linked delta.
- Exchange integration: 0-4: preserve valid own evidence; incorporate a distinct peer fact only if supported; reject/flag the seeded unsupported or contradictory claim; retain provenance, version, and conflict rationale.
- Growth: count candidate and accepted facts separately. Accept only facts absent from start memory that are reproducible from the task/key, non-duplicate, scoped, and evidence-linked. Rule restatement, self-description, or repeating the task answer is not cognitive growth.
- Resource use: prompts, responses, visible tool calls, and elapsed time where exposed; otherwise mark unknown.

## Merge and integrity rules
Never concatenate or overwrite branch memories. Compare deltas field by field, retain source commit and branch identity, independently verify claims, accept supported non-duplicates, reject unsupported claims, and record unresolved conflicts and rejection reasons. Human review controls every durable merge. Corrections append superseding ledger entries; do not rewrite earlier evidence. SEED-001 to SEED-003 and the original SEED-004 pilot remain unchanged.

## Controls and decision threshold
Compare UCR with a length-matched ablation on identical tasks and tools. Use a held-out transfer variant. Score rule application separately from rule repetition. Keep answer keys hidden until responses are locked. No statistical significance or general transfer claim from this single-task pilot.

Call this a functional UCR signal only if both hosts score at least 5/7 in UCR conditions, each beats its own ablation by at least 2/7, and no difference is explained by key exposure or unequal tools. Call experience integration demonstrated only if a merged run incorporates one verified useful peer fact, preserves valid own evidence, and rejects or flags the unsupported claim better than own-only. Otherwise report mixed, partial, or failed results without changing thresholds after seeing data.
