---
name: environments
description: "Skill for the Environments area of async-hermes-agent. 122 symbols across 28 files."
---

# Environments

122 symbols | 28 files | Cohesion: 62%

## When to Use

- Working with code in `tools/`
- Understanding how get_subprocess_home, test_passthrough_allows_blocklisted_var, test_make_run_env_passthrough work
- Modifying environments-related functionality

## Key Files

| File | Symbols |
|------|---------|
| `tools/environments/base.py` | get_sandbox_dir, get_temp_dir, __init__, _load_json_store, _save_json_store (+10) |
| `tools/environments/modal.py` | _load_snapshots, _save_snapshots, _direct_snapshot_key, _get_snapshot_restore_candidate, _store_direct_snapshot (+9) |
| `tools/environments/singularity.py` | _get_scratch_dir, _get_apptainer_cache_dir, _get_or_build_sif, _find_singularity_executable, _ensure_singularity_available (+6) |
| `tools/environments/managed_modal.py` | _start_modal_exec, _poll_modal_exec, _create_sandbox, _request, _cancel_exec (+4) |
| `environments/tool_context.py` | search, terminal, download_file, download_dir, write_file (+4) |
| `tools/environments/file_sync.py` | iter_sync_files, quoted_mkdir_command, unique_parent_dirs, quoted_rm_command, _sync_back_once (+2) |
| `tools/environments/ssh.py` | _ensure_ssh_available, __init__, _establish_connection, _detect_remote_home, _ensure_remote_dirs (+2) |
| `tools/environments/docker.py` | _normalize_env_dict, find_docker, _ensure_docker_available, __init__, _storage_opt_supported (+1) |
| `environments/web_research_env.py` | WebResearchEnvConfig, compute_reward, _llm_judge, _parse_judge_json, _heuristic_score |
| `environments/agentic_opd_env.py` | AgenticOPDConfig, compute_reward, _apply_opd_pipeline, _opd_for_sequence, _extract_hint |

## Entry Points

Start here when exploring this area:

- **`get_subprocess_home`** (Function) — `hermes_constants.py:113`
- **`test_passthrough_allows_blocklisted_var`** (Function) — `tests/tools/test_env_passthrough.py:174`
- **`test_make_run_env_passthrough`** (Function) — `tests/tools/test_env_passthrough.py:185`
- **`get_sandbox_dir`** (Function) — `tools/environments/base.py:65`
- **`get_skills_directory_mount`** (Function) — `tools/credential_files.py:200`

## Key Symbols

| Symbol | Type | File | Line |
|--------|------|------|------|
| `WebResearchEnvConfig` | Class | `environments/web_research_env.py` | 148 |
| `HermesAgentEnvConfig` | Class | `environments/hermes_base_env.py` | 77 |
| `AgenticOPDConfig` | Class | `environments/agentic_opd_env.py` | 317 |
| `TerminalTestEnvConfig` | Class | `environments/terminal_test_env/terminal_test_env.py` | 84 |
| `HermesSweEnvConfig` | Class | `environments/hermes_swe_env/hermes_swe_env.py` | 55 |
| `YCBenchEvalConfig` | Class | `environments/benchmarks/yc_bench/yc_bench_env.py` | 178 |
| `TerminalBench2EvalConfig` | Class | `environments/benchmarks/terminalbench_2/terminalbench2_env.py` | 75 |
| `TBLiteEvalConfig` | Class | `environments/benchmarks/tblite/tblite_env.py` | 43 |
| `SingularityEnvironment` | Class | `tools/environments/singularity.py` | 155 |
| `BaseModalExecutionEnvironment` | Class | `tools/environments/modal_utils.py` | 57 |
| `ManagedModalEnvironment` | Class | `tools/environments/managed_modal.py` | 35 |
| `DaytonaEnvironment` | Class | `tools/environments/daytona.py` | 29 |
| `BaseEnvironment` | Class | `tools/environments/base.py` | 251 |
| `ModalEnvironment` | Class | `tools/environments/modal.py` | 146 |
| `DockerEnvironment` | Class | `tools/environments/docker.py` | 234 |
| `HermesAgentBaseEnv` | Class | `environments/hermes_base_env.py` | 220 |
| `TerminalBench2EvalEnv` | Class | `environments/benchmarks/terminalbench_2/terminalbench2_env.py` | 220 |
| `get_subprocess_home` | Function | `hermes_constants.py` | 113 |
| `test_passthrough_allows_blocklisted_var` | Function | `tests/tools/test_env_passthrough.py` | 174 |
| `test_make_run_env_passthrough` | Function | `tests/tools/test_env_passthrough.py` | 185 |

## Execution Flows

| Flow | Type | Steps |
|------|------|-------|
| `Main → LocalEnvironment` | cross_community | 5 |
| `Main → DockerEnvironment` | cross_community | 5 |
| `Main → ModalEnvironment` | cross_community | 5 |

## Connected Areas

| Area | Connections |
|------|-------------|
| Tools | 39 calls |
| Hermes_cli | 4 calls |
| Agent | 2 calls |
| Platforms | 2 calls |
| Retaindb | 1 calls |
| Run_agent | 1 calls |
| Terminalbench_2 | 1 calls |

## How to Explore

1. `gitnexus_context({name: "get_subprocess_home"})` — see callers and callees
2. `gitnexus_query({query: "environments"})` — find related execution flows
3. Read key files listed above for implementation details
