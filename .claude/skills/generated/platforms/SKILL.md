---
name: platforms
description: "Skill for the Platforms area of async-hermes-agent. 680 symbols across 61 files."
---

# Platforms

680 symbols | 61 files | Cohesion: 54%

## When to Use

- Working with code in `gateway/`
- Understanding how test_reads_config_from_extra, test_falls_back_to_env_vars, test_send_uses_passive_reply_stream_when_reply_context_exists work
- Modifying platforms-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `gateway/platforms/feishu.py` | FeishuNormalizedMessage, parse_feishu_post_payload, normalize_feishu_message, _normalize_merge_forward_message, _normalize_share_chat_message (+107) |
| `gateway/platforms/weixin.py` | _random_wechat_uin, _headers, get, _download_bytes, _media_reference (+56) |
| `gateway/platforms/wecom.py` | WeComAdapter, _dispatch_payload, _send_request, _payload_req_id, _reply_req_id_for_message (+43) |
| `gateway/platforms/qqbot.py` | _on_message, _handle_c2c_message, _handle_group_message, _handle_guild_message, _handle_dm_message (+42) |
| `gateway/platforms/matrix.py` | _handle_media_message, _check_e2ee_deps, check_matrix_requirements, edit_message, _on_invite (+35) |
| `gateway/platforms/api_server.py` | check_api_server_requirements, _normalize_chat_content, get_or_set, _make_request_fingerprint, _derive_chat_session_id (+35) |
| `gateway/platforms/discord.py` | send_image, send_animation, leave_voice_channel, _reset_voice_timeout, _voice_timeout_handler (+33) |
| `gateway/platforms/telegram.py` | _metadata_thread_id, _message_thread_id_for_send, send_voice, send_image_file, send_document (+24) |
| `gateway/platforms/base.py` | cache_image_from_bytes, cache_audio_from_bytes, build_source, send, send_voice (+22) |
| `gateway/platforms/slack.py` | _download_slack_file, _get_client, send, _resolve_thread_ts, _add_reaction (+17) |

## Entry Points

Start here when exploring this area:

- **`test_reads_config_from_extra`** (Function) — `tests/gateway/test_wecom.py:38`
- **`test_falls_back_to_env_vars`** (Function) — `tests/gateway/test_wecom.py:59`
- **`test_send_uses_passive_reply_stream_when_reply_context_exists`** (Function) — `tests/gateway/test_wecom.py:121`
- **`test_send_image_file_uses_passive_reply_media_when_reply_context_exists`** (Function) — `tests/gateway/test_wecom.py:141`
- **`test_dispatch_accepts_new_and_legacy_callback_cmds`** (Function) — `tests/gateway/test_wecom.py:217`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `WeComAdapter` | Class | `gateway/platforms/wecom.py` | 140 |
| `FeishuNormalizedMessage` | Class | `gateway/platforms/feishu.py` | 273 |
| `ContentURI` | Class | `tests/gateway/test_matrix.py` | 57 |
| `UserID` | Class | `tests/gateway/test_matrix.py` | 48 |
| `RoomID` | Class | `tests/gateway/test_matrix.py` | 51 |
| `MessageDeduplicator` | Class | `gateway/platforms/helpers.py` | 24 |
| `WeComCryptoError` | Class | `gateway/platforms/wecom_crypto.py` | 21 |
| `SignatureError` | Class | `gateway/platforms/wecom_crypto.py` | 25 |
| `DecryptError` | Class | `gateway/platforms/wecom_crypto.py` | 29 |
| `EncryptError` | Class | `gateway/platforms/wecom_crypto.py` | 33 |
| `BlueBubblesAdapter` | Class | `gateway/platforms/bluebubbles.py` | 99 |
| `EventID` | Class | `tests/gateway/test_matrix.py` | 54 |
| `FeishuPostMediaRef` | Class | `gateway/platforms/feishu.py` | 258 |
| `QQCloseError` | Class | `gateway/platforms/qqbot.py` | 75 |
| `ContextTokenStore` | Class | `gateway/platforms/weixin.py` | 229 |
| `ThreadParticipationTracker` | Class | `gateway/platforms/helpers.py` | 189 |
| `FeishuBatchState` | Class | `gateway/platforms/feishu.py` | 325 |
| `test_reads_config_from_extra` | Function | `tests/gateway/test_wecom.py` | 38 |
| `test_falls_back_to_env_vars` | Function | `tests/gateway/test_wecom.py` | 59 |
| `test_send_uses_passive_reply_stream_when_reply_context_exists` | Function | `tests/gateway/test_wecom.py` | 121 |

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
| `Run_sync → _key` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Gateway | 340 calls |
| Tools | 47 calls |
| Hermes_cli | 21 calls |
| Skills | 9 calls |
| Cron | 6 calls |
| Agent | 3 calls |
| Scripts | 3 calls |
| Tests | 2 calls |

## How to Explore

1. `gitnexus_context({name: "test_reads_config_from_extra"})` — see callers and callees
2. `gitnexus_query({query: "platforms"})` — find related execution flows
3. Read key files listed above for implementation details
