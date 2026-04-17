---
name: cli
description: "Skill for the Cli area of async-hermes-agent. 360 symbols across 37 files."
---

# Cli

360 symbols | 37 files | Cohesion: 67%

## When to Use

- Working with code in `tests/`
- Understanding how test_simple_history_shows_user_and_assistant, test_system_messages_hidden, test_tool_messages_hidden work
- Modifying cli-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `cli.py` | retry_last, _manual_compress, _get_plugin_cmd_handler_names, save_conversation, process_command (+66) |
| `tests/cli/test_resume_display.py` | _make_cli, _simple_history, _tool_call_history, _capture_display, test_simple_history_shows_user_and_assistant (+26) |
| `tests/cli/test_reasoning_command.py` | _make_cli, test_streamed_reasoning_chunks_wait_for_boundary, test_pending_reasoning_flushes_when_thinking_stops, test_reasoning_preview_compacts_newlines_and_wraps_to_terminal, test_reasoning_flush_threshold_tracks_terminal_width (+21) |
| `tests/cli/test_cli_status_bar.py` | test_minimal_tui_chrome_threshold, test_bottom_input_rule_hides_on_narrow_terminals, test_context_style_thresholds, test_fragments_fit_within_announced_width, _make_cli (+20) |
| `tests/cli/test_personality_none.py` | _make_cli, test_none_clears_system_prompt, test_default_clears_system_prompt, test_neutral_clears_system_prompt, test_none_forces_agent_reinit (+16) |
| `tests/cli/test_quick_commands.py` | _make_cli, test_exec_command_stderr_shown_on_no_stdout, test_exec_command_no_output_shows_fallback, test_alias_command_routes_to_target, test_alias_command_passes_args (+13) |
| `tests/cli/test_cli_prefix_matching.py` | _make_cli, test_unique_prefix_dispatches_command, test_unique_prefix_with_args_does_not_recurse, test_exact_command_with_args_does_not_recurse, test_ambiguous_prefix_shows_suggestions (+7) |
| `tests/cli/test_worktree.py` | _setup_worktree, _cleanup_worktree, test_clean_worktree_removed, test_dirty_worktree_cleaned_when_no_unpushed, test_worktree_with_unpushed_commits_kept (+7) |
| `tests/cli/test_cli_tools_command.py` | _make_cli, test_bare_tools_shows_tool_list, test_unknown_subcommand_falls_back_to_show_tools, test_list_calls_backend, test_list_does_not_modify_enabled_toolsets (+6) |
| `tests/cli/test_cli_approval_ui.py` | _FakeBuffer, _make_cli_stub, test_sudo_prompt_restores_existing_draft_after_response, test_approval_callback_includes_view_for_long_commands, test_approval_display_places_title_inside_box_not_border (+6) |

## Entry Points

Start here when exploring this area:

- **`test_simple_history_shows_user_and_assistant`** (Function) — `tests/cli/test_resume_display.py:128`
- **`test_system_messages_hidden`** (Function) — `tests/cli/test_resume_display.py:139`
- **`test_tool_messages_hidden`** (Function) — `tests/cli/test_resume_display.py:146`
- **`test_tool_calls_shown_as_summary`** (Function) — `tests/cli/test_resume_display.py:155`
- **`test_long_user_message_truncated`** (Function) — `tests/cli/test_resume_display.py:164`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `test_simple_history_shows_user_and_assistant` | Function | `tests/cli/test_resume_display.py` | 128 |
| `test_system_messages_hidden` | Function | `tests/cli/test_resume_display.py` | 139 |
| `test_tool_messages_hidden` | Function | `tests/cli/test_resume_display.py` | 146 |
| `test_tool_calls_shown_as_summary` | Function | `tests/cli/test_resume_display.py` | 155 |
| `test_long_user_message_truncated` | Function | `tests/cli/test_resume_display.py` | 164 |
| `test_long_assistant_message_truncated` | Function | `tests/cli/test_resume_display.py` | 181 |
| `test_multiline_assistant_truncated` | Function | `tests/cli/test_resume_display.py` | 198 |
| `test_last_assistant_response_shown_in_full` | Function | `tests/cli/test_resume_display.py` | 217 |
| `test_last_assistant_multiline_shown_in_full` | Function | `tests/cli/test_resume_display.py` | 232 |
| `test_large_history_shows_truncation_indicator` | Function | `tests/cli/test_resume_display.py` | 247 |
| `test_multimodal_content_handled` | Function | `tests/cli/test_resume_display.py` | 257 |
| `test_empty_history_no_output` | Function | `tests/cli/test_resume_display.py` | 265 |
| `test_minimal_config_suppresses_display` | Function | `tests/cli/test_resume_display.py` | 272 |
| `test_panel_has_title` | Function | `tests/cli/test_resume_display.py` | 281 |
| `test_assistant_with_no_content_no_tools_skipped` | Function | `tests/cli/test_resume_display.py` | 288 |
| `test_only_system_messages_no_output` | Function | `tests/cli/test_resume_display.py` | 302 |
| `test_reasoning_scratchpad_stripped` | Function | `tests/cli/test_resume_display.py` | 311 |
| `test_pure_reasoning_message_skipped` | Function | `tests/cli/test_resume_display.py` | 330 |
| `test_assistant_with_text_and_tool_calls` | Function | `tests/cli/test_resume_display.py` | 346 |
| `test_loads_session_successfully` | Function | `tests/cli/test_resume_display.py` | 414 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Process_loop → _preserve_file_mode` | cross_community | 8 |
| `Process_loop → _restore_file_mode` | cross_community | 8 |
| `Process_loop → Strip_ansi` | cross_community | 6 |
| `Process_loop → _is_host_pid_alive` | cross_community | 5 |
| `Handle_ctrl_c → Invalidate` | cross_community | 5 |
| `Handle_escape_modal → Invalidate` | cross_community | 5 |
| `Handle_enter → Invalidate` | cross_community | 4 |
| `Process_loop → Get_hermes_home` | cross_community | 4 |
| `Handle_ctrl_c → Put` | cross_community | 4 |
| `Cmd_insights → Format_duration_compact` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Hermes_cli | 59 calls |
| Tools | 38 calls |
| Agent | 33 calls |
| Tests | 32 calls |
| Gateway | 24 calls |
| Cron | 8 calls |
| Cluster_84 | 4 calls |
| Cluster_14 | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_simple_history_shows_user_and_assistant"})` — see callers and callees
2. `gitnexus_query({query: "cli"})` — find related execution flows
3. Read key files listed above for implementation details
