---
name: agent
description: "Skill for the Agent area of async-hermes-agent. 895 symbols across 97 files."
---

# Agent

895 symbols | 97 files | Cohesion: 71%

## When to Use

- Working with code in `tests/`
- Understanding how close, update_token_counts, db work
- Modifying agent-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/agent/test_error_classifier.py` | MockAPIError, test_from_body_attr, test_401_classified_as_auth, test_403_classified_as_auth, test_403_key_limit_classified_as_billing (+71) |
| `agent/auxiliary_client.py` | _select_pool_entry, _pool_runtime_api_key, _pool_runtime_base_url, _read_nous_auth, _read_codex_access_token (+44) |
| `tests/agent/test_memory_provider.py` | FakeMemoryProvider, test_default_optional_hooks_are_noop, test_empty_manager, test_add_provider, test_get_provider_by_name (+43) |
| `tests/agent/test_insights.py` | db, test_empty_db_returns_empty_report, test_empty_db_terminal_format, test_empty_db_gateway_format, test_generate_returns_all_sections (+35) |
| `agent/credential_pool.py` | from_dict, has_credentials, entries, select, acquire_lease (+35) |
| `tests/agent/test_credential_pool.py` | _write_auth_store, test_fill_first_selection_skips_recently_exhausted_entry, test_select_clears_expired_exhaustion, test_round_robin_strategy_rotates_priorities, test_random_strategy_uses_random_choice (+26) |
| `agent/google_oauth.py` | _credentials_path, _lock_path, _credentials_lock, load_credentials, clear_credentials (+26) |
| `agent/display.py` | _diff_ansi, _hex_fg, _diff_dim, _diff_file, _diff_hunk (+25) |
| `agent/anthropic_adapter.py` | normalize_anthropic_response, _convert_content_part_to_anthropic, _convert_content_to_anthropic, convert_messages_to_anthropic, _normalize_base_url_text (+19) |
| `agent/model_metadata.py` | _infer_provider_from_url, _is_known_provider_base_url, _get_context_cache_path, _load_context_cache, save_context_length (+18) |

## Entry Points

Start here when exploring this area:

- **`close`** (Function) — `hermes_state.py:236`
- **`update_token_counts`** (Function) — `hermes_state.py:411`
- **`db`** (Function) — `tests/test_hermes_state.py:10`
- **`test_migration_from_v2`** (Function) — `tests/test_hermes_state.py:945`
- **`get_sessions`** (Function) — `hermes_cli/web_server.py:479`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `SessionDB` | Class | `hermes_state.py` | 114 |
| `InsightsEngine` | Class | `agent/insights.py` | 92 |
| `MockAPIError` | Class | `tests/agent/test_error_classifier.py` | 16 |
| `StringBodyError` | Class | `tests/agent/test_error_classifier.py` | 660 |
| `ListBodyError` | Class | `tests/agent/test_error_classifier.py` | 667 |
| `WeirdSuccess` | Class | `tests/agent/test_error_classifier.py` | 712 |
| `MemoryManager` | Class | `agent/memory_manager.py` | 82 |
| `FakeMemoryProvider` | Class | `tests/agent/test_memory_provider.py` | 14 |
| `SubdirectoryHintTracker` | Class | `agent/subdirectory_hints.py` | 47 |
| `ContextCompressor` | Class | `agent/context_compressor.py` | 187 |
| `ProviderConfig` | Class | `hermes_cli/auth.py` | 90 |
| `CodexAuxiliaryClient` | Class | `agent/auxiliary_client.py` | 434 |
| `StubEngine` | Class | `tests/agent/test_context_engine.py` | 14 |
| `Mem0MemoryProvider` | Class | `plugins/memory/mem0/__init__.py` | 118 |
| `RedactingFormatter` | Class | `agent/redact.py` | 189 |
| `GoogleOAuthError` | Class | `agent/google_oauth.py` | 143 |
| `RefreshParts` | Class | `agent/google_oauth.py` | 392 |
| `CodeAssistError` | Class | `agent/google_code_assist.py` | 69 |
| `KawaiiSpinner` | Class | `agent/display.py` | 570 |
| `GoogleCredentials` | Class | `agent/google_oauth.py` | 421 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Cmd_insights → BillingRoute` | cross_community | 8 |
| `Cmd_insights → PricingEntry` | cross_community | 7 |
| `Handle_paste → Get_hermes_home` | cross_community | 7 |
| `Main → Get_hermes_home` | cross_community | 6 |
| `Get_model_info → Get_hermes_home` | cross_community | 6 |
| `Cmd_insights → CostResult` | cross_community | 6 |
| `Select_provider_and_model → Has_credentials` | cross_community | 5 |
| `Get_model_info → _normalize_base_url` | cross_community | 5 |
| `Get_model_info → Items` | cross_community | 5 |
| `Get_skills → Yaml_load` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Hermes_cli | 104 calls |
| Tests | 50 calls |
| Tools | 45 calls |
| Skills | 19 calls |
| Gateway | 13 calls |
| Platforms | 3 calls |
| Honcho_plugin | 3 calls |
| Cli | 2 calls |

## How to Explore

1. `gitnexus_context({name: "close"})` — see callers and callees
2. `gitnexus_query({query: "agent"})` — find related execution flows
3. Read key files listed above for implementation details
