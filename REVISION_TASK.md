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
| 3.4 | Reviewer 3 item 4 | Implemented and validated; pending review |
| 3.5 | Reviewer 3 item 5 | Clarification implemented; pending review |
| 3.6 | Reviewer 3 item 6 | Clarification implemented; pending review |
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

Review Comment 3.4 and Fig. 11. Keep 3.1–3.4 red/pending; accepted statuses unchanged. Review PDFs: `output/pdf/main_comment_3_4_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`.

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

- 2026-09-26. Comment 3.4 started with user-selected 50/100/150/200 gateways; one nested seed-0 placement, all five methods, fixed physical settings and raw user demand, fresh fixed-traffic optimization. Pending validation and plotting.

- 2026-09-26. Comment 3.4 implemented and validated, pending review (red). Completed 20 evaluations for 50/100/150/200 gateways on the 5090 workstation, with one nested seed-0 placement and fixed geometry/raw demand. Added Fig. 11 and one blue paragraph; response quotations match exactly. Matched-input, route/rate, capacity and independent result audits passed. Both isolated document builds and affected-page visual inspections passed; no undefined references or overfull boxes. Response retains the existing h-to-ht warning. Results and source provenance are archived under code sim_alg_v1_res/test_tcom_gateway_count/comment-3-4-20260926-ail/ and remote gateway-results/. Paper and code changes are uncommitted.

- 2026-09-26. Extended Comment 3.4 to 400 gateways. All 25 cases passed preflight, matched-input, route/rate and independent capacity/result audits; original 20 rows unchanged. DuJo at 400: 150.60 Gbps / 42.46%, below its 200-gateway peak but highest among the five methods. Manuscript and response now state the nonmonotonic result. Fig. 11 copies Fig. 10 canvas dimensions, axis/legend boxes, typography and marker sizes; only experiment-specific axes/data differ. Layout constants checked directly against source, and compiled manuscript/response pages visually inspected. No undefined references or overfull boxes; underfull spacing warnings and the existing response h-to-ht warning remain. Both review PDFs refreshed. Comment 3.4 remains red/pending; both repos uncommitted.

- 2026-09-26. Replaced the displayed 400-gateway case with 250 as requested. Completed all five new evaluations on the 5090 workstation; 25 active cases passed independent audits and original 50–200 results are unchanged. DuJo at 250 is 150.98 Gbps / 41.35%. Fig. 11 retains Fig. 10 layout constants. Manuscript and response quotations synchronized; isolated builds and affected-page inspections passed, with no undefined references or overfull boxes. Prior 400 results remain archived, excluded from the displayed sweep. Comment 3.4 remains pending/red; paper and code uncommitted.

- 2026-09-27. User requested displaying only 50/100/150/200 gateways. Removed 250 from the plotting filter and synchronized manuscript/response to the displayed range; preserved all raw 250/400 measurements. Fig. 10 layout settings unchanged. No simulations rerun. Comment 3.4 remains pending, changes uncommitted.

- 2026-09-28. Preserved the user’s current gateway-count paragraph verbatim, including removal of the fixed-geometry/traffic and 500-iteration sentence. Synchronized only the Comment 3.4 manuscript quotation. Main text unchanged; pending status preserved.

- 2026-09-28. Replaced the numerical gateway-performance sentence at the user’s request with a qualitative increase over the evaluated range; synchronized the response quotation. Other wording and pending status unchanged.

- 2026-09-28. User authorized commit/push of Comment 3.4 paper and supporting experiment code to both main branches. Final display is 50/100/150/200, Fig. 10 layout retained, latest user wording preserved and quotation exact. Raw extended cases remain archived. Acceptance status unchanged.

- 2026-09-28. Replaced “site catalogue” with “list of ground-station locations” in the gateway-count paragraph and response quotation. Preserved other user edits and comment status.

- 2026-09-28. Synchronized Comment 3.4 to the latest manuscript, including the user’s removal of the reference epoch from the figure caption. Paragraph and caption match verbatim; manuscript and pending status preserved.

- 2026-09-28. Comment 3.5: code inspection confirmed population-derived aggregate demand and per-satellite gateway supply, with no radio-access beam/scheduler model. Added one blue paragraph in the Traffic Profile Model and exact response quotation. No unsupported payload type or simultaneous-user count assigned. All other responses/statuses preserved.

