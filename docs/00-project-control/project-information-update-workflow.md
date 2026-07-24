---
document_id: SAC-GOV-005
title: Project Information Update Workflow
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-24
---

# Project Information Update Workflow

## Control state

- This Draft governs proposed information updates in the public Git working source.
- It does not approve a document, baseline, merge, publication, synchronization, or external action.
- Hoang Quy Nguyen (`frwkHoangQuy`) is the Human Authority. The Lead PM/SA is read-only; the repository Agent executes only personally transmitted, bounded instructions.

## Core controls

Each update receives one unique, never-reused `SAC-UPD-NNN` ID in the [Information Update Register](../../registers/information-update-register.md). Sources and atomic statements must be classified before impact mapping:

- **Source:** identified input whose existence alone establishes neither truth nor authority.
- **Evidence:** inspectable support with an immutable reference where practical.
- **Human Authority instruction/decision/approval:** an explicit bounded instruction or choice; discussion and silence are not authority.
- **Confirmed:** supported by identified authoritative evidence or an explicit authorized decision.
- **Assumption:** working proposition requiring validation.
- **Unknown/TBD:** unavailable or unverified; record `TBD`.
- **Decision required:** requires an identified authorized human choice.
- **Proposal/plan/review artifact:** non-canonical material that cannot authorize itself.
- **Canonical record:** designated Git working source under governance; Git presence alone is insufficient.
- **Historical record:** retained evidence that does not automatically control current authority.

PLAN and APPLY are separate. PLAN must name the immutable base, branch, exact ordinal path allowlist, per-file intent, commit/push counts, validations, safety boundary, rollback/partial-state rules, retained work, report path/parent, exclusions, and exact requested authorization. APPLY begins only after the Human Authority accepts the immutable plan and personally authorizes every transaction field.

## Thirteen-state lifecycle

No state authorizes the next state by itself. After each authorized transition, update the register and checkpoint only within a separately authorized allowlist.

| State | Entry and preconditions | Activity and required output | Role and decision boundary | Success, failure, correction, evidence, and stop |
|---|---|---|---|---|
| 1. `INTAKE` | Public-safe request or source; scope identifiable | Allocate ID; record source, request, date/timezone, phase, provisional classes, owner/approver, urgency, conflicts, questions, outcome | Authorized record owner or Agent prepares; no approval | Receipt is not acceptance. Unsafe or unidentified source stops; correction appends history. |
| 2. `SOURCE AND AUTHORITY ASSESSMENT` | Complete intake and accessible source | Record provenance, authority class, mutability, authenticity limits, and verification need | Owner/reviewer assesses; Human Authority decides disputed authority | Unverified remains unverified. False or ambiguous authority stops; retain evidence. |
| 3. `CLASSIFICATION` | Source assessment and atomic statements | Classify source, evidence, facts, instructions, proposals, assumptions, unknowns, decisions, approval, canonical/review/historical records | Owner/verifier prepares; Human Authority alone decides required choices | Unsupported claims remain `TBD`; changed classifications append evidence and rationale. |
| 4. `EVIDENCE CAPTURE` | Classification and public-safety clearance | Record immutable/sanitized evidence references, verification date, verifier, and limitations | Authorized verifier; no inferred approval | Missing, inaccessible, restricted, or contradictory evidence stops confirmation and returns to assessment/classification. |
| 5. `IMPACT MAPPING` | Classified change with evidence | Complete direct/indirect paths, registers, navigation, templates, downstream phases, history, links, owners, safety, consistency, validation, rollback, exclusions | Plan author prepares; reviewer tests completeness | Open-ended, hidden, unsafe, or unresolved impact stops; correction creates a new map version. |
| 6. `PLAN` | Accepted impact-map scope | Immutable proposal using the [PLAN template](../../templates/information-update-plan-template.md) | Agent/author prepares under bounded authority | Plan cannot self-approve. Missing base/path/intent/count/rollback/report field stops. |
| 7. `IMMUTABLE REVIEW` | Full plan SHA, path, blob, and live-state evidence | Versioned [review artifact](../../templates/review-artifact-template.md) with findings and recommendation | Lead PM/SA reviews read-only | Review artifact is non-canonical, has no PR, is never merged, and approves nothing; correction is a new commit/version. |
| 8. `HUMAN AUTHORITY AUTHORIZATION` | Reviewed immutable plan and resolved findings | Explicit Gate 2 decision naming subject SHA/path/blob, base, branch, allowlists, commit roles/counts, pushes, report path/parent, validation, safety, retained work, partial-state rules, exclusions, and stop | Human Authority only | Any absent, ambiguous, stale, or conflicting field stops. Authorization is limited to the named APPLY. |
| 9. `BOUNDED APPLY AND VALIDATION` | Personally transmitted complete authorization; live preflight matches | Exact canonical content commit, non-self-referential checkpoint commit, remote read-back, and Gate 3 execution report | Repository Agent executes; Lead PM/SA later verifies read-only | Extra path/action, unsafe content, failed validation, drift, or ambiguous remote state stops without amend, rebase, force, compensation, or guessed values. No implied PR. |
| 10. `PR AUTHORIZATION` | Accepted implementation/report SHAs and current live head, when a PR is applicable | Explicit permission naming PR action, base, head, and limits | Human Authority only; Agent executes if separately instructed | No PR by default. Drift or absent authority stops; PR presence is not approval. |
| 11. `MERGE AUTHORIZATION` | Reviewed PR head and required checks, when a PR exists | Explicit target, method, and exact-head decision | Human Authority only | Failed/drifted checks stop. PR approval or capability does not authorize merge. |
| 12. `BASELINE DECISION` | Verified canonical/merge state and exact content SHA | Explicit accept, reject, or correction decision with register scope | Human Authority only | Merge does not imply baseline. Rejection preserves history; correction returns to PLAN. |
| 13. `PUBLICATION / SYNCHRONIZATION AUTHORIZATION` | Accepted baseline; exact approved content SHA; classified publication copy; verified destination/workflow and public/private boundary; passed safety review; named executor | Separate authorization naming content, destination, executor, validation, evidence, and later register-update scope | Human Authority authorizes; authorized human performs external action; Agent changes Git only under another bounded instruction | Authorization is not publication. Success requires external evidence and later authorized register update. Failure leaves the Git baseline and publication fields unchanged; not-applicable requires an explicit decision. Missing destination, approval, safety, or SHA stops. |

