---
name: acp-adapter
description: "Skill for the Acp_adapter area of async-hermes-agent. 45 symbols across 13 files."
---

# Acp_adapter

45 symbols | 13 files | Cohesion: 60%

## When to Use

- Working with code in `acp_adapter/`
- Understanding how delete_session, test_delete_orphans_children, cleanup work
- Modifying acp_adapter-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `acp_adapter/server.py` | load_session, fork_session, _available_commands, _send_available_commands_update, _schedule_available_commands_update (+5) |
| `acp_adapter/session.py` | cleanup, _get_db, _delete_persisted, _clear_task_cwd, remove_session (+4) |
| `acp_adapter/tools.py` | get_tool_kind, build_tool_title, build_tool_start, build_tool_complete, extract_locations (+1) |
| `tests/acp/test_session.py` | test_create_session_writes_to_db, test_cleanup_removes_all_from_db, test_only_restores_acp_sessions, test_remove_session, test_remove_session_deletes_from_db |
| `acp_adapter/events.py` | _send_update, _tool_progress, _step, make_tool_progress_cb, make_step_cb |
| `tests/acp/test_mcp_e2e.py` | test_load_session_registers_mcp, test_fork_session_registers_mcp |
| `acp_adapter/auth.py` | detect_provider, has_provider |
| `hermes_state.py` | delete_session |
| `tests/test_hermes_state.py` | test_delete_orphans_children |
| `tools/terminal_tool.py` | clear_task_env_overrides |

## Entry Points

Start here when exploring this area:

- **`delete_session`** (Function) — `hermes_state.py:1174`
- **`test_delete_orphans_children`** (Function) — `tests/test_hermes_state.py:724`
- **`cleanup`** (Function) — `acp_adapter/session.py:217`
- **`test_create_session_writes_to_db`** (Function) — `tests/acp/test_session.py:131`
- **`test_cleanup_removes_all_from_db`** (Function) — `tests/acp/test_session.py:183`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `SessionState` | Class | `acp_adapter/session.py` | 58 |
| `HermesACPAgent` | Class | `acp_adapter/server.py` | 92 |
| `delete_session` | Function | `hermes_state.py` | 1174 |
| `test_delete_orphans_children` | Function | `tests/test_hermes_state.py` | 724 |
| `cleanup` | Function | `acp_adapter/session.py` | 217 |
| `test_create_session_writes_to_db` | Function | `tests/acp/test_session.py` | 131 |
| `test_cleanup_removes_all_from_db` | Function | `tests/acp/test_session.py` | 183 |
| `test_only_restores_acp_sessions` | Function | `tests/acp/test_session.py` | 239 |
| `load_session` | Function | `acp_adapter/server.py` | 277 |
| `fork_session` | Function | `acp_adapter/server.py` | 320 |
| `test_load_session_registers_mcp` | Function | `tests/acp/test_mcp_e2e.py` | 271 |
| `test_fork_session_registers_mcp` | Function | `tests/acp/test_mcp_e2e.py` | 326 |
| `clear_task_env_overrides` | Function | `tools/terminal_tool.py` | 571 |
| `remove_session` | Function | `acp_adapter/session.py` | 126 |
| `test_remove_session` | Function | `tests/acp/test_session.py` | 115 |
| `test_remove_session_deletes_from_db` | Function | `tests/acp/test_session.py` | 176 |
| `get_tool_kind` | Function | `acp_adapter/tools.py` | 52 |
| `build_tool_title` | Function | `acp_adapter/tools.py` | 62 |
| `build_tool_start` | Function | `acp_adapter/tools.py` | 103 |
| `build_tool_complete` | Function | `acp_adapter/tools.py` | 176 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Delete_session_endpoint → _try_wal_checkpoint` | cross_community | 4 |
| `Delete_session_endpoint → Uniform` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Acp | 16 calls |
| Tests | 6 calls |
| Hermes_cli | 6 calls |
| Tools | 2 calls |
| Agent | 1 calls |

## How to Explore

1. `gitnexus_context({name: "delete_session"})` — see callers and callees
2. `gitnexus_query({query: "acp_adapter"})` — find related execution flows
3. Read key files listed above for implementation details
