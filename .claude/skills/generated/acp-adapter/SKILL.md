---
name: acp-adapter
description: "Skill for the Acp_adapter area of async-hermes-agent. 44 symbols across 12 files."
---

# Acp_adapter

44 symbols | 12 files | Cohesion: 60%

## When to Use

- Working with code in `acp_adapter/`
- Understanding how load_session, fork_session, test_load_session_registers_mcp work
- Modifying acp_adapter-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `acp_adapter/server.py` | load_session, fork_session, _available_commands, _send_available_commands_update, _schedule_available_commands_update (+5) |
| `acp_adapter/session.py` | cleanup, _get_db, _delete_persisted, _clear_task_cwd, remove_session (+4) |
| `acp_adapter/tools.py` | make_tool_call_id, build_tool_title, build_tool_start, extract_locations, get_tool_kind (+1) |
| `tests/acp/test_session.py` | test_create_session_writes_to_db, test_cleanup_removes_all_from_db, test_only_restores_acp_sessions, test_remove_session, test_remove_session_deletes_from_db |
| `acp_adapter/events.py` | _tool_progress, _send_update, _step, make_tool_progress_cb, make_step_cb |
| `tests/acp/test_mcp_e2e.py` | test_load_session_registers_mcp, test_fork_session_registers_mcp |
| `acp_adapter/auth.py` | detect_provider, has_provider |
| `tools/terminal_tool.py` | clear_task_env_overrides |
| `hermes_cli/models.py` | parse_model_input |
| `acp_adapter/entry.py` | main |

## Entry Points

Start here when exploring this area:

- **`load_session`** (Function) — `acp_adapter/server.py:277`
- **`fork_session`** (Function) — `acp_adapter/server.py:320`
- **`test_load_session_registers_mcp`** (Function) — `tests/acp/test_mcp_e2e.py:271`
- **`test_fork_session_registers_mcp`** (Function) — `tests/acp/test_mcp_e2e.py:326`
- **`cleanup`** (Function) — `acp_adapter/session.py:217`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `HermesACPAgent` | Class | `acp_adapter/server.py` | 92 |
| `SessionState` | Class | `acp_adapter/session.py` | 58 |
| `load_session` | Function | `acp_adapter/server.py` | 277 |
| `fork_session` | Function | `acp_adapter/server.py` | 320 |
| `test_load_session_registers_mcp` | Function | `tests/acp/test_mcp_e2e.py` | 271 |
| `test_fork_session_registers_mcp` | Function | `tests/acp/test_mcp_e2e.py` | 326 |
| `cleanup` | Function | `acp_adapter/session.py` | 217 |
| `test_create_session_writes_to_db` | Function | `tests/acp/test_session.py` | 131 |
| `test_cleanup_removes_all_from_db` | Function | `tests/acp/test_session.py` | 183 |
| `test_only_restores_acp_sessions` | Function | `tests/acp/test_session.py` | 239 |
| `clear_task_env_overrides` | Function | `tools/terminal_tool.py` | 571 |
| `remove_session` | Function | `acp_adapter/session.py` | 126 |
| `test_remove_session` | Function | `tests/acp/test_session.py` | 115 |
| `test_remove_session_deletes_from_db` | Function | `tests/acp/test_session.py` | 176 |
| `parse_model_input` | Function | `hermes_cli/models.py` | 946 |
| `main` | Function | `acp_adapter/entry.py` | 57 |
| `test_model_switch_uses_requested_provider` | Function | `tests/acp/test_server.py` | 567 |
| `make_tool_call_id` | Function | `acp_adapter/tools.py` | 57 |
| `build_tool_title` | Function | `acp_adapter/tools.py` | 62 |
| `build_tool_start` | Function | `acp_adapter/tools.py` | 103 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Acp | 16 calls |
| Hermes_cli | 5 calls |
| Tests | 5 calls |
| Tools | 3 calls |
| Agent | 3 calls |

## How to Explore

1. `gitnexus_context({name: "load_session"})` — see callers and callees
2. `gitnexus_query({query: "acp_adapter"})` — find related execution flows
3. Read key files listed above for implementation details
