---
plan_id: SAC-PLAN-0002
title: Current-State Discovery and Decision Readiness
status: Approved
version: 0.2
repository: frwkHoangQuy/-Doc-SAC
plan_branch: plan/0002-current-state-discovery-readiness
prepared_by: Codex
human_authority: Hoang Quy Nguyen
created_date: 2026-07-22
review_commit: 4ce275b0ecb3cd297636bade6168407de4e3b2d0
approval_status: Approved
implementation_authorization: Approved for exactly the Section 4 six-file allowlist
---

# Current-State Discovery and Decision Readiness Plan

## Control state

- **Confirmed:** SAC-PLAN-0002 v0.2 was approved on 2026-07-22 at commit `4ce275b0ecb3cd297636bade6168407de4e3b2d0` as the controlling Phase 3 plan.
- **Confirmed:** The repository working source is Git; SharePoint is the official manual publication and approval target under the existing governance documents.
- **Confirmed:** The repository is public and its public-repository restrictions apply to all Phase 3 work.
- **Confirmed:** Phase 3 Discovery Draft implementation is authorized only on `implementation/0002-current-state-discovery-readiness` and only for the exact six-file allowlist in Section 4.
- **Decision required:** Merge authorization is not granted by this plan, its approval, its implementation authorization, or any review artifact.

## Execution record

- **Confirmed:** The controlling plan was approved on 2026-07-22, and the authorized implementation branch is `implementation/0002-current-state-discovery-readiness`.
- **Confirmed:** The Discovery Draft package was created under the exact Section 4 six-file allowlist.
- **Confirmed:** `SAC-DOC-001`, `SAC-DOC-002`, and `SAC-REG-004` remain Draft / Not Approved.
- **Unknown/TBD:** Factual evidence review remains pending; the 2026-07-23 evidence update requires separate explicit authorization.
- **Decision required:** Merge, Ready transition, SharePoint action, factual closure, architecture design, and software implementation remain unauthorized.

## 1. Phase 3 objective

- **Confirmed:** Phase 3 will prepare a public-safe Discovery Draft package that exposes evidence gaps, prepares a complete confirmation inventory for 2026-07-23, and supports later delivery-strategy decisions without inventing project facts.
- **Unknown/TBD:** Project mandate, objectives, stakeholders, software condition, delivery scope, schedule, architecture, and delivery ownership are not confirmed by this plan.
- **Assumption:** Authorized evidence and human answers can be reviewed on 2026-07-23; this is a planning assumption rather than a schedule commitment.

## 2. Mandatory classification and evidence rules

Every material statement in the Phase 3 Discovery Draft package must use one of these classifications:

| Classification | Required meaning and handling |
|---|---|
| **Confirmed** | Supported by an identified authoritative source or explicit authorized human decision; cite a sanitized reference or authorized access-controlled evidence link. |
| **Assumption** | A working proposition requiring validation; do not present it as fact or approval. |
| **Unknown/TBD** | Unavailable or unverified information; write `TBD` and identify the evidence or answer needed where practical. |
| **Decision required** | An authorized human choice is outstanding; identify the decision, authority, options where known, and evidence needed. |

- **Confirmed:** Receipt of information is not confirmation, verification, acceptance, approval, or closure.
- **Confirmed:** Chat and email are not authoritative project-document stores under the repository governance.
- **Unknown/TBD:** Any claim without identified supporting evidence remains `TBD` rather than being inferred from this plan.

## 3. Boundaries and required TBD decisions

- **Decision required:** Delivery ownership is TBD: the Hanoi team and Ho Chi Minh City team must not be assigned ownership until an authorized human decision and supporting handover evidence are recorded.
- **Decision required:** Delivery strategy is TBD: whether to build new software, extend or reuse existing software, or use a hybrid approach requires an authorized decision after evidence review.
- **Unknown/TBD:** No team assignment, reuse conclusion, architecture choice, scope commitment, schedule commitment, or other unverified project fact is established by this plan.
- **Confirmed:** Phase 3 may document questions, evidence references, statuses, gaps, and decision requirements; it must not convert an unverified item into a confirmed fact.

