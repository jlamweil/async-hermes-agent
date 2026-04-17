---
name: honcho
description: "Skill for the Honcho area of async-hermes-agent. 72 symbols across 9 files."
---

# Honcho

72 symbols | 9 files | Cohesion: 62%

## When to Use

- Working with code in `plugins/`
- Understanding how test_reports_connection_failure_when_session_setup_fails, get_or_create, get_peer_card work
- Modifying honcho-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `plugins/memory/honcho/cli.py` | cmd_enable, cmd_disable, _host_key, _config_path, _local_config_path (+22) |
| `plugins/memory/honcho/session.py` | get_or_create, get_peer_card, seed_ai_identity, get_ai_representation, delete (+16) |
| `plugins/memory/honcho/client.py` | reset_honcho_client, resolve_active_host, resolve_config_path, _resolve_optional_float, from_env (+2) |
| `plugins/memory/honcho/__init__.py` | _chunk_message, _sync, queue_prefetch, _do_session_init, _ensure_session |
| `tests/honcho_plugin/test_session.py` | test_delete_cached_session, test_delete_nonexistent_returns_false, test_get_prefetch_context_fetches_user_and_ai_from_peer_api, test_first_turn_dialectic_does_not_double_fire |
| `tests/honcho_plugin/test_client.py` | test_passes_timeout_from_config, test_hermes_config_timeout_override_used_when_config_timeout_missing, test_hermes_request_timeout_alias_used |
| `hermes_cli/doctor.py` | _honcho_is_configured_for_doctor, _apply_doctor_tool_availability_overrides |
| `tests/honcho_plugin/test_async_memory.py` | test_set_and_pop_dialectic_result, test_set_and_pop_context_result |
| `tests/honcho_plugin/test_cli.py` | test_reports_connection_failure_when_session_setup_fails |

## Entry Points

Start here when exploring this area:

- **`test_reports_connection_failure_when_session_setup_fails`** (Function) — `tests/honcho_plugin/test_cli.py:6`
- **`get_or_create`** (Function) — `plugins/memory/honcho/session.py:260`
- **`get_peer_card`** (Function) — `plugins/memory/honcho/session.py:1005`
- **`seed_ai_identity`** (Function) — `plugins/memory/honcho/session.py:1178`
- **`get_ai_representation`** (Function) — `plugins/memory/honcho/session.py:1223`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `test_reports_connection_failure_when_session_setup_fails` | Function | `tests/honcho_plugin/test_cli.py` | 6 |
| `get_or_create` | Function | `plugins/memory/honcho/session.py` | 260 |
| `get_peer_card` | Function | `plugins/memory/honcho/session.py` | 1005 |
| `seed_ai_identity` | Function | `plugins/memory/honcho/session.py` | 1178 |
| `get_ai_representation` | Function | `plugins/memory/honcho/session.py` | 1223 |
| `reset_honcho_client` | Function | `plugins/memory/honcho/client.py` | 672 |
| `cmd_enable` | Function | `plugins/memory/honcho/cli.py` | 93 |
| `cmd_disable` | Function | `plugins/memory/honcho/cli.py` | 136 |
| `cmd_setup` | Function | `plugins/memory/honcho/cli.py` | 326 |
| `cmd_status` | Function | `plugins/memory/honcho/cli.py` | 576 |
| `cmd_peers` | Function | `plugins/memory/honcho/cli.py` | 721 |
| `cmd_sessions` | Function | `plugins/memory/honcho/cli.py` | 738 |
| `cmd_map` | Function | `plugins/memory/honcho/cli.py` | 757 |
| `cmd_peer` | Function | `plugins/memory/honcho/cli.py` | 782 |
| `cmd_mode` | Function | `plugins/memory/honcho/cli.py` | 838 |
| `cmd_strategy` | Function | `plugins/memory/honcho/cli.py` | 872 |
| `cmd_tokens` | Function | `plugins/memory/honcho/cli.py` | 907 |
| `cmd_identity` | Function | `plugins/memory/honcho/cli.py` | 951 |
| `cmd_migrate` | Function | `plugins/memory/honcho/cli.py` | 1025 |
| `honcho_command` | Function | `plugins/memory/honcho/cli.py` | 1254 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Cmd_identity → Resolve_gateway_approval` | cross_community | 7 |
| `Cmd_migrate → Get_hermes_home` | cross_community | 6 |
| `Cmd_migrate → _validate` | cross_community | 6 |
| `Cmd_migrate → _dedupe_by_id` | cross_community | 6 |
| `Cmd_identity → Get_hermes_home` | cross_community | 6 |
| `Honcho_command → Is_available` | cross_community | 5 |
| `Honcho_command → Get_hermes_home` | cross_community | 5 |
| `Honcho_command → Items` | cross_community | 5 |
| `Honcho_command → Read_text` | cross_community | 5 |
| `Cmd_migrate → Read` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Honcho_plugin | 26 calls |
| Hermes_cli | 11 calls |
| Skills | 5 calls |
| Tools | 4 calls |
| Platforms | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_reports_connection_failure_when_session_setup_fails"})` — see callers and callees
2. `gitnexus_query({query: "honcho"})` — find related execution flows
3. Read key files listed above for implementation details
