---
name: platforms
description: "Skill for the Platforms area of async-hermes-agent. 670 symbols across 63 files."
---

# Platforms

670 symbols | 63 files | Cohesion: 53%

## When to Use

- Working with code in `gateway/`
- Understanding how label_from_token, test_verifier_and_challenge_s256_roundtrip, test_image_builder_aes_key_is_base64_of_hex work
- Modifying platforms-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `gateway/platforms/feishu.py` | FeishuNormalizedMessage, parse_feishu_post_payload, normalize_feishu_message, _normalize_merge_forward_message, _normalize_share_chat_message (+106) |
| `gateway/platforms/weixin.py` | _random_wechat_uin, _headers, get, _download_bytes, _media_reference (+55) |
| `gateway/platforms/qqbot.py` | check_qq_requirements, _on_message, _handle_c2c_message, _handle_group_message, _handle_guild_message (+42) |
| `gateway/platforms/wecom.py` | check_wecom_requirements, _reply_req_id_for_message, _send_followup_markdown, _send_media_source, send_image_file (+40) |
| `gateway/platforms/matrix.py` | _check_e2ee_deps, check_matrix_requirements, _handle_media_message, edit_message, _on_invite (+35) |
| `gateway/platforms/api_server.py` | check_api_server_requirements, _normalize_chat_content, get_or_set, _make_request_fingerprint, _derive_chat_session_id (+35) |
| `gateway/platforms/discord.py` | send_image, send_animation, _cache_discord_document, leave_voice_channel, _reset_voice_timeout (+33) |
| `gateway/platforms/telegram.py` | _metadata_thread_id, _message_thread_id_for_send, send_voice, send_image_file, send_document (+24) |
| `gateway/platforms/slack.py` | _download_slack_file, _get_client, send, _resolve_thread_ts, _add_reaction (+17) |
| `gateway/platforms/base.py` | cache_image_from_bytes, cache_audio_from_bytes, build_source, resolve_proxy_url, proxy_kwargs_for_aiohttp (+16) |

## Entry Points

Start here when exploring this area:

- **`label_from_token`** (Function) — `agent/credential_pool.py:173`
- **`test_verifier_and_challenge_s256_roundtrip`** (Function) — `tests/agent/test_gemini_cloudcode.py:56`
- **`test_image_builder_aes_key_is_base64_of_hex`** (Function) — `tests/gateway/test_weixin.py:459`
- **`iter_any`** (Function) — `tests/gateway/test_proxy_mode.py:51`
- **`test_signature_valid_passes`** (Function) — `tests/gateway/test_feishu.py:2659`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `EncryptError` | Class | `gateway/platforms/wecom_crypto.py` | 33 |
| `FeishuNormalizedMessage` | Class | `gateway/platforms/feishu.py` | 273 |
| `ContentURI` | Class | `tests/gateway/test_matrix.py` | 57 |
| `UserID` | Class | `tests/gateway/test_matrix.py` | 48 |
| `RoomID` | Class | `tests/gateway/test_matrix.py` | 51 |
| `MessageDeduplicator` | Class | `gateway/platforms/helpers.py` | 24 |
| `BlueBubblesAdapter` | Class | `gateway/platforms/bluebubbles.py` | 99 |
| `EventID` | Class | `tests/gateway/test_matrix.py` | 54 |
| `WeComCryptoError` | Class | `gateway/platforms/wecom_crypto.py` | 21 |
| `SignatureError` | Class | `gateway/platforms/wecom_crypto.py` | 25 |
| `DecryptError` | Class | `gateway/platforms/wecom_crypto.py` | 29 |
| `FeishuPostMediaRef` | Class | `gateway/platforms/feishu.py` | 258 |
| `QQCloseError` | Class | `gateway/platforms/qqbot.py` | 75 |
| `ContextTokenStore` | Class | `gateway/platforms/weixin.py` | 229 |
| `ThreadParticipationTracker` | Class | `gateway/platforms/helpers.py` | 189 |
| `FeishuBatchState` | Class | `gateway/platforms/feishu.py` | 325 |
| `label_from_token` | Function | `agent/credential_pool.py` | 173 |
| `test_verifier_and_challenge_s256_roundtrip` | Function | `tests/agent/test_gemini_cloudcode.py` | 56 |
| `test_image_builder_aes_key_is_base64_of_hex` | Function | `tests/gateway/test_weixin.py` | 459 |
| `iter_any` | Function | `tests/gateway/test_proxy_mode.py` | 51 |

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
| Gateway | 364 calls |
| Tools | 32 calls |
| Hermes_cli | 23 calls |
| Skills | 9 calls |
| Cron | 5 calls |
| Agent | 4 calls |
| Scripts | 3 calls |
| Tests | 2 calls |

## How to Explore

1. `gitnexus_context({name: "label_from_token"})` — see callers and callees
2. `gitnexus_query({query: "platforms"})` — find related execution flows
3. Read key files listed above for implementation details