## 4. Proposed exact Phase 3 implementation allowlist

After explicit plan-SHA approval, the implementation branch may create or modify only the following paths:

| Path | Intended Phase 3 action |
|---|---|
| `docs/plans/0002-current-state-discovery-and-decision-readiness-plan.md` | Update only the plan's execution/status record to state whether the three Discovery Draft documents and consolidated confirmation inventory were created, which items remain awaiting evidence review, and that approval/merge remain ungranted. Do not use this update to claim factual closure or approval. |
| `docs/02-handover-and-discovery/current-state-brief.md` | Create a public-safe Discovery Draft current-state brief using explicit classifications and sanitized evidence references. |
| `docs/02-handover-and-discovery/handover-checklist.md` | Create a public-safe handover checklist that records requested evidence, receipt/review state, gaps, and verification status without sensitive detail. |
| `docs/02-handover-and-discovery/confirmation-register.md` | Create the consolidated confirmation inventory for evidence, answers, classification, owner, due/target context where authorized, and decision readiness. |
| `registers/document-register.md` | Add `Project Document` as a permitted classification and add only the three Phase 3 document rows defined in Section 5; leave approval, `approved_content_commit`, and SharePoint fields unapproved or `TBD`. |
| `registers/decision-log.md` | Preserve `SAC-DEC-001` through `SAC-DEC-006` exactly and add only the two authorized decision records defined in Section 6. |

- **Confirmed:** The plan file is included only because Phase 3 implementation is expected to make the narrow execution/status-record update described in the first allowlist row.
- **Decision required:** The exact allowlist above requires explicit human approval against this pushed plan SHA before implementation begins.
- **Confirmed:** No other repository file is authorized for Phase 3 implementation by this plan.

## 5. Document-control mapping

The following are the only Phase 3 document-control identifiers authorized for later implementation. Their initial control states are not approvals.

| Document ID | Title | Classification | Initial status | Path |
|---|---|---|---|---|
| `SAC-DOC-001` | Current-State Brief | Project Document | Draft / Not Approved | `docs/02-handover-and-discovery/current-state-brief.md` |
| `SAC-DOC-002` | Handover Checklist | Project Document | Draft / Not Approved | `docs/02-handover-and-discovery/handover-checklist.md` |
| `SAC-REG-004` | Confirmation Register | Register | Draft / Not Approved | `docs/02-handover-and-discovery/confirmation-register.md` |

- **Confirmed:** Later authorized implementation must update `registers/document-register.md` to add `Project Document` as a permitted classification and add only the three rows above.
- **Confirmed:** The three new rows must leave approval, `approved_content_commit`, and all SharePoint fields unapproved or `TBD`.
- **Confirmed:** No additional document ID or document-register row is authorized by this plan.
- **Decision required:** Plan approval and implementation authorization approve the controlling plan and permit only the six-file implementation; they do not approve `SAC-DOC-001`, `SAC-DOC-002`, or `SAC-REG-004`.

## 6. Decision-log mapping and authorization state

- **Confirmed:** Later authorized implementation must preserve `SAC-DEC-001` through `SAC-DEC-006` exactly, including wording, status, evidence, scope, and order.
- **Confirmed:** Later authorized implementation may add only `SAC-DEC-007` for explicit approval of the final SAC-PLAN-0002 SHA and `SAC-DEC-008` for explicit authorization of the exact six-file Phase 3 implementation allowlist.
- **Confirmed:** Each permitted new decision record must cite the immutable approved plan SHA and explicit human authorization.
- **Confirmed:** No Proposed, Approved, or inferred decision record may be created for Hanoi versus Ho Chi Minh City delivery ownership or new-build versus reuse/extension versus hybrid delivery strategy.
- **Decision required:** Delivery ownership and delivery strategy remain separate unresolved human decisions, even after plan approval and implementation authorization.
- **Confirmed:** Plan approval and implementation authorization do not authorize merge, Ready transition, SharePoint action, factual closure, delivery ownership, delivery strategy, architecture design, or software implementation.

