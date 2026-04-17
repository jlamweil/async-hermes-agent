---
name: honcho-plugin
description: "Skill for the Honcho_plugin area of async-hermes-agent. 140 symbols across 7 files."
---

# Honcho_plugin

140 symbols | 7 files | Cohesion: 66%

## When to Use

- Working with code in `tests/`
- Understanding how test_manual_override, test_derive_from_dirname, test_peer_prefix work
- Modifying honcho_plugin-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/honcho_plugin/test_session.py` | _make_session, test_add_message, test_add_message_with_kwargs, test_add_message_updates_timestamp, test_get_history (+60) |
| `tests/honcho_plugin/test_async_memory.py` | test_manual_override_beats_title, test_title_beats_dirname, test_title_with_peer_prefix, test_title_sanitized, test_title_all_invalid_chars_falls_back_to_dirname (+27) |
| `plugins/memory/honcho/session.py` | HonchoSession, add_message, get_history, clear, flush_all (+11) |
| `tests/honcho_plugin/test_client.py` | test_manual_override, test_derive_from_dirname, test_peer_prefix, test_no_peer_prefix_when_no_peer_name, test_default_cwd (+8) |
| `plugins/memory/honcho/__init__.py` | HonchoMemoryProvider, handle_tool_call, _signal_sufficient, _run_dialectic_depth, prefetch (+5) |
| `plugins/memory/honcho/client.py` | HonchoClientConfig, resolve_session_name |
| `tests/agent/test_memory_user_id.py` | test_gateway_user_id_overrides_peer_name, test_no_user_id_preserves_config_peer_name |

## Entry Points

Start here when exploring this area:

- **`test_manual_override`** (Function) — `tests/honcho_plugin/test_client.py:280`
- **`test_derive_from_dirname`** (Function) — `tests/honcho_plugin/test_client.py:284`
- **`test_peer_prefix`** (Function) — `tests/honcho_plugin/test_client.py:289`
- **`test_no_peer_prefix_when_no_peer_name`** (Function) — `tests/honcho_plugin/test_client.py:294`
- **`test_default_cwd`** (Function) — `tests/honcho_plugin/test_client.py:299`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `HonchoClientConfig` | Class | `plugins/memory/honcho/client.py` | 214 |
| `HonchoSession` | Class | `plugins/memory/honcho/session.py` | 24 |
| `HonchoMemoryProvider` | Class | `plugins/memory/honcho/__init__.py` | 185 |
| `HonchoSessionManager` | Class | `plugins/memory/honcho/session.py` | 67 |
| `test_manual_override` | Function | `tests/honcho_plugin/test_client.py` | 280 |
| `test_derive_from_dirname` | Function | `tests/honcho_plugin/test_client.py` | 284 |
| `test_peer_prefix` | Function | `tests/honcho_plugin/test_client.py` | 289 |
| `test_no_peer_prefix_when_no_peer_name` | Function | `tests/honcho_plugin/test_client.py` | 294 |
| `test_default_cwd` | Function | `tests/honcho_plugin/test_client.py` | 299 |
| `test_per_repo_uses_git_root` | Function | `tests/honcho_plugin/test_client.py` | 305 |
| `test_per_repo_with_peer_prefix` | Function | `tests/honcho_plugin/test_client.py` | 313 |
| `test_per_repo_falls_back_to_dirname_outside_git` | Function | `tests/honcho_plugin/test_client.py` | 323 |
| `test_per_repo_manual_override_still_wins` | Function | `tests/honcho_plugin/test_client.py` | 331 |
| `test_gateway_key_overrides_per_session_strategy` | Function | `tests/honcho_plugin/test_client.py` | 620 |
| `test_session_title_still_wins_over_gateway_key` | Function | `tests/honcho_plugin/test_client.py` | 629 |
| `test_per_session_fallback_without_gateway_key` | Function | `tests/honcho_plugin/test_client.py` | 639 |
| `test_gateway_key_sanitizes_special_chars` | Function | `tests/honcho_plugin/test_client.py` | 648 |
| `test_manual_override_beats_title` | Function | `tests/honcho_plugin/test_async_memory.py` | 110 |
| `test_title_beats_dirname` | Function | `tests/honcho_plugin/test_async_memory.py` | 115 |
| `test_title_with_peer_prefix` | Function | `tests/honcho_plugin/test_async_memory.py` | 120 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Honcho | 23 calls |
| Platforms | 4 calls |
| Cron | 2 calls |
| Gateway | 2 calls |
| Run_agent | 1 calls |
| Tools | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_manual_override"})` — see callers and callees
2. `gitnexus_query({query: "honcho_plugin"})` — find related execution flows
3. Read key files listed above for implementation details
