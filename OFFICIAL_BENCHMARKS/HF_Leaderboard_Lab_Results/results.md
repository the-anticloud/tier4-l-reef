# HF_Leaderboard_Lab_Results

**Project:** `L_REEF`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `letta-ai/letta`  
**Commit:** ``  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **55.51 ms** |
| Min latency | 47.67 ms |
| Max latency | 67.03 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **29** |
| Tokenization latency | 2.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5775 |
| Classification latency | 74.49 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_REEF (letta-ai/letta) — 0 files, 0 source lines, licence unknown, primary language []
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'reef', '(', 'let', '##ta', '-', 'ai', '/', 'let', '##ta', ')', '—', '0', 'files', ',', '0', 'source', 'lines']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_