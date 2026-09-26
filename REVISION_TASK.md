# Round 2 Revision Brief

This is a lower-precedence current-state brief. Read the three core agent files first.

## Round and Sources

- Active manuscript identifier is `TCOM-TPS-26-1250`; the editor is Dr. Jianqing Liu, IEEE Transactions on Communications.
- The decision letter is dated 28-Aug-2026 and recommends a major revision within 60 days.
- RV2 remains the local round label. The new identifier is used in `response_letter_TCOM_RV2.tex`.
- The local-only, gitignored `TCOM_RV2_decision_letter.txt` preserves the entire supplied attachment byte-for-byte, including the administrative instructions and reviewer report headers.
- Active response source is `response_letter_TCOM_RV2.tex`; the compiled response draft is `output/pdf/response_letter_TCOM_RV2_draft.pdf`.
- The manuscript content baseline is `main.tex` at `4cd632f`, with all prior-round blue wrappers and the blue-to-black override now removed. RV2 changes comprise the blue Comment 1.2 runtime paragraph and the Comment 2.1 added simulation setup/evaluation passages and combined Fig. 5 containing single-shell and two-shell subfigures. Comment 1.2 is unchanged by this extension; Comments 1.2 and 2.1 are accepted.
- Prior-round response and cover-letter files, their build files, and response progress remain in `archive/rv1/`. Manuscript files and figures are outside this response-only archive.

## Review-Item State

| Local item | Source item | State |
| --- | --- | --- |
| E.1 | Editor substantive assessment paragraph | Planned response drafted, pending |
| 1.general | Reviewer 1 opening assessment | Preserved as an unnumbered introduction |
| 1.1 | Reviewer 1 item 1 | Implemented, validated, and accepted |
| 1.2 | Reviewer 1 item 2 | Accepted; comment marked black |
| 2.general | Reviewer 2 opening assessment | Preserved as an unnumbered introduction |
| 2.1 | Reviewer 2 item 1 | Accepted; comment marked black |
| 2.2 | Reviewer 2 item 2 | Accepted; comment marked black |
| 2.3 | Reviewer 2 item 3 | Accepted; comment marked black |
| 2.4 | Reviewer 2 item 4 | Accepted; comment marked black |
| 3.general | Reviewer 3 opening assessment | Preserved as an unnumbered introduction |
| 3.1 | Reviewer 3 item 1 | Implemented and validated; pending review |
| 3.2 | Reviewer 3 item 2 | Implemented and validated; pending review |
| 3.3 | Reviewer 3 item 3 | Figure updated by user; response completed, pending review |
| 3.4 | Reviewer 3 item 4 | Planned response drafted, pending |
| 3.5 | Reviewer 3 item 5 | Planned response drafted, pending |
| 3.6 | Reviewer 3 item 6 | Planned response drafted, pending |
| 3.7 | Reviewer 3 item 7 | Planned response drafted, pending |

- The response follows `../2025-zg-isl-routing/response_letter_ToN_RR.tex` directly. Comments 1.2 and 2.1 have completed `Response:` and `Manuscript changes:` fields with verbatim quotations; Comment 2.1 also reproduces the revised figure. Comments 2.2 and 2.3 have completed readability and proofreading responses; the other 10 entries retain drafted plans. Three reviewer opening assessments remain unnumbered introductory paragraphs, followed by topic-specific acknowledgments.
- Comment wording is unchanged. Original list markers are replaced with reference-style `Comment 1.1:` labels, without duplicate numbering. Comments 1.1, 1.2, and 2.1–2.4 are accepted and bold black; other substantive comments remain red and pending.
- The complete administrative editor email remains in `TCOM_RV2_decision_letter.txt`; only its substantive assessment appears as E.1 in the response.

## Evidence Gaps

