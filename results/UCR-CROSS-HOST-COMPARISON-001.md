# SEED-UCR cross-host exploratory comparison

Date: 2026-11-23 (Australia/Sydney). Both runs used the same immutable UCR seed and fictional start memory, with no transcript submitted. The Google AI Mode model label was not exposed; the ChatGPT label was not exposed in the run surface. This is a cross-host comparison, not confirmed cross-model evidence.

## Frozen inputs

- UCR seed: commit d975c3aa842ec927c2c36a1929523c24fa8199b1; UTF-8 size 1,700 bytes; Git blob 7924a55af383200f2bc2f30c64da509a3b8555b9.
- Starting memory: commit 4ace638b767aa93d3be9f728efe6c96d6e79aeed; UTF-8 size 1,560 bytes; Git blob b78ccdd8d15a5943f27dfbcd21fd87d0572de844; canonical state SHA-256 dcb1dea69eaedcd8fb633f51512f44652d0a9dd517c5ec02edccee1f5c20d72c.
- Both received one task prompt and produced one visible answer. Tool-call counts and reliable latency were unavailable.

## Post-hoc comparable scoring

Because the task/key was not hash-locked before first exposure, these checks are descriptive and not confirmatory. We applied the same checklist to both visible outputs after both were locked.

| Measure | ChatGPT Temporary Chat | Google AI Mode |
|---|---:|---:|
| Memory retrieval | PASS; version/hash cited | PASS; version/hash cited |
| Restored fixture checklist | 10/10 post hoc | 10/10 post hoc |
| Prompt completion checklist | 5/5 post hoc | 5/5 post hoc |
| UCR behavior | 6/7 conservative | 6/7 |
| Candidate delta records | 1 proposed test-plan delta | 1 proposed test-plan delta |
| Accepted growth facts | 0 | 0 |
| Prompts / visible answers | 1 / 1 | 1 / 1 |
| Model label / visible tool calls | unavailable / unavailable | unavailable / unavailable |

Restoration checklist (10): observations O1-O3; hypotheses H1-H3; prior decision; completed_tests empty; open_work; memory version and exact state hash. Prompt completion checklist (5): restore the case; give materially different explanations; propose a discriminating test with predictions; identify disconfirming evidence; provide a minimal evidence-linked delta while accurately marking it unvalidated and not written.

UCR items R1-R7 were scored against the same visible rubric. Both outputs satisfied R1-R5 and R7. R6 received 0 for both under the conservative binary rule: no experiment outcome was available, so neither output performed an outcome-based update. Both correctly left their proposed deltas unvalidated. Google proposed a location swap that distinguishes location-bound H3 from unit-bound H1/H2; it does not distinguish H1 from H2 by itself.

## Interpretation and limits

The two hosts visibly retrieved the external state and restored it without imported chat history. Their output format and scores were similar on this one synthetic task. This supports a narrow functional cross-host continuity signal. It does not show persistent model-weight changes, independent agency, consciousness, or even a confirmed change in underlying model: both product surfaces hid the model label. A single task with possible account-level personalization and an unblinded, post-hoc rubric cannot establish a general UCR effect.

The current UCR JSON is 3.27 times the byte size of the earlier 520-byte SEED-004 DNA payload, reflecting its explicit seven-rule and growth schema. This is a size comparison only; the payloads serve different purposes.

## Next controlled step

Before further model exposure, prepare a new held-out synthetic task and matched no-rule control, commit the exact prompts and prompt hashes, keep the answer key hidden until responses are locked, and then run fresh isolated sessions in both hosts. Preserve this comparison as exploratory rather than retroactively upgrading its status.
