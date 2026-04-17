---
name: tests
description: "Skill for the Tests area of async-hermes-agent. 329 symbols across 37 files."
---

# Tests

329 symbols | 37 files | Cohesion: 61%

## When to Use

- Working with code in `tests/`
- Understanding how create_session, update_system_prompt, append_message work
- Modifying tests-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/test_hermes_state.py` | test_update_system_prompt, test_append_and_get_messages, test_message_increments_session_count, test_tool_response_does_not_increment_tool_count, test_assistant_tool_calls_increment_by_count (+91) |
| `tests/test_mcp_serve.py` | test_enqueue_and_poll, test_cursor_filter, test_wait_immediate, test_wait_timeout, test_wait_wakes_on_enqueue (+23) |
| `tests/test_trajectory_compressor.py` | test_to_dict, test_default_values, _make_compressor, test_protect_last_n_zero, test_disable_protect_first_system (+19) |
| `hermes_state.py` | _execute_write, create_session, update_system_prompt, append_message, get_messages (+18) |
| `trajectory_compressor.py` | TrajectoryMetrics, to_dict, count_trajectory_tokens, count_turn_tokens, compress_trajectory (+15) |
| `mcp_serve.py` | QueueEvent, wait_for_event, respond_to_approval, _enqueue, EventBridge (+8) |
| `tests/test_model_tools_async_bridge.py` | _get_current_loop, test_loop_not_closed_after_run_async, test_same_loop_reused_across_calls, test_cached_transport_survives_between_calls, _run_on_worker (+8) |
| `tests/test_plugin_skills.py` | _setup_bundle, test_banner_present, test_banner_lists_siblings_not_self, test_single_skill_no_sibling_line, test_original_content_preserved (+8) |
| `tests/test_cli_skin_integration.py` | test_default_compact_banner_keeps_legacy_nous_hermes_branding, test_poseidon_compact_banner_uses_skin_branding_instead_of_nous_hermes, test_poseidon_compact_banner_uses_skin_colors, test_compact_banner_shows_version_label, _make_cli_stub (+6) |
| `tests/test_evidence_store.py` | test_evidence_store_add, test_evidence_store_add_persists, test_evidence_store_sequential_ids, test_evidence_store_list, test_evidence_store_verify_integrity (+5) |

## Entry Points

Start here when exploring this area:

- **`create_session`** (Function) — `hermes_state.py:354`
- **`update_system_prompt`** (Function) — `hermes_state.py:402`
- **`append_message`** (Function) — `hermes_state.py:790`
- **`get_messages`** (Function) — `hermes_state.py:865`
- **`get_messages_as_conversation`** (Function) — `hermes_state.py:885`

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
| `append_message` | Function | `hermes_state.py` | 790 |
| `get_messages` | Function | `hermes_state.py` | 865 |
| `get_messages_as_conversation` | Function | `hermes_state.py` | 885 |
| `search_messages` | Function | `hermes_state.py` | 989 |
| `message_count` | Function | `hermes_state.py` | 1127 |
| `export_session` | Function | `hermes_state.py` | 1142 |
| `export_all` | Function | `hermes_state.py` | 1150 |
| `test_update_system_prompt` | Function | `tests/test_hermes_state.py` | 48 |
| `test_append_and_get_messages` | Function | `tests/test_hermes_state.py` | 91 |
| `test_message_increments_session_count` | Function | `tests/test_hermes_state.py` | 102 |
| `test_tool_response_does_not_increment_tool_count` | Function | `tests/test_hermes_state.py` | 110 |

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
| Hermes_cli | 24 calls |
| Tools | 19 calls |
| Agent | 11 calls |
| Gateway | 10 calls |
| Cli | 7 calls |
| Scripts | 4 calls |
| Acp_adapter | 2 calls |
| Platforms | 2 calls |

## How to Explore

1. `gitnexus_context({name: "create_session"})` — see callers and callees
2. `gitnexus_query({query: "tests"})` — find related execution flows
3. Read key files listed above for implementation details
