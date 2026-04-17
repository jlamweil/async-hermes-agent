---
name: honcho
description: "Skill for the Honcho area of async-hermes-agent. 68 symbols across 7 files."
---

# Honcho

68 symbols | 7 files | Cohesion: 67%

## When to Use

- Working with code in `plugins/`
- Understanding how test_reports_connection_failure_when_session_setup_fails, get_or_create, get_peer_card work
- Modifying honcho-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `plugins/memory/honcho/cli.py` | clone_honcho_for_profile, _ensure_peer_exists, cmd_enable, cmd_disable, cmd_sync (+25) |
| `plugins/memory/honcho/session.py` | get_or_create, get_peer_card, seed_ai_identity, get_ai_representation, _run (+15) |
| `plugins/memory/honcho/client.py` | resolve_active_host, resolve_config_path, _resolve_optional_float, from_env, from_global_config (+2) |
| `plugins/memory/honcho/__init__.py` | _chunk_message, _sync, queue_prefetch, _do_session_init, _ensure_session |
| `tests/honcho_plugin/test_session.py` | test_get_prefetch_context_fetches_user_and_ai_from_peer_api, test_long_query_truncated, test_first_turn_dialectic_does_not_double_fire |
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
| `resolve_active_host` | Function | `plugins/memory/honcho/client.py` | 33 |
| `resolve_config_path` | Function | `plugins/memory/honcho/client.py` | 55 |
| `from_env` | Function | `plugins/memory/honcho/client.py` | 287 |
| `from_global_config` | Function | `plugins/memory/honcho/client.py` | 309 |
| `get_honcho_client` | Function | `plugins/memory/honcho/client.py` | 582 |
| `reset_honcho_client` | Function | `plugins/memory/honcho/client.py` | 672 |
| `clone_honcho_for_profile` | Function | `plugins/memory/honcho/cli.py` | 16 |
| `cmd_enable` | Function | `plugins/memory/honcho/cli.py` | 93 |
| `cmd_disable` | Function | `plugins/memory/honcho/cli.py` | 136 |
| `cmd_sync` | Function | `plugins/memory/honcho/cli.py` | 153 |
| `sync_honcho_profiles_quiet` | Function | `plugins/memory/honcho/cli.py` | 199 |
| `cmd_setup` | Function | `plugins/memory/honcho/cli.py` | 326 |
| `cmd_status` | Function | `plugins/memory/honcho/cli.py` | 576 |
| `cmd_peers` | Function | `plugins/memory/honcho/cli.py` | 721 |
| `cmd_sessions` | Function | `plugins/memory/honcho/cli.py` | 738 |

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
| Honcho_plugin | 22 calls |
| Hermes_cli | 12 calls |
| Skills | 5 calls |
| Tools | 4 calls |
| Run_agent | 1 calls |
| Platforms | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_reports_connection_failure_when_session_setup_fails"})` — see callers and callees
2. `gitnexus_query({query: "honcho"})` — find related execution flows
3. Read key files listed above for implementation details
