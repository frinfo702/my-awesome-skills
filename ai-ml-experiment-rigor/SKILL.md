---
name: ai-ml-experiment-rigor
description: Design and audit AI/ML experiments for comparability, reproducibility, and realistic compute use. Use when the user needs help defining baselines, ablations, metrics, data splits, seed handling, experiment tracking, statistical interpretation, compute budgets, or a reproducible experiment spec before running large jobs.
---

# AI/ML Experiment Rigor

Treat the experiment as a specification, not a pile of runs.

## Workflow

1. Freeze the claim.
   - What exact statement should the results support?
   - What would falsify it?
2. Define the comparison set.
   - Minimum baselines.
   - Fairness conditions.
   - Required ablations.
3. Write the experiment spec before running jobs.
   - Data splits.
   - Preprocessing.
   - Metrics.
   - Hyperparameter search space.
   - Logging and saved artifacts.
4. Budget the runs.
   - Cheap sanity checks.
   - Coarse search.
   - Final reruns with fixed settings.
5. Audit reproducibility.
   - Seeds.
   - Non-deterministic operators.
   - Dependency versions.
   - Dataset versioning.

## Defaults

- Separate pilot runs from paper runs.
- Keep one source of truth for config values.
- Log enough to reconstruct a run without guessing.
- Prefer a smaller, repeatable study over a larger but irrecoverable search.

## Statistical Guardrails

- Do not use a small p-value as a substitute for effect size or practical value.
- Report spread and uncertainty, not only the best run.
- State the unit of variation: seeds, folds, tasks, or users.
- Explain unfair comparisons when budgets or pretrained assets differ.

## Output Contract

Return one or more of:

- `experiment_spec`: ready-to-run design
- `comparison_table`: baselines, metrics, and fairness notes
- `reproducibility_risks`: likely failure points
- `compute_budget`: staged plan with must-have and optional runs

## References

- Use `references/experiment-checklists.md` for the experiment-spec template, run checklist, and common failure modes.
