# Review Workflow

## Pass Structure

### Pass 1

Spend a few minutes per paper.

Capture:

- problem
- method family
- claimed contribution
- evaluation setting
- initial keep/drop decision

### Pass 2

Read enough to explain the paper without rereading the abstract.

Capture:

- exact task and setting
- model or algorithm sketch
- datasets and metrics
- main baselines
- strongest result
- obvious threats to validity

### Pass 3

Use only for papers central to your direction.

Capture:

- what would be hard to reproduce
- what assumptions are fragile
- which component likely carries the gain
- what follow-up experiment you would run

## Note Template

Use this schema:

| Field | Content |
| --- | --- |
| Citation | Short citation key |
| Question | What problem does the paper solve? |
| Claim | Main take-away in one sentence |
| Method | Architecture, objective, or algorithm summary |
| Evidence | Datasets, metrics, and headline result |
| Limits | Failure mode, caveat, or missing comparison |
| Relevance | Why it matters to the current project |

## Related-Work Matrix

Group papers by rows and compare with these columns:

- supervision or feedback source
- model class
- data scale
- compute scale
- core inductive bias
- benchmark family
- reproducibility status
- weakness

## Exit Criteria

Stop expanding the review when:

- the same design pattern appears repeatedly
- new papers only shift benchmark numbers
- the gap statement is specific enough to imply a pilot experiment
