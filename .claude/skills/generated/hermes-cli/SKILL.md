---
name: hermes-cli
description: "Skill for the Hermes_cli area of async-hermes-agent. 1515 symbols across 165 files."
---

# Hermes_cli

1515 symbols | 165 files | Cohesion: 60%

## When to Use

- Working with code in `hermes_cli/`
- Understanding how display_hermes_home, managed_nous_tools_enabled, has_direct_modal_credentials work
- Modifying hermes_cli-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `hermes_cli/gateway.py` | get_installed_systemd_scopes, has_conflicting_systemd_units, print_systemd_scope_conflict_warning, _system_service_identity, prompt_linux_gateway_install_scope (+69) |
| `hermes_cli/auth.py` | get_anthropic_key, get_active_provider, _reset_config_provider, logout_command, deactivate_provider (+67) |
| `hermes_cli/main.py` | cmd_whatsapp, _clear_stale_openai_base_url, cmd_tools, _has_any_provider_configured, select_provider_and_model (+57) |
| `hermes_cli/config.py` | is_managed, managed_error, get_config_path, get_env_path, _secure_file (+43) |
| `tests/hermes_cli/test_plugins.py` | _make_plugin_dir, test_discover_user_plugins, test_discover_project_plugins, test_discover_project_plugins_skipped_by_default, test_discover_is_idempotent (+40) |
| `hermes_cli/models.py` | probe_api_models, fetch_api_models, validate_requested_model, _is_model_free, filter_nous_free_models (+37) |
| `hermes_cli/setup.py` | print_header, print_noninteractive_setup_guidance, prompt, _curses_prompt_choice, prompt_choice (+35) |
| `tests/hermes_cli/test_backup.py` | test_missing_files_skipped, test_list_snapshots, test_list_limit, test_auto_prune, test_manual_prune (+28) |
| `hermes_cli/web_server.py` | get_status, get_toolsets, get_skills, toggle_skill, set_dashboard_theme (+27) |
| `hermes_cli/tools_config.py` | _get_effective_configurable_toolsets, _get_plugin_toolset_keys, _run_post_setup, _get_enabled_platforms, _platform_toolset_summary (+24) |

## Entry Points

Start here when exploring this area:

- **`display_hermes_home`** (Function) — `hermes_constants.py:93`
- **`managed_nous_tools_enabled`** (Function) — `tools/tool_backend_helpers.py:14`
- **`has_direct_modal_credentials`** (Function) — `tools/tool_backend_helpers.py:56`
- **`resolve_openai_audio_api_key`** (Function) — `tools/tool_backend_helpers.py:100`
- **`prefers_gateway`** (Function) — `tools/tool_backend_helpers.py:108`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `LoadedPlugin` | Class | `hermes_cli/plugins.py` | 107 |
| `PluginManager` | Class | `hermes_cli/plugins.py` | 395 |
| `GitHubAuth` | Class | `tools/skills_hub.py` | 128 |
| `PluginManifest` | Class | `hermes_cli/plugins.py` | 92 |
| `PluginContext` | Class | `hermes_cli/plugins.py` | 123 |
| `AuthError` | Class | `hermes_cli/auth.py` | 508 |
| `SlashCommandCompleter` | Class | `hermes_cli/commands.py` | 716 |
| `DirectAlias` | Class | `hermes_cli/model_switch.py` | 164 |
| `FakeTool` | Class | `tests/hermes_cli/test_mcp_config.py` | 66 |
| `NousFeatureState` | Class | `hermes_cli/nous_subscription.py` | 27 |
| `NousSubscriptionFeatures` | Class | `hermes_cli/nous_subscription.py` | 41 |
| `FakeDB` | Class | `tests/hermes_cli/test_sessions_delete.py` | 9 |
| `ProviderDef` | Class | `hermes_cli/providers.py` | 159 |
| `HermesCLI` | Class | `cli.py` | 1589 |
| `ModelSwitchResult` | Class | `hermes_cli/model_switch.py` | 226 |
| `RegistrationError` | Class | `hermes_cli/dingtalk_auth.py` | 37 |
| `SlashCommandAutoSuggest` | Class | `hermes_cli/commands.py` | 1163 |
| `PooledCredential` | Class | `agent/credential_pool.py` | 91 |
| `ConfigIssue` | Class | `hermes_cli/config.py` | 1943 |
| `SkinConfig` | Class | `hermes_cli/skin_engine.py` | 120 |

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
| `Cmd_mcp_configure → _is_container` | cross_community | 8 |
| `Run_background → _preserve_file_mode` | cross_community | 7 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 173 calls |
| Agent | 98 calls |
| Gateway | 40 calls |
| Skills | 33 calls |
| Platforms | 21 calls |
| Cron | 19 calls |
| Tests | 19 calls |
| Cli | 16 calls |

## How to Explore

1. `gitnexus_context({name: "display_hermes_home"})` — see callers and callees
2. `gitnexus_query({query: "hermes_cli"})` — find related execution flows
3. Read key files listed above for implementation details
