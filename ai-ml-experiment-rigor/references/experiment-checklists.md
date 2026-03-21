# Experiment Checklists

## Experiment Spec Template

Fill this before large runs:

1. Claim
   - One sentence.
2. Dataset
   - Source.
   - Version.
   - Split logic.
   - License or usage constraint.
3. Baselines
   - Name.
   - Implementation source.
   - Any approximation or deviation.
4. Metrics
   - Primary metric.
   - Secondary metrics.
   - Failure metric.
5. Search plan
   - Tuned parameters.
   - Search ranges.
   - Number of trials.
6. Logging
   - Config snapshot.
   - Metrics.
   - Checkpoints.
   - Code revision.
7. Reproducibility
   - Seeds.
   - Environment lock.
   - Determinism notes.

## Run Checklist

- Config committed before launch.
- Dataset path and version recorded.
- Seed policy documented.
- Evaluation script separated from training script.
- Output directory structure fixed in advance.
- Run names carry enough metadata to compare later.

## Common Failure Modes

- Data leakage from preprocessing before split.
- Reporting only the best seed.
- Mixing search budget between methods.
- Changing preprocessing mid-project without rerunning baselines.
- Forgetting to record pretrained checkpoint origin.
- Discovering after submission week that a result cannot be regenerated.
