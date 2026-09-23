# Round 2 Revision Brief

This is a lower-precedence current-state brief. Read the three core agent files first.

## Round and Sources

- Active manuscript identifier is `TCOM-TPS-26-1250`; the editor is Dr. Jianqing Liu, IEEE Transactions on Communications.
- The decision letter is dated 28-Aug-2026 and recommends a major revision within 60 days.
- RV2 remains the local round label. The new identifier is used in `response_letter_TCOM_RV2.tex`.
- The local-only, gitignored `TCOM_RV2_decision_letter.txt` preserves the entire supplied attachment byte-for-byte, including the administrative instructions and reviewer report headers.
- Active response source is `response_letter_TCOM_RV2.tex`; the compiled response draft is `output/pdf/response_letter_TCOM_RV2_draft.pdf`.
- The manuscript content baseline is `main.tex` at `4cd632f`, with all prior-round blue wrappers and the blue-to-black override now removed. RV2 changes comprise the blue Comment 1.2 runtime paragraph and the Comment 2.1 added simulation setup/evaluation passages and combined Fig. 5 containing single-shell and two-shell subfigures. Comment 1.2 is unchanged by this extension; both items remain pending acceptance.
- Prior-round response and cover-letter files, their build files, and response progress remain in `archive/rv1/`. Manuscript files and figures are outside this response-only archive.

## Review-Item State

| Local item | Source item | State |
| --- | --- | --- |
| E.1 | Editor substantive assessment paragraph | Planned response drafted, pending |
| 1.general | Reviewer 1 opening assessment | Preserved as an unnumbered introduction |
| 1.1 | Reviewer 1 item 1 | Planned response drafted, pending |
| 1.2 | Reviewer 1 item 2 | Implemented, synchronized, and validated; acceptance pending |
| 2.general | Reviewer 2 opening assessment | Preserved as an unnumbered introduction |
| 2.1 | Reviewer 2 item 1 | Implemented, synchronized, and validated; acceptance pending |
| 2.2 | Reviewer 2 item 2 | Planned response drafted, pending |
| 2.3 | Reviewer 2 item 3 | Planned response drafted, pending |
| 2.4 | Reviewer 2 item 4 | Planned response drafted, pending |
| 3.general | Reviewer 3 opening assessment | Preserved as an unnumbered introduction |
| 3.1 | Reviewer 3 item 1 | Planned response drafted, pending |
| 3.2 | Reviewer 3 item 2 | Planned response drafted, pending |
| 3.3 | Reviewer 3 item 3 | Planned response drafted, pending |
| 3.4 | Reviewer 3 item 4 | Planned response drafted, pending |
| 3.5 | Reviewer 3 item 5 | Planned response drafted, pending |
| 3.6 | Reviewer 3 item 6 | Planned response drafted, pending |
| 3.7 | Reviewer 3 item 7 | Planned response drafted, pending |

- The response follows `../2025-zg-isl-routing/response_letter_ToN_RR.tex` directly. Comments 1.2 and 2.1 have completed `Response:` and `Manuscript changes:` fields with verbatim quotations; Comment 2.1 also reproduces the revised figure. The other 12 entries retain their drafted responses and planned changes. Three reviewer opening assessments remain unnumbered introductory paragraphs, followed by topic-specific acknowledgments.
- Comment wording is unchanged. Original list markers are replaced with reference-style `Comment 1.1:` labels, without duplicate numbering. All comments remain bold red and pending.
- The complete administrative editor email remains in `TCOM_RV2_decision_letter.txt`; only its substantive assessment appears as E.1 in the response.

## Evidence Gaps

- Plans are grounded in the current manuscript, neighboring responses, and read-only inspection of the ATP and terminal-availability simulation code. Comment 2.1 now has 270 completed evaluations across 54 matched snapshot instances. The manuscript displays mixed selection 0 (6 snapshots / 30 evaluations), where DuJo leads at all six times. The other selections, including the 0.4% deficit to SaTE/MRate, remain archived. The complete archived matrix has 53/54 wins. Comment 1.2 adds one deployment-limitation paragraph; the other 12 item plans remain unimplemented.
- Outstanding studies include longer ATP settings (60/120 s), cold-start replay, long-term epoch/precession coverage, route propagation delay, throughput bottleneck and optimization-gap diagnostics, gateway-count sensitivity, and explicit two-/three-/four-terminal layouts.
- Comment 1.2 now distinguishes measured optimization/conversion time from additional control-cycle overhead, states conditional advance-planning requirements, and identifies incorporating DeepLaDu as a further-research direction to accelerate approximate multiplier estimation. Those overheads and end-to-end feasibility remain unmeasured. Payload scope, FOR axis interpretation, served-demand accounting, figure edits, and proofreading remain planned.
- The two suggested routing studies have been identified for review. Full technical comparisons and verified bibliography entries remain to be added during implementation.

