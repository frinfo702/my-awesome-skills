# Tag Taxonomy

Use stable tags so later search is reliable. Prefer a small controlled vocabulary over free-form tags.

## Topic Tags

- `array`
- `string`
- `math`
- `greedy`
- `binary-search`
- `two-pointers`
- `cumulative-sum`
- `difference-array`
- `sorting`
- `graph`
- `tree`
- `shortest-path`
- `union-find`
- `topological-sort`
- `dp`
- `bit-dp`
- `tree-dp`
- `digit-dp`
- `data-structure`
- `segment-tree`
- `fenwick-tree`
- `heap`
- `set-map`
- `combinatorics`
- `number-theory`
- `geometry`
- `simulation`

## Pattern Tags

- `constraint-drives-solution`
- `monotonicity`
- `binary-search-on-answer`
- `prefix-aggregation`
- `offline-processing`
- `coordinate-compression`
- `state-definition`
- `transition-design`
- `case-splitting`
- `invariant-maintenance`
- `root-fixing`
- `rerooting`
- `small-to-large`
- `meet-in-the-middle`
- `modular-counting`
- `parity-observation`
- `reverse-thinking`
- `constructive-greedy`

## Failure Tags

- `missed-constraint-signal`
- `complexity-underestimate`
- `wrong-monotonicity-assumption`
- `state-definition-too-vague`
- `transition-missing-case`
- `greedy-without-proof`
- `implementation-bug-off-by-one`
- `implementation-bug-indexing`
- `overflow-risk`
- `forgot-initialization`
- `double-counting`
- `tree-root-dependence-overlooked`
- `prefix-sum-but-no-search-combination`
- `binary-search-without-feasibility-design`
- `editorial-gap-could-not-bridge`

## Similarity Axes

Use these axes for `similar_problem_cues`.

- `constraint_similarity`: same order of growth, same bottleneck, same accepted complexity class
- `idea_similarity`: same decisive observation or reduction
- `failure_similarity`: same failure tag or same stuck pattern
- `implementation_similarity`: same source of bugs or edge-case handling burden

## Tagging Rules

- Assign 2 to 4 `topic_tags`.
- Assign 1 to 3 `pattern_tags`.
- Assign 0 to 3 `failure_tags`.
- Prefer existing tags. Add a new tag only when the current list clearly fails to capture an important repeated pattern.
- When two tags overlap, choose the narrower one only if it improves later retrieval.
