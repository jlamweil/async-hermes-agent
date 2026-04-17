---
name: run-agent
description: "Skill for the Run_agent area of async-hermes-agent. 353 symbols across 44 files."
---

# Run_agent

353 symbols | 44 files | Cohesion: 77%

## When to Use

- Working with code in `tests/`
- Understanding how evaluate, cleanup, collect_trajectories work
- Modifying run_agent-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/run_agent/test_run_agent.py` | _mock_response, test_run_conversation_suppresses_retry_noise_in_parseable_quiet_mode, _RateLimitError, _setup_agent, test_stop_finish_reason_returns_response (+73) |
| `tests/run_agent/test_run_agent_codex_responses.py` | _patch_agent_bootstrap, _build_agent, _build_copilot_agent, _codex_request_kwargs, test_run_codex_stream_retries_when_completed_event_missing (+27) |
| `tests/run_agent/test_agent_loop.py` | MockChoice, MockChatCompletion, MockServer, chat_completion, make_text_response (+21) |
| `tests/run_agent/test_primary_runtime_restore.py` | _make_tool_defs, _make_agent, _make_transport_error, test_recovers_on_read_timeout, test_recovers_on_connect_timeout (+17) |
| `tests/run_agent/test_anthropic_error_handling.py` | _make_agent_cls, _run_with_agent, test_429_rate_limit_is_retried_and_recovers, test_529_overloaded_is_retried_and_recovers, test_429_exhausts_all_retries_before_raising (+11) |
| `tests/run_agent/test_fallback_model.py` | _make_agent, _mock_resolve, test_activates_openrouter_fallback, test_activates_zai_fallback, test_fallback_uses_resolved_normalized_model (+10) |
| `cli.py` | _accent_hex, _rich_text_from_ansi, _cprint, _termux_example_image_path, ChatConsole (+9) |
| `tests/run_agent/test_tool_arg_coercion.py` | _mock_schema, test_coerces_integer_arg, test_coerces_boolean_arg, test_coerces_number_arg, test_leaves_string_args_alone (+5) |
| `tests/run_agent/test_openai_client_lifecycle.py` | FakeRequestClient, FakeSharedClient, OpenAIFactory, _build_agent, _connection_error (+5) |
| `tests/run_agent/test_compression_boundary.py` | _tool_result, _assistant_with_tools, _make_compressor, test_boundary_at_clean_position, test_boundary_after_assistant_with_tools (+4) |

## Entry Points

Start here when exploring this area:

- **`evaluate`** (Function) — `environments/web_research_env.py:426`
- **`cleanup`** (Function) — `environments/tool_context.py:439`
- **`collect_trajectories`** (Function) — `environments/hermes_base_env.py:349`
- **`collect_trajectory`** (Function) — `environments/hermes_base_env.py:488`
- **`collect_trajectories`** (Function) — `environments/agentic_opd_env.py:642`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `ToolContext` | Class | `environments/tool_context.py` | 66 |
| `AgentResult` | Class | `environments/agent_loop.py` | 63 |
| `HermesAgentLoop` | Class | `environments/agent_loop.py` | 118 |
| `MockChoice` | Class | `tests/run_agent/test_agent_loop.py` | 59 |
| `MockChatCompletion` | Class | `tests/run_agent/test_agent_loop.py` | 66 |
| `MockServer` | Class | `tests/run_agent/test_agent_loop.py` | 72 |
| `ChatConsole` | Class | `cli.py` | 1344 |
| `FakeRequestClient` | Class | `tests/run_agent/test_openai_client_lifecycle.py` | 16 |
| `FakeSharedClient` | Class | `tests/run_agent/test_openai_client_lifecycle.py` | 34 |
| `OpenAIFactory` | Class | `tests/run_agent/test_openai_client_lifecycle.py` | 38 |
| `MockMessage` | Class | `tests/run_agent/test_agent_loop.py` | 49 |
| `evaluate` | Function | `environments/web_research_env.py` | 426 |
| `cleanup` | Function | `environments/tool_context.py` | 439 |
| `collect_trajectories` | Function | `environments/hermes_base_env.py` | 349 |
| `collect_trajectory` | Function | `environments/hermes_base_env.py` | 488 |
| `collect_trajectories` | Function | `environments/agentic_opd_env.py` | 642 |
| `evaluate` | Function | `environments/agentic_opd_env.py` | 1007 |
| `run` | Function | `environments/agent_loop.py` | 174 |
| `chat_completion` | Function | `tests/run_agent/test_agent_loop.py` | 83 |
| `make_text_response` | Function | `tests/run_agent/test_agent_loop.py` | 95 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Process_loop → _preserve_file_mode` | cross_community | 8 |
| `Process_loop → _restore_file_mode` | cross_community | 8 |
| `Run_background → _preserve_file_mode` | cross_community | 7 |
| `Run_background → _restore_file_mode` | cross_community | 7 |
| `Run_btw → _preserve_file_mode` | cross_community | 7 |
| `Run_btw → _restore_file_mode` | cross_community | 7 |
| `Process_loop → Strip_ansi` | cross_community | 6 |
| `Run_background → Get_hermes_home` | cross_community | 6 |
| `Run_background → SkinConfig` | cross_community | 6 |
| `Collect_trajectory → Get_registered_toolset_aliases` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 37 calls |
| Hermes_cli | 22 calls |
| Gateway | 16 calls |
| Cli | 14 calls |
| Agent | 14 calls |
| Tests | 13 calls |
| Environments | 3 calls |
| Integration | 2 calls |

## How to Explore

1. `gitnexus_context({name: "evaluate"})` — see callers and callees
2. `gitnexus_query({query: "run_agent"})` — find related execution flows
3. Read key files listed above for implementation details
