---
name: integration
description: "Skill for the Integration area of async-hermes-agent. 97 symbols across 14 files."
---

# Integration

97 symbols | 14 files | Cohesion: 73%

## When to Use

- Working with code in `tests/`
- Understanding how test_valid_encrypted_packet_buffered, test_wrong_key_packet_dropped, test_bot_ssrc_ignored work
- Modifying integration-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tests/integration/test_voice_channel_flow.py` | _make_secret_key, _build_encrypted_rtp_packet, _build_padded_rtp_packet, _make_voice_receiver, test_valid_encrypted_packet_buffered (+33) |
| `tests/integration/test_web_tools.py` | print_section, print_error, log_result, test_environment, test_web_search (+8) |
| `tests/integration/test_ha_integration.py` | test_list_entities_returns_all, test_list_entities_domain_filter, test_rest_unauthorized, test_rest_server_error, _adapter_for (+6) |
| `tests/integration/test_modal_terminal.py` | test_modal_requirements, test_simple_command, test_python_execution, test_pip_install, test_filesystem_persistence (+2) |
| `gateway/platforms/discord.py` | stop, pause, resume, map_ssrc, _on_packet |
| `tests/integration/test_checkpoint_resumption.py` | create_test_dataset, _cleanup_test_artifacts, test_current_implementation, test_interruption_and_resume, main |
| `tests/gateway/test_voice_command.py` | test_pause_resume, test_on_packet_skips_when_paused, test_paused_receiver_ignores_packets, test_resumed_receiver_accepts_packets |
| `tools/terminal_tool.py` | _parse_env_var, _get_env_config, cleanup_vm |
| `tests/integration/test_daytona_terminal.py` | _run, test_filesystem_survives_stop_and_resume, test_different_tasks_isolated |
| `tools/homeassistant_tool.py` | _filter_and_summarize, _async_list_entities |

## Entry Points

Start here when exploring this area:

- **`test_valid_encrypted_packet_buffered`** (Function) — `tests/integration/test_voice_channel_flow.py:145`
- **`test_wrong_key_packet_dropped`** (Function) — `tests/integration/test_voice_channel_flow.py:157`
- **`test_bot_ssrc_ignored`** (Function) — `tests/integration/test_voice_channel_flow.py:169`
- **`test_multiple_packets_accumulate`** (Function) — `tests/integration/test_voice_channel_flow.py:179`
- **`test_different_ssrcs_separate_buffers`** (Function) — `tests/integration/test_voice_channel_flow.py:194`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `FakeHAServer` | Class | `tests/fakes/fake_ha_server.py` | 76 |
| `BatchRunner` | Class | `batch_runner.py` | 513 |
| `test_valid_encrypted_packet_buffered` | Function | `tests/integration/test_voice_channel_flow.py` | 145 |
| `test_wrong_key_packet_dropped` | Function | `tests/integration/test_voice_channel_flow.py` | 157 |
| `test_bot_ssrc_ignored` | Function | `tests/integration/test_voice_channel_flow.py` | 169 |
| `test_multiple_packets_accumulate` | Function | `tests/integration/test_voice_channel_flow.py` | 179 |
| `test_different_ssrcs_separate_buffers` | Function | `tests/integration/test_voice_channel_flow.py` | 194 |
| `test_dave_unknown_ssrc_passthrough` | Function | `tests/integration/test_voice_channel_flow.py` | 211 |
| `test_dave_unencrypted_error_passthrough` | Function | `tests/integration/test_voice_channel_flow.py` | 226 |
| `test_dave_real_error_drops` | Function | `tests/integration/test_voice_channel_flow.py` | 244 |
| `test_padded_packet_stripped_and_buffered` | Function | `tests/integration/test_voice_channel_flow.py` | 261 |
| `test_padded_packet_matches_unpadded_output` | Function | `tests/integration/test_voice_channel_flow.py` | 274 |
| `test_padding_with_dave_passthrough` | Function | `tests/integration/test_voice_channel_flow.py` | 291 |
| `test_invalid_padding_length_zero_dropped` | Function | `tests/integration/test_voice_channel_flow.py` | 305 |
| `test_invalid_padding_length_overflow_dropped` | Function | `tests/integration/test_voice_channel_flow.py` | 318 |
| `test_padding_consuming_entire_payload_dropped` | Function | `tests/integration/test_voice_channel_flow.py` | 331 |
| `test_padding_with_extension_stripped_correctly` | Function | `tests/integration/test_voice_channel_flow.py` | 342 |
| `test_single_utterance_flow` | Function | `tests/integration/test_voice_channel_flow.py` | 368 |
| `test_utterance_with_ssrc_automap` | Function | `tests/integration/test_voice_channel_flow.py` | 392 |
| `test_pause_blocks_during_playback` | Function | `tests/integration/test_voice_channel_flow.py` | 416 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Play_tts → Stop` | cross_community | 6 |
| `Evaluate → Clear_file_ops_cache` | cross_community | 4 |
| `Evaluate → Stop` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 25 calls |
| Gateway | 19 calls |
| Platforms | 5 calls |
| Cron | 3 calls |
| Hermes_cli | 2 calls |
| Cluster_151 | 2 calls |
| Scripts | 1 calls |
| Agent | 1 calls |

## How to Explore

1. `gitnexus_context({name: "test_valid_encrypted_packet_buffered"})` — see callers and callees
2. `gitnexus_query({query: "integration"})` — find related execution flows
3. Read key files listed above for implementation details
