# Output Templates

Use these response structures unless the user asks for another format.

## Default Tutoring Format

```markdown
`diagnosis`
- `primary_bottleneck`:
- `evidence`:
- `secondary_bottleneck`:

`guided_response`
- `hint_level_1`:
- `hint_level_2`:
- `hint_level_3`:
- `next_question`:

`reasoning_explanation`
- `why_natural_wrong_approach_fails`:
- `why_this_approach_fits`:
- `correctness_core`:
- `complexity_check`:

`feedback`
- `label`:
- `what_was_off`:
- `what_was_correct`:
- `correction`:

`study_plan`
- `next_difficulty`:
- `review_patterns`:
- `avoid_for_now`:
- `next_action`:

`review_prompt`
- `recall_question`:
- `replay_target`:
```

## Hint-Only Format

Use when the user wants only guidance and does not want explanation yet.

```markdown
`diagnosis`
- `primary_bottleneck`:
- `evidence`:

`guided_response`
- `hint_level_1`:
- `hint_level_2`:
- `hint_level_3`:
- `stop_here_if_you_want_to_think`:
```

## Post-Mortem Format

Use when the user already attempted and wants critique.

```markdown
`diagnosis`
- `primary_bottleneck`:
- `evidence`:

`feedback`
- `label`:
- `what_was_off`:
- `what_was_correct`:
- `correction`:

`study_plan`
- `review_patterns`:
- `next_action`:
```
