---
document_id: SAC-TPL-007
title: Review Artifact Template
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-24
---

# Review Artifact Template

> Review artifacts are immutable, non-canonical, have no Pull Request, are never merged, and never approve themselves.

## Control and subject

| Field | Exact value |
|---|---|
| Issue / gate / artifact type | TBD |
| Plan review, correction successor, or execution report | TBD |
| Artifact path / required parent | TBD |
| Immutable subject SHA/path/blob/parent | TBD |
| Prompt and authorization IDs/hashes | TBD |
| Inspection timestamp/timezone | TBD |
| Repository/base/branch/live heads | TBD |

## Scope, evidence, and findings

Record read-only sources, exact inspected paths, classifications, public-safety result, reviewer limitations, findings with severity/evidence, disposition recommendation, and unresolved decisions. A correction identifies its predecessor and uses a new version/path/commit.

## Execution-report contract

When used for Gate 3, record implementation branch/base, exact per-commit paths and modes, content SHA, checkpoint commit SHA, current remote head, report parent, ancestry/counts, validation/link/ID/metadata/diff/safety results, live Issue/PR state, worktree state, drift/partial state/ambiguity, unauthorized-action absence, and exact next decision. Never guess or embed the report commit's own SHA.

## Human Authority boundary and next action

State what the reviewer recommends, what only the Human Authority may decide, every action still prohibited, and the exact stop. Review presence, reviewer recommendation, branch, commit, or technical capability grants no authority.
