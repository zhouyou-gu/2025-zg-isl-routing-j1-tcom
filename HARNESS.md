# Workspace Harness

This file is the reusable playbook for operating in this workspace. It captures generalized workflow and user preferences that should remain useful across multiple tasks. It is not the live task log.

## Standard Operating Loop

1. Read `AGENT.md`, then `HARNESS.md`, then `PROGRESS.md`.
2. Identify the single reviewer comment or concrete revision step currently in scope.
3. Read the corresponding manuscript section and response-letter section before editing.
4. Refine the argument first if the claim is weak or the user has challenged the framing.
5. Edit the manuscript and response letter in sync.
6. Validate the result against the checklist below.
7. Update `PROGRESS.md` for the concrete state change.
8. Update `HARNESS.md` only if the interaction revealed a reusable preference or workflow rule.
9. Stop and wait for user satisfaction before advancing to the next reviewer comment.
10. If the user rejects the current addressment or asks to restart from a comment, reset scope to that comment and do not treat later items as approved.

## Control-File Maintenance

- Keep `PROGRESS.md` factual, compressed, and current.
- Record only durable outcomes plus the minimum rejected history needed to explain the accepted direction.
- Move reusable workflow and generalized user intent into `HARNESS.md`, not `PROGRESS.md`.
- Avoid duplicating the same rule across multiple sections unless the duplication is operationally necessary.

## Per-Comment Workflow Checklist

- Confirm the current target comment from `PROGRESS.md`.
- Read the relevant `main.tex` and `response_letter_TCOM_RV1.tex` sections directly from file.
- Identify whether the step is:
  - manuscript-only refinement
  - response-letter-only refinement
  - synchronized manuscript/response update
  - review/check without edits
- If the user says they made minor changes or asks to double-check again, re-read both files and verify title, notation, citations, and quoted text directly from file.
- If the argument is weak, interact to refine the key points before rewriting.
- Keep the manuscript body concise; shorten the body first, and move detailed extension material to the appendix only if it is still needed.
- Keep notation aligned with the existing paper and avoid symbol/index collisions.
- Avoid referencing symbols before they are defined.
- Add supporting citations inline where claims are made.
- If a coarse approximation is technically weak or user-rejected, prefer an explicit scope limitation plus a principled future-work extension.

## Synchronization Checklist

- `main.tex` and `response_letter_TCOM_RV1.tex` make the same technical claim.
- Scope limitations in the response letter match the manuscript wording and tone.
- Once a revision is actually present in the files, phrase the response letter as completed work rather than future planned work.
- Any quoted manuscript change in the response letter must be copied verbatim from the latest manuscript text, including the final `\blue{...}` wording and citations.
- If a later comment revises a manuscript passage that was already quoted or summarized in an earlier response-letter block, revisit the earlier block and resynchronize it to the latest manuscript text before treating either comment as stable.
- Citations used to support new claims are present where needed.
- Added terminology and notation are consistent across manuscript and response letter.

## Validation Checklist

- The revised argument is technically honest and does not overclaim.
- New appendix content is checked for notation consistency.
- New appendix content is checked for likely PDF issues such as overfull lines or awkward paragraph endings.
- The current comment is satisfactory before moving to the next one.

## Handoff Checklist

- `PROGRESS.md` reflects the latest concrete state of work.
- The current reviewer-comment status is accurate.
- The next safe resume point is explicit.
- Any newly inferred reusable preference has been moved into `HARNESS.md`.
- No temporary assumption is left undocumented if it affects the next agent.

## Compact Per-Comment Template

Use this as a mental or written template when handling a comment:

- Target comment:
- Goal of this step:
- Manuscript action:
- Response-letter action:
- Validation performed:
- `PROGRESS.md` updates required:
- Wait condition before next comment:

## Inferred Generic User Intent and Reusable Preferences

- Handle one reviewer comment at a time.
- Do not move to the next comment until the user confirms satisfaction with the current one.
- If the user rejects an addressment or asks to restart from a comment, resume from that comment.
- If a reviewer comment requires additional simulation results and the user chooses to defer it, mark that comment as deferred, keep it out of the approved set, and move to the next comment that can be addressed without those simulations.
- Prefer technically honest scope limitations over weak defenses.
- If a claim feels shaky, refine the key points interactively before rewriting.
- Keep the control files low entropy: durable outcomes in `PROGRESS.md`, reusable guidance in `HARNESS.md`.
- Keep quoted `\blue{...}` text verbatim between manuscript and response letter.
- When quoting manuscript text in the response letter, omit non-blue surrounding text unless it is needed for meaning, location, or a displayed block that would otherwise become unclear.
- When a quoted manuscript excerpt omits preceding text, begin the retained quote with `\dots` to mark the omission explicitly.
- In `main.tex`, highlight substantive manuscript revisions in `\blue{...}` by default; leave grammar-only or typo-only fixes unhighlighted unless the user asks otherwise.
- Re-check directly from file after user edits or repeated requests to double-check.
- Keep notation aligned with the existing paper and avoid index conflicts.
- Avoid reusing the same symbol for semantically different roles in proofs, such as using a commodity count and a decision threshold with the same letter.
- Avoid referencing symbols before they are defined.
- Add supporting references inline where claims are made.
- Prefer formal prose in manuscript proofs and avoid directional shorthand such as `($\Rightarrow$)` and `($\Leftarrow$)` when plain language is clearer.
- Check new appendix material for likely render/layout issues.
- Use title case for a formal problem name only where it functions as a formal heading, definition label, or exact name introduction; in ordinary prose, prefer lowercase phrasing plus the acronym when needed.
- In the response letter, prefer plain text or `\textbf{...}` labels over `\textit{...}` or `\emph{...}` unless italic emphasis is genuinely necessary.
- In response-letter prose, lead with the mathematical reasoning or writing principle behind a revision before enumerating the concrete manuscript edits.
- In completed response-letter sections, describe manuscript changes in past tense rather than present tense.
- When a reviewer questions a proof or claim, explain the mathematical standard being enforced and why the revised statement is the correct one, rather than mainly narrating what text was moved or added.
- In both manuscript prose and response-letter prose, avoid `:` by default. Prefer full sentences, commas, or a separate lead-in sentence unless a colon is genuinely necessary for a formal label, a definition, a list, or displayed material.
