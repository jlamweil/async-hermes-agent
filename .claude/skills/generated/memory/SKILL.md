---
name: memory
description: "Skill for the Memory area of async-hermes-agent. 60 symbols across 10 files."
---

# Memory

60 symbols | 10 files | Cohesion: 62%

## When to Use

- Working with code in `tests/`
- Understanding how test_search_uses_filters, test_profile_uses_filters, test_prefetch_uses_filters work
- Modifying memory-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/plugins/memory/test_supermemory_provider.py` | test_handle_tool_call_returns_error_when_unconfigured, test_multi_container_tool_store_with_custom_tag, test_multi_container_rejects_unlisted_tag, test_get_config_schema_minimal, test_identity_template_resolved_in_container_tag (+9) |
| `tests/plugins/memory/test_mem0_v2.py` | FakeClientV2, _make_provider, test_search_uses_filters, test_profile_uses_filters, test_prefetch_uses_filters (+7) |
| `plugins/memory/__init__.py` | discover_memory_providers, load_memory_provider, _load_provider_from_dir, _ProviderCollector, _get_user_plugins_dir (+5) |
| `tests/plugins/memory/test_hindsight_provider.py` | _make_mock_client, provider, _make, test_available_with_api_key, test_not_available_without_config (+4) |
| `plugins/memory/supermemory/__init__.py` | SupermemoryMemoryProvider, handle_tool_call, _save_supermemory_config, get_tool_schemas, initialize (+1) |
| `plugins/memory/hindsight/__init__.py` | _load_config, initialize, HindsightMemoryProvider, is_available, sync_turn |
| `plugins/memory/mem0/__init__.py` | handle_tool_call |
| `hermes_cli/memory_setup.py` | _get_available_providers |
| `tests/hermes_cli/test_plugin_cli_registration.py` | test_register_cli_command_is_noop |
| `tests/agent/test_memory_provider.py` | test_bundled_takes_precedence |

## Entry Points

Start here when exploring this area:

- **`test_search_uses_filters`** (Function) — `tests/plugins/memory/test_mem0_v2.py:49`
- **`test_profile_uses_filters`** (Function) — `tests/plugins/memory/test_mem0_v2.py:62`
- **`test_prefetch_uses_filters`** (Function) — `tests/plugins/memory/test_mem0_v2.py:71`
- **`test_sync_turn_uses_write_filters`** (Function) — `tests/plugins/memory/test_mem0_v2.py:82`
- **`test_conclude_uses_write_filters`** (Function) — `tests/plugins/memory/test_mem0_v2.py:94`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `FakeClientV2` | Class | `tests/plugins/memory/test_mem0_v2.py` | 11 |
| `SupermemoryMemoryProvider` | Class | `plugins/memory/supermemory/__init__.py` | 419 |
| `HindsightMemoryProvider` | Class | `plugins/memory/hindsight/__init__.py` | 184 |
| `test_search_uses_filters` | Function | `tests/plugins/memory/test_mem0_v2.py` | 49 |
| `test_profile_uses_filters` | Function | `tests/plugins/memory/test_mem0_v2.py` | 62 |
| `test_prefetch_uses_filters` | Function | `tests/plugins/memory/test_mem0_v2.py` | 71 |
| `test_sync_turn_uses_write_filters` | Function | `tests/plugins/memory/test_mem0_v2.py` | 82 |
| `test_conclude_uses_write_filters` | Function | `tests/plugins/memory/test_mem0_v2.py` | 94 |
| `test_profile_dict_response` | Function | `tests/plugins/memory/test_mem0_v2.py` | 135 |
| `test_profile_list_response_backward_compat` | Function | `tests/plugins/memory/test_mem0_v2.py` | 145 |
| `test_search_dict_response` | Function | `tests/plugins/memory/test_mem0_v2.py` | 154 |
| `test_search_list_response_backward_compat` | Function | `tests/plugins/memory/test_mem0_v2.py` | 167 |
| `handle_tool_call` | Function | `plugins/memory/mem0/__init__.py` | 299 |
| `test_register_cli_command_is_noop` | Function | `tests/hermes_cli/test_plugin_cli_registration.py` | 179 |
| `test_bundled_takes_precedence` | Function | `tests/agent/test_memory_provider.py` | 452 |
| `discover_memory_providers` | Function | `plugins/memory/__init__.py` | 121 |
| `load_memory_provider` | Function | `plugins/memory/__init__.py` | 158 |
| `find_provider_dir` | Function | `plugins/memory/__init__.py` | 99 |
| `discover_plugin_cli_commands` | Function | `plugins/memory/__init__.py` | 321 |
| `test_handle_tool_call_returns_error_when_unconfigured` | Function | `tests/plugins/memory/test_supermemory_provider.py` | 258 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Honcho_command → Is_available` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Mem0 | 9 calls |
| Supermemory | 6 calls |
| Tools | 5 calls |
| Agent | 4 calls |
| Skills | 3 calls |
| Hermes_cli | 3 calls |

## How to Explore

1. `gitnexus_context({name: "test_search_uses_filters"})` — see callers and callees
2. `gitnexus_query({query: "memory"})` — find related execution flows
3. Read key files listed above for implementation details
