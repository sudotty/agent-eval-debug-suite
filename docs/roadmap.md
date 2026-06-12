# Roadmap

## Phase 1: Evaluation model

- Design eval dataset, eval case, eval run, and eval result.
- Define expected behavior and acceptable failure conditions.
- Add sample cases for RAG, external actions, workflow, and coding tasks.

## Phase 2: Trace ingestion

- Ingest run records, step records, model calls, retrieval logs, and external calls.
- Build a trace timeline.
- Link failure labels to specific steps.

## Phase 3: Scoring

- Add deterministic checks for schema, citations, arguments, and policy compliance.
- Add LLM judge scoring for answer quality.
- Track success rate, latency, token cost, and cost per success.

## Phase 4: Regression decision

- Compare baseline and candidate versions.
- Highlight improved, unchanged, and regressed cases.
- Generate release recommendation.

## Phase 5: Interview package

- Add failure deep-dive examples.
- Add eval report.
- Add notes on judge limitations and production trade-offs.
