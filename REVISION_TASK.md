# Round 2 Revision Brief

This is a lower-precedence current-state brief. Read the three core agent files first.

## Round and Sources

- Active manuscript identifier is `TCOM-TPS-26-1250`; the editor is Dr. Jianqing Liu, IEEE Transactions on Communications.
- The decision letter is dated 28-Aug-2026 and recommends a major revision within 60 days.
- RV2 remains the local round label. The new identifier is used in `response_letter_TCOM_RV2.tex`.
- The local-only, gitignored `TCOM_RV2_decision_letter.txt` preserves the entire supplied attachment byte-for-byte, including the administrative instructions and reviewer report headers.
- Active response source is `response_letter_TCOM_RV2.tex`; the compiled response draft is `output/pdf/response_letter_TCOM_RV2_draft.pdf`.
- The manuscript content baseline is `main.tex` at `4cd632f`, with all prior-round blue wrappers and the blue-to-black override now removed. The sole substantive RV2 manuscript addition is the blue Comment 1.2 paragraph after the existing computing-time discussion. All pre-existing manuscript text is preserved; the addition uses `\blue` at the user's request while review remains pending.
- Prior-round response and cover-letter files, their build files, and response progress remain in `archive/rv1/`. Manuscript files and figures are outside this response-only archive.

## Review-Item State

| Local item | Source item | State |
| --- | --- | --- |
| E.1 | Editor substantive assessment paragraph | Planned response drafted, pending |
| 1.general | Reviewer 1 opening assessment | Preserved as an unnumbered introduction |
| 1.1 | Reviewer 1 item 1 | Planned response drafted, pending |
| 1.2 | Reviewer 1 item 2 | Implemented, synchronized, and validated; acceptance pending |
| 2.general | Reviewer 2 opening assessment | Preserved as an unnumbered introduction |
| 2.1 | Reviewer 2 item 1 | Planned response drafted, pending |
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

- The response follows `../2025-zg-isl-routing/response_letter_ToN_RR.tex` directly. Comment 1.2 has completed `Response:` and `Manuscript changes:` fields with one verbatim quotation. The other 13 inline comment entries retain their drafted responses and planned changes. Three reviewer opening assessments remain unnumbered introductory paragraphs, followed by topic-specific acknowledgments.
- Comment wording is unchanged. Original list markers are replaced with reference-style `Comment 1.1:` labels, without duplicate numbering. All comments remain bold red and pending.
- The complete administrative editor email remains in `TCOM_RV2_decision_letter.txt`; only its substantive assessment appears as E.1 in the response.

## Evidence Gaps

- Plans are grounded in the current manuscript, neighboring responses, and read-only inspection of the ATP and terminal-availability simulation code. No new simulations have been performed. Comment 1.2 now adds one deployment-limitation paragraph; all other item plans remain unimplemented.
- Outstanding studies include longer ATP settings (60/120 s), cold-start replay, broader shell/epoch coverage, route propagation delay, throughput bottleneck and optimization-gap diagnostics, gateway-count sensitivity, and explicit two-/three-/four-terminal layouts.
- Comment 1.2 now distinguishes measured optimization/conversion time from additional control-cycle overhead, states conditional advance-planning requirements, and identifies incorporating DeepLaDu as a further-research direction to accelerate approximate multiplier estimation. Those overheads and end-to-end feasibility remain unmeasured. Payload scope, FOR axis interpretation, served-demand accounting, figure edits, and proofreading remain planned.
- The two suggested routing studies have been identified for review. Full technical comparisons and verified bibliography entries remain to be added during implementation.

## Next Item-Local Step

Review the implemented and validated Comment 1.2 with the user. Its only manuscript change is an appended paragraph in Section V, under "Evaluation of Computational Complexity," reproduced verbatim in the response. Two sentences now describe graph-learning acceleration using the existing `gu2026deepladu` citation; the response includes its bibliography. The system-operation remark and ATP discussion are unchanged. Keep Comment 1.2 pending acceptance and preserve the other item statuses.

Review PDFs are `output/pdf/main_comment_1_2_review.pdf` and `output/pdf/response_letter_TCOM_RV2_draft.pdf`; build and visual-validation details are recorded in `AGENT_PROGRESS.md`.
