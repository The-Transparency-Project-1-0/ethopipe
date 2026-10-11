# Solo Maintainer Guardrails & Anti-Bloat Audit Report

**Generated:** `2026-10-11 19:02:18Z`
**Audit Mode:** `Standard`
**Verdict:** ![Status](https://img.shields.io/badge/Solo_Maintainer_Audit-FAILED-red)

## Executive Summary

This automated scorecard enforces the **EthoPipe Solo Maintainer Charter**: protecting the repository from dependency creep, polyglot sprawl, out-of-scope enterprise cloud plugins, and cognitive debt.

| Pillar | Status | Passed | Issues |
| :--- | :---: | :---: | :---: |
| Language Monoculture | ❌ FAIL | 0/2 | 2 |
| Dependency & Supply Chain Budget | ✅ PASS | 3/3 | 0 |
| Agent Plugin & Skill Hygiene | ✅ PASS | 2/2 | 0 |
| Architectural Simplicity & Cognitive Budget | ✅ PASS | 2/2 | 0 |
| Toolchain Consolidation | ✅ PASS | 2/2 | 0 |

---

## Detailed Check Breakdown

### Language Monoculture

#### ❌ Foreign Package Managers

**Details:**
```text
Forbidden foreign package managers detected:
  - `git-sync\go.mod` (Go module manifest)
```
**Action Required:** Remove secondary language manifests. Maintain pure Python.

#### ❌ Pure Python Source Monoculture

**Details:**
```text
Unauthorized non-Python source files detected:
  - `git-sync\client.go` (Go runtime and compilation overhead)
  - `git-sync\client_test.go` (Go runtime and compilation overhead)
  - `git-sync\doc.go` (Go runtime and compilation overhead)
  - `git-sync\errors.go` (Go runtime and compilation overhead)
  - `git-sync\errors_test.go` (Go runtime and compilation overhead)
  - `git-sync\example_test.go` (Go runtime and compilation overhead)
  - `git-sync\identity.go` (Go runtime and compilation overhead)
  - `git-sync\identity_test.go` (Go runtime and compilation overhead)
  - `git-sync\results.go` (Go runtime and compilation overhead)
  - `git-sync\results_test.go` (Go runtime and compilation overhead)
  - `git-sync\types.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\args_test.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\bootstrap.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\convert_sha256.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\convert_sha256_test.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\fetch.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\flags.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\flags_test.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\main.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\main_test.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\probe.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\root.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\syncplan.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\version.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\internal\sha256convert\sha256convert.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\internal\sha256convert\sha256convert_test.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync\internal\versioninfo\versioninfo.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync-bench\main.go` (Go runtime and compilation overhead)
  - `git-sync\cmd\git-sync-bench\main_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\auth\auth.go` (Go runtime and compilation overhead)
  - `git-sync\internal\auth\auth_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\convert\convert.go` (Go runtime and compilation overhead)
  - `git-sync\internal\convert\convert_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\benchmark_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\capability.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\capability_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\commitparents.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\commitparents_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\conn.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\fetch.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\fetch_helpers_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\fetch_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\helper.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\helper_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\pktline.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\pktline_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\push.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\push_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\readers.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\readers_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\refnames.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\refnames_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\refs.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\refs_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\samesite.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\samesite_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\smarthttp.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\smarthttp_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\ssh.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\ssh_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\target_features.go` (Go runtime and compilation overhead)
  - `git-sync\internal\gitproto\target_features_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\benchmark_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\checkpoint.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\checkpoint_from_parents_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\checkpoint_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\exclude_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\include_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\planner.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\planner_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\relay.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\targetscope_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\planner\types.go` (Go runtime and compilation overhead)
  - `git-sync\internal\redact\redact.go` (Go runtime and compilation overhead)
  - `git-sync\internal\redact\redact_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\sanitize\sanitize.go` (Go runtime and compilation overhead)
  - `git-sync\internal\sanitize\sanitize_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\bootstrap.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\bootstrap_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\pack_observer.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\pack_observer_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\push_diagnostics.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\bootstrap\push_diagnostics_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\incremental\incremental.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\incremental\incremental_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\materialized\materialized.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\materialized\materialized_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\replicate\replicate.go` (Go runtime and compilation overhead)
  - `git-sync\internal\strategy\replicate\replicate_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\auth_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\benchmark_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\empty_scope_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\empty_source.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\empty_source_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\git_http_backend_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\integration_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\live_bootstrap_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\measurement.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\measurement_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\objectlimit.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\objectlimit_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\progress.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\progress_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\ssh_docker_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\ssh_integration_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\stats.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\syncer.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\syncer_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncer\throughput_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncertest\configguard.go` (Go runtime and compilation overhead)
  - `git-sync\internal\syncertest\repo.go` (Go runtime and compilation overhead)
  - `git-sync\internal\useragent\useragent.go` (Go runtime and compilation overhead)
  - `git-sync\internal\useragent\useragent_test.go` (Go runtime and compilation overhead)
  - `git-sync\internal\validation\validation.go` (Go runtime and compilation overhead)
  - `git-sync\internal\validation\validation_test.go` (Go runtime and compilation overhead)
  - `git-sync\unstable\client.go` (Go runtime and compilation overhead)
  - `git-sync\unstable\client_test.go` (Go runtime and compilation overhead)
  - `git-sync\unstable\doc.go` (Go runtime and compilation overhead)
```
**Action Required:** Consolidate logic into standard library, FastAPI, or Pydantic.

### Dependency & Supply Chain Budget

#### ✅ Runtime Dependency Budget

**Details:**
```text
Active runtime dependencies: 8/8 (within budget).
```

#### ✅ Heavyweight / Daemon Proscription

**Details:**
```text
Zero heavyweight (PyTorch/Spark) or broker (Celery/Kafka) deps.
```

#### ✅ Deterministic uv.lock File

**Details:**
```text
uv.lock is present and non-empty (436 KB).
```

### Agent Plugin & Skill Hygiene

#### ✅ Enterprise Cloud Skill Pollution

**Details:**
```text
Clean workspace skills (9 domain skills, zero cloud).
```

#### ✅ Essential EthoPipe Skills

**Details:**
```text
Core agent skills (code-quality, companion, handoff) present.
```

### Architectural Simplicity & Cognitive Budget

#### ✅ Infrastructure Overhead

**Details:**
```text
Zero enterprise Kubernetes/Helm/Terraform infrastructure bloat.
```

#### ✅ Single-File Cognitive Limit (< 600 lines)

**Details:**
```text
All files in `src/` are bounded under 600 lines.
```

### Toolchain Consolidation

#### ✅ Linter & Formatter Consolidation

**Details:**
```text
Toolchain cleanly consolidated on Ruff (replaces black, isort).
```

#### ✅ Single-Command QA Pipeline

**Details:**
```text
Runner `scripts/run_qa.ps1` configured for zero-friction audit.
```

---

## The 5 Invariants of the Solo Maintainer Charter

1. **Language Monoculture**: 100% Python (>= 3.11). Zero secondary compiled or JavaScript runtimes.
2. **Strict Dependency Budget**: Maximum 8 runtime packages in `pyproject.toml`. No heavy AI or broker daemons.
3. **Skill & Plugin Cleanliness**: Zero out-of-scope enterprise cloud skills (GCP, BigQuery, Airflow, Spark).
4. **Architectural Simplicity**: Pure modular Python. Files bounded under 600 lines. Single Docker container.
5. **Unified Toolchain**: Exclusively `uv`, `ruff`, `mypy`, `pytest` with a single-command QA script (`run_qa.ps1`).
