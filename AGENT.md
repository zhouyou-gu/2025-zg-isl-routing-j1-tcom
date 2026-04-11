# Agent Control

This workspace uses a three-file control system:

- `AGENT.md`: stable repo policy and the authority on which control file to update
- `AGENT_HARNESS.md`: reusable execution playbook and generalized inferred user intent
- `AGENT_PROGRESS.md`: live task state, concrete progress, and the next safe resume point

## Agent-File Contract

These files are intended to be reusable onboarding and control files for later agents working in this workspace. If a user says to read the agent files, interpret that as an instruction to read all three files in the mandatory order below and treat them together as the workspace operating contract.

- `AGENT.md` defines the control contract: file roles, read order, update routing, and conflict handling.
- `AGENT_HARNESS.md` stores durable reusable workflow rules and generalized user preferences. Keep it low entropy and reusable across tasks.
- `AGENT_PROGRESS.md` stores the current factual state, concrete recent changes, blockers, and the next safe resume point.

Design expectations:

- Another agent should be able to recover both how to operate and where the work stands by reading these files alone.
- Stable reusable guidance belongs in `AGENT_HARNESS.md`, while transient task state belongs in `AGENT_PROGRESS.md`.
- If information drifts into the wrong file, restore the boundary instead of duplicating the same content across files.

## Functional Boundary by File

- `AGENT.md` is the control file. It defines file roles, read order, precedence, update routing, and boundary enforcement. It should not become a task log, a reusable playbook, or a store of detailed project progress.
- `AGENT_HARNESS.md` is the reusable playbook. It stores durable workflows, generalized user preferences, stable review habits, and reusable execution rules. It should not become a chronological history, a current blocker list, or a step-by-step log of the active task.
- `AGENT_PROGRESS.md` is the live state file. It stores the current objective, current factual status, concrete edits already present, current blockers or risks, immediate next actions, and the next safe resume point. It should not become the authority on workflow policy or a duplicate copy of the reusable harness.

When deciding where information belongs, classify it by function first:

- if it tells a later agent how to operate across tasks, it belongs in `AGENT_HARNESS.md`
- if it tells a later agent what is true right now in this workspace, it belongs in `AGENT_PROGRESS.md`
- if it tells a later agent how the control files themselves are supposed to work, it belongs in `AGENT.md`

## Mandatory Read Order

Before substantive work, read these files in order:

1. `AGENT.md`
2. `AGENT_HARNESS.md`
3. `AGENT_PROGRESS.md`

While processing the workspace:

- use `AGENT_HARNESS.md` for how to operate
- use `AGENT_PROGRESS.md` for what the current state of work is
- update the appropriate file as soon as the triggering condition below is met

## Control-File Precedence

- Use `AGENT.md` to decide which control file governs a question.
- Use `AGENT_HARNESS.md` for durable workflow and generalized preference guidance unless `AGENT.md` says otherwise.
- Use `AGENT_PROGRESS.md` for current task state, current blockers, and the safe resume point.
- If current-state information elsewhere conflicts with `AGENT_PROGRESS.md`, treat `AGENT_PROGRESS.md` as authoritative and clean up the drift.
- If a durable reusable rule appears only in `AGENT_PROGRESS.md`, move it to `AGENT_HARNESS.md` and keep only the current-state residue in the progress file.

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
