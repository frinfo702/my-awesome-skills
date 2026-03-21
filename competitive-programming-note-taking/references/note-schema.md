# Note Schema

Use this schema for `note_entry`. Omit fields only when the input is missing and the value cannot be inferred safely.

## Core Metadata

- `problem_name`: official title if available
- `source`: contest or platform
- `date`: note creation date or solve date
- `url`: canonical problem URL
- `difficulty`: stated or estimated
- `solved_independently`: `yes`, `partial`, or `no`
- `time_spent_min`: total time before accepted solution or abandonment
- `submission_result`: `ac`, `wa`, `tle`, `mle`, `re`, `ce`, `unsolved`, or a short sequence like `wa x2 -> ac`

## Retrieval Tags

- `topic_tags`: domain tags such as graph, dp, data-structure
- `pattern_tags`: reusable ideas such as cumulative-sum, binary-search-on-answer, rerooting
- `failure_tags`: stable failure-pattern names from `references/tag-taxonomy.md`
- `constraint_scale`: summarize `N`, value range, query count, and whether the accepted idea is linear, n log n, quadratic, or another bound

## Problem Compression

- `problem_summary`: 2 to 4 sentences; describe the task and the decisive structure
- `one_thing_to_remember`: one sentence; the single recall target for later review
- `why_this_problem_matters`: one sentence; what this problem was meant to train

## Attempt Timeline

- `first_plan`: the user's first serious approach
- `wrong_hypotheses`: short list of incorrect assumptions or dead ends
- `stuck_point`: where progress stopped
- `breakthrough_trigger`: what changed the user's view
- `mistake_type`: short plain-language summary such as "state definition too vague" or "missed monotonicity"

## Solution Capture

- `final_solution`: 2 to 5 sentences; core approach and reason it fits the constraints
- `alternative_solutions`: optional; include only if pedagogically useful
- `implementation_pitfalls`: short list of code-level hazards

## Reflection

- `learning`: 1 to 3 bullets or sentences; transferable lessons
- `next_time_warning`: imperative one-liner beginning with a verb
- `review_trigger`: optional; a future cue such as "revisit before tree DP set" or "review after next binary search miss"

## Filling Rules

- Prefer the user's own words for `first_plan`, `wrong_hypotheses`, and `stuck_point`.
- Compress long explanations aggressively.
- Distinguish algorithm failure from implementation failure.
- If the user solved it quickly with no real struggle, keep the reflection short and record the main idea plus one recall point.
