---
document_id: SAC-REG-005
title: Information Update Register
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-24
---

# Information Update Register

## Control state

This Draft register records append-only intake, classification, authority, state, and evidence history under [SAC-GOV-005](../docs/00-project-control/project-information-update-workflow.md). A row, commit, or status grants no authority.

## Stable ID and required fields

Allocate the lowest unused `SAC-UPD-NNN`; never reuse or renumber an ID. Each update record must deterministically contain:

- ID, title/request, controlling Issue, intake timestamp/timezone, phase, urgency, expected outcome;
- source, submitter class, source authority, source location, immutable evidence, mutability, verification, and confidentiality/public-safety class;
- statement-level fact/proposal/assumption/unknown/decision classifications and classification history;
- direct/indirect impacted paths, impact-map path/SHA, owners, downstream effects, exclusions, and unresolved impacts;
- PLAN path/SHA/blob, review path/SHA/disposition, and Human Authority authorization evidence;
- APPLY branch, immutable base, ordinal allowlist, per-file intent, commit/push counts, validation and partial-state rules;
- implementation content SHA, checkpoint-record commit SHA, current branch-head SHA, execution-report review SHA/path;
- validation/correction history; retained predecessors; migration/supersession decision; next/prohibited action;
- PR, merge, baseline, and publication authorization/execution/evidence as separate fields; and
- append-only state history with actor, authority evidence, timestamp, result, limitations, and next stop.

## Entries

`SAC-UPD-001` is reserved for the future separately authorized Mandate pilot. Gate 3 does not execute or populate it. No substantive update entry is recorded.

| Update ID | Title/request | Controlling Issue | Current state | Source/authority | Safety class | PLAN/review | APPLY branch/base | Content SHA | Checkpoint commit | Current head | Execution report | PR decision | Merge decision | Baseline decision | Publication authorization/execution | Retained/migration | Next action |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

## Append-only history

| Update ID | Timestamp/timezone | From state | To state | Actor/role | Authority evidence | Evidence/classification change | Validation/result | Limitations/correction | Next stop |
|---|---|---|---|---|---|---|---|---|---|

Never erase prior evidence or state. Corrections append a successor entry and reference the superseded assertion.

## Current classifications

- **Confirmed:** The register structure and `SAC-UPD-001` reservation are governance records only.
- **Assumption:** None recorded.
- **Unknown/TBD:** Substantive Mandate and Discovery updates are TBD.
- **Decision required:** Any entry transition requires its applicable authorization.
