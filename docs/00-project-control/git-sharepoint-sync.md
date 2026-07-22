---
document_id: SAC-GOV-004
title: Git-SharePoint Synchronization Procedure
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# Git-SharePoint Synchronization Procedure

## Control state

- Git is the sole working source for editable SAC documentation.
- SharePoint is the official manual publication and approval target.
- This procedure is Draft. Phase 2 performs no SharePoint publication, approval, or synchronization.
- The SharePoint site, library, and approval workflow are **Unknown/TBD**.

## Source-of-truth rule

Each authoritative document has one working source in Git. Email, chat, local exports, and SharePoint copies must not become parallel editing sources. SharePoint changes must be reconciled back into Git before further editing continues.

## Publication prerequisites

Before publication, verify that:

- the document passed review and has explicit human approval for the identified version;
- merge authorization was granted and the controlled content is present on `main`;
- the exact content commit is known and the working tree is clean;
- metadata, register entry, relative links, and evidence references are valid;
- the public-repository confidentiality review passed; and
- the authorized SharePoint destination and required corporate approval workflow are known.

If any prerequisite is missing, stop synchronization and record the state as `TBD` or a controlled exception; do not infer success.

## Manual synchronization ownership

Hoang Quy Nguyen (`frwkHoangQuy`) is the initial owner of the manual Git-to-SharePoint synchronization action. Automation, delegation, or another synchronization owner is **Unknown/TBD** until explicitly approved. Uploading or publishing is a separate authorized action and is never implied by merge.

## Required synchronization sequence

1. **Author:** Create or revise the document in Git using evidence-backed content and explicit TBDs.
2. **Review:** Validate content, metadata, links, classification, sensitive-data absence, and exact diff scope in a branch or pull request.
3. **Human approval:** Obtain an explicit approval decision from the designated approver.
4. **Merge:** Merge only after separate merge authorization.
5. **Identify content commit:** Record the exact Git commit containing the controlled content; do not infer it from a local workspace.
6. **Export or copy:** Produce the publication copy from that exact commit.
7. **SharePoint publication:** The human authority manually places the copy in the authorized SharePoint location and completes the official approval process.
8. **Update register:** Record `approved_content_commit`, SharePoint URL, SharePoint status, SharePoint version, and synchronization timestamp in the document register through a reviewed Git change.

## SharePoint-originated corrections

1. Stop parallel editing of the affected Git document.
2. Identify the exact SharePoint revision, correction, source, and approval context.
3. Reconcile the correction into a Git branch.
4. Review and approve the Git change under document governance.
5. Merge only when separately authorized.
6. Republish the reconciled Git-controlled version to SharePoint.
7. Update the document register.

## Exception and failure handling

- **Approval missing or rejected:** Do not publish; return the document to the applicable lifecycle state and record the decision evidence.
- **Content changed during export:** Discard the export, identify the intended Git content commit again, and regenerate it.
- **SharePoint unavailable or upload fails:** Leave all SharePoint register fields unchanged or `TBD`; record the failure outside sensitive content and retry only when authorized.
- **SharePoint copy differs from Git:** Stop further editing and publication, compare against the identified content commit, and reconcile through Git review.
- **Unauthorized SharePoint edit:** Treat it as a proposed correction; do not overwrite Git or accept it silently.
- **Sensitive information discovered:** Stop immediately, do not publish or commit it, notify the human authority, and follow the applicable security process.
- **Incorrect register entry:** Correct the register through a reviewed Git change; never rewrite Git history or fabricate timestamps.

Exceptions do not waive approval, confidentiality, traceability, or reconciliation requirements.

## Sensitive information

The repository is public. Never synchronize into Git any secret, credential, customer-identifying data, sensitive handover detail, non-public architecture, confidential operational information, production data, or production log. Use a sanitized reference to an access-controlled SharePoint record when authorized.

## Phase 2 synchronization status

| Field | Value |
|---|---|
| Approval | Not approved |
| SharePoint URL | TBD |
| SharePoint status | TBD |
| SharePoint version | TBD |
| SharePoint synchronized at | TBD |

## Current classifications

- **Confirmed:** Synchronization is manual and performed by the human authority after the required gates.
- **Assumption:** None recorded.
- **Unknown/TBD:** SharePoint location and corporate approval mechanics are TBD.
- **Decision required:** Publication and synchronization require separate human authorization.
