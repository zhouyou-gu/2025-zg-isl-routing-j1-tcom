# Round 2 Revision Brief

This is a lower-precedence current-state brief. Read the three core agent files first.

## Round and Sources

- Active manuscript identifier is `TCOM-TPS-26-1250`; the editor is Dr. Jianqing Liu, IEEE Transactions on Communications.
- The decision letter is dated 28-Aug-2026 and recommends a major revision within 60 days.
- RV2 remains the local round label. The new identifier is used in `response_letter_TCOM_RV2.tex`.
- The local-only, gitignored `TCOM_RV2_decision_letter.txt` preserves the entire supplied attachment byte-for-byte, including the administrative instructions and reviewer report headers.
- Active response source is `response_letter_TCOM_RV2.tex`; the compiled planned-response draft is `output/pdf/response_letter_TCOM_RV2_draft.pdf`.
- The manuscript content baseline is `main.tex` at `4cd632f`, with all prior-round blue wrappers and the blue-to-black override now removed. No substantive RV2 manuscript changes have been made. The `\blue` macro remains available for new revisions.
- Prior-round response and cover-letter files, their build files, and response progress remain in `archive/rv1/`. Manuscript files and figures are outside this response-only archive.

## Review-Item State

| Local item | Source item | State |
| --- | --- | --- |
| E.1 | Editor substantive assessment paragraph | Planned response drafted, pending |
| 1.general | Reviewer 1 opening assessment | Preserved as an unnumbered introduction |
| 1.1 | Reviewer 1 item 1 | Planned response drafted, pending |
| 1.2 | Reviewer 1 item 2 | Planned response drafted, pending |
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

- The response follows `../2025-zg-isl-routing/response_letter_ToN_RR.tex` directly. Fourteen inline comment entries (E.1 and 13 reviewer items) have drafted `Response:` and `Planned manuscript changes:` fields. Three reviewer opening assessments remain unnumbered introductory paragraphs, followed by topic-specific acknowledgments.
- Comment wording is unchanged. Original list markers are replaced with reference-style `Comment 1.1:` labels, without duplicate numbering. All comments remain bold red and pending.
- The complete administrative editor email remains in `TCOM_RV2_decision_letter.txt`; only its substantive assessment appears as E.1 in the response.

## Evidence Gaps

- Plans are grounded in the current manuscript, neighboring responses, and read-only inspection of the ATP and terminal-availability simulation code. No new simulations or RV2 manuscript edits have been performed.
- Outstanding studies include longer ATP settings (60/120 s), cold-start replay, broader shell/epoch coverage, route propagation delay, throughput bottleneck and optimization-gap diagnostics, gateway-count sensitivity, and explicit two-/three-/four-terminal layouts.
- Controller timing beyond solver measurements, payload scope, FOR axis interpretation, and served-demand accounting need the planned clarification or audit. Figure edits and proofreading remain planned.
- The two suggested routing studies have been identified for review. Full technical comparisons and verified bibliography entries remain to be added during implementation.

## Next Item-Local Step

All requested plans are drafted and pending review. Resume with the user's feedback or selection of an item for implementation.
