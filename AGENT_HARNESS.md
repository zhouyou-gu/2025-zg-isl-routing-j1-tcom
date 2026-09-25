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
- Use normal LaTeX line breaking for prose revisions. Do not add manual line-fitting commands such as `\looseness` unless the user requests them.
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
- When a quoted manuscript excerpt omits preceding text, begin the retained quote with literal `...` before the first blue paragraph, following the reference response-letter standard.
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
- If prior text is omitted from a quote, mark the omission with literal `...` before the first blue paragraph.
- Substantive manuscript revisions are highlighted by default.
- Grammar-only or typo-only fixes remain unhighlighted unless requested otherwise.
- While one review item is actively being refined, temporarily mark the active substantive manuscript edits in a distinct in-progress highlight color. Once that item is accepted or treated as stable, convert the same substantive text back to the standard revision color.
- If a whole section or subsection is changed or newly added for the revision, highlight its title in the same color as the body text for that revision state.
- Re-check directly from file after user edits or repeated requests to double-check.
- Keep notation aligned with the existing document and avoid index conflicts.
- Avoid reusing the same symbol for semantically different roles.
- Add supporting citations inline where claims are made.
- Prefer formal prose in technical explanations and proofs, and avoid symbolic directional shorthand when plain language is clearer.
- Describe related work in third person, using the authors or method name; avoid ownership phrases such as "our related work."
- In manuscript prose, avoid response-letter or conversational framing such as explaining what the paper does not claim "here," defending why a proof is scoped a certain way, or saying "we do not propose" as a reviewer-facing caveat. State scope limitations as formal manuscript claims instead.
- Check new appendix or auxiliary technical material for likely render or layout issues.
- Use title case for a formal problem or method name only when it functions as a formal heading, definition label, or exact name introduction. In ordinary prose, prefer lowercase phrasing plus the acronym when needed.
- In response documents, prefer plain text or `\textbf{...}` labels over decorative emphasis unless stronger emphasis is genuinely necessary.
- In response-document prose, lead with the mathematical reasoning or writing principle behind a revision before enumerating the concrete edits.
- In response-document prose, answer the reviewer's actual question in the first response paragraph before explaining manuscript edits, technical background, figures, or appendices.
- Response-letter answers must be self-contained enough for a reviewer to understand the answer without reading the revised manuscript. When the answer relies on a proof, metric, figure, or appendix, include the key reasoning, definition, or interpretation directly in the response letter before pointing to the manuscript excerpt.
- In completed response-document sections, describe manuscript changes in past tense rather than present tense.
- When a reviewer questions a proof or claim, explain the standard being enforced and why the revised statement is the correct one, rather than mainly narrating what text was moved or added.
- In manuscript prose and response-document prose, avoid `:` by default. Prefer full sentences, commas, or a separate lead-in sentence unless a colon is genuinely necessary for a formal label, a definition, a list, or displayed material.
- If generated experiment, rerun, or merge artifacts are involved, treat them as artifacts rather than source and keep them aligned with the repository ignore conventions.
- If supporting code or remote repositories are involved, verify sync before closeout.

## Project Context for This Workspace

- Primary manuscript source: `main.tex`
- Identify the active round and response-letter source from `AGENT_PROGRESS.md`; preserve earlier-round letters as historical artifacts.
- Progress tracker: `AGENT_PROGRESS.md`
- Supporting code and experiment repo: `../leo-sat-flow`
- Supporting remote code checkout may exist on the SSH host and may need sync verification when code-backed revisions are part of the work

## Revision-Response Playbook

These durable rules apply only when active work involves coordinated manuscript and response-letter revision. They are reusable operating rules, not mission scope or current task state.

