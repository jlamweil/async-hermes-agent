---
name: tools
description: "Skill for the Tools area of async-hermes-agent. 2137 symbols across 205 files."
---

# Tools

2137 symbols | 205 files | Cohesion: 65%

## When to Use

- Working with code in `tests/`
- Understanding how resolve_toolset, resolve_multiple_toolsets, validate_toolset work
- Modifying tools-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tools/skills_hub.py` | search, _featured_skills, _fetch_detail_page, _parse_detail_page, _extract_weekly_installs (+111) |
| `tests/tools/test_mcp_tool.py` | _make_mcp_tool, test_tools_registered_in_registry, test_toolset_resolves_live_from_registry, test_schema_format_correct, _mock_stdio_and_session (+97) |
| `tools/mcp_tool.py` | _refresh_tools, _register_server_tools, _discover_and_register_server, SamplingHandler, shutdown_mcp_servers (+55) |
| `tests/tools/test_skills_hub.py` | _source, _source, _make_source, test_dedup_keeps_first_seen, test_dedup_prefers_trusted_over_community (+55) |
| `tests/tools/test_delegate.py` | _make_mock_parent, test_depth_limit, test_no_goal_or_tasks, test_empty_goal, test_task_missing_goal (+52) |
| `tests/tools/test_voice_cli_integration.py` | _make_voice_cli, _cli, test_guard_not_recording, test_no_recorder_returns_early, test_no_speech_detected (+38) |
| `tools/browser_tool.py` | _requires_real_termux_browser_install, _extract_screenshot_path_from_text, _run_browser_command, _truncate_snapshot, browser_snapshot (+36) |
| `tests/tools/test_send_message_tool.py` | _install_telegram_mock, test_sends_text_then_photo_for_media_tag, test_sends_voice_for_ogg_with_voice_directive, test_sends_audio_for_mp3, test_missing_media_returns_error_without_leaking_raw_tag (+36) |
| `tools/web_tools.py` | _resolve_web_extract_auxiliary, _call_summarizer_llm, _process_large_content_chunked, summarize_chunk, check_auxiliary_model (+34) |
| `tools/file_operations.py` | _is_write_denied, WriteResult, SearchMatch, SearchResult, _exec (+32) |

## Entry Points

Start here when exploring this area:

- **`resolve_toolset`** (Function) — `toolsets.py:446`
- **`resolve_multiple_toolsets`** (Function) — `toolsets.py:499`
- **`validate_toolset`** (Function) — `toolsets.py:592`
- **`create_custom_toolset`** (Function) — `toolsets.py:612`
- **`get_tool_definitions`** (Function) — `model_tools.py:195`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `ToolRegistry` | Class | `tools/registry.py` | 99 |
| `TodoStore` | Class | `tools/todo_tool.py` | 24 |
| `AudioRecorder` | Class | `tools/voice_mode.py` | 371 |
| `SamplingHandler` | Class | `tools/mcp_tool.py` | 402 |
| `WriteResult` | Class | `tools/file_operations.py` | 143 |
| `SearchMatch` | Class | `tools/file_operations.py` | 183 |
| `SearchResult` | Class | `tools/file_operations.py` | 192 |
| `Finding` | Class | `tools/skills_guard.py` | 56 |
| `ProcessSession` | Class | `tools/process_registry.py` | 67 |
| `FileSyncManager` | Class | `tools/environments/file_sync.py` | 100 |
| `SkillSource` | Class | `tools/skills_hub.py` | 251 |
| `GitHubSource` | Class | `tools/skills_hub.py` | 283 |
| `WellKnownSkillSource` | Class | `tools/skills_hub.py` | 706 |
| `SkillsShSource` | Class | `tools/skills_hub.py` | 936 |
| `ClawHubSource` | Class | `tools/skills_hub.py` | 1408 |
| `ClaudeMarketplaceSource` | Class | `tools/skills_hub.py` | 1895 |
| `LobeHubSource` | Class | `tools/skills_hub.py` | 1993 |
| `OptionalSkillSource` | Class | `tools/skills_hub.py` | 2152 |
| `HermesIndexSource` | Class | `tools/skills_hub.py` | 2760 |
| `SkillMeta` | Class | `tools/skills_hub.py` | 63 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Cmd_mcp_configure → Get_hermes_home` | cross_community | 10 |
| `Camofox_vision → Get_managed_system` | cross_community | 10 |
| `Get_config → Get_hermes_home` | cross_community | 9 |
| `Camofox_vision → _is_container` | cross_community | 9 |
| `Camofox_vision → Get_hermes_home` | cross_community | 9 |
| `Cmd_profile → Resolve_gateway_approval` | cross_community | 8 |
| `Process_loop → _preserve_file_mode` | cross_community | 8 |
| `Process_loop → _restore_file_mode` | cross_community | 8 |
| `Run_background → _preserve_file_mode` | cross_community | 7 |
| `Run_background → _restore_file_mode` | cross_community | 7 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Hermes_cli | 152 calls |
| Gateway | 51 calls |
| Platforms | 34 calls |
| Run_agent | 33 calls |
| Agent | 32 calls |
| Environments | 32 calls |
| Skills | 19 calls |
| Tests | 17 calls |

## How to Explore

1. `gitnexus_context({name: "resolve_toolset"})` — see callers and callees
2. `gitnexus_query({query: "tools"})` — find related execution flows
3. Read key files listed above for implementation details
