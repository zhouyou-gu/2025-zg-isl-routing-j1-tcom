# Workspace Harness

This file is the reusable playbook for operating in this workspace. It captures durable workflow rules and user preferences that should remain useful across multiple tasks. It is not the live task log.

## Task Context

This workspace supports technical revision work that spans multiple synchronized artifacts. The work commonly involves a primary manuscript source, a reviewer-response document, a live progress tracker, and supporting experiment or figure-generation assets. Some revisions are local to one artifact, while others must remain aligned across narrative text, quoted revisions, reproduced figures, validation outputs, and supporting code or remote execution environments.

## Standard Operating Loop

1. Read the local operating instructions and the current progress tracker first.
2. Identify the single review item or concrete revision step currently in scope.
3. Read the corresponding manuscript and response sections before editing.
4. Refine the argument first if the claim is weak or the user has challenged the framing.
5. Edit synchronized artifacts together when the change affects more than one artifact.
6. Validate the result against the checklist below before advancing.
7. Update the progress tracker for the concrete state change.
8. Update the harness only if the interaction revealed a durable reusable rule.
9. Stop and wait for user satisfaction before advancing to the next review item.
10. If the user rejects the current addressment or asks to restart from an earlier item, reset scope to that item and do not treat later items as approved.
11. If supporting code or remote repositories were involved, verify their sync state before final closeout.

## Control-File Maintenance

- Keep the progress file factual, compressed, and current.
- Record durable outcomes plus the minimum rejected history needed to explain the accepted direction.
- Keep reusable workflow and generalized user intent in the harness file, not in the progress file.
- Avoid duplicating the same rule across multiple sections unless the duplication changes behavior at a different step.

## Per-Comment Workflow Checklist

- Confirm the current target item from the progress tracker.
- Read the relevant source sections directly from file before editing.
- Identify whether the step is manuscript-only, response-only, synchronized manuscript/response, or review-only.
- If the user says they made minor changes or asks to double-check again, re-read the relevant files directly and verify title, notation, citations, figures, and quoted text from source.
- If the argument is weak, refine the key points before rewriting.
- Keep the manuscript body concise. Shorten the body first, and move extension material elsewhere only if it is still needed.
- Keep notation aligned with the existing document and avoid symbol or index collisions.
- Avoid referencing symbols before they are defined.
- Add supporting citations inline where claims are made.
- If a coarse approximation or weak defense is challenged, prefer an explicit scope limitation plus a principled future-work extension.

## Synchronization Checklist

- The manuscript and the response document make the same technical claim.
- Keep artifact-local narrative voice. The manuscript should read as a standalone paper rather than a revision record, while the response document may describe what was added, revised, or clarified.
- Once a revision is actually present in the files, phrase the response document as completed work rather than future planned work.
- Any quoted manuscript change in the response document is copied verbatim from the latest highlighted manuscript text, including citations.
- If a later review item revises a passage already quoted or summarized in an earlier response block, revisit the earlier block and resynchronize it before treating either item as stable.
- If reviewer comment text is reproduced, keep it verbatim where applicable.
- Citations used to support new claims are present where needed.
- Added terminology and notation are consistent across the synchronized artifacts.
- When quoting manuscript text in the response document, omit non-highlighted surrounding text unless it is needed for meaning, location, or a displayed block that would otherwise become unclear.
- When a quoted manuscript excerpt omits preceding text, begin the retained quote with `\dots` to mark the omission explicitly.
- For figure-driven comments, prefer embedding the revised figure directly in the response document near the relevant response block rather than relying only on prose description.
- Add a short bridge sentence before an embedded response figure.
- For an embedded response figure, start the caption with `(Fig. \ref{fig:xxx} in the revised manuscript)` and use a response-specific `\label{fig:resp_...}` instead of reusing the manuscript figure label.
- If the source figure caption is highlighted, keep the reproduced response caption synchronized.
- Refer to figures explicitly by number, not by relative placement words such as `above` or `below`.
- Do not use standalone `Supporting references:` blocks. Cite sources inline where they are needed.

## Validation Checklist

