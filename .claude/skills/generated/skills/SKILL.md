---
name: skills
description: "Skill for the Skills area of async-hermes-agent. 56 symbols across 11 files."
---

# Skills

56 symbols | 11 files | Cohesion: 47%

## When to Use

- Working with code in `tests/`
- Understanding how get_config_raw, load_module, test_migrator_copies_skill_and_merges_allowlist work
- Modifying skills-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/skills/test_openclaw_migration.py` | load_module, test_migrator_copies_skill_and_merges_allowlist, test_migrator_optionally_imports_supported_secrets_and_messaging_settings, test_messaging_cwd_skipped_when_inside_source, test_migrator_can_execute_only_selected_categories (+24) |
| `tests/skills/test_telephony_skill.py` | load_module, test_save_twilio_writes_env_and_state, test_messages_after_checkpoint_returns_only_newer_items, test_twilio_buy_number_saves_env_and_state, test_vapi_import_twilio_number_saves_phone_number_id (+1) |
| `tests/skills/test_youtube_quiz.py` | _run, _make_mock_module, test_successful_fetch, test_fetch_error, test_empty_transcript |
| `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | read_text, resolve_selected_options, main, rebrand_text |
| `tests/hermes_cli/test_config.py` | test_v11_upgrade_moves_custom_providers_into_providers, test_migrate_to_v15_adds_interim_assistant_message_gate, test_migrate_adds_discord_channel_prompts_default |
| `tests/skills/test_google_workspace_api.py` | _write_token, test_bridge_main_injects_token_env, test_api_get_credentials_refresh_persists_authorized_user_type |
| `tests/skills/test_memento_cards.py` | test_import_without_collection_column, test_import_skips_empty_rows |
| `hermes_cli/web_server.py` | get_config_raw |
| `optional-skills/mcp/fastmcp/templates/file_processor.py` | _read_text |
| `optional-skills/productivity/telephony/scripts/telephony.py` | _messages_after_checkpoint |

## Entry Points

Start here when exploring this area:

- **`get_config_raw`** (Function) — `hermes_cli/web_server.py:1963`
- **`load_module`** (Function) — `tests/skills/test_openclaw_migration.py:18`
- **`test_migrator_copies_skill_and_merges_allowlist`** (Function) — `tests/skills/test_openclaw_migration.py:104`
- **`test_migrator_optionally_imports_supported_secrets_and_messaging_settings`** (Function) — `tests/skills/test_openclaw_migration.py:149`
- **`test_messaging_cwd_skipped_when_inside_source`** (Function) — `tests/skills/test_openclaw_migration.py:187`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `get_config_raw` | Function | `hermes_cli/web_server.py` | 1963 |
| `load_module` | Function | `tests/skills/test_openclaw_migration.py` | 18 |
| `test_migrator_copies_skill_and_merges_allowlist` | Function | `tests/skills/test_openclaw_migration.py` | 104 |
| `test_migrator_optionally_imports_supported_secrets_and_messaging_settings` | Function | `tests/skills/test_openclaw_migration.py` | 149 |
| `test_messaging_cwd_skipped_when_inside_source` | Function | `tests/skills/test_openclaw_migration.py` | 187 |
| `test_migrator_can_execute_only_selected_categories` | Function | `tests/skills/test_openclaw_migration.py` | 219 |
| `test_migrator_exports_full_overflow_entries` | Function | `tests/skills/test_openclaw_migration.py` | 282 |
| `test_migrator_can_rename_conflicting_imported_skill` | Function | `tests/skills/test_openclaw_migration.py` | 313 |
| `test_migrator_can_overwrite_conflicting_imported_skill_with_backup` | Function | `tests/skills/test_openclaw_migration.py` | 352 |
| `test_discord_settings_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 389 |
| `test_slack_settings_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 420 |
| `test_signal_settings_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 453 |
| `test_model_config_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 486 |
| `test_model_config_object_format` | Function | `tests/skills/test_openclaw_migration.py` | 513 |
| `test_tts_config_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 539 |
| `test_shared_skills_migrated` | Function | `tests/skills/test_openclaw_migration.py` | 574 |
| `test_daily_memory_merged` | Function | `tests/skills/test_openclaw_migration.py` | 598 |
| `test_provider_keys_require_migrate_secrets_flag` | Function | `tests/skills/test_openclaw_migration.py` | 629 |
| `test_workspace_agents_records_skip_when_missing` | Function | `tests/skills/test_openclaw_migration.py` | 673 |
| `test_cron_store_is_archived_without_config_cron_section` | Function | `tests/skills/test_openclaw_migration.py` | 692 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Honcho_command → Read_text` | cross_community | 5 |
| `Get_skills → Read_text` | cross_community | 5 |
| `Cmd_migrate → Read_text` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Scripts | 32 calls |
| Hermes_cli | 7 calls |
| Tools | 1 calls |

## How to Explore

1. `gitnexus_context({name: "get_config_raw"})` — see callers and callees
2. `gitnexus_query({query: "skills"})` — find related execution flows
3. Read key files listed above for implementation details
