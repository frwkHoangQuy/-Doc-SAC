---
document_id: SAC-GOV-001
title: SAC Documentation Repository Overview
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# SAC Documentation Repository Overview

## Control state

- **Confirmed:** Git is the working source for SAC project documentation.
- **Confirmed:** SharePoint is the official publication and approval target, synchronized manually by the human authority.
- **Confirmed:** This baseline is Draft; no Phase 2 document is approved or synchronized to SharePoint.
- **Confirmed:** The repository is currently public.

> **Public-repository warning:** Never add secrets, credentials, customer-identifying data, sensitive handover details, non-public architecture, confidential operational information, production data, or production logs while this repository remains public.

## Purpose and early-stage boundary

This repository controls project and technical documentation for the early discovery and governance stage of SAC. It provides working history, review evidence, document templates, registers, and links to approved publication records. It does not establish project facts that have not been supported by evidence.

Project-content paths are created only when an evidence-backed document is ready to occupy them. Do not create speculative category directories or placeholder project documents.

## Repository boundaries

### Belongs in this Git repository

- Governance, plans, registers, templates, and evidence-backed project documentation.
- Drafts, review history, approved working versions, decisions, and sanitized references.
- Links to source-code artifacts and SharePoint records when those locations are authoritative.

### Belongs in the software source-code repository

- Application source code, executable tests, build automation, infrastructure-as-code, and code-coupled configuration.
- Technical artifacts whose changes must remain atomic with software changes.

The source-code repository location is **Unknown/TBD**.

### Belongs in SharePoint

- Official publication and approval copies.
- Signed acceptance records and access-controlled corporate records.
- Restricted source material that must not be stored in this repository.

The SharePoint location and approval workflow are **Unknown/TBD**.

### Never store in Git

- Passwords, tokens, API keys, private keys, connection strings, or other credentials.
- Customer-identifying or personal data.
- Sensitive handover information, non-public architecture, or confidential operational details.
- Production datasets, database exports, environment secrets, or production logs.
- Signed originals controlled in SharePoint.
- Chat or email as an authoritative document record.

## Human-authority model

Hoang Quy Nguyen (`frwkHoangQuy`) is the initial owner, approver, and human authority. A commit, push, or pull request records a proposal; it does not itself approve a document, authorize a merge, or prove SharePoint publication.

## Document lifecycle

- **Draft:** Active authoring; content may be incomplete and must expose gaps.
- **In Review:** Stable enough for formal review but not approved.
- **Approved:** Explicitly approved by the designated human authority under the governance workflow.
- **Superseded:** Replaced by a later approved version while history remains preserved.

## Fact and TBD policy

Classify information as one of:

- **Confirmed:** Supported by an identified authoritative source.
- **Assumption:** A working proposition awaiting validation.
- **Unknown/TBD:** Information is unavailable or unverified.
- **Decision required:** A choice must be made by an authorized person.

Never convert an assumption or TBD into a fact without evidence. Unknown project, customer, team, schedule, architecture, scope, or technical information remains `TBD`.

## Documentation language

- English is the authoritative standard language for documents maintained in Git.
- Create a Vietnamese or bilingual variant only for a defined audience or delivery obligation.
- Every translation must identify and remain traceable to its authoritative English source, including document ID, source path, and controlled version.
- Translation requirements do not authorize additional files unless their paths are explicitly approved.

## Navigation

| ID | Document |
|---|---|
| `SAC-GOV-001` | [SAC Documentation Repository Overview](README.md) |
| `SAC-GOV-002` | [Repository Agent Instructions](AGENTS.md) |
| `SAC-GOV-003` | [Document Governance](docs/00-project-control/document-governance.md) |
| `SAC-GOV-004` | [Git-SharePoint Synchronization Procedure](docs/00-project-control/git-sharepoint-sync.md) |
| `SAC-REG-001` | [Document Register](registers/document-register.md) |
| `SAC-REG-002` | [RAID Log](registers/raid-log.md) |
| `SAC-REG-003` | [Decision Log](registers/decision-log.md) |
| `SAC-TPL-001` | [Project Document Template](templates/project-document-template.md) |
| `SAC-TPL-002` | [Current-State Brief Template](templates/current-state-brief-template.md) |
| `SAC-TPL-003` | [Meeting Minutes Template](templates/meeting-minutes-template.md) |
| `SAC-TPL-004` | [Handover Checklist Template](templates/handover-checklist-template.md) |

## Current classifications

- **Confirmed:** This repository contains governance-only baseline material.
- **Assumption:** None recorded in this overview.
- **Unknown/TBD:** Project facts and external repository/SharePoint locations remain TBD.
- **Decision required:** None required to read or review this Draft baseline.
