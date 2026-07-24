---
document_id: SAC-REG-003
title: Decision Log
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# Decision Log

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This register is Draft and has not been approved or synchronized to SharePoint.
- The decisions below authorize the repository bootstrap described; they do not constitute SharePoint publication or document approval beyond their stated scope.

## Field definitions

| Field | Meaning |
|---|---|
| Decision ID | Stable identifier |
| Date | ISO decision date |
| Status | Proposed, Approved, Superseded, or Rejected |
| Decision | Authorized choice |
| Authority | Named decision maker |
| Evidence | Controlling instruction or immutable reference |
| Scope | Exact effect and boundary |

## Status definitions

- **Proposed:** Awaiting an explicit authorized decision.
- **Approved:** Explicitly accepted by the named authority within the recorded scope.
- **Superseded:** Replaced by a later linked decision; history is retained.
- **Rejected:** Explicitly declined by the named authority.

## Traceability rules

- Record only explicit decisions made by an authorized person.
- Cite the controlling plan SHA or other immutable evidence where available.
- Do not infer unstated project facts, approval, publication, or expanded scope.
- A later change must reference the affected decision and preserve history.

## Maintenance rules

- Never alter the wording or scope of an Approved decision silently; record a new linked decision when it changes.
- Validate decision IDs, dates, status values, authority, evidence links, and affected scope before commit.
- Update supersession references in both the old and replacement records when applicable.

## Approved bootstrap decisions

| Decision ID | Date | Status | Decision | Authority | Evidence | Scope |
|---|---|---|---|---|---|---|
| `SAC-DEC-001` | 2026-07-22 | Approved | Approve SAC-PLAN-0001 v0.2 at commit `270c85c1f114ef903275b0663eb70497eb5fa3ff` as the controlling Phase 2 plan | Hoang Quy Nguyen (`frwkHoangQuy`) | Human Phase 2 authorization | Controls this repository initialization only |
| `SAC-DEC-002` | 2026-07-22 | Approved | Authorize Phase 2 implementation using exactly the 11-file set in the controlling plan | Hoang Quy Nguyen (`frwkHoangQuy`) | Human Phase 2 authorization | Authorizes branch, files, validation, commit, push, and Draft PR; does not authorize merge |
| `SAC-DEC-003` | 2026-07-22 | Approved | Use English as the standard language in Git | Hoang Quy Nguyen (`frwkHoangQuy`) | SAC-PLAN-0001 v0.2 | Vietnamese or bilingual variants require a defined audience or delivery obligation |
| `SAC-DEC-004` | 2026-07-22 | Approved | Initialize governance baseline documents as Draft, version 0.1 | Hoang Quy Nguyen (`frwkHoangQuy`) | SAC-PLAN-0001 v0.2 | Does not approve the documents |
| `SAC-DEC-005` | 2026-07-22 | Approved | Assign Hoang Quy Nguyen as initial owner and approver, mapped to `frwkHoangQuy` | Hoang Quy Nguyen (`frwkHoangQuy`) | SAC-PLAN-0001 v0.2 | Applies to the 11-file initial baseline |
| `SAC-DEC-006` | 2026-07-22 | Approved | Temporarily accept public visibility for governance-only bootstrap | Hoang Quy Nguyen (`frwkHoangQuy`) | SAC-PLAN-0001 v0.2 | Prohibits secrets and sensitive or non-public project content; private conversion remains deferred |
| `SAC-DEC-009` | 2026-07-24 | Approved | Accept Gate 1 Plan v2 at commit `62a89ec56e738c6a291470a398ddc51ffed0987a`, path `agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v2.md`, blob `c44a7b7013a1fe368078f3c28381a3f84118ffde`, after independent review | Hoang Quy Nguyen (`frwkHoangQuy`) | Personally activated `SAC-GOV-PIUW-GATE2-AUTHORIZATION-RECORD-v1` | Accepts only the exact reviewed plan object; no Gate 3 completion, PR, merge, baseline, publication, migration, or phase advancement |
| `SAC-DEC-010` | 2026-07-24 | Approved | Authorize Gate 3 only under `SAC-GOV-PIUW-GATE2-AUTHORIZATION-RECORD-v1` SHA-256 `5a6cb20288bd8605a0482946bb726bf13641ab30320b3c9b4070527a45c38625` and `SAC-GOV-PIUW-GATE3-PROMPT-v1` SHA-256 `3a629d4868c05b344acb87c93626b34f54855e627ce320becb2e42a0c0f14d32` | Hoang Quy Nguyen (`frwkHoangQuy`) | Personal Human Authority activation for Issue #5 Gate 3 | Base `53479ad5694071555cbb97bdea5bbe3316271d45`; branch `implementation/0005-project-information-update-workflow`; exact eleven-path content commit then journal-only checkpoint; report `agent-artifacts/issue-5/gate-3/2026-07-24-canonical-implementation-execution-report-v1.md` with parent `62a89ec56e738c6a291470a398ddc51ffed0987a`; exactly three commits, two pushes, one new branch, zero PRs and Issue/PR mutations; permitted public governance identity only; retain Issue #2, PR #3, PR #4, SAC-PLAN-0002 and IDs 007/008; stop on partial/ambiguous state; excludes merge, baseline, publication, SharePoint, pilot, migration, Discovery, architecture, software, and later gates |

## Reserved decision IDs

`SAC-DEC-007` and `SAC-DEC-008` remain reserved because retained Draft PR #3 uses them. They are not reused, promoted, or restated as canonical decisions in this branch.

## Publication boundary

These decisions are Git governance records only. They do not claim SharePoint publication, SharePoint approval, synchronization, PR merge authorization, or approval of the Draft Phase 2 documents.

## Current classifications

- **Confirmed:** The six bootstrap decisions were explicitly authorized on 2026-07-22; `SAC-DEC-009` and `SAC-DEC-010` record the 2026-07-24 Human Authority decisions for Issue #5.
- **Assumption:** None recorded.
- **Unknown/TBD:** Future project decisions and SharePoint publication details are TBD.
- **Decision required:** Merge and any SharePoint action require separate human authorization.
