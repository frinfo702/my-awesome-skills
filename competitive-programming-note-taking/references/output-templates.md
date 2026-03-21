# Output Templates

Use these templates unless the user explicitly asks for another format.

## Default Compact Format

```markdown
`note_entry`
- `problem_name`:
- `source`:
- `date`:
- `url`:
- `difficulty`:
- `solved_independently`:
- `time_spent_min`:
- `submission_result`:
- `topic_tags`:
- `pattern_tags`:
- `failure_tags`:
- `constraint_scale`:
- `problem_summary`:
- `one_thing_to_remember`:
- `why_this_problem_matters`:
- `first_plan`:
- `wrong_hypotheses`:
- `stuck_point`:
- `breakthrough_trigger`:
- `mistake_type`:
- `final_solution`:
- `alternative_solutions`:
- `implementation_pitfalls`:
- `learning`:
- `next_time_warning`:
- `review_trigger`:

`review_card`
- `core_idea`:
- `failure_point`:
- `recall_check`:
- `next_time_warning`:

`weakness_update`
- `reinforced_patterns`:
- `evidence_from_this_problem`:

`similar_problem_cues`
- `constraint_similarity`:
- `idea_similarity`:
- `failure_similarity`:
- `implementation_similarity`:
```

## Weakness Summary Format

Use this when the user asks for a cross-problem weakness view.

```markdown
`weakness_summary`
- `theme`:
- `symptom`:
- `evidence`:
- `training_focus`:
- `next_problem_filter`:
```

## Related Candidate Format

Use this only when real candidates are present in the current corpus or context.

```markdown
`related_problem_candidates`
- `problem`:
  - `why_similar`:
  - `what_to_compare`:
```

If no grounded candidate exists, return retrieval cues instead of inventing examples.
