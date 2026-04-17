---
name: scripts
description: "Skill for the Scripts area of async-hermes-agent. 341 symbols across 42 files."
---

# Scripts

341 symbols | 42 files | Cohesion: 79%

## When to Use

- Working with code in `optional-skills/`
- Understanding how sha256_file, ensure_parent, resolve_secret_input work
- Modifying scripts-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | sha256_file, ensure_parent, resolve_secret_input, load_yaml_file, dump_yaml_file (+65) |
| `optional-skills/productivity/telephony/scripts/telephony.py` | TelephonyError, _env_path, _load_dotenv_values, _env_or_config, _normalize_phone (+39) |
| `optional-skills/blockchain/base/scripts/base_client.py` | _http_get_json, _rpc_call, _rpc_batch_chunk, rpc_batch, wei_to_eth (+19) |
| `skills/productivity/google-workspace/scripts/google_api.py` | _gws_binary, _run_gws, _headers_dict, build_service, gmail_search (+17) |
| `optional-skills/productivity/memento-flashcards/scripts/memento_cards.py` | _now, _iso, _parse_iso, _load, _save (+12) |
| `optional-skills/creative/meme-generation/scripts/generate_meme.py` | _default_fields, find_font, _wrap_text, draw_outlined_text, _overlay_on_image (+12) |
| `optional-skills/blockchain/solana/scripts/solana_client.py` | main, _http_get_json, print_json, fetch_prices, resolve_token_name (+11) |
| `skills/research/polymarket/scripts/polymarket.py` | _get, _fmt_pct, cmd_price, cmd_book, cmd_history (+9) |
| `skills/productivity/google-workspace/scripts/setup.py` | _normalize_authorized_user_payload, _missing_scopes_from_payload, install_deps, _ensure_deps, check_auth (+5) |
| `scripts/discord-voice-doctor.py` | check, warn, section, check_packages, check_system_tools (+4) |

## Entry Points

Start here when exploring this area:

- **`sha256_file`** (Function) — `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py:286`
- **`ensure_parent`** (Function) — `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py:302`
- **`resolve_secret_input`** (Function) — `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py:306`
- **`load_yaml_file`** (Function) — `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py:329`
- **`dump_yaml_file`** (Function) — `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py:336`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `TelephonyError` | Class | `optional-skills/productivity/telephony/scripts/telephony.py` | 58 |
| `TrajectoryCompressor` | Class | `trajectory_compressor.py` | 306 |
| `sha256_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 286 |
| `ensure_parent` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 302 |
| `resolve_secret_input` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 306 |
| `load_yaml_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 329 |
| `dump_yaml_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 336 |
| `parse_env_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 346 |
| `save_env_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 359 |
| `backup_existing` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 365 |
| `parse_existing_memory_entries` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 396 |
| `record` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 612 |
| `source_candidate` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 632 |
| `resolve_skill_destination` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 652 |
| `migrate` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 664 |
| `run_if_selected` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 738 |
| `maybe_backup` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 788 |
| `write_overflow_entries` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 793 |
| `copy_file` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 802 |
| `migrate_soul` | Function | `optional-skills/migration/openclaw-migration/scripts/openclaw_to_hermes.py` | 829 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Main → Get_hermes_home` | cross_community | 6 |
| `Main → Add_trajectory_metrics` | cross_community | 6 |
| `Main → _print_summary` | cross_community | 5 |
| `Migrate_daily_memory → Context_prefix` | cross_community | 4 |
| `Main → _get_zoneinfo` | cross_community | 4 |
| `Cmd_wallet → Load` | cross_community | 4 |
| `Cmd_tx → Load` | cross_community | 4 |
| `Cmd_gas → Load` | cross_community | 4 |
| `Cmd_contract → Load` | cross_community | 4 |
| `Main → _validate` | cross_community | 4 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Skills | 32 calls |
| Hermes_cli | 28 calls |
| Tools | 20 calls |
| Agent | 11 calls |
| Platforms | 6 calls |
| Cron | 4 calls |
| Tests | 2 calls |
| Integration | 2 calls |

## How to Explore

1. `gitnexus_context({name: "sha256_file"})` — see callers and callees
2. `gitnexus_query({query: "scripts"})` — find related execution flows
3. Read key files listed above for implementation details
