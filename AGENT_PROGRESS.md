# Progress

This is the live-state record for the current paper revision. Historical RV1 details are preserved in `archive/rv1/AGENT_PROGRESS_RV1.md`.

## Current Objective

- Comment 2.1 is implemented and validated. All 54 snapshot instances / 270 method evaluations completed on the RTX 5090 workstation. The single-shell and two-shell plots are stacked in one manuscript column as Fig. 5(a)/(b); blue setup/results passages and the response are synchronized; explicit user acceptance remains pending.
- Both panels now use one fixed population at six times. The two-shell plot uses predetermined selection 0 (initial minimum-span RAAN blocks), 6 snapshots / 30 evaluations, with DuJo leading at all six times. No averaging or shading. All 270 evaluations remain archived, including the unfavorable mixed-selection result.

- Comment 1.2 remains implemented, validated, pending acceptance, and unchanged. The other 12 items retain their drafted plans. All 14 comments remain red and pending.

## Repository State

- Work began on `main` at `4cd632f` (`Render revision text in black`) with a clean worktree.
- `main.tex` now has prior-round blue wrappers removed without changing their enclosed content. `main.bib` and existing experiment assets are unchanged. RV2 manuscript changes are the Comment 1.2 runtime paragraph and the Comment 2.1 added setup/evaluation passages and combined Fig. 5 with single-shell and two-shell subfigures. The RV2 source contains the exact new-round comments. RV1-specific files were moved byte-for-byte into `archive/rv1/`.
- The old blue-to-black color remap was removed from `main.tex`. The active Comment 1.2 addition and its response quotation both use the standard `\blue` macro, as requested by the user. The color change does not change the pending review status.
- The existing three-file agent contract remains active. The four-file migration skill's required `agent_files_init` tool is unavailable. No `AGENT_GOAL.md` was created and `AGENT.md` was not replaced.
- The user authorized committing and pushing this RV2 planning checkpoint to `origin/main` on 2026-09-22. Git history and remote branch state record its publication status.

## Workspace Artifacts

- `response_letter_TCOM_RV2.tex` is the active response draft for `TCOM-TPS-26-1250`, with completed-work replies for Comments 1.2 and 2.1 and planned replies for the remaining items. RV2 is the local round label.
- `TCOM_RV2_decision_letter.txt` is a local-only, gitignored, byte-identical copy of the supplied editor letter and reviewer reports.
- `REVISION_TASK.md` holds submission metadata, item-by-item plan status, and outstanding evidence needs.
- `archive/rv1/AGENT_PROGRESS_RV1.md` preserves the previous progress file verbatim as historical context, including its older repository-state statements.
- `archive/rv1/response_letter_TCOM_RV1.tex` and `archive/rv1/cover_letter_TCOM_RV1.tex` remain prior-round records.

- `archive/rv1/` contains only the RV1 response letter, cover letter, their build files, and the RV1 progress record (18 files). Manuscript variants remain at the repository root.

## Status by Comment

- RV1 comments were recorded as complete in the historical tracker.
- E.1 contains the editor's substantive assessment; 13 numbered reviewer items use the reference's inline `Comment n.m:` labels. Three opening assessments remain unnumbered introductions. Reviewer 1 has two items, Reviewer 2 has four, and Reviewer 3 has seven.
- Comment 1.2 has a completed-work `Response:` and `Manuscript changes:` block quoting its single new manuscript paragraph verbatim. Comment 2.1 also has a completed-work response, verbatim quotations, and the reproduced revised figure. The remaining 12 entries retain planned responses and changes. All 14 comments remain red and pending; implementation does not constitute approval.

## Rolling Progress Log

- 2026-09-23. Committed and pushed manuscript/evidence checkpoint `4ad8122` and simulator implementation `e85a867` to their respective `origin/main` branches, as requested. This follow-up records the publication state. Comment review statuses remain pending.

- 2026-09-23. Prepared the user-requested main-branch commit/push in the manuscript repository, covering synchronized Comment 2.1 source, stacked single-/two-shell plots, complete experiment evidence, and reproducible code patch. Removed one trailing space; manuscript wording is unchanged. Existing build/quotation/figure checks passed. The separate simulator checkout remains uncommitted; all comment review statuses remain pending.

