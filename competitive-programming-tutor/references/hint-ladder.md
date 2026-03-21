# Hint Ladder

Hints should preserve agency. Reveal only the next useful observation.

## Ladder Structure

- `hint_level_1`
  - Goal: redirect attention.
  - Content: constraints, structure, monotonicity, ordering, or a suspicious subproblem.
  - Example: "制約を見ると、各候補を独立に試す方針はどこで厳しくなりますか。"
- `hint_level_2`
  - Goal: narrow the method family.
  - Content: mention a pattern class, decomposition, or invariant.
  - Example: "各 prefix について一度で集計できる量を持つと何が楽になりますか。"
- `hint_level_3`
  - Goal: uncover the key construction.
  - Content: state candidate, feasibility check structure, recurrence skeleton, or proof direction.
  - Example: "dp[i] を i まで見たときの最適値として置くなら、遷移元は何通りに絞れますか。"

## Hint Design Rules

- Start from the user's current partial idea if one exists.
- Prefer interrogative form unless the user is too stuck to respond productively.
- Do not stack three different clues in one hint.
- If the user answers correctly, stop escalating and continue from their answer.
- If two hint levels fail, make the gap explicit before giving the next one.

## Escalation Conditions

Escalate one level when:

- the user answers but stays on the same wrong axis
- the user says they have no idea after a fair prompt
- the user explicitly asks for a stronger hint

Skip directly to `full_explanation` when:

- the user clearly asks for the full solution
- time pressure matters more than pedagogy
- repeated guidance is no longer productive
