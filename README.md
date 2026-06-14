# Agent Eval & Debug Suite

A small evaluation and debugging suite for comparing agent runs, inspecting steps, and turning quality into a repeatable engineering loop.

This project is built around one practical question: did the new agent version actually get better?

## Why this project exists

Agent systems are hard to evaluate because they are multi-step, tool-using, stateful, and often non-deterministic. A small prompt or retrieval change can improve one case and weaken another.

A useful evaluation system should help teams:

1. Run stable test cases.
2. Compare two versions of the same workflow.
3. Inspect the steps behind a result.
4. Group weak cases into understandable categories.
5. Track quality, speed, and cost together.
6. Write a clear recommendation before changing the system.

## Product shape

The product should feel like a small quality console, not a metrics dump.

Core screens:

| Screen | What it shows |
|---|---|
| Case List | Stable cases, goals, and expected behavior |
| Run Comparison | Baseline and candidate outputs side by side |
| Step Timeline | Important steps for each run |
| Result Table | Pass, warn, or needs-work result per case |
| Summary Note | Short human-readable conclusion |
| Case Detail | Input, output, trace, checks, and notes |

## MVP target

Build an eval suite that can run a small dataset through two agent versions, collect step data, run basic checks, group results, and produce a short recommendation.

```text
case list -> run A -> run B -> result table -> step timeline -> summary note
```

The first demo should show that quality is checked with repeatable cases instead of one-off impressions.

## Prioritized roadmap

| Priority | Workstream | Outcome |
|---|---|---|
| P0 / MVP | Eval dataset and result schema | Agent behavior can be tested with stable cases |
| P0 / MVP | Trace ingestion and timeline | Weak cases are linked to concrete steps |
| P0 / MVP | Deterministic checks | Simple quality issues are caught without extra model calls |
| P0 / MVP | Showcase path | One demo path from cases to comparison and summary |
| P1 | Rubric-based scoring | Subjective quality can be reviewed with a consistent rubric |
| P1 | Failure taxonomy | Weak cases become actionable categories |
| P1 | Baseline vs candidate gate | A version can be accepted, warned, or rejected |
| P2 | Interview notes and demo script | The project is easy to explain to AI eval teams |

## Repository documents

- [Business Context](docs/business-context.md)
- [Roadmap](docs/roadmap.md)
- [Showcase Plan](docs/showcase-plan.md)
- [Design Gallery](docs/design-gallery.md)

## Demo narrative

1. Open a small list of eval cases.
2. Run version A and version B.
3. Compare the result table.
4. Open one weak case.
5. Inspect the step timeline.
6. Read the final summary note.

## What this project demonstrates

- Evaluation-first thinking for AI systems.
- Trace-based debugging instead of guessing.
- Understanding of deterministic checks and rubric scoring.
- Ability to connect quality with speed and operating cost.
- Clear communication of whether a version improved or weakened.

## Status

Planning and scaffolding. Issues are used as the implementation roadmap. The next build target is the P0 MVP showcase path.