- 2026-09-23. Synchronized Comment 2.1 to the user-edited manuscript: copied the latest Fig. 5 caption verbatim and aligned the performance-summary wording. Verified all five blue text/caption/subcaption blocks against main.tex. Preserved the user's latest response shortening and did not alter the manuscript. Rebuilt both PDFs and inspected main page 10 and response page 6; no undefined references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Shortened only Comment 2.1 performance/scope paragraphs to two sentences, preserving the performance result and continuous-feasibility/precession limits. Rebuilt and inspected response page 4; refreshed the PDF. Pending status unchanged.

- 2026-09-23. Reordered only the Comment 2.1 opening response: first clarified that the original evaluation was not a single static snapshot, then explained fixed membership and propagation to six times in Fig. 5(a), then introduced the added two-shell case in Fig. 5(b). Retained performance, limitations, all manuscript quotations, and other responses. Two direct LaTeX passes succeeded with no unresolved references or overfull boxes; inspected page 4 and refreshed the response PDF. Comment 2.1 remains pending.

- 2026-09-23. Matched the two-shell presentation to the single-shell case at the user's explicit request: selection 0, one fixed population, six snapshots, no averaging. The plotter reads exactly 30 matching records and preserves the original style. Verified DuJo leads on both metrics at all six times; 316–349 inter-cluster links are selected. Updated manuscript performance/caption, only Comment 2.1 response, and evidence metadata/docs/patch. All other selections and unfavorable results are preserved. Synchronized code/PDF/docs to the isolated 5090 run. Both documents compile without unresolved references or overfull boxes; inspected main page 10 and response page 6 and refreshed PDFs. Comment 2.1 remains pending.

- 2026-09-23. Added one performance sentence to the concise structured-shell passage. DuJo leads at all six single-shell times and has the highest two-shell mean throughput/served ratio across three selections. Verified the latter directly against the saved CSV at each time; this does not claim a win in every individual mixed instance. Synchronized the response quotation, rebuilt and visually checked both PDFs with no unresolved references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Simplified the requested results passage to two sentences introducing the single-shell/two-shell comparison and multiple link-geometry instances over six times. Removed the longer replacement discussion as directed; detailed experimental results and limitations remain in the response and evidence. Synchronized the quotation and removed the stale claim that the manuscript explicitly states the limitations. Rebuilt both PDFs, inspected main page 10 and response page 5, and verified quotation equality; no unresolved references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Rewrote the requested structured-shell discussion as two concise blue paragraphs comparing single-shell and two-shell results. Explained six propagated snapshot times, three overlapping fixed populations / 18 two-shell instances, 17/18 DuJo wins with the unfavorable case, selected inter-cluster links, and limits on continuous feasibility and long-term precession. Synchronized the Comment 2.1 quotation verbatim; other response blocks are unchanged. Direct isolated builds have no undefined references or overfull boxes; inspected main page 10 and response page 5. Review PDFs refreshed; Comment 2.1 remains pending.

- 2026-09-23. Rewrote only the requested setup line to introduce the 1000-satellite single-shell and 500+500 two-shell configurations and fixed membership over the six offsets. Preserved the user's removal of the longer setup paragraphs; replaced their stale response quotation with the new sentence pair verbatim. Both documents rebuilt without unresolved references or overfull boxes; Comment 2.1 remains pending.

- 2026-09-23. Changed the combined Fig. 5 to one manuscript column, stacking subfigures (a)/(b) vertically. Matched the response figure layout. Plot assets, data, captions, and pending statuses are unchanged. Rebuilt both PDFs with no undefined references or overfull boxes; inspected the stacked figure on manuscript page 10 and response page 6. Refreshed the review PDFs.

- 2026-09-23. Combined the single-shell and two-shell assets into one full-width Fig. 5 with side-by-side subfigures (a)/(b), as requested. Both assets and their data remain unchanged, with no shading. Added synchronized blue subcaptions and a shared caption, preserved panel-specific references through subfigure labels, and reproduced the combined figure in Comment 2.1. Later figure numbering returns to its original sequence. Direct isolated builds passed with no unresolved references or overfull boxes; inspected manuscript page 11 and response page 6. All other response blocks and pending statuses remain unchanged. Refreshed review PDFs.

