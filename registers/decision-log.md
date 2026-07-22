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
- The decisions below authorize the repository bootstrap and the narrowly scoped Phase 3 Discovery Draft work; they do not constitute SharePoint publication or document approval beyond their stated scope.

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
| `SAC-DEC-007` | 2026-07-22 | Approved | Approve SAC-PLAN-0002 v0.2 at commit `4ce275b0ecb3cd297636bade6168407de4e3b2d0` as the controlling Phase 3 plan | Hoang Quy Nguyen (`frwkHoangQuy`) | Explicit human authorization against immutable plan SHA `4ce275b0ecb3cd297636bade6168407de4e3b2d0` | Controls Phase 3 Discovery Draft only; does not approve the deliverables, factual closure, merge, Ready transition, SharePoint action, delivery ownership, delivery strategy, architecture design, or software implementation |
| `SAC-DEC-008` | 2026-07-22 | Approved | Authorize Phase 3 Discovery Draft implementation on `implementation/0002-current-state-discovery-readiness`, created from the approved plan SHA, using exactly the six Section 4 paths | Hoang Quy Nguyen (`frwkHoangQuy`) | Explicit human implementation authorization and SAC-PLAN-0002 v0.2 at immutable approved SHA `4ce275b0ecb3cd297636bade6168407de4e3b2d0` | Authorizes branch creation, the six files, validation, one new non-amended commit, normal push, and one Draft PR. It does not authorize merge, Ready transition, SharePoint action, factual closure, architecture design, software implementation, or the 2026-07-23 evidence update |

## Publication boundary

These decisions are Git governance records only. They do not claim SharePoint publication, SharePoint approval, synchronization, PR merge authorization, or approval of the Draft Phase 2 documents.

## Current classifications

- **Confirmed:** The six bootstrap decisions and two narrowly scoped Phase 3 decisions above were explicitly authorized on 2026-07-22.
- **Assumption:** None recorded.
- **Unknown/TBD:** Future project decisions and SharePoint publication details are TBD.
- **Decision required:** Merge and any SharePoint action require separate human authorization.
