# Architecture

## Goal

Build a small quality console that compares two runs of the same AI workflow and makes the result easy to inspect.

## System boundary

The first version should focus on repeatable cases, simple checks, result comparison, and step timeline. It does not need a full observability platform.

## Components

| Component | Responsibility |
|---|---|
| Web UI | Case list, run comparison, result table, step timeline, summary note |
| Eval API | Create runs, fetch cases, compare results, return summary |
| Case store | Stable eval cases with goals and expected behavior |
| Run collector | Stores outputs and step records for each run |
| Check engine | Runs deterministic checks and simple scoring rules |
| Comparison engine | Compares run A and run B across cases |
| Summary writer | Produces a short human-readable recommendation |
| Storage | Cases, runs, steps, checks, comparisons, notes |

## MVP flow

```text
Create cases
  -> run version A
  -> run version B
  -> collect steps
  -> run checks
  -> compare results
  -> open weak case
  -> read summary note
```

## Recommended first stack

- Frontend: React / Next.js / Tailwind
- Backend: FastAPI or Spring Boot
- Database: SQLite or PostgreSQL
- Worker: simple local runner first
- Output format: JSON records, then UI views

## Design principle

The system should help answer whether a change improved the workflow. It should not hide behind a single score. The timeline and case details are part of the product.