- 2026-09-23. Removed shaded ranges from Fig. 6 at the user's request, retaining the same mean curves, markers, colors, and layout. Synchronized both captions, the Comment 2.1 response summary, evidence documentation, and reproduction script. Per-selection data are unchanged; Comment 2.1 remains pending. Rebuilt both documents and inspected main page 10 and response page 6; no shading, unresolved references, or overfull boxes. Refreshed both review PDFs and verified quotation equality and code-patch consistency.

- 2026-09-23. At the user's request, restored the original Fig. 5, caption, setup wording, heading, and discussion, then added the two-shell experiment as Fig. 6 using the same stacked two-panel layout, size, legend, colors, and markers. Means/ranges use all three mixed selections. Narrowed the blue passages and Comment 2.1 to the displayed 18 snapshots, preserving the unfavorable case and all 270 archived evaluations. The full-width plot remains an unused supporting artifact. Added a dedicated plotter and synchronized it, its PDF, and instructions to the isolated 5090 run; no simulations were rerun.

- 2026-09-22. Completed Comment 2.1. All 270 evaluations and all pilot/full jobs passed. Tailscale connectivity was restored after a temporary interruption; the detached run completed normally. Added the full-width two-row/three-column figure, blue setup/evaluation changes, explicit 53/54 result and 0.4% exception, selection-overlap disclosure, and temporal-scope limitation. Updated only Comment 2.1 with verbatim excerpts and the figure. Evidence and a reproducible code patch are in `revision_data/comment_2_1/`. All comments remain pending.

- 2026-09-22. All 15 pilot evaluations passed matched-input, feasible-matching, and throughput consistency checks. Three regression tests passed (RAAN wraparound, shifted selection membership, and rejection of failures/nonfinite states at any evaluation epoch). Full-matrix execution started with six workers on the RTX 5090 workstation. The last confirmed remote count was 244/270 evaluations with no failed jobs; 180 records are synchronized locally. SSH to both the campus and Tailscale IPs subsequently timed out. The detached run may continue remotely; awaiting restored connectivity before retrieving the full results. Selected TLE epochs span 2025-07-14 23:55 UTC to 2025-07-16 06:00 UTC.

- 2026-09-22. User specified the 5090 GPU workstation. Confirmed the configured host at `10.34.23.184` has an RTX 5090 and working CUDA. Geometry checks use CPU; pilots/full DRL inference will use GPU 0, while DuJo and heuristic computations remain CPU-based.

- 2026-09-22. Implemented opt-in historical-epoch TLE validation and shifted cluster selection, a gated/resumable multi-shell driver, and a complete-matrix plotter in `../leo-sat-flow`. Running an isolated local-source snapshot at `/home/zhouyou/tcom-comment21-ail` on the configured workstation; existing remote edits are preserved. Epoch-valid catalogue has 7,960 records; the original selected block matches saved IDs/order exactly. All 54 geometry checks passed, including Skyfield agreement and feasible inter-shell candidates in all 18 mixed instances. All three five-method pilots passed with GPU DRL inference. The full matrix is running with six workers; no final results claims have been written.

- 2026-09-22. Started implementation of the approved Comment 2.1 experiment plan. Code work is in `../leo-sat-flow`; manuscript claims will be updated only after measured results pass validation.

- 2026-09-22. Updated the Comment 1.2 response summary to use "Further research can..." and explain that learned multiplier estimation retains matching, routing, and rate allocation. The manuscript quotation remains verbatim; all other responses and pending statuses are unchanged. Preparing the user-requested commit and push to `origin/main`.

- 2026-09-22. Reframed the DeepLaDu extension as "Further research can accelerate..." at the user's request and made the following sentence conditional. Synchronized the response summary and verbatim quotation while retaining the existing citation and blue highlighting.

- 2026-09-22. Replaced "our related work" with third-person attribution to Gu et al. in the DeepLaDu sentence and synchronized both the response summary and verbatim quotation. Recorded the third-person related-work preference in the harness. Both documents rebuilt with no undefined references/citations or overfull boxes; review PDFs were refreshed. Comment 1.2 remains pending.

- 2026-09-22. Added two sentences to the existing blue Comment 1.2 paragraph describing DeepLaDu as an offline-trained GNN that approximates optimal multipliers in one forward pass, replacing iterative online dual updates while retaining decision conversion. Used the existing `gu2026deepladu` reference, synchronized the response and verbatim quotation, and added the response bibliography needed to resolve that citation. No bibliography-database or neighboring-project changes were made. Validation passed; Comment 1.2 remains pending.