- 2026-09-28. Comment 3.5 validation passed: only one manuscript paragraph added, exact quotation, other responses unchanged. Both documents compiled in an isolated directory with no undefined references or overfull boxes; underfull warnings and existing response float warning remain. Inspected manuscript page 4 and response page 12. Review PDFs refreshed; no commit or acceptance.

- 2026-09-28. Comment 3.6: verified config_l_mask in the original failure-rate driver and disabled lateral terminals in the default configuration. Replaced the first two LCT-evaluation sentences with the expected-count definition and qualified four-terminal discussion. Replaced the provisional experiment promise with a direct answer; no new experimental evidence or linear-scaling claim. Other comment statuses unchanged.

- 2026-09-28. Comment 3.6 quotation and unrelated-response preservation verified. Both isolated builds passed without undefined references or overfull boxes; existing response float warning remains. Manuscript/response review PDFs refreshed. No code/figure changes or new simulations; pending explicit acceptance.

- 2026-09-28. User authorized the focused 2/3/4 installed-LCT comparison. Separate driver preserves default experiments, enables front/back then right/left lateral directions with all installed terminals available, and runs 15 fresh evaluations on the 5090 host. Preflight passed: same geometry/traffic/gateways, nested candidate links, orthogonal mounting directions, and original two-terminal input fingerprint. DuJo uses fixed traffic, 500 iterations/final iterate; DRL uses frozen checkpoint. Results pending.

- 2026-09-28. Completed 15 fresh 2/3/4-LCT evaluations on the 5090 workstation. Independent audits passed; two-LCT DuJo reproduces the existing benchmark. DuJo 147.17/257.35/218.29 Gbps; MRate leads at four LCTs with 272.94 Gbps. Per user steering, added an appendix table (no figure) with throughput/served ratios, one paragraph, and main-text pointer. Response reproduces all additions and table exactly, preserving unfavorable outcomes. Direct isolated builds and table/page visual checks passed; no undefined references or overfull boxes. Raw data/source hashes archived in code test_tcom_lct_count/comment-3-6-20260928 and remote lct-results. Comment 3.6 remains pending; both repos uncommitted.

- 2026-09-28. Corrected LCT comparison freezes ordered gateway-source pairs to the two-LCT reference, including the final conversion traffic refresh. All 15 cases passed cross-count/method inputs, matching/routes, source/target budgets and directed-link capacities. Two-LCT results unchanged exactly. Corrected DuJo 147.17/254.13/209.76 Gbps; MRate four-LCT 276.47 Gbps. Previous matchings remain feasible with added terminals, so remaining drop is an algorithm-output limitation. Replaced appendix/response numbers and stated fixed-pair protocol. Archived prior results as superseded. Saved revision ATP (1295 rows), multi-shell (270), delay (185) and gateway (25) input audits passed; delay numerical/artifact audit rerun passed. Full historical Fig. 8 raw-state revalidation is unavailable. No claim that every historical figure was rerun. Pending review, uncommitted.

- Fixed-pair final validation: exact manuscript/response table and quotation, both isolated builds without undefined references/overfull boxes, and visual inspection of manuscript p.15 / response p.13 passed. Refreshed review PDFs. Source/provenance and independent audit reports synchronized to the 5090 host. No commit or acceptance.

- 2026-09-28. Corrected gu2024graph authors (Kishore Chikkam and Pasquale Aliberti), pages (2479–2494), and DOI (10.1109/TNET.2024.3355935), verified against author arXiv 2402.00879 and SUTD institutional record 9912748609846. Citation key/title/venue/year unchanged; other bibliography entries preserved.

- 2026-09-28. Audited all 79 main.bib entries: 78 identities source-verified, one 3GPP overview webpage remains incomplete because primary access returns HTTP 403. Corrected/completed 17 entries relative to Git baseline, including prior gu2024graph correction; documented every entry/source in REFERENCE_AUDIT.md. All-entry BibTeX check and isolated manuscript/response builds passed; bibliography pages visually inspected, no undefined citations/references or overfull boxes. Existing response float warning unchanged. Manuscript wording, reviewer statuses and code untouched by this audit; changes uncommitted.

