# Business Context

## Who this is for

This project is for teams that already have an AI agent prototype and need to know whether it is getting better in a measurable way.

Typical users:

- AI engineers improving agent prompts, retrieval, tools, or policies.
- AgentOps and LLMOps teams that need quality evidence.
- Product teams that need to understand failure patterns before a wider rollout.
- Engineering managers who want a clear quality signal before approving a version.

## Business problem

AI agents are hard to evaluate because they are multi-step systems. A single run may include retrieval, model calls, external actions, state transitions, and human review.

Without an eval suite, teams often rely on subjective demos. That creates four practical problems:

1. A new version fixes one example but weakens another.
2. Failures cannot be traced to a concrete step.
3. Cost and latency are invisible until late.
4. Users lose trust when the team cannot explain failures.

## Product wedge

This suite turns agent quality into a measurable loop:

- stable eval cases
- trace ingestion
- deterministic checks
- scoring rubrics
- failure taxonomy
- baseline vs candidate comparison
- cost per successful task

The practical message is simple: an agent should be judged by repeatable cases, not by a polished demo alone.

## Demo story

A baseline agent and a candidate agent are run on the same dataset. The suite compares outcomes, links failures to traces, classifies failure types, and summarizes whether the candidate version is stronger.

## Hiring signal

This project demonstrates production thinking. It shows that the builder understands quality, observability, version comparison, and the operating cost of AI systems.
