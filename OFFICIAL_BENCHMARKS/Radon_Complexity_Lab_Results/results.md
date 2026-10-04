# Radon_Complexity_Lab_Results
**Project:** `L_REEF` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 3.6875}`
- **complexity_grade:** `A`
- **complexity_score:** `3.6875`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_REEF\UPSTREAM\test_watchdog_hang.py - A (70.05)
E:\fenta\Down`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_REEF\UPSTREAM\test_watchdog_hang.py
    F 29:0 test_watchdog_detection - A (2)
    F 84:0 main - A (2)
    F 22:0 blocking_operation - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_REEF\UPSTREAM\alembic\env.py
    F 46:0 run_migrations_offline - A (1)
    F 70:0 run_migrations_online - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_REEF\UPSTREAM\letta\agent.py
    M 445:4 Agent._handle_ai_response - E (39)
    M 300:4 Agent._get_ai_reply - E (33)
    M 857:4 Agent.inner_step - D (28)
    M 1434:4 Agent.get_context_window_from_anthropic_async - D (24)
    M 1307:4 Agent.get_context_window_from_tiktoken_async - D (21)
    M 1598:4 Agent.execute_tool_and_persist_state - C (18)
    M 1204:4 Agent.get_context_window - C (14)
    M 753:4 Agent.step - C (13)
    C 96:0 Agent - C (12)
    M 97:4 Agent.__init__ - B (8)
    M 176:4 Agent.load_last_function_response - B (8)
    M 277:4 Agent._runtime_override_tool_json_schema - B (7)
    M 1107:4 Agent.summarize_messages_inplace - B (6)
    F 1706:0 save_agent - A (5)
    M 200:4 Agent.update_memory_if_changed - A (5)
    M 191:4 Agent.ensure_read_only_block_not_modified - A (4)
    M 1074:4 Agent.step_user_message - A (3)
    M 1302:4 Agent.get_context_window_async - A (3)
    F 1734:0 strip_name_field_from_user_message - A (2)
    F 1750:0 validate_json - A (2)
    C 79:0 BaseAgent - A (2)
    M 236:4 Agent._handle_function_error_response -
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_