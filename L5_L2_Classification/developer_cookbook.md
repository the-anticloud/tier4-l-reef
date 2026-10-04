# Developer Cookbook — L_REEF
**Stack:** Python 3.11, PyTorch 2.10+, RLHF/RLAIF framework, PAX 27B, sandbox executor, AIOSS_FORMAT
**Domain:** REEF: reinforcement learning from execution feedback for PAX 27B code generation improvement

## Run REEF training loop
```python
from l_reef import REEFTrainer

trainer = REEFTrainer(
    pax_model="./pax-27b-fp16.safetensors",
    output_dir="./reef_checkpoints/",
    aioss_chain="./reef.aioss"
)

# Define code execution reward
def code_reward(generated_code: str) -> float:
    # Execute in sandbox, return 1.0 if tests pass, 0.0 if fail
    result = trainer.sandbox_execute(generated_code, test_suite="anticloud_tests")
    return 1.0 if result.all_tests_passed else 0.0

trainer.train(
    prompts_dataset="./anticloud_code_prompts.jsonl",
    reward_fn=code_reward,
    n_episodes=1000,
    ppo_epochs=4
)
```

## Evaluate improvement
```python
eval_result = trainer.evaluate(
    checkpoint="./reef_checkpoints/step_1000/",
    benchmark="anticloud_coding_bench"
)
print(f"Pass@1: {eval_result.pass_at_1:.2f} (baseline: {eval_result.baseline:.2f})")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