- After completing the mandatory core AGENT-file read order, consult `REVISION_TASK.md` only when it exists and active work involves joint manuscript and response-letter revision; treat it as a lower-precedence current-state brief, not as a control file.
- Do not patch `AGENT.md` to register `REVISION_TASK.md`; the control file is immutable after scaffold. These rules may describe when the sidecar is useful and which revision facts it owns, but they do not change core read order, precedence, file roles, or update-dispatcher authority.
- Handle one review item at a time unless the user explicitly asks for grouped handling.
- When the user requests plans for every comment, draft all requested items together. Separate existing facts from proposed work, use future tense and `Planned manuscript changes:` for unimplemented revisions, and keep comments pending. Neighboring responses may inform the approach, but their numerical results and method-specific claims are not evidence for this paper.
- For each review item, identify the manuscript change, response-letter claim, supporting evidence, and any highlighted-manuscript effect before marking the item resolved.
- Revise manuscript content before finalizing response-letter text when the response depends on a technical or textual manuscript change.
- Keep manuscript, response letter, highlighted manuscript, appendix material, figures, simulations, and bibliography mutually consistent when one of them changes the substance of the reply.
- Do not claim that a reviewer concern has been addressed unless the manuscript source and response-letter draft make compatible claims and cite or point to the same supporting evidence.
- Keep response-letter drafting concise, specific, and respectful. State what changed, where it changed, and why the change addresses the concern.
- Vary response-letter openings and avoid starting most responses with `We agree`; use it only when agreement is substantive, and otherwise state the revision action directly.
- When a reviewer comment uses numbered references to papers, tables, figures, or equations, preserve the reviewer's original number in the response text. For paper references, append an immediate parenthetical mapping in the form `(\cite{...} in this letter)`. For table, figure, and equation references whose numbers changed, use mappings such as `(now Table~\ref{...})`, `(now Fig.~\ref{...})`, or `(now \eqref{...})` rather than replacing the reviewer-supplied number. If the number is unchanged, refer to it directly and do not add a redundant mapping such as `Fig. 1 (now Fig. 1)`.
- In response-letter entries, keep the visual paragraph structure consistent: put a blank line after the reviewer comment, after `\textbf{Response:}` text, after `\textbf{Manuscript changes:}` or `\textbf{Planned manuscript changes:}` text, and before the next reviewer comment.
- When a response-letter change entry describes completed manuscript edits, use the label `\textbf{Manuscript changes:}`, name the manuscript location, and introduce each quoted change with a short sentence ending in "as". Quote a single-paragraph change as ``...\blue{revised text.}''. Quote a contiguous multi-paragraph change in the same style, with the literal `...` only before the first blue paragraph:

~~~tex
``...\blue{first paragraph.}

\blue{second paragraph.}

\blue{final paragraph.}''
~~~

Use separate quoted excerpts only for non-contiguous manuscript changes.
- When reproducing a manuscript table in a response letter, preserve the manuscript table's semantic content, caption identity, and reviewer traceability, while adapting only the local presentation needed for the response-letter class and page geometry. Use a caption prefix such as ``(Table~\ref{...} in the manuscript)'' when needed to distinguish the reproduced letter table from the manuscript table. Keep the reproduced table fixed under the relevant reviewer comment so it does not float past the next comment. Validate by rendering the response-letter PDF and visually comparing the reproduced table against the manuscript table. Do not rely on source equality or text extraction alone for table-layout checks.
- When reproducing a manuscript figure in a response letter, use the manuscript figure artifact directly and preserve its visual content, caption meaning, manuscript figure identity, and reviewer traceability, while adapting only the local size needed for the response-letter class and page geometry. Place the reproduced figure after the relevant quoted manuscript change, use a caption prefix such as ``(Fig.~\ref{...} in the manuscript)'' to distinguish the response-letter figure number from the manuscript figure number, and use normal LaTeX float placement. Do not impose `[H]` or forced placement unless the user requests it. Validate by rendering the response-letter PDF and visually comparing the reproduced figure and caption against the manuscript figure. Do not rely on matching source paths, file hashes, or text extraction alone for figure-layout checks.
- Format reviewer and editor comments in the response letter in bold; keep responses and planned/manuscript-change notes under their existing labels.
- Render unchecked reviewer and editor comments in red. Keep a comment red and pending after drafting, editing, synchronization, or successful validation; these actions do not constitute approval. Remove the pending-comment color and mark a comment checked only when the user explicitly says ``OK'' for that specific comment.
- Treat highlighting as a derivative artifact of concrete manuscript edits. Do not use highlighting notes as the source of truth for manuscript content.
- Only when the user explicitly requests final PDF variants for a revision submission, compile each requested existing LaTeX source entry point directly without creating alternate `.tex` files. Put temporary build state in the gitignored `tmp/` directory and final PDFs in the gitignored `output/pdf/` directory. Treat `<source-stem>_untracked.pdf` as the primary target and remap every tracked-content color declaration at compile time, including macros and direct color commands in prose, tables, and equations, so all revised document text renders in the normal uncolored text color. Name the blue tracked companion `<source-stem>_blue_tracked.pdf` and force only tracked document content to blue. Produce a suffix-free `<source-stem>.pdf` that preserves source-defined coloring only when the user specifically requests a direct source-colored build. Leave embedded figure content unchanged, and do not run this export workflow as routine validation.
- Highlight all revised manuscript text in blue, using the manuscript's existing blue-text convention or a minimal LaTeX blue-text macro introduced before the first highlighted edit.
- Treat proofreading-only language cleanup as an exception to the blue-highlight and quoted-change rules when the user asks for proofreading rather than a substantive manuscript change. Do not individually blue-highlight or quote minor proofreading edits; state in the response letter that the manuscript was proofread.
- Record active review item state, artifact mapping, evidence gaps, and the next review-item-local coordination step in `REVISION_TASK.md`. Record execution blockers, cross-item resume needs, and the canonical resume point in `AGENT_PROGRESS.md`, not in this playbook.


