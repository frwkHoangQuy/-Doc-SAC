---
document_id: SAC-GOV-003
title: Document Governance
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-24
---

# Document Governance

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This governance document is Draft and has not been approved or synchronized to SharePoint.
- The repository is public; restricted information must not be stored here.

## Authority model

Hoang Quy Nguyen (`frwkHoangQuy`) is the initial document owner, approver, and human authority. Material scope, baseline, lifecycle, publication, or governance changes require explicit human approval. A commit or pull request provides review history but does not itself constitute approval.

## Scope and exclusions

This governance applies to controlled Markdown governance documents, registers, templates, and later evidence-backed project documents maintained in this repository.

It excludes application source code, executable tests, build or deployment automation, infrastructure-as-code, secrets, production data, signed originals controlled in SharePoint, and speculative project-content placeholders. Software-coupled artifacts belong in the applicable source-code repository; restricted corporate records belong in an authorized access-controlled system.

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

## Documentation language and translations

- English is the authoritative standard language for documents maintained in Git.
- Vietnamese or bilingual variants are created only for a defined audience or delivery obligation and an explicitly approved path.
- Each translation must identify its authoritative English source by document ID, Git path, and controlled version.
- A translation must be reconciled when its English source changes; it must not become an independent working source.

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

The following synchronization fields are maintained only in the document register, not embedded in each document:

| Register-only field | Purpose |
|---|---|
| `approved_content_commit` | Exact approved Git content commit |
| `sharepoint_url` | Verified official SharePoint location |
| `sharepoint_status` | Current SharePoint workflow/publication state |
| `sharepoint_version` | SharePoint-controlled version or reference |
| `sharepoint_synced_at` | Verified manual synchronization timestamp |

## Evidence and unknowns

Classify statements as:

- **Confirmed:** Supported by a cited authoritative source.
- **Assumption:** A working proposition awaiting validation.
- **Unknown/TBD:** Information is unavailable or unverified.
- **Decision required:** An authorized choice is outstanding.

Never invent facts or use `TBD` as implied approval. Customer, mandate, team, schedule, scope, architecture, and technical information remain TBD until evidence is supplied.

## Authoritative sources and links

- Cite the authoritative source for every substantive claim; identify its owner, stable reference, or controlled location where available.
- Chat and email may initiate work but are not authoritative document stores.
- Classify each source as authoritative evidence, supporting evidence, Human Authority instruction, discussion, Agent analysis, proposal/plan, review artifact, approved decision, canonical record, or historical record. Source existence does not establish truth or authority.
- Process proposed project-information changes through [SAC-GOV-005](project-information-update-workflow.md) using a stable `SAC-UPD-NNN`, statement classifications, evidence capture, exact impact mapping, and separate PLAN/APPLY authority.
- Use relative links for repository files. Resolve each link from the directory containing the source Markdown file and validate that its target exists.
- Use sanitized authorized links for restricted external evidence. Do not copy restricted content into this public repository.

## Review, approval, and supersession workflow

1. Owner authors in Git and cites evidence.
2. Owner validates metadata, links, classifications, security, and diff scope.
3. Reviewer evaluates the proposed content in a branch or pull request.
4. Human approver records an explicit decision.
5. Authorized content is merged without implying SharePoint publication.
6. The exact content commit is recorded in the document register when approved.
7. SharePoint synchronization follows the separate synchronization procedure.
8. A replacement document identifies the superseded version; Git history is retained.

The reusable information-update lifecycle has thirteen separately controlled states: `INTAKE`, `SOURCE AND AUTHORITY ASSESSMENT`, `CLASSIFICATION`, `EVIDENCE CAPTURE`, `IMPACT MAPPING`, `PLAN`, `IMMUTABLE REVIEW`, `HUMAN AUTHORITY AUTHORIZATION`, `BOUNDED APPLY AND VALIDATION`, `PR AUTHORIZATION`, `MERGE AUTHORIZATION`, `BASELINE DECISION`, and `PUBLICATION / SYNCHRONIZATION AUTHORIZATION`. No state authorizes the next.

Immutable review artifacts are versioned non-canonical evidence on `review/agent-artifacts`; they have no Document Register row, Pull Request, or merge path and cannot approve themselves. Canonical APPLY uses exact allowlists and a non-self-referential journal checkpoint: the journal records the content commit, while Git supplies the containing checkpoint and execution-report SHAs after creation. Fresh-context recovery must verify subject, parent, live head, report, and retained work.

Migration or supersession requires an explicit Human Authority mapping for every predecessor; history remains preserved. PR creation, merge, baseline acceptance, and publication/synchronization are separate decisions. Publication authorization requires an accepted baseline, exact approved content SHA, classified copy, verified destination/workflow and boundary, successful safety review, executor, validation, evidence, and a later separately authorized register update. Authorization is not external completion; failure leaves the Git baseline and publication fields unchanged.

## Correction handling

1. Record the correction source, affected document/version, evidence, and requested outcome.
2. Stop parallel editing when an authoritative SharePoint correction affects the Git working source.
3. Reconcile the correction on an explicitly authorized Git branch without overwriting history.
4. Revalidate facts, metadata, links, confidentiality, register impact, and supersession impact.
5. Obtain review and human approval before merge.
6. If publication is required, republish from the exact reconciled Git content commit and update the document register.

For immutable plans, reviews, checkpoints, or partial transactions, correction uses a new bounded version and new commits. Never amend, rebase, reset, force-push, delete history, guess a self-referential SHA, or automatically compensate for ambiguous remote state.

## Public-repository confidentiality restrictions

While this repository remains public, never store secrets, credentials, tokens, keys, connection strings, customer-identifying or personal data, sensitive handover details, non-public architecture, confidential operational information, production data, database exports, environment secrets, production logs, restricted commercial records, or signed originals. Future sensitive or non-public project content requires verified private visibility and appropriate access controls first.

## Current classifications

- **Confirmed:** The initial governance baseline uses Draft status and version 0.1.
- **Assumption:** None recorded.
- **Unknown/TBD:** Future delegated roles and SharePoint location are TBD.
- **Decision required:** Approval and synchronization of this Draft require later explicit decisions.
