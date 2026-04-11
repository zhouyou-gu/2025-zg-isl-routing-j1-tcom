# Agent Control

This workspace uses a three-file control system:

- `AGENT.md`: stable repo policy and the authority on which control file to update
- `AGENT_HARNESS.md`: reusable execution playbook and generalized inferred user intent
- `AGENT_PROGRESS.md`: live task state, concrete progress, and the next safe resume point

## Mandatory Read Order

Before substantive work, read these files in order:

1. `AGENT.md`
2. `AGENT_HARNESS.md`
3. `AGENT_PROGRESS.md`

While processing the workspace:

- use `AGENT_HARNESS.md` for how to operate
- use `AGENT_PROGRESS.md` for what the current state of work is
- update the appropriate file as soon as the triggering condition below is met

## Core Working Rules

- Work one reviewer comment or one concrete revision step at a time.
- Do not advance to the next reviewer comment until the user is satisfied with the current one.
- Keep `main.tex` and `response_letter_TCOM_RV1.tex` synchronized.
- When the response letter quotes a manuscript change, the quoted `\blue{...}` text must match the manuscript verbatim.
- Preserve existing uncommitted changes and do not overwrite unrelated work in the dirty tree.

## Update Dispatcher

`AGENT.md` is the authority on whether an agent should update `AGENT_HARNESS.md`, `AGENT_PROGRESS.md`, or both.

### Update `AGENT_PROGRESS.md` when concrete workspace state changes

Update `AGENT_PROGRESS.md` in the same turn when any concrete task or workspace state changes, including when:

- any repo file is edited, added, renamed, or removed
- a reviewer comment changes status
- the response letter is synchronized to a manuscript change
- a new appendix, citation, or supporting artifact is added
- the current blocker, next action, or next safe resume point changes
- a review or check changes confidence in the current state of the work

How to update `AGENT_PROGRESS.md`:

- record the new current objective if it changed
- refresh repository state and concrete edits already present
- update comment-by-comment status
- append a concise rolling-log entry for the meaningful change
- revise blockers, immediate next actions, and next safe resume point as needed
- keep it factual and current; do not move stable workflow policy into this file

### Update `AGENT_HARNESS.md` only for durable reusable rules

Update `AGENT_HARNESS.md` when a reusable user preference, workflow rule, or execution pattern becomes clear from the interaction, for example when:

- a user preference becomes clearly reusable beyond the current step
- a generic workflow pattern is inferred from the user's requests or corrections
- a stable review or validation habit is established
- a recurring acceptance criterion or writing standard emerges
- an interaction reveals a general operating principle that future agents should follow on later tasks too

How to update `AGENT_HARNESS.md`:

- capture the explicit or inferred generic user intention in reusable form
- generalize the lesson into a reusable rule, checklist item, or playbook entry
- place it in the relevant workflow or inferred-intent section
- keep it independent of the current step's transient status
- do not log one-off events or current blockers here

### Update both when both conditions are true

Update both `AGENT_PROGRESS.md` and `AGENT_HARNESS.md` when:

- a concrete task advance also reveals a reusable operating preference
- a user correction changes both the current task state and future workflow expectations

## Role Boundary

- `AGENT.md` defines rules and update routing, but does not store live task status.
- `AGENT_HARNESS.md` stores reusable workflow and generalized user intent, but not the current task log.
- `AGENT_PROGRESS.md` stores live state and rolling progress, but not stable repo policy.

If unsure where a new piece of information belongs:

- put it in `AGENT_HARNESS.md` if it should still guide future agents after the current task is complete
- put it in `AGENT_PROGRESS.md` if it only describes the current state of work