## Review, checkpoint, and recovery

Review artifacts use literal versioned paths under `agent-artifacts/issue-<n>/gate-<n>/`, are immutable, non-canonical, never registered in the Document Register, never used for a PR, and never merged. Corrections add successor artifacts and preserve predecessors.

Gate 3 uses four non-self-referential identifiers:

1. implementation content SHA (content commit);
2. checkpoint-record commit SHA (journal-only child);
3. current implementation branch head (the checkpoint commit after read-back); and
4. execution-report review SHA (returned after the report commit).

The journal records the content SHA, not its own containing SHA. A fresh reviewer uses [AGENTS.md](../../AGENTS.md), [README](../../README.md), this workflow, both registers, controlling Issue, exact SHAs/paths, and live refs to verify journal subject = checkpoint parent, live implementation head = checkpoint commit, and report values = both commits and head. Any mismatch freezes progression.

## Correction, migration, and retained history

- Corrections use new bounded plans, commits, and review-artifact versions; never amend, rebase, reset, force-push, delete, or conceal history.
- Migration/supersession requires an explicit Human Authority mapping of each predecessor to continue, migrate, supersede, retain, or close.
- Paused Issue #2, Draft PR #3, PR #4, `SAC-PLAN-0002`, and existing branches remain retained history until a later explicit decision.
- Partial or ambiguous transactions stop at the observed boundary. Preserve created local commits or verified remote commits and request new authority; do not compensate automatically.

## Public safety and stop rules

Only the necessary public governance identity `Hoang Quy Nguyen` (`frwkHoangQuy`) is permitted. Stop before recording any other personal/customer/stakeholder identity, private contact, credential, token, key, endpoint, production/confidential detail, private corporate/SharePoint content, or sensitive personal data. Technical capability, a state, commit, branch, review, PR, merge, baseline, or successful validation never authorizes the next action.

## Current classifications

- **Confirmed:** This file defines a Draft governance workflow and no project facts.
- **Assumption:** None recorded.
- **Unknown/TBD:** Future delegated authorities and publication destination remain TBD.
- **Decision required:** Approval, PR, merge, baseline, publication, migration, and later gates require separate explicit decisions.
