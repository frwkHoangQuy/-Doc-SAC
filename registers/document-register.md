---
document_id: SAC-REG-001
title: Document Register
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# Document Register

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This register and every listed Phase 2 document are Draft and version 0.1.
- No listed document has an approved content commit or SharePoint synchronization record.
- The repository is public; no sensitive or customer-identifying information may be recorded.

## Purpose

This register provides version, ownership, approval, Git-content, and SharePoint traceability for the exact 11 Phase 2 baseline files. The controlling plan artifact is intentionally not a register row.

## Classifications

- **Governance:** Repository rules, scope, authority, or operating procedures.
- **Register:** Controlled structured records maintained over time.
- **Template:** Controlled reusable structures; a template is not a completed project-content document.

## Registered documents

| Document ID | Git path | Title | Classification | Status | Version | Owner | Approver | GitHub identity | approved_content_commit | sharepoint_url | sharepoint_status | sharepoint_version | sharepoint_synced_at |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `SAC-GOV-001` | `README.md` | SAC Documentation Repository Overview | Governance | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-GOV-002` | `AGENTS.md` | Repository Agent Instructions | Governance | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-GOV-003` | `docs/00-project-control/document-governance.md` | Document Governance | Governance | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-GOV-004` | `docs/00-project-control/git-sharepoint-sync.md` | Git-SharePoint Synchronization Procedure | Governance | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-REG-001` | `registers/document-register.md` | Document Register | Register | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-REG-002` | `registers/raid-log.md` | RAID Log | Register | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-REG-003` | `registers/decision-log.md` | Decision Log | Register | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-TPL-001` | `templates/project-document-template.md` | Project Document Template | Template | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-TPL-002` | `templates/current-state-brief-template.md` | Current-State Brief Template | Template | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-TPL-003` | `templates/meeting-minutes-template.md` | Meeting Minutes Template | Template | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |
| `SAC-TPL-004` | `templates/handover-checklist-template.md` | Handover Checklist Template | Template | Draft | 0.1 | Hoang Quy Nguyen | Hoang Quy Nguyen | `frwkHoangQuy` | TBD | TBD | TBD | TBD | TBD |

## Maintenance rules

- Update a row only through a reviewed Git change.
- Record `approved_content_commit` only after the controlled content commit exists and is approved.
- Populate SharePoint fields only from verified publication evidence.
- Use ISO dates and `Asia/Ho_Chi_Minh` for synchronization timestamps.
- Do not embed the current commit SHA in a document's own metadata.

## Current classifications

- **Confirmed:** Exactly 11 Phase 2 baseline files are registered.
- **Assumption:** None recorded.
- **Unknown/TBD:** All approval-commit and SharePoint fields are TBD.
- **Decision required:** Approval and publication require later explicit human decisions.