- Plans are grounded in the current manuscript, neighboring responses, and read-only inspection of the ATP and terminal-availability simulation code. Comment 2.1 now has 270 completed evaluations across 54 matched snapshot instances. The manuscript displays mixed selection 0 (6 snapshots / 30 evaluations), where DuJo leads at all six times. The other selections, including the 0.4% deficit to SaTE/MRate, remain archived. The complete archived matrix has 53/54 wins. Comment 1.2 adds one deployment-limitation paragraph; Comment 2.2 now implements figure readability; Comment 2.3 implements proofreading; the other 10 item plans remain unimplemented.
- Outstanding studies include longer ATP settings (60/120 s), cold-start replay, long-term epoch/precession coverage, route propagation delay, throughput bottleneck and optimization-gap diagnostics, gateway-count sensitivity, and explicit two-/three-/four-terminal layouts.
- Comment 1.2 now distinguishes measured optimization/conversion time from additional control-cycle overhead, states conditional advance-planning requirements, and identifies incorporating DeepLaDu as a further-research direction to accelerate approximate multiplier estimation. Those overheads and end-to-end feasibility remain unmeasured. Payload scope, FOR axis interpretation, served-demand accounting and proofreading remain planned.
- The two suggested routing studies have been identified for review. Full technical comparisons and verified bibliography entries remain to be added during implementation.

## Comment 2.1 Evidence and Review

- Two TLE-derived clusters (53.22 degrees / 15.087 rev/day and 43 degrees / 15.024 rev/day), 1,000 satellites per configuration, and a 500+500 mixture were evaluated using three overlapping selections at six offsets. All methods used matched snapshot inputs, fixed traffic, and the frozen PG checkpoint; DuJo used 500 updates and final-iterate conversion.
- Fig. 5 combines the unchanged single-shell plot (a) and two-shell plot (b) stacked vertically in one column, each with the same stacked throughput/served-ratio layout. Panel (b) displays the mixed configuration only, using the first predetermined fixed population at six times, with no averaging or shading, as requested by the user. Overlapping membership and the lack of continuous-schedule or long-term-precession validation are stated explicitly. The complete three-configuration data and full-width plot remain supporting artifacts. No simulations were rerun for this presentation change.
- `revision_data/comment_2_1/` contains the complete CSV, summaries, manifest, geometry/validation records, execution settings, and implementation patch. The driver, plotter, tests, and reproduction instructions are in `../leo-sat-flow`.

## Next Item-Local Step

Review Comment 3.2’s served-demand definition and cached-state diagnostics. Keep 3.1 and 3.2 red pending acceptance; other statuses unchanged. Current PDFs are `output/pdf/main_comment_3_2_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`.

### Historical steps

- 2026-09-23. Rechecked the 5090 workstation at the user's direction. Recovered exact raw runs for Figs. 3/7 into local ignored data directories. Located Fig. 5(a) in the load-scaling CSV at load 0.0001 and verified all ten curves against the original vector PDF (maximum error 0.000011 pt). Figs. 5(b)/6/10 also have saved data. Only the augmented DRL/SaTE merged inputs for Figs. 4/8/9 remain unlocated; older base runs are not substitutes. Recorded paths/hashes in revision_data/comment_2_2/data_inventory.json. Current figure styling is unchanged.

Review Comment 2.2 readability changes: approximately 11% larger fonts in Figs. 3–10, 25% wider bars in Figs. 4/8, and two abbreviated axis labels. Values are unchanged. Current PDFs are `output/pdf/main_comment_2_2_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`. Reproduction sources and geometry checks are in `revision_data/comment_2_2/` and the code repository. The isolated 5090 copy is synchronized. All comments remain pending; these readability edits are uncommitted.

Previous publication checkpoint: manuscript/evidence `4ad8122` (tracking update `1c553ab`) and simulator implementation `e85a867` were pushed to their respective `origin/main` branches on 2026-09-23.

- Fig. 8 readability follow-up: bars are now 40% wider than the original (12% wider than the first readability edit); Fig. 4 remains at 25%. Figure rendered and both documents compiled successfully. Comment 2.2 remains pending.

- 2026-09-23 Fig. 8 follow-up: displayed LCT 0.8/1.2/1.6/2.0 and FOR 30/50/70/90 only, retaining all original source data. Regenerated from recovered six-decimal tables with wider bars and 10-point fonts; verified all 48 bar heights against retained rows and inspected rendering. Updated response 2.2, compiled both documents, and refreshed review PDFs. Pending review; uncommitted.

