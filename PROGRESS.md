# Progress

This file tracks the current state of the paper revision.

## Current Objective

- R1 C4 is complete and synchronized.
- R1 C5 is deferred for now because it needs additional simulation results.
- R1 C6 is also deferred for now because it needs additional simulation results.
- R1 C7 is complete and synchronized.
- R3 C1 is complete and synchronized.
- R3 C2 is complete and synchronized.
- R3 C3 is deferred for now because the user plans to address it together with later simulation results on stronger baselines.
- R3 C4 is complete and synchronized.
- R3 C5 is now the next addressable reviewer comment when the user asks to continue.

## Repository State

- The current branch is `main`.
- The latest committed synchronized reviewer-response revision includes the R3 C4 traffic-accounting clarification update set.
- The intended saved state of this file is a clean working tree after the current revision is committed.

## Concrete Edits Already Present

- R1 C1 is finalized and synchronized: the manuscript and response letter now clarify that the i.i.d. jitter assumption plays only a limited technical role in the current formulation.
- R1 C2 is finalized and synchronized: the manuscript now states an honest per-snapshot scope limitation for ATP, and `main.tex` includes the appendix `An Example MDP Extension for Future Work`.
- R1 C3 has been tightened and synchronized: the main body now defines the fixed-snapshot abstract decision problem `AS-JMR`, states Proposition `\ref{prop:np_hardness}` for `AS-JMR`, and adds an immediate clarification that the manuscript does not directly claim NP-hardness of the full geometric/orbital formulation.
- The appendix now proves NP-hardness of `AS-JMR` by a direct reduction from the integral 2-commodity flow problem in symmetric digraphs, with explicit source/target instances, threshold `\zeta`, unit-demand splitting, dedicated unit-rate LCT-pair gadgets, isolated-LCT padding, and separate polynomiality justification.
- `response_letter_TCOM_RV1.tex` has been synchronized to that scope and proof structure, including the clarification that the reduction target is `AS-JMR` rather than the full geometric/orbital model.
- The R1 C3 "manuscript changes" subsection in `response_letter_TCOM_RV1.tex` now quotes all non-appendix R1 C3 manuscript edits, including the abstract, introduction, contribution summary, main formulation block, post-proposition clarification, and conclusion.
- In the R1 C3 response-letter "manuscript changes" subsection, each quoted manuscript change is now preceded by a short location label stating where that text was revised in the paper.
- The response-letter quotation style has been normalized from literal `...` to `\dots` in the quoted manuscript-change excerpts.
- The R1 C3 main response paragraph in `response_letter_TCOM_RV1.tex` has been shortened to describe only the body-level revisions and no longer walks through the appendix proof steps.
- `HARNESS.md` now records the reusable style rule that formal problem names should not remain in title case in ordinary prose when lowercase wording suffices.
- `response_letter_TCOM_RV1.tex` has been synchronized again to the current `main.tex` wording for the R1 C3 non-appendix text, and unnecessary italic styling has been removed in favor of plain text or bold labels.
- The R1 C3 main response paragraph in `response_letter_TCOM_RV1.tex` has been rewritten again to focus on the mathematical reasoning behind the revision and the exact scope of the claim, rather than narrating the edit sequence.
- The completed R1 C3 "Manuscript changes" narration in `response_letter_TCOM_RV1.tex` has been converted to past tense, and the main response paragraph has been adjusted for tense consistency.
- The R1 C3 main response paragraph has been rewritten again to emphasize the proof philosophy explicitly: a hardness theorem must match the exact target class reached by the reduction, and the appendix carries the full construction for that precise claim.
- The R1 C3 main response paragraph has been sharpened again so it now frames the revision around theorem-proof alignment first, and only then explains why the appendix carries the full step-by-step reduction.
- The R1 C3 main response paragraph has been rewritten again to follow the manuscript's own structure and terminology more closely, centering the explanation on `(P1)`, the fixed-snapshot abstraction, Proposition `\ref{prop:np_hardness}`, and the appendix reduction.
- The R1 C3 main response paragraph has been rewritten again to follow the wording of the remark after Proposition `\ref{prop:np_hardness}` more directly, especially on why the paper does not directly claim NP-hardness of `(P1)`.
- The R1 C3 response paragraph has been freshly rewritten from scratch after the user requested a new pass, restoring the body text and centering it on the exact reason given in the remark after Proposition `\ref{prop:np_hardness}`.
- The R1 C3 response paragraph has now been replaced with the planned one-paragraph version that explicitly follows the user-requested order: acknowledge the issue, explain complexity via AS-JMR, explain the non-implication for `(P1)`, and briefly summarize the appendix reduction.
- The first mention of AS-JMR in the R1 C3 response paragraph now includes the full name "abstract snapshot joint matching and routing (AS-JMR)".
- The remaining R1 C3 wording defects found in review were corrected: Contribution 1 in `main.tex` no longer overstates "NP-hardness of the problem", the AS-JMR definition grammar was fixed in both `main.tex` and the quoted response-letter block, and the R1 C3 response paragraph was tightened to remove the duplicated AS-JMR appositive and to mirror the remark's conditional sentence more closely.
- R1 C4 is now drafted and synchronized: `main.tex` explicitly states that competing flows on bottleneck LISLs can cause transient subgradient oscillations, Theorem `\ref{theorem:convergence:classic}` is now phrased in terms of the best-so-far dual iterate and its dual-value gap, the manuscript again returns to the last iterate for the practical conversion step, and the numerical-results discussion no longer implies monotone per-iteration improvement.
- The R1 C4 block in `response_letter_TCOM_RV1.tex` has been rewritten from a proposed response to a completed response with verbatim quoted manuscript changes, and the response-letter preamble now defines `\argmax` so that the quoted theorem text compiles verbatim.
- The main R1 C4 response paragraph in `response_letter_TCOM_RV1.tex` has been tightened again at the user's request by removing the sentence that foregrounded the best-so-far iterate as a practical DuJo-procedure change; the response now keeps the emphasis on the oscillation/convergence distinction and the simulation-discussion clarification.
- The R1 C4 response paragraph has been revised again to avoid the colon-style continuation in the convergence sentence; it now uses full-sentence prose instead, matching the user's style preference.
- `main.pdf` and `response_letter_TCOM_RV1.pdf` were rebuilt successfully after the R1 C4 edits; the new response-letter overfull boxes introduced during drafting were removed, and only the pre-existing unrelated warning from a long bibliography entry remains there. During a later verification pass, a corrupted generated `main.aux` in the current-dir build path had to be cleared and regenerated before the manuscript build stabilized again.
- R1 C7 is now drafted and synchronized: `main.tex` includes a focused proofreading pass that improves the introduction, notation paragraph, LCT-mechanics exposition, figure captions, numerical-results wording, complexity discussion, and conclusion, those minor wording edits are now left unhighlighted in the manuscript, and `response_letter_TCOM_RV1.tex` presents R1 C7 as a completed response without foregrounding those minor edits through quoted manuscript excerpts.
- After a review pass on the R1 C7 addressment, several remaining draft-like sentences were tightened in `main.tex`, and the response-letter wording was narrowed from a manuscript-wide proofreading claim to a focused cleanup claim.
- `main.pdf` and `response_letter_TCOM_RV1.pdf` were rebuilt successfully after the R1 C7 edits. During verification, a generated zero-length `main.bbl` had to be refreshed with `bibtex main` before the manuscript build returned to the expected warning state. The manuscript still shows the same pre-existing duplicate-destination and layout warnings, and the response letter still shows the same pre-existing overfull-box warning from the long bibliography entry.
- R3 C1 is now drafted and synchronized in `response_letter_TCOM_RV1.tex`: the old proposed LOS/Earth-occlusion response has been replaced with a completed response that matches the actual manuscript revision, namely the explicit connectable-pair visibility condition in terms of the distance cap and the mutual FOR test used in the definition of `\mathcal{E}`.
- R3 C1 has now been tightened further and synchronized across `main.tex` and `response_letter_TCOM_RV1.tex`: the manuscript subsection is renamed to `LCT Visibility and Connection Constraints`, the subsection and defining visibility equation are now labeled as `subsec:lct_visibility_connection` and `eq:lct_visibility_condition`, and the response letter now cites those exact references while quoting the final manuscript wording verbatim.
- R3 C1 has now been revised again so the visible manuscript changes are highlighted in blue: the revised subsection title is now blue in `main.tex`, the two new visibility-framing sentences are blue, and the response-letter quotation has been resynchronized to match that visible blue manuscript text while avoiding the duplicate-label issue that would arise from quoting the manuscript's internal equation label literally.
- R3 C1 has now been extended further in `main.tex` with a short post-equation limitation note stating that the current visibility/connectability approximation does not model atmospheric effects or an explicit LOS/Earth-occlusion constraint, and `response_letter_TCOM_RV1.tex` has been synchronized to quote and explain that added scope limitation.
- `HARNESS.md` now records the reusable manuscript-markup preference that substantive `main.tex` revisions should be highlighted in blue, while grammar-only or typo-only fixes should remain unhighlighted unless the user asks otherwise.

