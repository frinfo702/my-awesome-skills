---
name: ai-ml-topic-selection
description: Choose and scope AI/ML research topics into a tractable problem statement with explicit tradeoffs around impact, novelty, feasibility, compute, data, and advisor fit. Use when the user is exploring thesis or project ideas, comparing candidate directions, narrowing a broad theme, or turning a vague idea into a 1-page research problem and first experiment plan.
---

# AI/ML Topic Selection

Turn candidate ideas into a ranked short list and one scoped direction that can survive an 8-12 week pilot.

## Workflow

1. Capture the operating constraints before discussing novelty.
   - Time horizon: class project, semester, thesis, paper cycle.
   - Available assets: data, compute, codebase, collaborators, advisor support.
   - Target community: core ML, applied ML, multimodal, agents, efficient ML, theory-heavy ML.
2. Rewrite each idea as a concrete problem.
   - Task.
   - Input/output.
   - Success metric.
   - Minimum believable baseline.
   - Failure condition.
3. Score each direction with the rubric in `references/scorecard.md`.
   - Penalize hidden dependencies on unavailable data, compute, or domain access.
   - Separate "technically hard" from "publishable in time".
4. Force a gap statement.
   - Existing methods fail because `X`.
   - Proposed direction changes `Y`.
   - The claim is believable if experiment `Z` works.
5. Pick one pilot direction and one backup.
   - Default to the option with the best feasibility-adjusted upside, not the most ambitious headline.

## Guardrails

- Reject ideas that need a private dataset, large-scale training budget, or unclear labeling pipeline unless the user already has them.
- Do not call something novel when it is only a different benchmark or prompt phrasing without a changed mechanism or insight.
- Prefer problems with an obvious baseline reproduction path in the first two weeks.
- Surface ethics, privacy, licensing, or human-subject constraints early if the idea touches them.

## Output Contract

Return:

- `candidate_table`: 3-7 ideas with short rationale and scores
- `recommended_direction`: one primary choice and one backup
- `problem_statement`: a 1-page style outline using the template in `references/scorecard.md`
- `first_experiments`: the smallest baseline, sanity check, and kill criteria

## References

- Use `references/scorecard.md` for the scoring matrix, 1-page problem statement template, and pilot feasibility checklist.
