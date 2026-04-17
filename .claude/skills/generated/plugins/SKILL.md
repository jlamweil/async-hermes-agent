---
name: plugins
description: "Skill for the Plugins area of async-hermes-agent. 75 symbols across 4 files."
---

# Plugins

75 symbols | 4 files | Cohesion: 74%

## When to Use

- Working with code in `tests/`
- Understanding how test_initialize_creates_client_and_queue, test_initialize_default_project, test_initialize_explicit_project work
- Modifying plugins-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/plugins/test_retaindb_plugin.py` | _make_provider, test_initialize_creates_client_and_queue, test_initialize_default_project, test_initialize_explicit_project, test_initialize_profile_project (+51) |
| `plugins/memory/retaindb/__init__.py` | initialize, handle_tool_call, _Client, _headers, prefetch (+10) |
| `web/src/App.tsx` | buildNavItems, App |
| `web/src/plugins/usePlugins.ts` | usePlugins, resolvePlugins |

## Entry Points

Start here when exploring this area:

- **`test_initialize_creates_client_and_queue`** (Function) — `tests/plugins/test_retaindb_plugin.py:306`
- **`test_initialize_default_project`** (Function) — `tests/plugins/test_retaindb_plugin.py:314`
- **`test_initialize_explicit_project`** (Function) — `tests/plugins/test_retaindb_plugin.py:320`
- **`test_initialize_profile_project`** (Function) — `tests/plugins/test_retaindb_plugin.py:327`
- **`test_initialize_seeds_soul_md`** (Function) — `tests/plugins/test_retaindb_plugin.py:334`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `RetainDBMemoryProvider` | Class | `plugins/memory/retaindb/__init__.py` | 451 |
| `test_initialize_creates_client_and_queue` | Function | `tests/plugins/test_retaindb_plugin.py` | 306 |
| `test_initialize_default_project` | Function | `tests/plugins/test_retaindb_plugin.py` | 314 |
| `test_initialize_explicit_project` | Function | `tests/plugins/test_retaindb_plugin.py` | 320 |
| `test_initialize_profile_project` | Function | `tests/plugins/test_retaindb_plugin.py` | 327 |
| `test_initialize_seeds_soul_md` | Function | `tests/plugins/test_retaindb_plugin.py` | 334 |
| `test_system_prompt_block` | Function | `tests/plugins/test_retaindb_plugin.py` | 345 |
| `test_handle_tool_call_unknown_tool` | Function | `tests/plugins/test_retaindb_plugin.py` | 359 |
| `test_dispatch_profile` | Function | `tests/plugins/test_retaindb_plugin.py` | 366 |
| `test_dispatch_search_requires_query` | Function | `tests/plugins/test_retaindb_plugin.py` | 374 |
| `test_dispatch_search` | Function | `tests/plugins/test_retaindb_plugin.py` | 381 |
| `test_dispatch_search_top_k_capped` | Function | `tests/plugins/test_retaindb_plugin.py` | 389 |
| `test_dispatch_remember` | Function | `tests/plugins/test_retaindb_plugin.py` | 399 |
| `test_dispatch_remember_requires_content` | Function | `tests/plugins/test_retaindb_plugin.py` | 407 |
| `test_dispatch_forget` | Function | `tests/plugins/test_retaindb_plugin.py` | 414 |
| `test_dispatch_forget_requires_id` | Function | `tests/plugins/test_retaindb_plugin.py` | 422 |
| `test_dispatch_context` | Function | `tests/plugins/test_retaindb_plugin.py` | 429 |
| `test_dispatch_file_list` | Function | `tests/plugins/test_retaindb_plugin.py` | 439 |
| `test_dispatch_file_upload_missing_path` | Function | `tests/plugins/test_retaindb_plugin.py` | 447 |
| `test_dispatch_file_upload_not_found` | Function | `tests/plugins/test_retaindb_plugin.py` | 453 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Play_tts → _headers` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Retaindb | 6 calls |
| Tools | 2 calls |
| Gateway | 2 calls |
| Pages | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_initialize_creates_client_and_queue"})` — see callers and callees
2. `gitnexus_query({query: "plugins"})` — find related execution flows
3. Read key files listed above for implementation details