- 2026-09-23 Comment 2.2 response finalized around the completed font enlargement, wider bars, and four displayed cases per Fig. 8 panel. Revised Figs. 4 and 8 reproduced in the letter; reviewer wording and other responses preserved. No prose addition to main.tex is needed for this graphics-only revision. Comment 2.2 remains red and pending explicit acceptance.

- Comment 2.2: removed the manuscript-change lead-in and both reproduced figures at the user’s request. Retained only the response describing the completed figure changes. Comment remains pending; other responses unchanged.

- Comment 2.3 proofreading implemented and validated, pending review. Minor grammar/capitalization/agreement corrections in manuscript; single-shell caption synchronized in response 2.1. Response 2.3 states completed corrections and the absence of the quoted typo in current source/available PDFs. Both documents compiled successfully and affected pages inspected; technical equations unchanged.

- Comment 2.4: added one blue sentence immediately after SaTE in the Introduction, citing MPAEE and sparrow-search energy-adaptive routing and stating this paper’s joint throughput objective. Bibliographic metadata verified against publisher/Crossref records. Response quotes the sentence verbatim; pending explicit acceptance.

- Comment 2.4 refined to a simple related-work sentence, removing the present-paper comparison and preserving the user’s removal of the MPAEE acronym. Response quotation synchronized; pending review.

- Comment 2.4 source review reopened at user request. Read the complete five-page publisher supplement for SSA-DW (saved under tmp/comment-2-4/papers) and MPAEE abstract. SSA-DW evaluates delay, throughput and hop count as well as energy; an energy-versus-throughput contrast is not justified. Full main texts remain inaccessible (Springer subscription, IEEE access challenge, SciEngine 403/429); do not claim both papers have been read in full. No manuscript edits during this check; the current simple citation sentence remains pending review.

- 2026-09-24: read both complete user-supplied papers in tmp/reference, plus SSA-DW supplement. MPAEE Sections II–III and Algorithm 2 optimize weighted paths over an input graph; SSA-DW equations (4)–(5) and algorithm discussion optimize routing costs over adjacent nodes. Neither formulates mechanical LCT matching as a joint decision. Replaced the generic citation sentence with one sentence describing this specific distinction; response quotation synchronized. Earlier full-text access blocker resolved. Comment 2.4 remains pending.

- Removed the repeated joint-optimization contrast from the existing SaTE sentence; retained its fixed-topology/routing description and the mechanical-LCT distinction in the following cited sentence. Meaning unchanged; Comment 2.4 quotation remains exact.

- Comment 2.4: combined SaTE and both added routing methods into one blue sentence, with a shared statement that none jointly optimizes LCT matching, routing and rate allocation under LCT mechanical constraints. Response quotation synchronized.

- Comment 2.4 response finalized with the completed citations and specific joint-decision distinction. One combined manuscript sentence retained verbatim in the letter; both full papers reviewed. No experiments added; other comments unchanged.

- Comment 1.1 approved implementation scope: ATP settings 0/10/20/30/50/70/90 s, unchanged 10 s intervals and 360 s horizon, pre-acquired initial links, five methods, existing legacy/last 500-step settings. Timer and cache round-trip tests passed; RTX 5090 run underway.

- 2026-09-25. Comment 1.1 completed: 185 decisions reused across seven delays, 1,295 replay records, 35 method/delay means excluding initialization. Independent timer/input/throughput validation passed. Fig. 10 and only its manuscript caption/discussion revised in blue; response quotes match verbatim. Direct isolated builds and visual checks passed. Pending review; no new approval or commit.

- 2026-09-25. Condensed the ATP discussion into one paragraph in the previous simulation-description style at the user’s request. Preserved protocol, timer behavior, measured results, and scope; retained the numerical timer example in the response opening. Synchronized the quotation and the user-shortened figure caption. Comment 1.1 remains pending.

- 2026-09-25. Based the Comment 1.1 passage on the user-restored wording with minimal changes: nine-interval range, pre-acquired initialization/excluded initial snapshot, newly selected pairs, persistent timers and drop/reselection behavior, and tested-window limitation. Preserved the original qualitative results discussion and synchronized the response quotation. Still pending review.