- The revised argument is technically honest and does not overclaim.
- New appendix or auxiliary technical content is checked for notation consistency.
- New appendix or auxiliary technical content is checked for likely render issues when relevant, such as overfull lines or awkward paragraph endings.
- Quoted source text is verbatim.
- Reproduced reviewer text is verbatim where applicable.
- Figure labels, captions, and references are synchronized.
- Generated or experimental artifacts are not confused with tracked source.
- The current item is satisfactory before moving to the next one.

## Handoff Checklist

- The progress tracker reflects the latest concrete state of work.
- The current review-item status is accurate.
- The next safe resume point is explicit.
- Any newly inferred reusable preference has been moved into the harness.
- No temporary assumption is left undocumented if it affects the next agent.
- If supporting code, secondary repositories, or remote environments were used, their sync state has been checked before closeout.

## Compact Per-Comment Template

Use this as a mental or written template when handling a review item:

- Target item:
- Goal of this step:
- Source-document action:
- Response-document action:
- Validation performed:
- Progress updates required:
- Wait condition before next item:

## Inferred Generic User Intent and Reusable Preferences

- Handle one review item at a time.
- Do not move to the next item until the current one is accepted or explicitly deferred.
- If the user rejects an addressment or asks to restart from an earlier item, resume from that item.
- If an item depends on additional simulations or unavailable evidence and the user chooses to defer it, mark it deferred and move only to the next item that can be addressed honestly.
- Prefer technically honest scope limitations over weak defenses.
- If a claim feels shaky, refine the key points before rewriting.
- Keep the control files low entropy: durable outcomes in the progress file, reusable guidance in the harness file.
- Keep quoted highlighted text verbatim between the manuscript and the response document.
- Omit non-highlighted surrounding text from quotes unless it is needed for meaning, location, or clarity.
- If prior text is omitted from a quote, mark the omission with `\dots`.
- Substantive manuscript revisions are highlighted by default.
- Grammar-only or typo-only fixes remain unhighlighted unless requested otherwise.
- While one review item is actively being refined, temporarily mark the active substantive manuscript edits in a distinct in-progress highlight color. Once that item is accepted or treated as stable, convert the same substantive text back to the standard revision color.
- If a whole section or subsection is changed or newly added for the revision, highlight its title in the same color as the body text for that revision state.
- Re-check directly from file after user edits or repeated requests to double-check.
- Keep notation aligned with the existing document and avoid index conflicts.
- Avoid reusing the same symbol for semantically different roles.
- Add supporting citations inline where claims are made.
- Prefer formal prose in technical explanations and proofs, and avoid symbolic directional shorthand when plain language is clearer.
- Check new appendix or auxiliary technical material for likely render or layout issues.
- Use title case for a formal problem or method name only when it functions as a formal heading, definition label, or exact name introduction. In ordinary prose, prefer lowercase phrasing plus the acronym when needed.
- In response documents, prefer plain text or `\textbf{...}` labels over decorative emphasis unless stronger emphasis is genuinely necessary.
- In response-document prose, lead with the mathematical reasoning or writing principle behind a revision before enumerating the concrete edits.
- In completed response-document sections, describe manuscript changes in past tense rather than present tense.
- When a reviewer questions a proof or claim, explain the standard being enforced and why the revised statement is the correct one, rather than mainly narrating what text was moved or added.
- In manuscript prose and response-document prose, avoid `:` by default. Prefer full sentences, commas, or a separate lead-in sentence unless a colon is genuinely necessary for a formal label, a definition, a list, or displayed material.
- If generated experiment, rerun, or merge artifacts are involved, treat them as artifacts rather than source and keep them aligned with the repository ignore conventions.
- If supporting code or remote repositories are involved, verify sync before closeout.

## Project Context for This Workspace

- Primary manuscript source: `main.tex`
- Primary response-letter source: `response_letter_TCOM_RV1.tex`
- Progress tracker: `AGENT_PROGRESS.md`
- Supporting code and experiment repo: `../leo-sat-flow`
- Supporting remote code checkout may exist on the SSH host and may need sync verification when code-backed revisions are part of the work
