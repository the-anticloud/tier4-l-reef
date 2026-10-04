# Ledger Status

**Project:** `L_REEF`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `letta-ai/letta` @ `5bcdd177d70f` (Apache-2.0)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `letta-ai/letta` |
| Commit | `5bcdd177d70fa2b31a754cfcd801e77b2e1ab16a` |
| Upstream licence | Apache-2.0 |
| Licence class | permissive |
| Clone size | 0.06 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 0 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
