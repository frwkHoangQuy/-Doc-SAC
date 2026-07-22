---
document_id: SAC-GOV-003
title: Document Governance
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# Document Governance

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This governance document is Draft and has not been approved or synchronized to SharePoint.
- The repository is public; restricted information must not be stored here.

## Authority model

Hoang Quy Nguyen (`frwkHoangQuy`) is the initial document owner, approver, and human authority. Material scope, baseline, lifecycle, publication, or governance changes require explicit human approval. A commit or pull request provides review history but does not itself constitute approval.

## Document lifecycle

| Status | Meaning | Entry condition | Exit condition |
|---|---|---|---|
| Draft | Active authoring; content may be incomplete | Document is created | Owner submits a stable revision for review |
| In Review | Content is stable enough for formal review | Owner identifies review scope and evidence | Approver accepts, rejects, or returns it to Draft |
| Approved | Human authority has explicitly approved the controlled version | Approval is recorded against an identified content version | A replacement is approved or approval is withdrawn |
| Superseded | A later approved version replaces the document | Replacement and relationship are recorded | Terminal state; history is retained |

SharePoint publication and synchronization are separate control fields in the document register. An `Approved` Git lifecycle status must not be used to claim SharePoint publication.

## Responsibilities

### Owner

- Maintains accuracy, evidence, metadata, links, and explicit TBDs.
- Prevents parallel working-source copies.
- Coordinates review and reconciliation.

### Approver

- Confirms evidence, scope, classification, and readiness.
- Approves or rejects explicitly; silence is not approval.
- Authorizes supersession and controlled publication actions.

The initial owner and approver are both Hoang Quy Nguyen by explicit human decision. Future delegation is **Unknown/TBD** until recorded.

## Naming and versioning

- Use lowercase `kebab-case` for repository paths except established root files such as `README.md` and `AGENTS.md`.
- Use ISO `YYYY-MM-DD` dates and `Asia/Ho_Chi_Minh` for timestamps that require a timezone.
- Keep stable filenames; store the controlled version in metadata, not the filename.
- Use `0.1`, `0.2`, and so on for Draft revisions.
- Use `1.0` for the first Approved release.
- Increment the minor version for compatible approved revisions and the major version for material baseline changes.
- Ordinary Git commits do not automatically require a document-version increment.

## Required metadata

| Field | Purpose |
|---|---|
| `document_id` | Stable identifier used in registers and references |
| `title` | Human-readable controlled title |
| `status` | Draft, In Review, Approved, or Superseded |
| `version` | Controlled document version |
| `owner` | Person accountable for maintenance |
| `approver` | Person authorized to approve |
| `github_identity` | GitHub identity mapped to the named authority |
| `last_updated` | ISO date of the document revision |

Do not embed the document's current Git commit SHA in its own metadata. A metadata update would create a new commit and immediately make the embedded SHA stale. Record `approved_content_commit` in the document register after the controlled content commit exists.

## Evidence and unknowns

Classify statements as:

- **Confirmed:** Supported by a cited authoritative source.
- **Assumption:** A working proposition awaiting validation.
- **Unknown/TBD:** Information is unavailable or unverified.
- **Decision required:** An authorized choice is outstanding.

Never invent facts or use `TBD` as implied approval. Customer, mandate, team, schedule, scope, architecture, and technical information remain TBD until evidence is supplied.

## Review, approval, and supersession workflow

1. Owner authors in Git and cites evidence.
2. Owner validates metadata, links, classifications, security, and diff scope.
3. Reviewer evaluates the proposed content in a branch or pull request.
4. Human approver records an explicit decision.
5. Authorized content is merged without implying SharePoint publication.
6. The exact content commit is recorded in the document register when approved.
7. SharePoint synchronization follows the separate synchronization procedure.
8. A replacement document identifies the superseded version; Git history is retained.

## Current classifications

- **Confirmed:** The initial governance baseline uses Draft status and version 0.1.
- **Assumption:** None recorded.
- **Unknown/TBD:** Future delegated roles and SharePoint location are TBD.
- **Decision required:** Approval and synchronization of this Draft require later explicit decisions.