### Starting a New Review Round

- When the user resets revision tracking for a new round, remove prior-round color wrappers with brace-aware editing while preserving their contents, and remove any old blue-to-black override so the retained highlight macro works for new changes. Keep archived prior-round markup unchanged.

- Create a separate response source using the next local `response_letter_TCOM_RV<n>.tex` stem. Treat that suffix as a workspace round label until the decision letter confirms the editorial round. Preserve previous response letters.
- Obtain the new decision letter and all reviewer reports before creating numbered comments or substantive replies. Preserve original wording and reviewer identifiers, and verify the current submission identifier and decision date instead of reusing prior-round metadata.
- If the reports are unavailable, create a visibly labeled draft with pending-input notices and a commented authoring template. Do not invent comments, assume the previous reviewer set, or claim revisions have been completed.
- Preserve the previous submission's manuscript baseline and color state when initializing a round. Distinguish new substantive edits before enabling their blue highlighting so previous-round changes are not presented as new.
- Keep manuscript labels out of quoted excerpts and give reproduced figures and tables response-specific labels. Do not disable all local labels or suppress reference warnings globally.

### Archiving a Completed Review Round

- Archive only round-specific response letters, cover letters, their build files, and response progress records in `archive/rv<n>/`. Preserve their contents and update active tracker links.
- Keep manuscript files, tracked manuscript variants, figures, bibliography databases, and class files outside the response archive. Do not add dependency snapshots or expand the archive beyond response-related files.
- Keep archival simple. Do not add manifests, archive documentation, or rebuild packages unless requested. Preserve existing Git tracking and ignore conventions.

### Verbatim Decision-Letter Intake

- Preserve supplied decision letters and reviewer reports as byte-identical source files. Build comment blocks directly from that source, retaining spelling errors, punctuation, original numbering, and Unicode symbols; apply only LaTeX escaping and layout markup.
- Follow the supplied reference response letter directly: use inline bold `Comment E.1:` / `Comment 1.1:` labels, then `Response:` and `Manuscript changes:`. Replace source list markers with those comment labels while preserving every word of the comment. Verify comment wording after reversing LaTeX escaping.
- For a scaffold-only request, leave the reference's response and manuscript-change fields empty. Do not add scaffold banners, separate comment headings, duplicated numbering, forced reviewer page breaks, bracketed drafting instructions, or custom comment environments. Do not draft substantive answers or mark items approved.
- Include the editor's substantive assessment as the editor comment. Keep the full administrative email in the original source file rather than reproducing its salutation, submission link, instructions, or signature in the response letter. Preserve reviewer opening assessments as unnumbered introductory paragraphs without separate response fields.
