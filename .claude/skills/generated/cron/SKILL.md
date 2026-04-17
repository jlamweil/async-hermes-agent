---
name: cron
description: "Skill for the Cron area of async-hermes-agent. 103 symbols across 15 files."
---

# Cron

103 symbols | 15 files | Cohesion: 70%

## When to Use

- Working with code in `tests/`
- Understanding how now, cronjob, test_cache_invalidation work
- Modifying cron-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/cron/test_jobs.py` | test_duration_becomes_once, test_once_future_returns_time, test_once_past_returns_none, test_interval_first_run, test_interval_subsequent_run (+27) |
| `cron/jobs.py` | _normalize_skill_list, _apply_skill_fields, parse_duration, parse_schedule, _ensure_aware (+19) |
| `tests/test_timezone.py` | _reset_hermes_time_cache, test_cache_invalidation, test_get_due_jobs_handles_naive_timestamps, test_ensure_aware_naive_preserves_absolute_time, test_ensure_aware_normalizes_aware_to_hermes_tz (+3) |
| `cron/scheduler.py` | tick, _resolve_origin, _resolve_delivery_target, run_job, _get_script_timeout (+2) |
| `tests/cron/test_scheduler.py` | _make_job, test_silent_response_suppresses_delivery, test_silent_with_note_suppresses_delivery, test_silent_trailing_suppresses_delivery, test_silent_is_case_insensitive (+2) |
| `tests/cron/test_cron_inactivity_timeout.py` | FakeAgent, get_activity_summary, SlowFakeAgent, get_activity_summary, test_active_agent_completes_normally (+2) |
| `tests/cron/test_codex_execution_paths.py` | _patch_agent_bootstrap, test_cron_run_job_codex_path_handles_internal_401_refresh, test_gateway_run_agent_codex_path_handles_internal_401_refresh, _UnauthorizedError, _fake_api_call |
| `tests/cron/test_cron_script.py` | test_create_job_with_script, test_update_job_add_script, test_update_job_clear_script |
| `cli.py` | _handle_cron_command, _cron_api |
| `tools/cronjob_tools.py` | _scan_cron_prompt, cronjob |

## Entry Points

Start here when exploring this area:

- **`now`** (Function) — `hermes_time.py:90`
- **`cronjob`** (Function) — `tools/cronjob_tools.py:220`
- **`test_cache_invalidation`** (Function) — `tests/test_timezone.py:92`
- **`test_get_due_jobs_handles_naive_timestamps`** (Function) — `tests/test_timezone.py:235`
- **`test_ensure_aware_naive_preserves_absolute_time`** (Function) — `tests/test_timezone.py:258`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `FakeAgent` | Class | `tests/cron/test_cron_inactivity_timeout.py` | 24 |
| `SlowFakeAgent` | Class | `tests/cron/test_cron_inactivity_timeout.py` | 56 |
| `now` | Function | `hermes_time.py` | 90 |
| `cronjob` | Function | `tools/cronjob_tools.py` | 220 |
| `test_cache_invalidation` | Function | `tests/test_timezone.py` | 92 |
| `test_get_due_jobs_handles_naive_timestamps` | Function | `tests/test_timezone.py` | 235 |
| `test_ensure_aware_naive_preserves_absolute_time` | Function | `tests/test_timezone.py` | 258 |
| `test_ensure_aware_normalizes_aware_to_hermes_tz` | Function | `tests/test_timezone.py` | 287 |
| `test_ensure_aware_due_job_not_skipped_when_system_ahead` | Function | `tests/test_timezone.py` | 304 |
| `test_get_due_jobs_naive_cross_timezone` | Function | `tests/test_timezone.py` | 337 |
| `test_create_job_stores_tz_aware_timestamps` | Function | `tests/test_timezone.py` | 365 |
| `parse_duration` | Function | `cron/jobs.py` | 95 |
| `parse_schedule` | Function | `cron/jobs.py` | 116 |
| `compute_next_run` | Function | `cron/jobs.py` | 283 |
| `load_jobs` | Function | `cron/jobs.py` | 319 |
| `save_jobs` | Function | `cron/jobs.py` | 348 |
| `create_job` | Function | `cron/jobs.py` | 367 |
| `get_job` | Function | `cron/jobs.py` | 469 |
| `update_job` | Function | `cron/jobs.py` | 486 |
| `pause_job` | Function | `cron/jobs.py` | 525 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Handle_paste → Get_hermes_home` | cross_community | 7 |
| `Main → Get_hermes_home` | cross_community | 6 |
| `Handle_paste → _get_zoneinfo` | cross_community | 5 |
| `Main → _get_zoneinfo` | cross_community | 4 |
| `Image_generate_tool → _get_zoneinfo` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 11 calls |
| Gateway | 10 calls |
| Hermes_cli | 8 calls |
| Agent | 7 calls |
| Cli | 1 calls |
| Tests | 1 calls |

## How to Explore

1. `gitnexus_context({name: "now"})` — see callers and callees
2. `gitnexus_query({query: "cron"})` — find related execution flows
3. Read key files listed above for implementation details
