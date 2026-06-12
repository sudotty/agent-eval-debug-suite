# Agent Eval & Debug Suite

An evaluation and debugging suite for comparing agent versions, diagnosing failures, and tracking cost per successful task.

This project is built around one practical question: did the new agent version actually get better?

## Why this project exists

Agent systems are hard to evaluate because they are multi-step, tool-using, stateful, and often non-deterministic. A small prompt change can fix one case and break another.

A production-oriented eval system should help teams:

1. Run stable test cases.
2. Compare baseline and candidate versions.
3. Inspect traces.
4. Classify failures.
5. Track cost, latency, and success rate.
6. Decide whether a version is ready.

## MVP target

Build an eval suite that can run a small dataset through two agent versions, ingest traces, run deterministic checks, classify failures, and produce a release recommendation.

```text
eval cases -> baseline run -> candidate run -> trace ingestion -> checks -> failure labels -> comparison -> recommendation
```

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Eval dataset and result schema | Agent behavior can be tested with stable cases |
| P0 / MVP | Trace ingestion and timeline | Failures are linked to concrete steps |
| P0 / MVP | Deterministic checks | Simple failures are caught without extra model calls |
| P1 | LLM judge scoring | Subjective quality can be scored with a rubric |
| P1 | Failure taxonomy | Failures become actionable categories |
| P1 | Baseline vs candidate gate | A version can be accepted, warned, or rejected |
| P2 | Interview notes and demo | The project is easy to explain to AI eval teams |

## Core features

| Feature | Purpose |
|---|---|
| Eval dataset | Stable test cases with expected behavior |
| Baseline vs candidate | Compare two agent versions |
| Trace viewer | Inspect model calls, retrieval, external actions, and state transitions |
| Deterministic checks | Validate schema, citations, arguments, and policy |
| LLM judge | Score answer quality when rule checks are insufficient |
| Failure taxonomy | Context, retrieval, action, policy, control, output |
| Cost per success | Tie quality to operating cost |
| Release recommendation | Decide whether a version is safe enough to ship |

## Interview value

This project helps explain agent evaluation, regression detection, failure debugging, careful use of LLM judging, and release decisions for production AI systems.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap.