## 7. Required confirmation inventory coverage

The consolidated confirmation inventory and related Discovery Draft documents must cover each item below. Unless evidence is supplied and cited, each item is **Unknown/TBD**.

| Coverage area | Required confirmation focus | Initial classification |
|---|---|---|
| Mandate, objectives, authority, and stakeholders | Authoritative mandate, intended outcomes, decision authority, stakeholder roles, and authorized contact references | **Unknown/TBD** |
| Team responsibilities and handover status | Hanoi and Ho Chi Minh City responsibilities, handover evidence, receiving-party verification, and unresolved ownership | **Unknown/TBD** |
| Existing software and reuse feasibility | Software inventory, ownership, condition, constraints, and evidence relevant to new-build, extension/reuse, or hybrid feasibility | **Unknown/TBD** |
| Repositories | Repository locations, ownership, branch controls, documentation boundaries, and authorized access process | **Unknown/TBD** |
| Scope and exclusions | Requested outcomes, included work, exclusions, constraints, and change-control source | **Unknown/TBD** |
| Customer requirements and acceptance criteria | Sanitized requirement sources, acceptance authority, criteria, traceability, and evidence gaps | **Unknown/TBD** |
| Schedule and milestones | Authoritative dates, milestone definitions, dependencies, and schedule owner | **Unknown/TBD** |
| Resources | Available roles, capacity, skills, budget context where authorized, and constraints | **Unknown/TBD** |
| Architecture and integrations | Sanitized architecture evidence, integration inventory, ownership, constraints, and unknowns | **Unknown/TBD** |
| Environments and access | Environment inventory, access-request process, accountable approvers, and gaps; never credentials or private endpoints | **Unknown/TBD** |
| Data and security | Data classifications, handling constraints, security responsibilities, review evidence, and gaps | **Unknown/TBD** |
| Defects and technical debt | Sanitized records, severity/triage process, ownership, and impacts without confidential detail | **Unknown/TBD** |
| Testing and UAT | Test assets, evidence, known gaps, UAT scope, acceptance authority, and status | **Unknown/TBD** |
| Deployment | Release/deployment process, approvals, rollback evidence, ownership, and readiness gaps | **Unknown/TBD** |
| Operations and support | Support model, operational ownership, monitoring/escalation evidence, and transition gaps | **Unknown/TBD** |
| Dependencies | Internal/external dependencies, owners, constraints, and evidence needed | **Unknown/TBD** |
| SharePoint workflow | Authorized site/library, publication and approval workflow, access process, and synchronization status | **Unknown/TBD** |
| Delivery ownership decision | Hanoi or Ho Chi Minh City delivery ownership; evidence and authority required | **Decision required** |
| Delivery strategy decision | New software, extension/reuse, or hybrid approach; evidence and authority required | **Decision required** |

## 8. Public-repository restrictions

- **Confirmed:** Do not include credentials, tokens, keys, connection strings, customer or personal identifiers, private endpoints, production information, confidential architecture, or sensitive handover details.
- **Confirmed:** Use sanitized references and authorized access-controlled evidence links only.
- **Confirmed:** An access-controlled evidence location may be referenced only when its link and description are safe for this public repository; restricted content must not be copied into Git.
- **Unknown/TBD:** Whether any proposed evidence is safe to reference remains TBD until its classification and access controls are verified.

## 9. Completion and evidence-review distinction

- **Confirmed:** Tonight, the Discovery Draft documents and a consolidated confirmation inventory may be completed as draft structures and evidence-gap records.
- **Assumption:** “Tonight” refers to 2026-07-22 in `Asia/Ho_Chi_Minh` for this planning context; it is not a commitment to confirm project facts by that date.
- **Confirmed:** Tomorrow, 2026-07-23 in `Asia/Ho_Chi_Minh`, evidence and human answers may update classifications.
- **Confirmed:** Phase 3 must not be described as factually confirmed or closed before evidence review.
- **Decision required:** Any statement that evidence review is complete, a decision is made, or a document is approved requires explicit authorized evidence or approval.

### Tomorrow's evidence update