- 2026-09-22. Removed the unsolicited `\looseness=-1` command at the user's direction. The new blue paragraph now uses normal LaTeX line breaking; its wording is unchanged. Refreshed the manuscript review PDF and recorded the no-unsolicited-line-fitting preference in the harness.

- 2026-09-22. Changed the Comment 1.2 manuscript addition from violet to blue at the user's request, preserving its wording and pending status. Refreshed the manuscript review PDF.

- 2026-09-22. Implemented the revised, narrow Comment 1.2 plan after the earlier version was reverted. Added only one violet paragraph after the computing-time discussion, preserving every pre-existing manuscript passage, including the RV1 system-operation remark and ATP discussion. Updated only Comment 1.2 with the agreed response and verbatim blue quotation. No equation, citation, bibliography, figure, simulation, or neighboring-project changes were made.

- 2026-09-22. Prepared the RV2 planning checkpoint for the user-requested commit and push to `main`. Verified byte-identical relocation of the four previously tracked RV1 artifacts, preservation of all 14 pending plans, and complete rollback of the Comment 1.2 implementation. The local decision letter and generated build/review artifacts remain ignored. `git diff --check` passed.

- 2026-09-22. Reverted the Comment 1.2 implementation at the user's request. Restored the pre-implementation manuscript, planned response, and revision brief; Comment 1.2 remains planned and pending. Restored the previous response-draft PDF and removed the Comment 1.2 manuscript review PDF. Earlier workspace changes were preserved.

- 2026-09-08. Created a separate RV2 response source with the existing TCOM title and authors, the reference IEEE one-column response layout, red pending-input notices, and a commented point-by-point template. Did not reuse the old manuscript ID, decision date, reviewer set, or revision claims.
- 2026-09-08. Imported the reference Revision-Response Playbook into the existing harness and reconciled quotation omission notation to its literal `...` convention. Added rules for new-round source intake, historical preservation, and response-local labels.
- 2026-09-08. Created the current-round revision brief, archived the prior progress record, and refreshed this tracker from the actual repository state.
- 2026-09-08. Added narrowly scoped ignore rules for RV2 generated outputs and temporary/output directories.

- 2026-09-08. Archived the RV1 response and cover-letter materials and historical progress. The initially overbroad manuscript snapshots were subsequently removed at the user's direction.

- 2026-09-08. Preserved the supplied decision letter verbatim, populated all 17 source blocks in RV2, and replaced unknown submission metadata with `TCOM-TPS-26-1250`. Original typos, punctuation, Unicode hyphens, theta, and reviewer numbering remain in the source. Added distinct navigation labels and pending response/planned-change fields without drafting substantive answers.

- 2026-09-08. Reset manuscript revision markup at the user's request by unwrapping 58 `\blue{...}` calls and 2 grouped `\color{blue}` blocks. Preserved the enclosed prose, equations, headings, labels, citations, and comments. Removed the old blue-to-black override while retaining the reusable color macro. Refreshed `main.pdf` from the validated build.

- 2026-09-08. Narrowed `archive/rv1/` to response-related files only after the user corrected the scope. Removed dependency snapshots and archive packaging, restored tracked manuscript outputs to the root, and replaced the overly broad archival harness rules.

- 2026-09-08. Corrected the RV2 scaffold to follow the reference response letter directly after the user rejected the added structure. Removed the scaffold banner, separate comment headings, repeated numbering, custom comment environments, forced page breaks, bracketed placeholders, and administrative email content. Retained all reviewer wording and the substantive editor paragraph, with inline comment labels and blank response/manuscript-change fields.

- 2026-09-08. Compared the newly pasted decision letter with `TCOM_RV2_decision_letter.txt`. The only difference was the missing `28-Aug-2026` date and following blank line. Updated the saved letter to match the latest attachment byte-for-byte; all remaining content was already identical. Updated date metadata without changing the response or manuscript.

- 2026-09-08. Added `/TCOM_RV2_decision_letter.txt` to `.gitignore` at the user's request. The file was untracked and remains present locally. Verified the ignore rule.

