---
name: ai-ml-paper-production
description: Turn AI/ML research outputs into a conference-ready paper package with claim-evidence mapping, venue-aware structure, figure planning, reproducibility materials, artifact packaging, and rebuttal drafting. Use when the user is drafting a paper, tightening contributions, preparing a submission checklist, assembling appendices or artifact docs, or responding to reviews.
---

# AI/ML Paper Production

Convert a finished or half-finished project into a submission package whose claims, figures, and reproducibility materials line up.

## Workflow

1. Inventory claims before writing prose.
   - Core contribution.
   - Evidence required for each claim.
   - Limits and non-claims.
2. Lock the venue constraints.
   - Latest CFP or author instructions.
   - Page limits and appendix rules.
   - Anonymization, checklist, and artifact requirements.
3. Build the paper around figures and tables.
   - One key figure per major claim.
   - A result without an interpretation note is incomplete.
4. Draft sections in dependency order.
   - Contributions and claim scope.
   - Method.
   - Experimental setup.
   - Results and failure cases.
   - Limitations.
5. Prepare the submission package.
   - Checklist answers.
   - Appendix.
   - Reproducibility details.
   - Artifact or code-release notes.
6. Handle reviews by resolving concerns, not arguing past them.

## Writing Rules

- Map every strong claim to an explicit figure, table, theorem, or ablation.
- Keep "why this matters" separate from "what number improved".
- State the boundary of the result when there is a known failure mode.
- Check current venue rules every time; do not rely on last year's template or limits.

## Rebuttal Rules

- Start with the reviewer concern, not the defense.
- Clarify misunderstandings plainly.
- Offer additional analysis only if it is feasible and decision-relevant.
- Narrow the claim when the evidence is weaker than the wording.

## Output Contract

Return one or more of:

- `claim_map`: claims to required evidence
- `paper_outline`: venue-aware section plan
- `submission_gap_list`: what is missing before submission
- `rebuttal_draft`: concern-by-concern response plan

## References

- Use `references/submission-playbook.md` for the section checklist, submission-week checklist, and rebuttal template.