- **Decision required:** Evidence and human answers on 2026-07-23, `Asia/Ho_Chi_Minh`, require separate explicit authorization before they are recorded in Git.
- **Confirmed:** If separately authorized, the evidence update must be recorded in a new non-amended commit on the same implementation branch and use the existing single Draft PR.
- **Confirmed:** That later evidence-update commit must be pushed normally without force and receive another SHA/PR review.
- **Decision required:** A second branch or PR for the evidence update is not authorized unless separately approved.

## 10. Required implementation workflow and prohibitions

The required workflow is:

```text
explicit plan-SHA approval
→ implementation branch `implementation/0002-current-state-discovery-readiness`
→ exact allowlist
→ validation
→ new non-amended commit
→ normal push
→ one Draft PR
→ SHA/PR review
```

- **Decision required:** Create `implementation/0002-current-state-discovery-readiness` only after explicit approval of the final pushed plan SHA and the exact six-file allowlist in Section 4.
- **Confirmed:** The implementation branch must be created from the approved plan SHA itself, not from `main`.
- **Confirmed:** This correction does not create, move, or otherwise modify the implementation branch.
- **Confirmed:** The implementation commit must be new and non-amended.
- **Confirmed:** The implementation must be normally pushed without force and reviewed through one Draft PR.
- **Confirmed:** This planning task does not authorize or perform substantive Phase 3 implementation, merge or Ready transition, SharePoint synchronization, architecture design, or software implementation.
- **Decision required:** Merge, a Ready transition, SharePoint synchronization, architecture design, and software implementation each require separate explicit authorization.

## 11. Validation and acceptance checks for later implementation

Before an authorized Phase 3 implementation commit, validate:

- **Confirmed:** Document metadata, Markdown structure, classifications, proposed allowlist conformance, register alignment, relative links, `Asia/Ho_Chi_Minh` dates, and public-safety restrictions.
- **Confirmed:** Every repository-relative Markdown link resolves from the source document directory.
- **Confirmed:** `git diff --check` passes and the complete staged diff is inspected.
- **Confirmed:** The staged paths deterministically equal the explicitly approved implementation allowlist, with no missing or extra path.
- **Confirmed:** No unstaged or untracked changes are present before committing, and remote topology/divergence is reconfirmed before pushing.
- **Confirmed:** The pushed implementation commit is checked to contain only the authorized paths, and the worktree is clean at handoff.
- **Decision required:** Any scope mismatch, missing authorization, sensitive-data finding, unresolved topology divergence, or unsupported claim stops implementation pending human direction.

## 12. Review state and authorization gate

- **Confirmed:** Plan status is **Proposed / Not Approved**.
- **Decision required:** This plan’s controlling review object is its pushed Git commit SHA; content pasted into chat or an issue is not a substitute for SHA-based review.
- **Decision required:** Substantive Phase 3 implementation and merge authorization are not effective until explicit human approval is issued against the pushed plan SHA.
- **Confirmed:** The document register intentionally has no controlling-plan row under current register design; the plan must not cause an unapproved register change during this planning task.

## 13. Plan-review acceptance criteria

- **Confirmed:** A reviewer can identify the Phase 3 objective, public-safety boundary, mandatory classifications, all required confirmation coverage, both unresolved delivery-strategy decisions, exact proposed implementation allowlist, completion distinction, workflow, and authorization gates from this plan.
- **Decision required:** Human approval must identify this exact pushed commit SHA and confirm the exact implementation allowlist before substantive Phase 3 work begins.

## Current classifications

- **Confirmed:** This is a public-safe planning artifact only; it establishes no project facts beyond the authorized planning instructions and existing repository governance.
- **Assumption:** Authorized evidence and human responses may be available for review on 2026-07-23, `Asia/Ho_Chi_Minh`.
- **Unknown/TBD:** All unverified project facts, including mandate, team responsibilities, software condition, scope, schedule, resources, architecture, and operational readiness, remain TBD.
- **Decision required:** Approve this pushed plan SHA and exact allowlist before implementation; separately decide delivery ownership, delivery strategy, merge, and any SharePoint action.