- 2026-09-08. Drafted plans for all 14 comments after checking the current manuscript, neighboring ToN responses, and local ATP/terminal-availability simulation code read-only. Plans cover longer acquisition times and cold starts, controller timing, broader constellation tests, readability/proofreading, suggested literature, propagation delay, unserved-demand diagnostics, theta annotation, gateway sensitivity, payload scope, installed terminal counts, and FOR interpretation. Distinguished existing six-snapshot tests from proposed extensions and expected available terminals from mounted terminals. No neighboring numerical results were reused as DuJo evidence; the manuscript, bibliography, and simulation assets were not edited.

## Validation

- 2026-09-23, Fig. 6 presentation update. Direct isolated builds in `tmp/comment-2-1-two-shell/build/` produced a 15-page manuscript and 12-page response. Inspected manuscript pages 8–11 and response pages 4–6. Fig. 6 follows Fig. 5 immediately on page 10. References/citations resolve and neither document has overfull boxes; the manuscript retains three existing underfull hboxes and one underfull vbox. All six quoted blue blocks/caption match. Original manuscript wording and Fig. 5 are preserved byte-for-byte; only additions remain relative to HEAD. Other responses, protected figures/bibliography, and neighboring ToN files are unchanged. Refreshed both review PDFs, evidence/plotter hashes, and the code patch, whose reverse-application check passed. Later figures shift by one; reviewer wording and inactive response blocks remain unchanged.

- 2026-09-22, Comment 2.1. All 54 geometry checks agree with Skyfield (maximum position difference 3.54e-10 km); the original selection matches saved membership/order exactly. All 270 evaluations passed matching feasibility, throughput bounds, and identical-input fingerprint checks. Three focused regression tests passed; incomplete plot inputs are rejected. Local simulator hashes match the isolated run; the code patch passes a reverse-application dry run.
- Direct isolated LaTeX/BibTeX builds in `tmp/comment-2-1/build/` produced a 15-page manuscript and 12-page response with no undefined references/citations or overfull boxes. The manuscript retains three existing underfull hboxes and one underfull vbox; the response has no LaTeX/box warnings. The new figure uses embedded TrueType fonts; Poppler warnings from unchanged older figures also occur in the preceding manuscript PDF. Inspected main pages 8–11 and response pages 4–6, including the reproduced figure/caption.
- Verified all five new manuscript paragraphs and the caption are quoted verbatim; all reviewer wording and every other response are unchanged. The manuscript diff is confined to the setup and structured-evaluation regions. Comment 1.2, bibliography, original figure artifact, and neighboring ToN sources are unchanged. `git diff --check` passed in both repositories.
- Current review PDFs are `output/pdf/main_comment_2_1_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`. Raw per-method JSON and logs are preserved in `../leo-sat-flow/sim_alg_v1_res/test_tcom_multishell/comment-2-1-20260922-ail/`; the isolated remote run is `/home/zhouyou/tcom-comment21-ail/` on `100.122.104.12` (campus IP `10.34.23.184`). Existing remote working-copy edits were not touched.

- 2026-09-22, response wording update. Two direct isolated LaTeX passes completed without warnings or unresolved references/citations. Inspected the affected page and refreshed the response PDF. Verified exact quotation equality, exactly one added manuscript paragraph relative to HEAD, and unchanged reviewer wording and other response blocks. `git diff --check` passed.

- 2026-09-22, DeepLaDu extension. Verified that the latest manuscript change adds exactly two sentences within the existing blue paragraph and that the full paragraph is quoted verbatim in Comment 1.2. All other response entries and reviewer wording are unchanged; the response bibliography now contains the existing `gu2026deepladu` entry. The bibliography database and neighboring ToN sources are unchanged.
- Rebuilt both sources with direct LaTeX/BibTeX passes in `tmp/comment-1-2-learning/build/`. The manuscript has 15 pages and the response has 10 pages. Both have no undefined citations/references or overfull boxes. The manuscript has the three existing underfull hboxes and one underfull vbox; the response has no LaTeX or box warnings. Page renders and affected-page inspection confirmed the blue addition, citation resolution, and response bibliography. No manual line-fitting commands were added. Refreshed both review PDFs; `git diff --check` passed. Pre-extension snapshots and renders are in `tmp/comment-1-2-learning/`.

