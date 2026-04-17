---
name: holographic
description: "Skill for the Holographic area of async-hermes-agent. 38 symbols across 6 files."
---

# Holographic

38 symbols | 6 files | Cohesion: 67%

## When to Use

- Working with code in `plugins/`
- Understanding how list_facts, search, probe work
- Modifying holographic-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `plugins/memory/holographic/store.py` | list_facts, _row_to_dict, remove_fact, _compute_hrr_vector, _rebuild_bank (+9) |
| `plugins/memory/holographic/holographic.py` | _require_numpy, encode_atom, bind, unbind, bundle (+6) |
| `plugins/memory/holographic/retrieval.py` | search, probe, related, reason, contradict (+1) |
| `plugins/memory/holographic/__init__.py` | _handle_fact_store, _load_plugin_config, HolographicMemoryProvider, register, _auto_extract_facts |
| `agent/memory_provider.py` | MemoryProvider |
| `plugins/memory/byterover/__init__.py` | ByteRoverMemoryProvider |

## Entry Points

Start here when exploring this area:

- **`list_facts`** (Function) — `plugins/memory/holographic/store.py:318`
- **`search`** (Function) — `plugins/memory/holographic/retrieval.py:47`
- **`probe`** (Function) — `plugins/memory/holographic/retrieval.py:113`
- **`related`** (Function) — `plugins/memory/holographic/retrieval.py:191`
- **`reason`** (Function) — `plugins/memory/holographic/retrieval.py:259`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `MemoryProvider` | Class | `agent/memory_provider.py` | 41 |
| `HolographicMemoryProvider` | Class | `plugins/memory/holographic/__init__.py` | 113 |
| `ByteRoverMemoryProvider` | Class | `plugins/memory/byterover/__init__.py` | 170 |
| `list_facts` | Function | `plugins/memory/holographic/store.py` | 318 |
| `search` | Function | `plugins/memory/holographic/retrieval.py` | 47 |
| `probe` | Function | `plugins/memory/holographic/retrieval.py` | 113 |
| `related` | Function | `plugins/memory/holographic/retrieval.py` | 191 |
| `reason` | Function | `plugins/memory/holographic/retrieval.py` | 259 |
| `contradict` | Function | `plugins/memory/holographic/retrieval.py` | 337 |
| `encode_atom` | Function | `plugins/memory/holographic/holographic.py` | 42 |
| `bind` | Function | `plugins/memory/holographic/holographic.py` | 69 |
| `unbind` | Function | `plugins/memory/holographic/holographic.py` | 79 |
| `bundle` | Function | `plugins/memory/holographic/holographic.py` | 89 |
| `similarity` | Function | `plugins/memory/holographic/holographic.py` | 100 |
| `encode_text` | Function | `plugins/memory/holographic/holographic.py` | 110 |
| `encode_fact` | Function | `plugins/memory/holographic/holographic.py` | 134 |
| `bytes_to_phases` | Function | `plugins/memory/holographic/holographic.py` | 168 |
| `remove_fact` | Function | `plugins/memory/holographic/store.py` | 301 |
| `rebuild_all_vectors` | Function | `plugins/memory/holographic/store.py` | 531 |
| `phases_to_bytes` | Function | `plugins/memory/holographic/holographic.py` | 162 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 3 calls |
| Hermes_cli | 1 calls |

## How to Explore

1. `gitnexus_context({name: "list_facts"})` — see callers and callees
2. `gitnexus_query({query: "holographic"})` — find related execution flows
3. Read key files listed above for implementation details