- 2026-09-28. Completed 2/3/4-LCT DuJo 500/1000/2000/5000-step diagnostic on the 5090 host. Final throughput at 5000: 153.62/267.33/220.24 Gbps; best among every-100-step samples: 157.23/280.08/238.79 at 4400/3600/3200. All 150 solutions passed independent route/rate/matching/capacity audits; 500-step routes/rates/matchings exactly reproduce earlier results. Larger budget does not remove four-LCT drop; final iterate fluctuates. Sources, traces and outputs archived in code test_tcom_lct_count/comment-3-6-iterations-20260928 and remote lct-iterations. See code TCOM_LCT_ITERATIONS.md. Manuscript/table and statuses unchanged; uncommitted.

- 2026-09-28. Completed user-requested installed-LCT study with full FOR 90 degrees (theta=45 half-angle); other experiment defaults unchanged. All 15 five-method cases rerun on 5090 host with same 500-step final-iterate protocol and original fixed flow pairs. All independent matching/routes/capacity audits passed; cross-FOR audit confirms unchanged geometry/traffic/gateways/flow pairs and no duplicate terminal assignments per satellite pair. DuJo 121.90/218.77/263.07 Gbps; all methods increase; MRate four-LCT 296.04 Gbps. Updated appendix paragraph/table and Comment 3.6 response verbatim. Both isolated builds and visual checks passed, no undefined references or overfull boxes; existing response float warning unchanged. Saved provenance/data locally in code comment-3-6-for90-20260928 and remotely lct-for90. Previous FOR120/iteration data preserved. Comment 3.6 pending, changes uncommitted.

- 2026-09-28. At user request, merged Flow Propagation Delay and Installed LCT Count under one blue Appendix: Ablation Study with two subsections. Added measured four-LCT explanation: capacity-based SaTE/MRate matching gives connected topology with shorter/higher-capacity links (794 vs 1261 km; 4.03 vs 2.67 Gbps), different routing costs, and finite-iteration DuJo limitation. Updated Comment 3.1/3.6 location wording and verbatim quotation. Tables and numbers unchanged. Isolated builds passed without undefined references or overfull boxes; affected pages visually inspected. Normal table floating retained. Review PDFs refreshed; statuses unchanged, uncommitted.

- 2026-09-28. Converted Installed LCT Count heading to inline noindent/textit blue lead-in. Flow-delay heading and prose were already absent on reread; requested clarification before restoring user-deleted content. Two-paragraph formatting pending that answer.

- 2026-09-28. User explicitly authorized restoring the missing flow-delay paragraph from the response letter. Ablation Study now has two prose paragraphs with noindent/textit blue lead-ins: Flow Propagation Delay. and Installed LCT Count. Both subsection headings removed; table contents and paragraph wording preserved. Manuscript compiles successfully; review PDF refreshed.

- 2026-09-28. Synchronized response-letter Comments 3.1 and 3.6 quotations verbatim to current Ablation Study paragraphs, including noindent/textit lead-ins. Added concise four-LCT baseline explanation to direct Response 3.6. Other comment texts/statuses unchanged. Direct isolated letter builds passed; review PDF refreshed.

- 2026-09-28. Reframed four-LCT explanation per user: more connection opportunities let capacity-based SaTE/MRate matching favor high-capacity links while retaining connectivity; this can reduce the capacity/connectivity tradeoff and outperform DuJo’s approximate joint solution. Replaced detailed link statistics/finite-iteration wording in appendix and synchronized response/quotation. Tables and experiment settings unchanged. Both isolated builds passed.

- 2026-09-28. Per user wording, changed “an approximate joint solution” to “an approximately optimal solution” in the four-LCT explanation, direct response and verbatim quotation.

- 2026-09-28. Updated the synchronized four-LCT explanation to the user-requested wording: “DuJo provides an approximation to the optimal solution.”

- 2026-09-28. User authorized commit/push of current paper and code to main. Code e6bba75 publishes controlled LCT-count/FOR and iteration drivers, audits and documentation. Paper checkpoint includes 90-degree full-FOR Table III, unified Ablation Study, synchronized Comment 3.6 response and bibliography audit/corrections (including tracked main.bbl). Final isolated manuscript/letter builds and quotation checks passed; no undefined references or overfull boxes. Comment 3.6 remains pending; one 3GPP web-reference verification remains incomplete as documented. Raw experiment archives remain ignored locally and preserved on 5090 host.