- 2026-09-25. Shortened only the Comment 1.1 response opening to directly answer range sufficiency and acquisition across multiple snapshots. Preserved manuscript quotations, figure, reviewer wording, and pending status.

- 2026-09-25. Comment 1.1 accepted by the user and marked black/done. Other statuses unchanged.

- 2026-09-25. Comment 3.1 implementation started under the approved plan: five methods, 37 snapshots, propagation-only delay, cached DuJo decisions, matched inputs, rate-weighted mean/p95 and throughput/served ratio in an appendix table. Pending review.

- 2026-09-25. Comment 3.1 implemented with the approved propagation-only metric, allocated-rate weighting, all 37 snapshots including initialization, and throughput/served-demand context. Appendix text/table and response are synchronized; both PDFs compiled and inspected. Pending review.

- 2026-09-25. At the user’s request, narrowed the Comment 3.1 appendix and reproduced table to propagation delay only. Removed throughput/served-demand columns and comparison prose; retained weighting and served-flow definition. Response synchronized; raw results unchanged and Comment 3.1 pending.

- 2026-09-25. Combined the delay appendix discussion into one paragraph without changing wording; synchronized the response quotation. Table and comment status unchanged.

- 2026-09-25. Added two sentences explaining +Grid’s alignment-based link selection and inverse-capacity routing costs, which do not directly minimize physical distance. Saved-route diagnostics confirm longer paths in this evaluation (traffic-weighted 7,109 km versus DuJo’s 3,375 km). Kept the appendix in one paragraph and synchronized the quotation; Comment 3.1 pending.

- 2026-09-25. Added the allocated-rate-weighted mean route distance (km) to the delay table and its response reproduction, calculated from full-precision results. Updated the metric description and caption; no simulations rerun.

- 2026-09-25. Preserved the user’s removal of the snapshot count and shortened caption in the delay appendix; synchronized the response quotation/caption. Experiment data unchanged.

- 2026-09-25. Finalized Comment 3.1’s direct response: explains the original throughput objective, identifies the added delay/distance table, defines rate weighting, summarizes DuJo’s measured delays, and states the modeled delay components. Manuscript and verbatim quotation/table unchanged; pending explicit acceptance.

- 2026-09-25. Comment 3.2 implemented: clarified residual demand/local-service accounting, measured selected-topology and candidate-graph maximum-flow upper bounds, and explicitly retained possible matching/routing improvement. One blue manuscript paragraph and exact response quote; both documents validated.

- 2026-09-25. Rewrote only the Comment 3.2 response opening to answer directly: selected-LISL connectivity/capacity limits, adequate aggregate gateway supply, possible optimization improvement, and residual-demand accounting. Removed detailed bound discussion from the opening; manuscript evidence and quotation unchanged.

- 2026-09-25. Shortened the Comment 3.2 manuscript addition to two sentences explaining residual demand and limited LISL connectivity/capacity, retaining possible matching/routing improvement. Removed numerical bounds from manuscript prose, synchronized the response quotation, and retained audit evidence in the code results.

- 2026-09-26. Shortened the Comment 3.2 response to directly identify LISL connectivity/capacity bottlenecks, distinguish them from aggregate gateway shortage in the audited snapshots, and acknowledge a possible optimization gap. Manuscript and quotation unchanged; pending review.

- 2026-09-26. Removed the two-LCT explanation from Comment 3.2 manuscript wording, response, and quotation at the user’s request. Retained the general LISL connectivity/capacity explanation.

- 2026-09-26. Replaced the manuscript’s matching/routing improvement sentence with increasing LCTs per satellite or satellite count, conditional on fixed traffic demand. Synchronized response and quotation; no new experimental claim.

- 2026-09-26. Comment 3.3: confirmed theta in user-updated Fig. 1(b), finalized the completed-work response, and preserved the figure unchanged. Pending acceptance.

- 2026-09-26. Reproduced the user-updated Fig. 1 in Comment 3.3 using the manuscript PDF directly, its exact caption with figure-reference prefix, a response-specific label, and normal float placement. Pending status unchanged.
