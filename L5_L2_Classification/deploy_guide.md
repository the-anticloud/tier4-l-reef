# Deploy Guide — L_REEF
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, PyTorch 2.10+, RLHF/RLAIF framework, PAX 27B, sandbox executor, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, trl 0.8+ (PPO), sandboxed Python executor, PAX 27B.

## Environment
80GB VRAM for training (A100). T4 for evaluation/inference only. 128GB RAM for training.

## AIOSS Integration
```bash
aioss init --module L_REEF --output ./l_reef.aioss
aioss append --chain ./l_reef.aioss --payload ./output.bin --module L_REEF
aioss verify --chain ./l_reef.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_REEF",
    aioss_chain="./L_REEF.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_REEF.aioss --verbose
python -m L_REEF.tests.smoke
```
