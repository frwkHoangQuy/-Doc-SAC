---
document_id: SAC-GOV-002
title: Repository Agent Instructions
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# Repository Agent Instructions

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This file and all Phase 2 baseline files are Draft, not approved, and not synchronized to SharePoint.
- The repository is public. The sensitive-data prohibitions below are mandatory.

## Authority and instruction precedence

1. Follow system and platform safety requirements.
2. Follow explicit instructions from human authority Hoang Quy Nguyen (`frwkHoangQuy`).
3. Follow the approved controlling plan and the narrow changed-file allowlist for the task.
4. Follow the nearest applicable `AGENTS.md` and repository governance documents.

If instructions conflict materially or authorization is unclear, stop without writing and report the conflict.

## Scope and allowlist discipline

- Read all applicable repository instructions before acting.
- Verify branch, HEAD, remote, status, and authorized file set before editing.
- Create, modify, stage, commit, and push only explicitly authorized paths.
- Never discard, overwrite, combine, or amend unrelated user work.
- Do not create placeholder files or directories outside the authorized set.
- Do not merge, change settings, publish, or synchronize unless separately authorized.

## Evidence and factual integrity

Never invent customer, project, team, mandate, schedule, architecture, scope, resource, RAID, test, or technical facts. Use these classifications explicitly:

- **Confirmed:** Supported by an identified source.
- **Assumption:** A working proposition requiring validation.
- **Unknown/TBD:** Not known or not verified; write `TBD`.
- **Decision required:** Requires an authorized human choice.

Do not silently promote assumptions or chat statements into confirmed repository facts.

## Approval discipline

- A branch, commit, push, or pull request is a review artifact, not approval.
- A Draft PR must remain unmerged until explicit human approval and merge authorization are recorded.
- Document status changes require the lifecycle workflow in `docs/00-project-control/document-governance.md`.
- Never embed a document's current Git commit SHA in its own metadata.

## Git and SharePoint reconciliation

- Git is the sole working source for editable documents.
- SharePoint is the official manual publication and approval target.
- Publish only the exact approved Git content commit.
- Record SharePoint URL, version, status, and synchronization time in the document register after synchronization.
- If a correction originates in SharePoint, stop parallel editing, reconcile the correction back into Git through review, and then republish the reconciled Git version.
- Email and chat are not authoritative document stores.

## Security and public-repository restrictions

Never add:

- secrets, credentials, tokens, keys, or connection strings;
- customer-identifying or personal data;
- sensitive handover information;
- non-public architecture or confidential operational information;
- production data, database exports, or production logs.

Private visibility and appropriate access controls must be verified before any sensitive or non-public project content is considered.

## Required validation

Before committing, verify the exact changed-file set, metadata, links, Markdown structure, sensitive-data absence, `git diff --check`, full diff, staged scope, and clean handling of unrelated work.

## Current classifications

- **Confirmed:** Hoang Quy Nguyen is the initial human authority, owner, and approver; GitHub identity is `frwkHoangQuy`.
- **Assumption:** None recorded in these instructions.
- **Unknown/TBD:** Future delegated authorities are TBD.
- **Decision required:** Any expanded scope or elevated action requires explicit human authorization.
