---
name: acp
description: "Skill for the Acp area of async-hermes-agent. 64 symbols across 9 files."
---

# Acp

64 symbols | 9 files | Cohesion: 51%

## When to Use

- Working with code in `tests/`
- Understanding how new_session, prompt, make_approval_callback work
- Modifying acp-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/acp/test_server.py` | test_prompt_returns_end_turn_for_empty_message, test_prompt_runs_agent, test_prompt_updates_history, test_prompt_sends_final_message_update, test_prompt_populates_usage_from_top_level_run_conversation_fields (+19) |
| `tests/acp/test_session.py` | test_update_cwd_restores_from_db, test_get_session_restores_from_db, test_save_session_updates_db, test_sessions_searchable_via_fts, test_tool_calls_persisted (+8) |
| `acp_adapter/server.py` | new_session, prompt, _register_session_mcp_servers, resume_session, _cmd_compact (+4) |
| `acp_adapter/session.py` | create_session, update_cwd, _persist, save_session, get_session (+3) |
| `tests/acp/test_mcp_e2e.py` | test_prompt_with_tool_calls_emits_acp_events, test_prompt_tool_results_paired_by_call_id, test_session_with_mcp_servers_registers_tools, test_slashed_server_name_registers_cleanly, test_resume_session_registers_mcp |
| `acp_adapter/events.py` | make_thinking_cb, make_message_cb |
| `acp_adapter/permissions.py` | make_approval_callback |
| `tests/acp/test_permissions.py` | _setup_callback |
| `hermes_state.py` | clear_messages |

## Entry Points

Start here when exploring this area:

- **`new_session`** (Function) — `acp_adapter/server.py:265`
- **`prompt`** (Function) — `acp_adapter/server.py:351`
- **`make_approval_callback`** (Function) — `acp_adapter/permissions.py:25`
- **`make_thinking_cb`** (Function) — `acp_adapter/events.py:96`
- **`make_message_cb`** (Function) — `acp_adapter/events.py:161`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `SessionManager` | Class | `acp_adapter/session.py` | 69 |
| `new_session` | Function | `acp_adapter/server.py` | 265 |
| `prompt` | Function | `acp_adapter/server.py` | 351 |
| `make_approval_callback` | Function | `acp_adapter/permissions.py` | 25 |
| `make_thinking_cb` | Function | `acp_adapter/events.py` | 96 |
| `make_message_cb` | Function | `acp_adapter/events.py` | 161 |
| `test_prompt_returns_end_turn_for_empty_message` | Function | `tests/acp/test_server.py` | 274 |
| `test_prompt_runs_agent` | Function | `tests/acp/test_server.py` | 281 |
| `test_prompt_updates_history` | Function | `tests/acp/test_server.py` | 308 |
| `test_prompt_sends_final_message_update` | Function | `tests/acp/test_server.py` | 332 |
| `test_prompt_populates_usage_from_top_level_run_conversation_fields` | Function | `tests/acp/test_server.py` | 357 |
| `test_prompt_cancelled_returns_cancelled_stop_reason` | Function | `tests/acp/test_server.py` | 388 |
| `test_slash_command_intercepted_in_prompt` | Function | `tests/acp/test_server.py` | 534 |
| `test_unknown_slash_falls_through_to_llm` | Function | `tests/acp/test_server.py` | 548 |
| `test_prompt_with_tool_calls_emits_acp_events` | Function | `tests/acp/test_mcp_e2e.py` | 113 |
| `test_prompt_tool_results_paired_by_call_id` | Function | `tests/acp/test_mcp_e2e.py` | 184 |
| `clear_messages` | Function | `hermes_state.py` | 1162 |
| `create_session` | Function | `acp_adapter/session.py` | 93 |
| `update_cwd` | Function | `acp_adapter/session.py` | 207 |
| `resume_session` | Function | `acp_adapter/server.py` | 293 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Acp_adapter | 18 calls |
| Tests | 5 calls |
| Gateway | 4 calls |
| Tools | 2 calls |
| Hermes_cli | 2 calls |
| Cli | 1 calls |

## How to Explore

1. `gitnexus_context({name: "new_session"})` — see callers and callees
2. `gitnexus_query({query: "acp"})` — find related execution flows
3. Read key files listed above for implementation details
