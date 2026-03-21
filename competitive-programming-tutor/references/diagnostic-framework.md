# Diagnostic Framework

Diagnose the learner before teaching. Pick the narrowest category that explains the current stall.

## Bottleneck Categories

- `problem-interpretation`
  - Symptom: misreads the task, objective, or operation semantics.
  - Typical evidence: solves a different problem than stated or ignores a condition.
- `constraint-analysis`
  - Symptom: does not convert constraints into allowed complexity.
  - Typical evidence: proposes quadratic search for `N=2e5`.
- `pattern-recall`
  - Symptom: knows local facts but does not retrieve the right method family.
  - Typical evidence: misses cumulative sum, binary search on answer, tree DP, or union-find cues.
- `modeling`
  - Symptom: cannot choose state, invariant, order, or decomposition.
  - Typical evidence: "DP っぽい" までは行くが state が置けない。
- `proof`
  - Symptom: has a candidate method but cannot justify correctness.
  - Typical evidence: greedy choice is asserted without exchange or invariant reasoning.
- `implementation`
  - Symptom: approach is acceptable but code breaks on details.
  - Typical evidence: off-by-one, indexing, initialization, overflow, corner cases.
- `review-habit`
  - Symptom: repeats similar mistakes because the reflection loop is weak.
  - Typical evidence: same failure tag across multiple attempts.

## Feedback Labels

Use one or more of these in `feedback`.

- `missed-problem-condition`
- `missed-constraint-signal`
- `typical-pattern-not-recalled`
- `state-definition-missing`
- `proof-gap`
- `boundary-case-bug`
- `complexity-overrun`
- `implementation-detail-slip`

## Diagnostic Questions

Choose the smallest next question that disambiguates the bottleneck.

- For `problem-interpretation`: "この問題で最終的に求める量を一文で言えますか"
- For `constraint-analysis`: "この制約だと何オーダーまで許せますか"
- For `pattern-recall`: "同じ制約でまず疑う典型は何ですか"
- For `modeling`: "状態や順序を固定すると何が残りますか"
- For `proof`: "その選択が常に損しない理由を言えますか"
- For `implementation`: "壊れやすい境界ケースを三つ挙げられますか"

## Diagnostic Rules

- Prefer evidence from the user's own words over your guess.
- If multiple bottlenecks appear, pick the earliest upstream one.
- Do not label an implementation issue when the algorithm itself is still wrong.
- If the user already knows the pattern name, investigate modeling or proof instead of repeating the name.
