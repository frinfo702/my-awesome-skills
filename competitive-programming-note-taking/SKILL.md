---
name: competitive-programming-note-taking
description: Use when the user wants to turn a competitive programming problem attempt into reusable review notes from a problem statement, URL, constraints, submission result, code, editorial, and the user's thinking process. Do not use for merely solving a new problem, debugging a submission without note-taking, or building a full problem archive. Produces a compact structured note, review card, weakness tags, and similar-problem retrieval cues.
---

# Competitive Programming Note Taking

Convert one solved or attempted problem into a review artifact that is easy to search later: what the problem was meant to teach, where the user got stuck, and what to watch next time.

## Workflow

1. Gather the minimum usable inputs.
   - Require a problem statement or a reliable summary, the problem URL, constraints, submission result, final code or final approach, editorial or accepted idea, and the user's thought process.
   - Prefer completing a partial note over blocking on missing details.
2. Reconstruct the attempt timeline.
   - Extract the first plan, wrong hypotheses, exact stuck point, breakthrough trigger, and final correction.
   - Mark any inferred step explicitly when the user did not state it.
3. Normalize the problem.
   - Write a short problem summary instead of copying the statement.
   - Record the constraint scale and the decisive observation.
   - Assign stable tags from `references/tag-taxonomy.md`.
4. Emphasize what should be learned.
   - Separate the core idea from the implementation pitfall.
   - State why this problem is worth revisiting.
   - Write `next_time_warning` as one short imperative sentence.
5. Return the note package.
   - Always return `note_entry`, `review_card`, `weakness_update`, and `similar_problem_cues`.
   - Return `related_problem_candidates` only when actual candidates are available from the current context or a provided corpus.

## Compression Rules

- Keep the note compact. Do not paste the full statement, full editorial, or full code unless the user asks.
- Summarize the user's thought log into decision points, not a diary.
- Keep each field to one or two sentences unless the schema explicitly allows a list.
- Optimize for later retrieval. A short precise tag is more valuable than a long explanation.

## Quality Bar

- Identify what skill the problem was supposed to train.
- Preserve the user's failure mode, not only the accepted solution.
- Prefer stable tags and mistake names over ad hoc phrasing.
- If the attempt contains no meaningful struggle, say so instead of inventing one.
- If similarity search is requested without a searchable corpus, return retrieval cues rather than fabricated problem names.

## Trigger Examples

Use when:
- "この問題の反省ノートを作って"
- "提出コードと解説から復習カード化して"
- "何を学ぶ問題だったか残したい"
- "同じミスをした問題を後で引ける形にしたい"

Do not use when:
- "この問題を解いて"
- "WA の原因だけ特定して"
- "おすすめの問題を出して"
- "問題文を日本語訳して"

## Output Contract

Return in this order:

- `note_entry`: follow `references/note-schema.md`
- `review_card`: one-screen review card
- `weakness_update`: cross-problem tendencies reinforced by this attempt
- `similar_problem_cues`: retrieval axes for later search
- `related_problem_candidates`: optional, only when grounded in actual candidates

## References

- Use `references/note-schema.md` for the field schema and fill rules.
- Use `references/tag-taxonomy.md` for normalized tags and failure-pattern naming.
- Use `references/output-templates.md` for compact output formats.
