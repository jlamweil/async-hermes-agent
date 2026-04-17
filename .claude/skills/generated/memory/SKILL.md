---
name: memory
description: "Skill for the Memory area of async-hermes-agent. 53 symbols across 7 files."
---

# Memory

53 symbols | 7 files | Cohesion: 63%

## When to Use

- Working with code in `tests/`
- Understanding how test_search_uses_filters, test_profile_uses_filters, test_prefetch_uses_filters work
- Modifying memory-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/plugins/memory/test_supermemory_provider.py` | test_handle_tool_call_returns_error_when_unconfigured, test_multi_container_tool_store_with_custom_tag, test_multi_container_rejects_unlisted_tag, test_get_config_schema_minimal, test_identity_template_resolved_in_container_tag (+9) |
| `tests/plugins/memory/test_mem0_v2.py` | FakeClientV2, _make_provider, test_search_uses_filters, test_profile_uses_filters, test_prefetch_uses_filters (+7) |
| `tests/plugins/memory/test_hindsight_provider.py` | _make_mock_client, provider, _make, test_available_with_api_key, test_not_available_without_config (+4) |
| `plugins/memory/__init__.py` | _get_user_plugins_dir, _is_memory_provider_dir, _iter_provider_dirs, find_provider_dir, _get_active_memory_provider (+1) |
| `plugins/memory/supermemory/__init__.py` | SupermemoryMemoryProvider, handle_tool_call, _save_supermemory_config, get_tool_schemas, initialize (+1) |
| `plugins/memory/hindsight/__init__.py` | _load_config, initialize, HindsightMemoryProvider, is_available, sync_turn |
| `plugins/memory/mem0/__init__.py` | handle_tool_call |

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
| `find_provider_dir` | Function | `plugins/memory/__init__.py` | 99 |
| `discover_plugin_cli_commands` | Function | `plugins/memory/__init__.py` | 321 |
| `test_handle_tool_call_returns_error_when_unconfigured` | Function | `tests/plugins/memory/test_supermemory_provider.py` | 258 |
| `test_multi_container_tool_store_with_custom_tag` | Function | `tests/plugins/memory/test_supermemory_provider.py` | 350 |
| `test_multi_container_rejects_unlisted_tag` | Function | `tests/plugins/memory/test_supermemory_provider.py` | 369 |
| `test_get_config_schema_minimal` | Function | `tests/plugins/memory/test_supermemory_provider.py` | 404 |
| `handle_tool_call` | Function | `plugins/memory/supermemory/__init__.py` | 775 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Mem0 | 9 calls |
| Supermemory | 6 calls |
| Tools | 5 calls |
| Agent | 4 calls |
| Skills | 3 calls |
| Hermes_cli | 2 calls |

## How to Explore

1. `gitnexus_context({name: "test_search_uses_filters"})` — see callers and callees
2. `gitnexus_query({query: "memory"})` — find related execution flows
3. Read key files listed above for implementation details