## Status by Comment

### Completed and synchronized

- R1 C1
- R1 C2
- R1 C3
- R1 C4
- R1 C7
- R3 C1
- R3 C2
- R3 C4

### Deferred pending additional simulation results

- R1 C5
- R1 C6
- R3 C3

### Still only proposed in the response letter

- R3 C5
- R3 C6
- R3 C7
- R3 C8
- R3 C9
- R3 C10

## Rolling Progress Log

- R1 C1 was rewritten around the limited role of the i.i.d. jitter assumption and synchronized between manuscript and response letter.
- R1 C2 was reframed to an explicit per-snapshot ATP limitation, extended with an illustrative MDP appendix, and synchronized with the response letter after notation and citation tightening.
- R1 C3 was upgraded from a terse NP-hardness claim to a formal proposition with a step-by-step EDP reduction, then left pending a final writing review.
- R1 C3 was revised after the writing review to make the reduction technically honest under the paper's own constraints, synchronized in the response letter, and checked by rendering both `main.tex` and `response_letter_TCOM_RV1.tex`.
- R1 C3 was further revised to move the full proof into the appendix and replace directional shorthand with formal proof prose, with the response letter updated to match that placement and wording; the revised manuscript and response letter both rendered successfully afterward.
- R1 C3 was revised again to replace the EDP-first appendix proof with a direct fixed-matching routing reduction framed via unit-demand, unit-capacity integral multicommodity routing, synchronized in the response letter, supported by a new UFP citation, and rebuilt successfully with BibTeX.
- R1 C3 was adjusted once more to stop reusing `k` as the decision threshold, replacing it with `\zeta` in both the appendix proof and synchronized response-letter explanation, and both files rendered successfully afterward.
- R1 C3 was tightened again after an adversarial proof review to make the continuous-`q` saturation argument explicit and to justify polynomiality not only for demand splitting but also for copied capacities and the common-`N'` dummy-padding gadget.
- R1 C3 was restructured again into explicit claims, the toy reduction figure was removed, and the response-letter summary was synchronized to the new proof structure.
- R1 C3 was corrected again after fixing the model constraint to `\sum_m c_{n,m}\leq 1`: the leftover-port and dummy-gadget part was removed, the appendix proof now uses isolated unused LCTs only, and the response letter was synchronized to the simpler reduction.
- R1 C3 narrative was tightened again so the appendix proof now flows as source problem -> construction -> forward direction -> `q=1` saturation -> path extraction -> converse -> polynomiality, with the forward-direction capacity wording corrected for bidirectional dedicated pairs and the response-letter summary compressed to the same structure.
- R1 C3 was clarified again to name the two instances explicitly as a source instance and a constructed target instance, with the appendix and response letter both rewritten to keep those roles consistent from start to finish.
- R1 C3 was aligned again across manuscript and response letter so the formal claim is only that `AS-JMR` is NP-hard, the post-proposition clarification explains why the full geometric/orbital formulation is not directly claimed NP-hard, and the response-letter quotation now matches that scope.
- A reusable style rule was recorded in `HARNESS.md`: do not keep formal problem names in title case in ordinary prose when lowercase wording plus the acronym is sufficient.
- The R1 C3 response-letter "manuscript changes" section was expanded again so it now includes every non-appendix manuscript change for that comment; `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The R1 C3 response-letter "manuscript changes" section was refined again so each quoted block is introduced by its manuscript location, and the quoted text was resynchronized to the latest `main.tex`; `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The response-letter quoted manuscript excerpts were normalized from ``... to ``\dots, and `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The R1 C3 main response paragraph was shortened again at the user's request so it now explains only what was revised in the manuscript body; the appendix-proof walkthrough was removed, and `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The response letter was synchronized again to the current `main.tex` wording for R1 C3, all remaining `\textit{...}` label styling was replaced with `\textbf{...}`, and the remaining `\emph{...}` emphasis was removed per the user's style preference.
- The R1 C3 response paragraph was rewritten once more to foreground the reasoning principle behind the revision, namely that the hardness statement should match exactly what the reduction proves, with the edit narration moved to the separate "Manuscript changes" block.
- The completed R1 C3 response-letter wording was revised again so the "Manuscript changes" narration now uses past tense throughout, matching the fact that those edits have already been made.
- The R1 C3 response paragraph was revised again at the user's request to push the explanation further toward mathematical philosophy: what a reduction proves, why the theorem must match that target exactly, and why the main text/body-versus-appendix split follows from that principle.
- The R1 C3 response paragraph was tightened again so it explains the revision as a matter of theorem-proof alignment rather than proof expansion alone: the abstract snapshot problem is the exact target reached by the reduction, and the appendix then supplies the detailed construction for that precise claim.
- The R1 C3 response paragraph was rewritten once more to connect the explanation directly to the paper's own wording: `(P1)` as the physical mixed-integer formulation, AS-JMR as the fixed-snapshot abstract decision problem used for hardness, and the appendix as the location of the detailed reduction from integral 2-commodity flow.
- The R1 C3 response paragraph was rewritten again to mirror the remark in `main.tex`: the reduction fixes the combinatorial snapshot input, does not derive it from the underlying geometry/FOR/distance/traffic rules, and therefore supports a direct NP-hardness statement for AS-JMR rather than for `(P1)`.
- The R1 C3 response paragraph was rewritten again from a blank state so it now cleanly explains: `(P1)` is the physical formulation, the current reduction fixes the combinatorial snapshot input, the direct theorem therefore concerns AS-JMR, and the appendix provides the requested step-by-step reduction to that problem.
- The R1 C3 response paragraph was replaced again to implement the final requested flow exactly, and `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The first AS-JMR mention in the R1 C3 response paragraph was expanded to the full problem name, and `response_letter_TCOM_RV1.pdf` was rebuilt successfully afterward.
- The R1 C3 materials were reviewed again and the remaining concrete defects were fixed in both the manuscript and response letter; `main.pdf` and `response_letter_TCOM_RV1.pdf` both rebuilt successfully afterward, with only the pre-existing unrelated LaTeX warnings remaining.
- The user marked R1 C3 done, so the status was advanced to completed and synchronized, and the next safe resume point was updated to R1 C4.
- The R1 C3 revision set was committed as `4ab0e78` (`Revise R1 C3 hardness statement and response`) and pushed to `origin/main`, so the repository state in this file now reflects a clean worktree.
- R1 C4 was revised to distinguish transient oscillations from the best-so-far dual-value guarantee, synchronize the response letter with verbatim quoted manuscript text, add the missing `\argmax` operator to the response-letter preamble for compilation, and rebuild both PDFs successfully afterward.
- The user requested a tighter R1 C4 response paragraph without the sentence about aligning the practical DuJo procedure to the best-so-far iterate, so that sentence was removed and `response_letter_TCOM_RV1.pdf` was rebuilt successfully with only the same pre-existing bibliography overfull warning remaining.
- A reusable writing preference was clarified and recorded in `HARNESS.md`: in both `main.tex` prose and response-letter prose, avoid `:` by default and use it only when structurally necessary.
- The user then asked to revert the manuscript-side practical-procedure change for R1 C4, so `main.tex` was restored to convert the last iterate rather than a retained best-so-far iterate, the corresponding quoted blocks were removed from `response_letter_TCOM_RV1.tex`, a corrupted generated `main.aux` was cleared, and both PDFs rebuilt successfully afterward.
- The user marked R1 C4 done, so the status was advanced to completed and synchronized, and the next safe resume point was updated to R1 C5.
- The user then chose to skip R1 C5 for now because it needs additional simulation results, so R1 C5 was marked deferred and the next safe resume point moved to R1 C6.
- The user then chose to skip R1 C6 for now because it also needs additional simulation results, so R1 C6 was marked deferred, the next safe resume point moved to R1 C7, and `HARNESS.md` was updated with the reusable rule for deferring simulation-dependent comments.
- R1 C7 was addressed with a manuscript-wide proofreading pass over several awkward or ambiguous passages, the response letter was converted from a proposal to a completed synchronized response, and both PDFs rebuilt successfully afterward with only the same pre-existing unrelated warnings remaining.
- At the user's request, the R1 C7 response-letter block was simplified further so it no longer highlights those minor edits with quoted manuscript changes.
- During the final R1 C7 verification pass, an unexpectedly empty generated `main.bbl` was recovered by rerunning `bibtex main`, after which `main.pdf` and `response_letter_TCOM_RV1.pdf` both rebuilt successfully again.
- At the user's request, the minor R1 C7 proofreading edits in `main.tex` were also left unblue while keeping the revised wording itself, and `main.pdf` rebuilt successfully afterward.
- A later review of R1 C7 found a few remaining awkward sentences, so the manuscript wording around the LCT-jitter description, simulation discussion, and conclusion was tightened again, the response-letter claim was narrowed to a focused cleanup, and both PDFs rebuilt successfully afterward.
- The user marked R1 C7 done, so the status was advanced to completed and synchronized, and the next safe resume point moved past R1 C7 to the next addressable reviewer comment outside the deferred simulation-dependent items.
- A later review pass identified Reviewer 3 Comment 1 as the next addressable comment after deferred R1 C5 and R1 C6, and `PROGRESS.md` was refreshed accordingly.
- The R3 C1 response-letter block was rewritten from a proposed LOS/Earth-occlusion response to a completed response aligned with the actual manuscript change, which states the explicit connectable-pair visibility condition through the maximum-distance bound and the mutual FOR inequalities in the definition of `\mathcal{E}`.
- R3 C1 was then revised again so the manuscript frames the block explicitly around visibility, adds labels for the subsection and defining equation, and the response letter now refers to Subsection `\ref{subsec:lct_visibility_connection}` and Equation `\eqref{eq:lct_visibility_condition}` directly; `main.pdf` and `response_letter_TCOM_RV1.pdf` both rebuilt successfully afterward with no undefined-reference warnings, while the same pre-existing unrelated LaTeX warnings remained.
- R3 C1 was revised once more to highlight the visible manuscript changes in blue, including the revised subsection title and the two new visibility-framing sentences. `main.pdf` rebuilt successfully with `latexmk`, and `response_letter_TCOM_RV1.pdf` rebuilt successfully with direct `pdflatex`; when run through `latexmk`, the response-letter build still surfaced a stale custom-dependency error from the external `main` subdocument helper even though the PDF itself was produced.
- The user then clarified a reusable writing standard: in `main.tex`, substantive manuscript changes should be highlighted in blue, while grammar-only or typo-only fixes should stay unhighlighted. `HARNESS.md` was updated accordingly; the active R3 C1 manuscript block already conforms to that rule.
- The user then asked for a short limitation note after the visibility equation, so `main.tex` was updated to add a blue scope-limitation sentence on atmosphere and LOS/Earth-occlusion immediately after `\eqref{eq:lct_visibility_condition}`, `response_letter_TCOM_RV1.tex` was synchronized to that exact new wording, `main.pdf` rebuilt successfully with `latexmk`, and `response_letter_TCOM_RV1.pdf` rebuilt successfully after `bibtex response_letter_TCOM_RV1` plus two `pdflatex` passes.
- During the final verification of that limitation-note addition, the quoted blue sentence in `response_letter_TCOM_RV1.tex` was resynchronized once more so it matches the manuscript verbatim, including the opening wording ``Note that this visibility model is simplified,'' and `response_letter_TCOM_RV1.pdf` rebuilt successfully afterward.
- A subsequent synchronization pass tightened the R3 C1 main response paragraph into completed-work past tense and aligned its wording more closely with the current `main.tex` visibility block and limitation note, while leaving the quoted manuscript excerpt unchanged because it already matched the manuscript text.
- A later cleanup pass expanded the abbreviations introduced by the R3 C1 revision itself, replacing `FOR` with `field-of-regard` and `LOS` with `line-of-sight` in the active `main.tex` visibility text and the synchronized R3 C1 response-letter wording.
- A manuscript-wide abbreviation cleanup then fixed several remaining issues in `main.tex`: the introduction now uses the plural acronym `LISLs` correctly, the notation table spells out the Earth-centered inertial frame instead of using `ECI` before expansion, the simulation setup spells out `TLE` on first use in that section and removes the one-off `GW` abbreviation, and the blue NP-hardness clarification now uses `field-of-regard constraints` rather than `FOR constraints`; the synchronized R1 C3 response-letter text was updated to match that blue wording.
- A follow-up terminology pass standardized the expansion of `FOR` to `field of regard` without hyphenation in the active manuscript text and in the synchronized response-letter quotations, so the wording now matches the original definition of the term in the LCT mechanics subsection.
- A subsequent review pass on R3 C1 found that the technical content is synchronized, but the response-letter presentation still has formatting/style inconsistencies relative to surrounding addressed comments, especially the mixed quote-plus-displayed-equation excerpt formatting in the `Manuscript changes` block and the opening tense/style mismatch against nearby finalized responses. R3 C1 therefore remains pending user-directed cleanup rather than ready to mark complete.
- A deeper comparison against the nearby completed addressments narrowed that presentation issue: the confirmed structural inconsistency is the R3 C1 `Manuscript changes` excerpt, which opens as a quoted prose snippet and then continues with an unframed displayed equation plus an unquoted continuation sentence. The opening sentence ``We agreed with this point'' remains a minor local style outlier, but it is not a strong formatting inconsistency on the same level.
- The user then clarified a reusable quoting preference: when manuscript text is quoted in the response letter, non-blue surrounding text may be omitted if it is not important. `HARNESS.md` was updated accordingly, and the active R3 C1 `Manuscript changes` excerpt in `response_letter_TCOM_RV1.tex` was trimmed to keep only the substantive added text and the defining equation.
- After that trimming pass, the active R3 C1 excerpt had dropped the leading `\dots` marker used elsewhere to signal omitted preceding text. That marker was restored at the start of the retained quoted sentence for local formatting consistency.
- The user then asked to make that omission marker explicit in the reusable workflow. `HARNESS.md` now states that when a quoted manuscript excerpt omits preceding text, the retained quote should begin with `\dots`.
- The user then approved the current R3 C1 update set for commit and push, so the comment status was advanced from drafted/pending review to complete and synchronized, and the next safe resume point moved to R3 C2.
- The user then asked to start R3 C2. The manuscript now narrows the high-level claim from a full global traffic profile to a snapshot-level spatial traffic profile, labels the traffic-profile subsection, and states explicitly that the current model omits temporal variation and purchasing-capability effects while citing richer demand-modeling directions including the reviewer-suggested paper. `response_letter_TCOM_RV1.tex` was synchronized to that completed revision, and R3 C2 is now drafted pending user review.
- The long DOI in the reviewer-provided R3 C2 reference comment was then wrapped with `\url{...}` in `response_letter_TCOM_RV1.tex` so the comment can break across lines cleanly without changing its content.
- After a small manuscript wording update in the R3 C2 introduction sentence, the corresponding quoted sentence in `response_letter_TCOM_RV1.tex` was resynchronized so the retained blue excerpt again matches `main.tex` verbatim.
- A later review pass on R3 C2 found two remaining presentation issues only: the main response paragraph still used present-tense revision phrasing, and the new traffic-scope wording was slightly inconsistent between the abstract and introduction. Those were then cleaned up by converting the response paragraph to completed-work past tense and aligning the introduction wording to the singular phrase `a snapshot-level spatial traffic profile over the globe`, with the quoted response-letter excerpt synchronized accordingly.
- Before closing R3 C2, the citation-support wording in the final traffic-model limitation sentence was tightened so that temporal and purchasing-capability modeling is supported by `zamacola2025profiling` and `qin2024satformer`, while `guo2021gateway` is cited more narrowly for gateway-aware traffic estimation. The response-letter summary and quoted blue excerpt were resynchronized to match this final manuscript wording.
- The user then approved R3 C2 as done and requested commit/push, so the comment status was advanced from drafted/pending review to complete and synchronized, and the next safe resume point moved to R3 C3.
- The user then chose to skip R3 C3 for now because it will be handled together with later simulation results on stronger baselines. R3 C3 is therefore deferred rather than abandoned, and the next addressable reviewer comment is now R3 C4.
- The user then asked to address R3 C4. `main.tex` now states explicitly that $Q$ is gateway service capacity between a gateway-connected satellite and the terrestrial Internet, that LISL transit capacity is constrained separately by the established optical-link capacities, that local user traffic consumes this gateway service capacity first, and that the simulation setup uses the same interpretation for $Q=20$ Gbps. `response_letter_TCOM_RV1.tex` was synchronized to that completed revision, and R3 C4 is now drafted pending user review.
- A review pass on R3 C4 then found no technical mismatch between the manuscript and response letter, but it did find two wording-consistency issues still worth cleaning up in `main.tex`: the notation table still uses the older generic label ``Gateway capacity per satellite'' for $Q$, and the simulation setup still mixes ``ground station'' with the now-preferred ``gateway'' terminology.
- Those two R3 C4 wording-consistency issues were then cleaned up in `main.tex`: the notation table now labels $Q$ as ``Gateway service capacity per satellite,'' and the simulation setup now uses ``ground gateway'' and ``gateway connections'' consistently. The reviewer-facing response text for R3 C4 did not need substantive changes because the technical claim and quoted blue manuscript text remained the same.
- The user then approved R3 C4 as done and requested commit/push, so the comment status was advanced from drafted/pending review to complete and synchronized, and the next safe resume point moved to R3 C5.

## Current Blockers or Risks

- R1 C5 now requires additional simulation results before it can be addressed fully.
- R1 C6 now also requires additional simulation results before it can be addressed fully.
- R3 C3 now also requires additional simulation results on stronger baselines before it should be finalized.
- The broader manuscript TeX build still reports pre-existing duplicate-destination and layout warnings outside the scope of the R1 C3 fix.
- When building `response_letter_TCOM_RV1.tex` via `latexmk`, the wrapper can still report a stale custom-dependency failure from the external `main` subdocument helper even after the PDF is produced; a direct `pdflatex response_letter_TCOM_RV1.tex` run succeeds on the current file state.

## Immediate Next-Agent Actions

1. Resume at R3 C5 if the user asks to continue with the next reviewer comment that does not depend on new simulations.
2. Return to R1 C5 or R1 C6 only when the user wants to generate and integrate the additional simulation results they require.
3. Return to R3 C3 when the user is ready to add the stronger-baseline simulation results it needs.
4. Preserve the existing unrelated LaTeX warnings unless the user explicitly asks to clean them.

## Next Safe Resume Point

- Resume from the next user instruction at R3 C5, unless the user explicitly reopens R1 C5, R1 C6, or R3 C3 for simulation work.
