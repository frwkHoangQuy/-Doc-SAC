---
document_id: SAC-REG-002
title: RAID Log
status: Draft
version: 0.1
owner: Hoang Quy Nguyen
approver: Hoang Quy Nguyen
github_identity: frwkHoangQuy
last_updated: 2026-07-22
---

# RAID Log

## Control state

- Git is the working source; SharePoint is the official manual publication and approval target.
- This register is Draft and has not been approved or synchronized to SharePoint.
- The repository is public; entries must not contain sensitive or customer-identifying information.

## Definitions

- **Risk:** An uncertain event that may affect an objective.
- **Assumption:** A proposition treated as true for planning but not yet confirmed.
- **Issue:** A current condition requiring resolution.
- **Dependency:** An external or internal prerequisite affecting progress.

## Field definitions

| Field | Meaning |
|---|---|
| ID | Stable identifier in the format `SAC-RAID-NNN` |
| Type | Risk, Assumption, Issue, or Dependency |
| Description | Concise statement without unsupported facts |
| Evidence | Source supporting the entry or `TBD` |
| Impact | Potential or actual consequence |
| Probability | Likelihood where applicable, otherwise `TBD` |
| Severity | Agreed severity, otherwise `TBD` |
| Owner | Accountable person or `TBD` |
| Date | ISO `YYYY-MM-DD` record date |
| Target date | ISO `YYYY-MM-DD` intended resolution/review date or `TBD` |
| Status | Proposed, Open, Monitoring, Closed, or `TBD` |
| Action | Next action or `TBD` |
| Related links | Valid relative repository links or sanitized authorized external references; otherwise `TBD` |

## Controlled values

- **Type:** `Risk`, `Assumption`, `Issue`, or `Dependency`.
- **Probability:** `Low`, `Medium`, `High`, `Not Applicable`, or `TBD`.
- **Severity:** `Low`, `Medium`, `High`, `Critical`, `Not Applicable`, or `TBD`.
- **Status:** `Proposed`, `Open`, `Monitoring`, `Closed`, or `TBD`.
- **Date and target date:** ISO `YYYY-MM-DD` or `TBD`.
- **Owner:** Authorized named owner or `TBD`; do not infer ownership.

## Entries

No entries recorded.

| ID | Type | Description | Evidence | Impact | Probability | Severity | Owner | Date | Target date | Status | Action | Related links |
|---|---|---|---|---|---|---|---|---|---|---|---|---|

## Current classifications

- **Confirmed:** The RAID log contains no entries.
- **Assumption:** None recorded.
- **Unknown/TBD:** Project risks, assumptions, issues, and dependencies are TBD pending evidence.
- **Decision required:** Entry acceptance and ownership require later review.
