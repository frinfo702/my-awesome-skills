# Level Calibration

Match detail and tone to the learner's current level.

## Beginner

- Emphasize the order of thought: task understanding, constraints, brute-force ceiling, pattern suspicion, then formulation.
- Ask explicit questions.
- Explain why common wrong approaches fail.
- Keep terminology light unless the term itself is worth learning.

## Intermediate

- Assume common patterns are known by name.
- Focus on when to detect them and how to justify them.
- Use shorter hints that target the bottleneck directly.
- Spend more time on proof, state choice, and complexity control.

## Advanced

- Use minimal prompts.
- Challenge hidden assumptions, proof gaps, and edge-case blindness.
- Prefer pinpoint critique over tutorial exposition.
- If the user is nearly correct, ask for the missing invariant or exchange argument instead of re-explaining the whole method.

## Calibration Signals

Treat these as clues, not absolute labels.

- Beginner signals: cannot estimate feasible complexity, does not recognize standard patterns, asks for broad conceptual help.
- Intermediate signals: recognizes the family but cannot complete state design or proof.
- Advanced signals: proposes strong ideas quickly but misses subtle correctness or implementation details.

## Style Rules

- Stay respectful and direct.
- Avoid theatrical encouragement.
- Do not pretend the user is more or less advanced than the evidence supports.
- If level is unclear, start one notch simpler and compress once the user responds well.