## Comment 2.1 Evidence and Review

- Two TLE-derived clusters (53.22 degrees / 15.087 rev/day and 43 degrees / 15.024 rev/day), 1,000 satellites per configuration, and a 500+500 mixture were evaluated using three overlapping selections at six offsets. All methods used matched snapshot inputs, fixed traffic, and the frozen PG checkpoint; DuJo used 500 updates and final-iterate conversion.
- Fig. 5 combines the unchanged single-shell plot (a) and two-shell plot (b) stacked vertically in one column, each with the same stacked throughput/served-ratio layout. Panel (b) displays the mixed configuration only, using the first predetermined fixed population at six times, with no averaging or shading, as requested by the user. Overlapping membership and the lack of continuous-schedule or long-term-precession validation are stated explicitly. The complete three-configuration data and full-width plot remain supporting artifacts. No simulations were rerun for this presentation change.
- `revision_data/comment_2_1/` contains the complete CSV, summaries, manifest, geometry/validation records, execution settings, and implementation patch. The driver, plotter, tests, and reproduction instructions are in `../leo-sat-flow`.

## Next Item-Local Step

- 2026-09-23. Synchronized Comment 2.1 to the user-edited manuscript: copied the latest Fig. 5 caption verbatim and aligned the performance-summary wording. Verified all five blue text/caption/subcaption blocks against main.tex. Preserved the user's latest response shortening and did not alter the manuscript. Rebuilt both PDFs and inspected main page 10 and response page 6; no undefined references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Shortened only Comment 2.1 performance/scope paragraphs to two sentences, preserving the performance result and continuous-feasibility/precession limits. Rebuilt and inspected response page 4; refreshed the PDF. Pending status unchanged.

- 2026-09-23. Reordered only the Comment 2.1 opening response: first clarified that the original evaluation was not a single static snapshot, then explained fixed membership and propagation to six times in Fig. 5(a), then introduced the added two-shell case in Fig. 5(b). Retained performance, limitations, all manuscript quotations, and other responses. Two direct LaTeX passes succeeded with no unresolved references or overfull boxes; inspected page 4 and refreshed the response PDF. Comment 2.1 remains pending.

- 2026-09-23. Matched the two-shell presentation to the single-shell case at the user's explicit request: selection 0, one fixed population, six snapshots, no averaging. The plotter reads exactly 30 matching records and preserves the original style. Verified DuJo leads on both metrics at all six times; 316–349 inter-cluster links are selected. Updated manuscript performance/caption, only Comment 2.1 response, and evidence metadata/docs/patch. All other selections and unfavorable results are preserved. Synchronized code/PDF/docs to the isolated 5090 run. Both documents compile without unresolved references or overfull boxes; inspected main page 10 and response page 6 and refreshed PDFs. Comment 2.1 remains pending.

- 2026-09-23. Added one performance sentence to the concise structured-shell passage. DuJo leads at all six single-shell times and has the highest two-shell mean throughput/served ratio across three selections. Verified the latter directly against the saved CSV at each time; this does not claim a win in every individual mixed instance. Synchronized the response quotation, rebuilt and visually checked both PDFs with no unresolved references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Simplified the requested results passage to two sentences introducing the single-shell/two-shell comparison and multiple link-geometry instances over six times. Removed the longer replacement discussion as directed; detailed experimental results and limitations remain in the response and evidence. Synchronized the quotation and removed the stale claim that the manuscript explicitly states the limitations. Rebuilt both PDFs, inspected main page 10 and response page 5, and verified quotation equality; no unresolved references or overfull boxes. Comment 2.1 remains pending.

- 2026-09-23. Rewrote the requested structured-shell discussion as two concise blue paragraphs comparing single-shell and two-shell results. Explained six propagated snapshot times, three overlapping fixed populations / 18 two-shell instances, 17/18 DuJo wins with the unfavorable case, selected inter-cluster links, and limits on continuous feasibility and long-term precession. Synchronized the Comment 2.1 quotation verbatim; other response blocks are unchanged. Direct isolated builds have no undefined references or overfull boxes; inspected main page 10 and response page 5. Review PDFs refreshed; Comment 2.1 remains pending.

2026-09-23. Rewrote only the requested setup line to introduce the 1000-satellite single-shell and 500+500 two-shell configurations and fixed membership over the six offsets. Preserved the user's removal of the longer setup paragraphs; replaced their stale response quotation with the new sentence pair verbatim. Both documents rebuilt without unresolved references or overfull boxes; Comment 2.1 remains pending.

Review the implemented Comment 2.1 with the user. Keep it pending until explicitly accepted and preserve all other statuses. Current PDFs are `output/pdf/main_comment_2_1_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`; validation and execution details are in `AGENT_PROGRESS.md`.
