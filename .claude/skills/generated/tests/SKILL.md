---
name: tests
description: "Skill for the Tests area of async-hermes-agent. 331 symbols across 35 files."
---

# Tests

331 symbols | 35 files | Cohesion: 59%

## When to Use

- Working with code in `tests/`
- Understanding how create_session, update_system_prompt, set_session_title work
- Modifying tests-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/test_hermes_state.py` | test_update_system_prompt, test_export_session, test_set_and_get_title, test_update_title, test_title_in_search_sessions (+90) |
| `tests/test_mcp_serve.py` | test_enqueue_and_poll, test_wait_immediate, test_wait_timeout, test_wait_wakes_on_enqueue, test_queue_limit (+23) |
| `tests/test_trajectory_compressor.py` | test_to_dict, test_default_values, _make_compressor, test_protect_last_n_zero, test_disable_protect_first_system (+19) |
| `hermes_state.py` | _execute_write, create_session, update_system_prompt, set_session_title, get_session_by_title (+17) |
| `trajectory_compressor.py` | TrajectoryMetrics, to_dict, count_trajectory_tokens, count_turn_tokens, compress_trajectory (+15) |
| `mcp_serve.py` | QueueEvent, wait_for_event, list_pending_approvals, respond_to_approval, _enqueue (+8) |
| `tests/test_model_tools_async_bridge.py` | _get_current_loop, test_loop_not_closed_after_run_async, test_same_loop_reused_across_calls, test_cached_transport_survives_between_calls, _run_on_worker (+8) |
| `tests/test_plugin_skills.py` | _setup_bundle, test_banner_present, test_banner_lists_siblings_not_self, test_single_skill_no_sibling_line, test_original_content_preserved (+8) |
| `tests/gateway/test_resume_command.py` | _make_event, _make_runner, test_no_session_db, test_list_named_sessions_when_no_arg, test_list_shows_usage_when_no_titled (+6) |
| `tests/test_cli_skin_integration.py` | test_default_compact_banner_keeps_legacy_nous_hermes_branding, test_poseidon_compact_banner_uses_skin_branding_instead_of_nous_hermes, test_poseidon_compact_banner_uses_skin_colors, test_compact_banner_shows_version_label, _make_cli_stub (+6) |

## Entry Points

Start here when exploring this area:

- **`create_session`** (Function) — `hermes_state.py:354`
- **`update_system_prompt`** (Function) — `hermes_state.py:402`
- **`set_session_title`** (Function) — `hermes_state.py:605`
- **`get_session_by_title`** (Function) — `hermes_state.py:643`
- **`resolve_session_by_title`** (Function) — `hermes_state.py:652`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `EvidenceStore` | Class | `optional-skills/security/oss-forensics/scripts/evidence-store.py` | 58 |
| `QueueEvent` | Class | `mcp_serve.py` | 176 |
| `EventBridge` | Class | `mcp_serve.py` | 184 |
| `TestDB` | Class | `tests/test_mcp_serve.py` | 967 |
| `TrajectoryMetrics` | Class | `trajectory_compressor.py` | 157 |
| `CompressionConfig` | Class | `trajectory_compressor.py` | 57 |
| `AggregateMetrics` | Class | `trajectory_compressor.py` | 202 |
| `create_session` | Function | `hermes_state.py` | 354 |
| `update_system_prompt` | Function | `hermes_state.py` | 402 |
| `set_session_title` | Function | `hermes_state.py` | 605 |
| `get_session_by_title` | Function | `hermes_state.py` | 643 |
| `resolve_session_by_title` | Function | `hermes_state.py` | 652 |
| `get_next_title_in_lineage` | Function | `hermes_state.py` | 681 |
| `export_session` | Function | `hermes_state.py` | 1142 |
| `test_update_system_prompt` | Function | `tests/test_hermes_state.py` | 48 |
| `test_export_session` | Function | `tests/test_hermes_state.py` | 581 |
| `test_set_and_get_title` | Function | `tests/test_hermes_state.py` | 753 |
| `test_update_title` | Function | `tests/test_hermes_state.py` | 768 |
| `test_title_in_search_sessions` | Function | `tests/test_hermes_state.py` | 776 |
| `test_title_in_export` | Function | `tests/test_hermes_state.py` | 786 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Collect_trajectory → Get_registered_toolset_aliases` | cross_community | 6 |
| `Evaluate → Get_registered_toolset_aliases` | cross_community | 6 |
| `Evaluate → Get_registered_toolset_aliases` | cross_community | 6 |
| `Rollout_and_score_eval → Get_registered_toolset_aliases` | cross_community | 6 |
| `Main → Add_trajectory_metrics` | cross_community | 6 |
| `Connect → Uniform` | cross_community | 5 |
| `Gateway_setup → Is_container` | cross_community | 4 |
| `Run → Get_branding` | cross_community | 4 |
| `Collect_trajectory → Get_distribution` | cross_community | 4 |
| `Evaluate → Get_distribution` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Agent | 27 calls |
| Gateway | 23 calls |
| Hermes_cli | 16 calls |
| Tools | 16 calls |
| Cli | 7 calls |
| Run_agent | 4 calls |
| Scripts | 4 calls |
| Cluster_29 | 2 calls |

## How to Explore

1. `gitnexus_context({name: "create_session"})` — see callers and callees
2. `gitnexus_query({query: "tests"})` — find related execution flows
3. Read key files listed above for implementation details