- 2026-09-22, focused Comment 1.2 revision. Verified that removing the single violet paragraph and its local line-fitting command restores `main.tex` byte-for-byte to the pre-edit source. The paragraph is quoted verbatim in the response; all reviewer wording and every response outside Comment 1.2 are unchanged. All 14 comments remain red/pending. Protected-file hashes confirm that the bibliography, figures, root PDFs, other tracked files, and neighboring ToN response are unchanged.
- Direct isolated LaTeX builds produced a 15-page manuscript and 10-page response with no undefined references/citations or overfull boxes. The manuscript retains three pre-existing underfull hbox warnings in unrelated passages; the response has no LaTeX or box warnings. Rendered all pages, inspected the document overviews and affected pages, and used local line-breaking adjustments to avoid a dangling word fragment without changing the approved wording. `git diff --check` passed.
- Review PDFs are `output/pdf/main_comment_1_2_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`. Pre-edit snapshots, the previous response PDF, builds, and renders are preserved in `tmp/comment-1-2-focused/`. Root PDFs were not overwritten. Earlier validation entries below concern the pre-implementation draft.

- Latest reference-format audit verified exact wording for E.1, all 13 reviewer comment bodies, and all three reviewer opening assessments. Only original list markers were replaced by reference-style comment labels. The full supplied source text remains unchanged.
- Two direct `pdflatex` passes produced the nine-page planned-response draft with no LaTeX warnings, undefined references/citations, or overfull/underfull boxes. All pages were inspected; the final two pages were reinspected after shortening response prose to remove a one-line last page.
- Verified all 17 original source blocks (14 comments and three opening assessments) are byte-identical to the pre-draft response source. All 14 response/change-plan pairs are populated. SHA-256 checks confirm `main.tex`, `main.bib`, and the local decision letter are unchanged during drafting; the decision letter still matches the latest attachment byte-for-byte and remains gitignored. `git diff --check` passed.
- Draft preview is `output/pdf/response_letter_TCOM_RV2_draft.pdf`; build files are in `tmp/rv2-build/` and this turn's comparison/QA files are in `tmp/rv2-plan/`.

- Archive correction verified all 18 retained response-related files are byte-identical, restored five `main_tracked_changes.*` files to their original root locations, and removed the 16 agent-created dependency copies plus the extra README and manifest. All pre-existing active root files were verified unchanged before tracker updates. `git diff --check` passed.

- Manuscript cleanup validation used brace-aware removal of color markup, verified no blue wrappers remain in the document body, and successfully built both pre-cleanup and post-cleanup sources in isolated directories. Both PDFs have 15 pages, zero overfull boxes, zero undefined references/citations, and the same four underfull warnings. Minor line/page-break changes followed removal of color scopes; affected layout was inspected. `git diff --check` passed. Retained RV1 response files remain unchanged.

- 2026-09-08. Independently rechecked `main.tex` against both the saved pre-edit source and committed HEAD. Tokenized TeX to remove only the 58 blue wrappers and two color groups, removed the old blue-to-black definition, and accounted for one trailing space on the Baseline Methods heading. The reconstructed source matched the current file byte-for-byte. Confirmed no manuscript wording, equations, citations, labels, or headings changed; this audit made no manuscript edits.

## Current Blockers or Risks


- Comment 1.2 clarifies timing limitations without establishing end-to-end deployment feasibility. Comment 2.1 establishes results only for the tested clusters/selections and three-hour window. Experiments and revisions for the other 12 items remain planned.
- The updated supplied letter confirms the decision date as 28-Aug-2026 and specifies a 60-day revision window.
- Four-file contract migration was not performed because the manuscript-writing scaffold skill requires an unavailable initialization tool. Response workflow updates use the existing three-file contract.
- The previous tracker records an external-subdocument post-processing issue in `latexmkrc`. Validate the RV2 scaffold with direct `pdflatex` passes and existing manuscript references to avoid external BibTeX/post-processing side effects.

## Next Safe Resume Point

- Review the completed Comment 2.1 manuscript, response, figure, and evidence with the user. Keep it red/pending until explicitly accepted. No automatic move to another review item, commit, or push. Comment 1.2 remains pending and unchanged. The paper checkpoint includes Comment 2.1 source, figures, and evidence; publication is recorded in Git history. The simulator implementation is committed as e85a867 and pushed to leo-sat-flow origin/main; it is also preserved in the paper's reproducible patch. The run is complete and does not need restarting.
