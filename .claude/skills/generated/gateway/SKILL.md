---
name: gateway
description: "Skill for the Gateway area of async-hermes-agent. 2649 symbols across 206 files."
---

# Gateway

2649 symbols | 206 files | Cohesion: 63%

## When to Use

- Working with code in `tests/`
- Understanding how test_qr_env_produces_valid_adapter_settings, test_open_dm_env_sets_correct_adapter_state, test_group_open_env_sets_adapter_group_policy work
- Modifying gateway-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/gateway/test_voice_command.py` | _make_discord_adapter, _make_discord_adapter, _make_discord_event, test_join_unsupported_platform, test_join_no_guild_id (+131) |
| `gateway/run.py` | _interim_assistant_cb, _session_expiry_watcher, _handle_stop_command, _handle_undo_command, _normalize_whatsapp_identifier (+123) |
| `tests/gateway/test_feishu.py` | test_connect_rejects_existing_app_lock, test_edit_message_updates_existing_feishu_message, _MessageAPI, test_edit_message_falls_back_to_text_when_post_update_is_rejected, test_get_chat_info_uses_real_feishu_chat_api (+100) |
| `tests/gateway/test_api_server.py` | _make_adapter, _create_app, test_security_headers_present, test_health_returns_ok, test_v1_health_alias_returns_ok (+95) |
| `tests/gateway/test_stream_consumer.py` | test_first_send_strips_media, test_edit_strips_media, test_media_only_skips_send, test_cursor_only_update_skips_send, test_short_text_with_cursor_skips_new_message (+48) |
| `tests/gateway/test_session.py` | test_session_entry_default, test_session_entry_roundtrip, test_update_session_sets_last_prompt_tokens, test_update_session_none_does_not_change, test_update_session_zero_resets (+46) |
| `gateway/platforms/feishu.py` | _strip_markdown_to_plain_text, _build_markdown_post_payload, FeishuAdapter, _build_event_handler, send (+32) |
| `tests/gateway/test_api_server_jobs.py` | test_list_jobs, test_list_jobs_include_disabled, test_list_jobs_default_excludes_disabled, test_get_job, test_get_job_not_found (+32) |
| `tests/gateway/test_telegram_network.py` | test_env_var_populates_config_extra, test_env_var_creates_platform_if_missing, test_env_var_strips_whitespace, test_empty_env_var_does_not_populate, _fake_transport_factory (+32) |
| `tests/gateway/test_sms.py` | _compute_twilio_signature, _make_adapter, test_valid_signature_accepted, test_invalid_signature_rejected, test_wrong_token_rejected (+31) |

## Entry Points

Start here when exploring this area:

- **`test_qr_env_produces_valid_adapter_settings`** (Function) — `tests/gateway/test_setup_feishu.py:244`
- **`test_open_dm_env_sets_correct_adapter_state`** (Function) — `tests/gateway/test_setup_feishu.py:258`
- **`test_group_open_env_sets_adapter_group_policy`** (Function) — `tests/gateway/test_setup_feishu.py:270`
- **`test_connect_rejects_existing_app_lock`** (Function) — `tests/gateway/test_feishu.py:253`
- **`test_edit_message_updates_existing_feishu_message`** (Function) — `tests/gateway/test_feishu.py:329`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `PlatformConfig` | Class | `gateway/config.py` | 143 |
| `FeishuAdapter` | Class | `gateway/platforms/feishu.py` | 1041 |
| `TestClient` | Class | `tests/plugins/test_retaindb_plugin.py` | 53 |
| `PairingStore` | Class | `gateway/pairing.py` | 74 |
| `StreamConsumerConfig` | Class | `gateway/stream_consumer.py` | 40 |
| `GatewayStreamConsumer` | Class | `gateway/stream_consumer.py` | 48 |
| `SessionEntry` | Class | `gateway/session.py` | 331 |
| `SessionResetPolicy` | Class | `gateway/config.py` | 100 |
| `GatewayConfig` | Class | `gateway/config.py` | 221 |
| `FakeTextChannel` | Class | `tests/gateway/test_discord_free_response.py` | 57 |
| `FakeForumChannel` | Class | `tests/gateway/test_discord_free_response.py` | 65 |
| `FakeThread` | Class | `tests/gateway/test_discord_free_response.py` | 74 |
| `DummyTelegramAdapter` | Class | `tests/gateway/test_base_topic_sessions.py` | 12 |
| `WeixinAdapter` | Class | `gateway/platforms/weixin.py` | 1038 |
| `SessionSource` | Class | `gateway/session.py` | 65 |
| `SendResult` | Class | `gateway/platforms/base.py` | 723 |
| `HookRegistry` | Class | `gateway/hooks.py` | 33 |
| `StubAdapter` | Class | `tests/gateway/test_platform_reconnect.py` | 13 |
| `MatrixAdapter` | Class | `gateway/platforms/matrix.py` | 198 |
| `HomeChannel` | Class | `gateway/config.py` | 72 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Play_tts → _get_lock_dir` | cross_community | 10 |
| `Play_tts → _read_json_file` | cross_community | 9 |
| `Play_tts → _get_process_start_time` | cross_community | 9 |
| `Connect → Get_hermes_home` | cross_community | 6 |
| `Connect → _get_process_start_time` | cross_community | 6 |
| `Connect → Get_hermes_home` | cross_community | 6 |
| `Connect → _get_process_start_time` | cross_community | 6 |
| `Play_tts → Stop` | cross_community | 6 |
| `Play_tts → Is_connected` | cross_community | 6 |
| `Run_sync → Build_session_key` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Platforms | 230 calls |
| Hermes_cli | 86 calls |
| Tools | 82 calls |
| Agent | 57 calls |
| Cron | 49 calls |
| Tests | 27 calls |
| Integration | 26 calls |
| Skills | 15 calls |

## How to Explore

1. `gitnexus_context({name: "test_qr_env_produces_valid_adapter_settings"})` — see callers and callees
2. `gitnexus_query({query: "gateway"})` — find related execution flows
3. Read key files listed above for implementation details
