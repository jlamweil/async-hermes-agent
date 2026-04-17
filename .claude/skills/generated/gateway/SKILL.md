---
name: gateway
description: "Skill for the Gateway area of async-hermes-agent. 2676 symbols across 204 files."
---

# Gateway

2676 symbols | 204 files | Cohesion: 62%

## When to Use

- Working with code in `tests/`
- Understanding how make_runner, make_adapter, test_qr_env_produces_valid_adapter_settings work
- Modifying gateway-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/gateway/test_voice_command.py` | _make_discord_adapter, _make_discord_adapter, test_input_reuses_bound_source_metadata, _make_discord_event, test_join_unsupported_platform (+135) |
| `gateway/run.py` | _run_agent_via_proxy, _interim_assistant_cb, _handle_voice_channel_input, _session_key_for_source, _handle_approve_command (+122) |
| `tests/gateway/test_feishu.py` | test_connect_rejects_existing_app_lock, test_edit_message_updates_existing_feishu_message, _MessageAPI, test_edit_message_falls_back_to_text_when_post_update_is_rejected, test_get_chat_info_uses_real_feishu_chat_api (+100) |
| `tests/gateway/test_api_server.py` | _make_adapter, _create_app, test_security_headers_present, test_health_returns_ok, test_v1_health_alias_returns_ok (+95) |
| `tests/gateway/test_stream_consumer.py` | test_first_send_strips_media, test_edit_strips_media, test_media_only_skips_send, test_cursor_only_update_skips_send, test_short_text_with_cursor_skips_new_message (+48) |
| `tests/gateway/test_session.py` | test_whatsapp_dm_includes_chat_id, test_store_delegates_to_build_session_key, test_telegram_dm_includes_chat_id, test_distinct_dm_chat_ids_get_distinct_session_keys, test_discord_group_includes_chat_id (+42) |
| `gateway/platforms/base.py` | set_message_handler, send, stop_typing, send_voice, play_tts (+35) |
| `gateway/platforms/feishu.py` | _strip_markdown_to_plain_text, _build_markdown_post_payload, FeishuAdapter, _build_event_handler, send (+33) |
| `tests/gateway/test_api_server_jobs.py` | test_list_jobs, test_list_jobs_include_disabled, test_list_jobs_default_excludes_disabled, test_get_job, test_get_job_not_found (+32) |
| `tests/gateway/test_telegram_network.py` | test_env_var_populates_config_extra, test_env_var_creates_platform_if_missing, test_env_var_strips_whitespace, test_empty_env_var_does_not_populate, _fake_transport_factory (+32) |

## Entry Points

Start here when exploring this area:

- **`make_runner`** (Function) — `tests/e2e/conftest.py:155`
- **`make_adapter`** (Function) — `tests/e2e/conftest.py:205`
- **`test_qr_env_produces_valid_adapter_settings`** (Function) — `tests/gateway/test_setup_feishu.py:244`
- **`test_open_dm_env_sets_correct_adapter_state`** (Function) — `tests/gateway/test_setup_feishu.py:258`
- **`test_group_open_env_sets_adapter_group_policy`** (Function) — `tests/gateway/test_setup_feishu.py:270`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `PlatformConfig` | Class | `gateway/config.py` | 143 |
| `FeishuAdapter` | Class | `gateway/platforms/feishu.py` | 1041 |
| `TestClient` | Class | `tests/plugins/test_retaindb_plugin.py` | 53 |
| `PairingStore` | Class | `gateway/pairing.py` | 74 |
| `StreamConsumerConfig` | Class | `gateway/stream_consumer.py` | 40 |
| `GatewayStreamConsumer` | Class | `gateway/stream_consumer.py` | 48 |
| `GatewayConfig` | Class | `gateway/config.py` | 221 |
| `DummyTelegramAdapter` | Class | `tests/gateway/test_base_topic_sessions.py` | 12 |
| `FakeTextChannel` | Class | `tests/gateway/test_discord_free_response.py` | 57 |
| `FakeForumChannel` | Class | `tests/gateway/test_discord_free_response.py` | 65 |
| `FakeThread` | Class | `tests/gateway/test_discord_free_response.py` | 74 |
| `SessionSource` | Class | `gateway/session.py` | 65 |
| `WeixinAdapter` | Class | `gateway/platforms/weixin.py` | 1038 |
| `SendResult` | Class | `gateway/platforms/base.py` | 723 |
| `HookRegistry` | Class | `gateway/hooks.py` | 33 |
| `StubAdapter` | Class | `tests/gateway/test_platform_reconnect.py` | 13 |
| `MatrixAdapter` | Class | `gateway/platforms/matrix.py` | 198 |
| `HomeChannel` | Class | `gateway/config.py` | 72 |
| `FakeClient` | Class | `tests/gateway/test_wecom_callback.py` | 115 |
| `WecomCallbackAdapter` | Class | `gateway/platforms/wecom_callback.py` | 54 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Play_tts → _get_lock_dir` | cross_community | 10 |
| `Play_tts → _read_json_file` | cross_community | 9 |
| `Play_tts → _get_process_start_time` | cross_community | 9 |
| `Cmd_profile → Resolve_gateway_approval` | cross_community | 8 |
| `Cmd_identity → Resolve_gateway_approval` | cross_community | 7 |
| `Gateway_setup → Resolve_gateway_approval` | cross_community | 6 |
| `Rollout_and_score_eval → Resolve_gateway_approval` | cross_community | 6 |
| `Connect → Get_hermes_home` | cross_community | 6 |
| `Connect → _get_process_start_time` | cross_community | 6 |
| `Connect → Get_hermes_home` | cross_community | 6 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Platforms | 222 calls |
| Hermes_cli | 125 calls |
| Tools | 72 calls |
| Cron | 51 calls |
| Tests | 39 calls |
| Agent | 34 calls |
| Integration | 26 calls |
| Skills | 15 calls |

## How to Explore

1. `gitnexus_context({name: "make_runner"})` — see callers and callees
2. `gitnexus_query({query: "gateway"})` — find related execution flows
3. Read key files listed above for implementation details
