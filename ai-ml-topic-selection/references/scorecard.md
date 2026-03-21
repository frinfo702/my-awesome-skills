# Topic Scorecard

Use 0-5 scores. Require one sentence of evidence for each score.

## Rubric

| Criterion | What to ask | 0-1 | 2-3 | 4-5 |
| --- | --- | --- | --- | --- |
| Impact | If this works, who cares and what changes? | No clear user or community | Useful but narrow | Important and legible to a target venue |
| Novelty | What is genuinely different from close prior work? | Mostly a rebranding | Some real variation | Clear mechanism, setting, or insight gap |
| Feasibility | Can a pilot succeed in 8-12 weeks? | Blocked by unknowns | Possible with risk | Straight path to first result |
| Resource fit | Do data and compute exist now? | Missing essentials | Partial access | Fully available |
| Advisor fit | Can the lab give useful feedback fast? | Weak fit | Moderate fit | Strong fit |
| Evaluation clarity | Are metrics, baselines, and datasets obvious? | Unclear | Partly defined | Clear and testable |

## 1-Page Problem Statement

Fill these sections in order:

1. Problem
   - One paragraph on the task and why current practice is insufficient.
2. Hypothesis
   - One sentence: "If we change `X`, metric `Y` should improve because `Z`."
3. Scope
   - What is in scope, what is not, and what the pilot will not claim.
4. Evaluation
   - Dataset or benchmark.
   - Metrics.
   - Minimum baselines.
   - Required ablations.
5. Resources
   - Compute budget.
   - Data access.
   - Existing code or models to build on.
6. Risks
   - Technical failure mode.
   - Resource failure mode.
   - Ethics or data-use concern.

## Pilot Feasibility Checklist

- Baseline can be reproduced or approximated in 2 weeks.
- At least one public dataset or benchmark is available now.
- The main metric is standard enough that reviewers will recognize it.
- The first experiment can run on available hardware.
- The idea still teaches something useful if it fails.
