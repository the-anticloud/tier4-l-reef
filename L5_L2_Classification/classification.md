# L5 Narrow / L2 General Classification — L_REEF
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_REEF implements reinforcement learning from execution feedback for PAX 27B code generation. Narrow scope: improving PAX 27B's code generation quality for the Anticloud codebase. Reward signal: whether generated code passes tests and AIOSS integration is correct.

## L2 General
L2 General: L_REEF continuously improves PAX 27B's code generation quality for all tiers. Better Anticloud code generation benefits TIER_3 API projects, TIER_4 inference agents, and all other tiers equally.

## PAX 27B Integration
PAX 27B is both the policy being improved and the inference engine. L_REEF samples PAX code outputs, executes them in a sandbox, collects pass/fail feedback, and updates PAX's generation behavior via PPO.

## AIOSS Audit Chain
Every RL training step (prompt hash + generated code hash + execution result + reward + policy update hash) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST SSDF (secure development with ML-generated code). ISO/IEC 42001 (AI system improvement).
