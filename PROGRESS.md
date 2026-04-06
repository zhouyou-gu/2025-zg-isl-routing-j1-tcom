# Progress

This file tracks the current state of the paper revision.

## Current Objective

- R1 C3 is complete and synchronized.
- Resume at R1 C4 when the next revision step begins.

## Repository State

- The paper workspace is already dirty.
- Tracked paper files currently modified are:
  - `main.bbl`
  - `main.bib`
  - `main.tex`
  - `response_letter_TCOM_RV1.bbl`
  - `response_letter_TCOM_RV1.tex`
- Untracked control files currently present are:
  - `AGENT.md`
  - `HARNESS.md`
  - `PROGRESS.md`

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

## Status by Comment

### Completed and synchronized

- R1 C1
- R1 C2
- R1 C3

### Still only proposed in the response letter

- R1 C4
- R1 C5
- R1 C6
- R1 C7
- R3 C1
- R3 C2
- R3 C3
- R3 C4
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

## Current Blockers or Risks

- The broader manuscript TeX build still reports pre-existing duplicate-destination and layout warnings outside the scope of the R1 C3 fix.
- The response-letter TeX build still reports pre-existing overfull-box warnings in other comments outside the scope of the R1 C3 fix.
- The manuscript worktree is already dirty, so unrelated tracked edits must be preserved.

## Immediate Next-Agent Actions

1. Resume from R1 C4 when the user asks for the next reviewer-comment revision.
2. Keep `main.tex` and `response_letter_TCOM_RV1.tex` synchronized for the next comment as well.
3. Preserve the existing unrelated LaTeX warnings unless the user explicitly asks to clean them.

## Next Safe Resume Point

- Resume from the next user instruction at R1 C4.
