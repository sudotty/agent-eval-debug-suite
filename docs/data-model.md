# Data Model

## Core tables

### eval_cases

| Field | Purpose |
|---|---|
| id | Case id |
| title | Short case name |
| input | User task or question |
| expected_behavior | What should happen |
| tags | retrieval, tool, workflow, output |
| status | active, archived |

### eval_runs

| Field | Purpose |
|---|---|
| id | Run id |
| version_name | Baseline or candidate name |
| config | Prompt, model, retrieval, or tool config |
| started_at | Start time |
| finished_at | End time |
| status | running, completed, failed |

### eval_results

| Field | Purpose |
|---|---|
| id | Result id |
| case_id | Eval case |
| run_id | Eval run |
| output | Produced result |
| status | pass, warn, fail |
| latency_ms | Runtime time |
| cost_estimate | Optional cost |

### step_records

| Field | Purpose |
|---|---|
| id | Step id |
| result_id | Parent result |
| step_index | Order in timeline |
| step_type | model, retrieval, tool, check, note |
| summary | Short step summary |
| payload | Structured step details |

### comparison_reports

| Field | Purpose |
|---|---|
| id | Report id |
| baseline_run_id | First run |
| candidate_run_id | Second run |
| improved_count | Improved cases |
| weakened_count | Weakened cases |
| unchanged_count | Unchanged cases |
| summary | Human-readable note |

## MVP rule

Start with a small number of cases. The value comes from repeatability, not volume.
