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

## Core workflow

```text
Eval dataset
  ↓
Run baseline agent
  ↓
Run candidate agent
  ↓
Collect trace and tool calls
  ↓
Run deterministic checks
  ↓
Run LLM-as-judge scoring
  ↓
Classify failures
  ↓
Compare quality, cost, and latency
  ↓
Generate release recommendation
```

## Core features

| Feature | Purpose |
|---|---|
| Eval dataset | Stable test cases with expected behavior |
| Baseline vs candidate | Compare two agent versions |
| Trace viewer | Inspect model calls, retrieval, tool calls, and state transitions |
| Deterministic checks | Validate schema, citations, tool args, and policies |
| LLM-as-judge | Score answer quality when deterministic checks are insufficient |
| Failure taxonomy | Context, retrieval, tool, policy, control, output |
| Cost per success | Tie quality to operating cost |
| Release recommendation | Decide whether a version is safe enough to ship |

## Interview value

This project helps explain agent evaluation, regression detection, failure debugging, careful use of LLM-as-judge, and release decisions for production AI systems.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap.
