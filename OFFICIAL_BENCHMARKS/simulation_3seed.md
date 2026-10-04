# 3-Seed Simulation — L_REEF

**Seeds:** `53827` · `85164` · `19363`

**Seed method:** `sha256("L_REEF")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_REEF`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.987 | 0.1103 | ±0.2162 |
| throughput_tokens_per_sec | 232.2 | 33.3336 | ±65.3339 |
| p50_latency_ms | 45.62 | 4.4566 | ±8.7349 |
| p99_latency_ms | 117.7233 | 12.6494 | ±24.7928 |
| ttft_ms | 29.8467 | 4.5251 | ±8.8692 |
| mmlu_proxy | 0.6967 | 0.0261 | ±0.0512 |
| hellaswag_proxy | 0.7886 | 0.0302 | ±0.0592 |
| truthfulqa_proxy | 0.5501 | 0.0205 | ±0.0402 |
| arc_proxy | 0.6899 | 0.0388 | ±0.076 |
| complexity_cyclomatic | 4.6467 | 0.2894 | ±0.5672 |
| maintainability_index | 67.2533 | 4.1201 | ±8.0754 |
| security_issues_high | 1.0 | 0.8165 | ±1.6003 |
| dependency_freshness_pct | 73.6333 | 2.2647 | ±4.4388 |
| test_coverage_pct | 57.2333 | 3.8003 | ±7.4486 |
| doc_coverage_pct | 70.3667 | 5.9779 | ±11.7167 |
| memory_mb | 50.0 | 0.0 | ±0.0 |
| gpu_util_pct | 68.2667 | 5.0678 | ±9.9329 |
| openssf_score | 6.69 | 0.5266 | ±1.0321 |
| eu_ai_act_compliance_pct | 86.9667 | 0.7134 | ±1.3983 |
| slsa_level | 1.3333 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 53827 | Seed 85164 | Seed 19363 |
|--------|------------|------------|------------|
| trl_score | 6.894 | 6.925 | 7.142 |
| throughput_tokens_per_sec | 185.4 | 250.7 | 260.5 |
| p50_latency_ms | 51.91 | 42.13 | 42.82 |
| p99_latency_ms | 125.02 | 128.22 | 99.93 |
| ttft_ms | 32.47 | 23.48 | 33.59 |
| mmlu_proxy | 0.6783 | 0.6782 | 0.7337 |
| hellaswag_proxy | 0.8252 | 0.7894 | 0.7513 |
| truthfulqa_proxy | 0.5769 | 0.546 | 0.5273 |
| arc_proxy | 0.6352 | 0.7215 | 0.713 |
| complexity_cyclomatic | 4.89 | 4.81 | 4.24 |
| maintainability_index | 64.31 | 73.08 | 64.37 |
| security_issues_high | 0 | 2 | 1 |
| dependency_freshness_pct | 71.3 | 76.7 | 72.9 |
| test_coverage_pct | 54.8 | 54.3 | 62.6 |
| doc_coverage_pct | 71.9 | 76.8 | 62.4 |
| memory_mb | 50 | 50 | 50 |
| gpu_util_pct | 74.3 | 68.6 | 61.9 |
| openssf_score | 6.12 | 7.39 | 6.56 |
| eu_ai_act_compliance_pct | 86.0 | 87.2 | 87.7 |
| slsa_level | 1 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._