---
name: ai-ml-literature-review
description: Run AI/ML literature review workflows using fast screening, Keshav-style 3-pass reading, paper note templates, and related-work mapping. Use when the user needs to survey a topic, build a reading list, compare papers, extract a research gap, or turn many papers into a structured related-work section.
---

# AI/ML Literature Review

Move from a vague topic to a defendable map of what is known, what is missing, and which papers actually matter.

## Workflow

1. Start from a sharp question, not a keyword pile.
   - Task or phenomenon.
   - Target setting.
   - Likely evaluation axis.
2. Build a seed set.
   - Canonical papers.
   - Recent papers from the target venue family.
   - One or two survey papers only if they accelerate orientation.
3. Screen quickly with pass 1.
   - Title, abstract, figures, intro, conclusion.
   - Keep, maybe, or drop.
4. Deepen with pass 2 and pass 3 only on papers that matter.
   - Extract assumptions, method category, supervision signal, datasets, metrics, and major weaknesses.
   - Trace citation links only when they change the decision.
5. Convert notes into a map.
   - Group by approach family or failure mode, not by publication year alone.
   - End with a one-paragraph gap statement.

## Review Rules

- Prefer primary papers over summaries when making technical claims.
- Track what each paper assumes about data scale, model size, and compute.
- Record negative evidence and limitations, not only wins.
- Stop reading breadth-first when the same idea repeats; switch to synthesis.

## Output Contract

Return one or more of:

- `screening_table`: papers, keep/drop decision, and why
- `deep_notes`: structured notes for the key papers
- `related_work_map`: clusters, representative papers, and fault lines
- `gap_statement`: the unresolved problem the user should work on next

## References

- Use `references/review-workflow.md` for the 3-pass template, note schema, and related-work matrix.
