---
plan_id: SAC-PLAN-0001
title: Repository Initialization Plan
status: Proposed
version: 0.2
repository: frwkHoangQuy/-Doc-SAC
plan_branch: plan/0001-repository-initialization
prepared_by: Codex
human_authority: Hoang Quy Nguyen
created_date: 2026-07-22
review_commit: TBD
approval_status: Not Approved
implementation_authorization: Not Approved
---

# Repository Initialization Plan

This plan is **Proposed** and **Not Approved**. Its persistence and push for review do not authorize implementation.

## 1. Executive conclusion

The repository was genuinely empty during Phase 1 discovery. It now contains the persisted plan as its root commit on `plan/0001-repository-initialization`; that branch is the first and only remote branch and was automatically designated as the default branch by GitHub. `main` does not yet exist.

The human authority has resolved the documentation language, initial lifecycle status and version, initial ownership and approval, exact Phase 2 file scope, bootstrap topology, document-register initialization, and temporary treatment of public visibility. These decisions revise the proposed plan but do not approve it or authorize implementation.

The candidate directory structure is too broad for the first baseline. The recommended initial baseline contains exactly 11 governance, register, and template files. Project-content directories should be created only when evidence-backed documents are ready.

No implementation was performed.

## 2. Verified repository checkpoints

### 2.1 Historical Phase 1 checkpoint

Verification date: 2026-07-22, Asia/Ho_Chi_Minh.

This is a time-bounded historical record of repository state before the plan artifact was persisted. It must not be used as the operational starting state for Phase 2.

| Item | Verified result | Evidence |
|---|---|---|
| Owner | `frwkHoangQuy` | GitHub API: `full_name: frwkHoangQuy/-Doc-SAC` |
| Exact repository | `frwkHoangQuy/-Doc-SAC` | GitHub API and configured origin |
| URL | `https://github.com/frwkHoangQuy/-Doc-SAC` | GitHub API and `git remote get-url origin` |
| Visibility | **Public** | GitHub API: `visibility: public`, `private: false` |
| Configured default branch | `main` | GitHub REST API: `default_branch: main` |
| Actual default-branch ref | None yet | GitHub `defaultBranchRef.name` was empty; repository has no commits |
| Remote branches | None | `git ls-remote --heads origin` returned no refs |
| Tags | None | Local tag list and remote tag query returned no refs |
| Current commit SHA | None | `git rev-parse --verify HEAD` failed with `Needed a single revision` |
| Repository empty | Yes | GitHub: `isEmpty: true`, `size: 0`; no remote refs or tracked files |
| Existing files/directories | Only local `.git/` metadata | Root listing showed only `.git`; `git ls-files` returned nothing |
| Issues | None | `gh issue list --state all` returned `[]` |
| Pull requests | None | `gh pr list --state all` returned `[]` |
| Issues feature | Enabled | GitHub API: `has_issues: true` |
| Archived/disabled | No | GitHub API: `archived: false`, `disabled: false` |
| Local checkout | Valid Git worktree | `git rev-parse --is-inside-work-tree` returned `true` |
| Local branch | Unborn `main` | `git branch --show-current` returned `main`; status reported `branch.oid (initial)` |
| Local upstream | Configured as `origin/main` | `git status --porcelain=v2 --branch` |
| Local status | No working-tree or index changes | Status contained only branch headers and no file entries |
| Configured remote | `origin` -> repository URL above | Sanitized remote inspection |

At that historical checkpoint, the distinction between "configured default branch" and "actual branch" was important: GitHub was configured to use `main`, but no `refs/heads/main` existed because the repository had no commit.

### 2.2 Post-plan-persistence checkpoint

Verification date: 2026-07-22, Asia/Ho_Chi_Minh.

| Item | Verified result | Evidence |
|---|---|---|
| Repository | `frwkHoangQuy/-Doc-SAC` | Configured origin and GitHub repository metadata |
| Visibility | **Public** | GitHub reported `visibility: PUBLIC` |
| Repository state | No longer empty | GitHub reported `isEmpty: false` |
| Root commit | `2fafae7f304ca5acdc675509da7f658f97a7903c` | Local HEAD and remote branch ref matched |
| Root-commit content | `docs/plans/0001-repository-initialization-plan.md` | Commit file inspection |
| Remote branch | `plan/0001-repository-initialization` | `git ls-remote --heads origin` |
| Current default branch | `plan/0001-repository-initialization` | GitHub `defaultBranchRef`; automatically designated because it was the first and only branch |
| `main` | Does not exist | No local or remote `refs/heads/main` |
| Pull requests | None | `gh pr list --state all` returned `[]` |
| Local/remote divergence | None | Both branch heads were the root commit; ahead/behind was `0/0` |
| Local status | Clean | `git status --short --branch` had no file entries |

The former "empty repository / no commit / first commit choice" condition is no longer an active blocker. The operational starting point for any separately authorized Phase 2 is a future human-approved plan revision commit on the plan branch, using the bootstrap topology in Section 12.

## 3. Authority and instruction files read

The following authority/instructions were considered:

- The complete Phase 1 instruction supplied by Hoang Quy Nguyen in this conversation.
- The Phase 1 plan-persistence instruction and the v0.2 revision instruction supplied by Hoang Quy Nguyen.
- The GitHub repository-orientation skill instructions used for read-only repository verification.
- Repository root and tracked-file searches for:
  - `AGENTS.md`;
  - `CONTRIBUTING*`;
  - `CODE_OF_CONDUCT*`;
  - `SECURITY*`;
  - `.github/**`;
  - workflow, governance, and instruction files.

No repository-level instruction, contribution, workflow, security, or governance files exist. There are no descendant paths containing additional `AGENTS.md` files.

## 4. Confirmed facts

### Repository-confirmed current facts

- The exact repository is `frwkHoangQuy/-Doc-SAC`.
- It is public.
- Its current default branch is `plan/0001-repository-initialization`.
- It has root commit `2fafae7f304ca5acdc675509da7f658f97a7903c`, which contains the plan artifact.
- The plan branch exists remotely; `main` does not exist.
- It has no pull requests.
- The local checkout points to the stated GitHub repository.
- The local checkout was clean and matched the remote plan branch at the v0.2 pre-write checkpoint.

### Confirmed by the task authority

- This repository is intended for SAC project documentation.
- Git is the working and version-history source.
- SharePoint is the company's official publication and approval repository.
- Hoang Quy Nguyen is the human authority for material scope and implementation gates.
- Synchronization of approved Git versions to SharePoint will be manual.
- Current-State Brief v0 must remain a discovery artifact and must not be represented as an approved current-state baseline.
- English is the standard language for documents maintained in Git. Vietnamese or bilingual variants are created only for a defined audience or delivery obligation and must remain traceable to the authoritative English source.
- Initial Phase 2 governance baseline documents use status `Draft` and version `0.1`.
- Hoang Quy Nguyen is the initial document owner and approver; the mapped GitHub identity is `frwkHoangQuy`.
- The exact Phase 2 changed-file set is the 11 files in Section 10.
- Public visibility is temporarily accepted. Conversion to private is a deferred administrative action owned by the human authority.

No customer, software, team, schedule, scope, resource, or technical-condition facts were supplied.

## 5. Assumptions

These are planning assumptions only, not approved policy:

- Markdown will be the normal editable format in Git because the requested baseline uses `.md` files.
- Stable filenames without embedded version numbers will reduce broken links.
- The first baseline should contain operational governance and reusable structures, but no substantive project claims.
- Formal binaries or signed approval records may be linked from Git rather than duplicated into it.

## 6. Unknown/TBD items

The following remain unknown:

- Repository confidentiality/data-classification requirements.
- Customer identity and permitted level of identification.
- SAC mandate, business objectives, scope, exclusions, schedule, budget, and resources.
- Hanoi and Ho Chi Minh City team identities and responsibilities.
- Handover status and available evidence.
- Software/source-code repository URL and ownership.
- Current architecture, environments, integrations, data, security posture, and technical debt.
- SharePoint site, library, approval workflow, permissions, and link format.
- Required regulatory, retention, contractual, or records-management rules.
- Branch-protection and required-review settings after `main` exists.

These must remain explicitly `TBD` until supported by evidence or human decision.

## 7. Conflicts or blockers

### Active constraints

- The repository is currently public. This does not block this plan revision and is not automatically a blocker for a separately authorized governance-only Phase 2.
- While it remains public, no secrets, credentials, customer-identifying data, sensitive handover details, non-public architecture details, or confidential operational information may be added.
- Any future need to store sensitive or non-public project content requires private visibility and appropriate access controls first.
- Phase 2 remains blocked by the separate plan-approval and implementation-authorization gates, not by the obsolete empty-repository first-commit choice.

### Non-blocking observations

- GitHub automatically designated the plan branch as the default because it was the first and only remote branch; `main` remains absent.
- The proposed 11 documentation categories are not repository reality; they are only a candidate design.
- No existing instructions conflict with the task because no repository instruction files exist.

## 8. Recommended repository scope and boundaries

### Belongs in this documentation repository

- Project governance and documentation procedures.
- Mandate and stakeholder documentation once confirmed.
- Hanoi-to-Ho Chi Minh City handover records.
- Sanitized customer-discovery findings.
- Requirements, assumptions, scope, exclusions, and traceability.
- Technical assessments, architecture decisions, and non-secret diagrams.
- Plans, milestones, status reports, RAID records, and decision records.
- Test strategy, test evidence references, and UAT coordination.
- Deployment, training, transition, acceptance, and support documentation.
- Approved-document history and SharePoint synchronization records.

### Belongs in the software/source-code repository

- Application source code.
- Build and deployment automation.
- Executable tests and test fixtures.
- Infrastructure-as-code.
- Runtime configuration templates.
- API schemas or code-coupled technical material whose changes must remain atomic with software changes.
- Code-specific issue tracking and release artifacts.

The documentation repository may link to these items but should not duplicate them.

### Belongs only in SharePoint or another authorized corporate system

- Signed acceptance records and formal approval artifacts.
- Corporate-controlled publication copies.
- Documents requiring SharePoint permissions, retention, or approval workflows.
- Restricted attachments or office-format originals that cannot safely be stored in Git.
- Customer-provided confidential source material.
- Personal information and access-controlled commercial records.

Git should contain a sanitized reference, identifier, status, and authorized link where appropriate.

### Must not be stored in Git

- Passwords, tokens, API keys, private keys, connection strings, or credentials.
- Production secrets or environment files.
- Customer personal data, production datasets, raw database exports, or unredacted logs.
- Customer-identifying data, sensitive handover details, non-public architecture details, or confidential operational information while the repository remains public.
- Signed originals where SharePoint is the controlled record.
- Large generated exports or duplicate working copies.
- Chat/email transcripts as authoritative records.
- Material prohibited by contract, privacy rules, or company policy.

Current public visibility is temporarily accepted for plan review and is not automatically a blocker for a separately authorized governance-only Phase 2. The human authority owns the deferred administrative action to make the repository private. Sensitive or non-public project content must not be introduced until private visibility and appropriate access controls are verified.

## 9. Recommended initial structure

Only directories containing an initial necessary file should be created:

```text
/
|-- README.md
|-- AGENTS.md
|-- docs/
|   `-- 00-project-control/
|       |-- document-governance.md
|       `-- git-sharepoint-sync.md
|-- registers/
|   |-- document-register.md
|   |-- raid-log.md
|   `-- decision-log.md
`-- templates/
    |-- project-document-template.md
    |-- current-state-brief-template.md
    |-- meeting-minutes-template.md
    `-- handover-checklist-template.md
```

### Candidate paths to defer

All of these should be deferred until a factual document is ready:

- `docs/01-mandate-and-stakeholders/`
- `docs/02-handover-from-hanoi/`
- `docs/03-customer-discovery/`
- `docs/04-requirements-and-scope/`
- `docs/05-technical-assessment/`
- `docs/06-planning-and-tracking/`
- `docs/07-test-and-uat/`
- `docs/08-deployment-and-training/`
- `docs/09-acceptance-and-support/`
- `docs/10-reports-and-decisions/`

### Structural refinements for later consideration

The candidate structure has several overlaps:

- Stakeholder documents overlap a stakeholder register.
- Handover and customer discovery may produce shared evidence.
- Planning/tracking overlaps RAID and reporting.
- Testing/UAT, deployment/training, and acceptance/support form one release-transition lifecycle.
- Reports/decisions overlaps the decision register.

When substantive content exists, a simpler future hierarchy may be preferable:

```text
01-context-and-stakeholders/
02-handover-and-discovery/
03-requirements-and-scope/
04-technical-assessment/
05-planning-and-status/
06-quality-release-and-transition/
07-reports/
```

That future structure is not part of the proposed Phase 2 changed-file set.

## 10. Exact proposed Phase 2 changed-file set

If the plan and Phase 2 are separately approved, Phase 2 should create exactly these 11 files:

1. `README.md`
2. `AGENTS.md`
3. `docs/00-project-control/document-governance.md`
4. `docs/00-project-control/git-sharepoint-sync.md`
5. `registers/document-register.md`
6. `registers/raid-log.md`
7. `registers/decision-log.md`
8. `templates/project-document-template.md`
9. `templates/current-state-brief-template.md`
10. `templates/meeting-minutes-template.md`
11. `templates/handover-checklist-template.md`

No other files or directories are proposed for Phase 2. In particular, no `.gitignore`, license, issue template, PR template, workflow, requirements register, stakeholder register, contribution register, or project-content document is included.

## 11. File-by-file content outline

| File | Purpose and minimum content | Why needed initially | Content type |
|---|---|---|---|
| `README.md` | Repository purpose, boundaries, authority model, navigation, lifecycle summary, confidentiality warning, Git/SharePoint roles, and TBD policy | Gives every user a safe entry point | Confirmed repository/authority facts plus governance |
| `AGENTS.md` | Read-before-edit rules, instruction precedence, factual/TBD rules, sensitive-data prohibition, allowed paths, approval gates, exact-scope discipline, and verification requirements | Protects future agent-assisted work | Governance only |
| `docs/00-project-control/document-governance.md` | Lifecycle, roles, metadata, naming/versioning, review/approval, supersession, link rules, approved language policy, and sensitive-data handling | Central governance source avoids duplication | Governance only |
| `docs/00-project-control/git-sharepoint-sync.md` | Candidate preparation, Git approval, merge, export, SharePoint publication, register update, reconciliation, and correction workflow | Manual synchronization is a core operational boundary | Governance only |
| `registers/document-register.md` | Column definitions and initial rows for all 11 controlled governance, register, and template files, including versions, content SHAs, and SharePoint status | Provides the cross-system control record | Governance structure; no project facts |
| `registers/raid-log.md` | Definitions for risk, assumption, issue, and dependency; controlled status/severity fields; initially no factual entries | Needed early without inventing risks | Governance structure; no project facts |
| `registers/decision-log.md` | Decision ID, date, status, owner, decision, rationale, alternatives, evidence, and affected documents; initially no decisions beyond approved bootstrap decisions | Prevents decisions being lost in chat/email | Governance structure; approved decisions only when supplied |
| `templates/project-document-template.md` | Standard metadata and headings for purpose, context, evidence, content, open items, approvals, and references | Establishes consistent authoring | Template only |
| `templates/current-state-brief-template.md` | Discovery Draft warning and sections for mandate, stakeholders, software, scope, schedule, resources, technical condition, evidence, gaps, and questions | Enables discovery without asserting a baseline | Template only |
| `templates/meeting-minutes-template.md` | Date, participants, purpose, evidence discussed, decisions, actions, owners, due dates, and links | Meetings are a likely early evidence source | Template only |
| `templates/handover-checklist-template.md` | Evidence-request checklist covering ownership, scope, architecture, environments, access, data, operations, defects, tests, deployment, support, risks, and unresolved questions | Handover is an explicit initialization concern | Template only |

### Register/template disposition

Safe to initialize now:

- Document register.
- RAID log with no invented entries.
- Decision log with no invented entries.
- Current-State Brief template.
- Meeting-minutes template.
- Handover-checklist template.

### Initial document-register rows

Phase 2 initializes the document register with the following 11 rows. Governance and register files are controlled operational documents; templates are controlled template assets and use the `SAC-TPL` type. Templates are registered for version and source traceability but do not represent completed project-content documents.

All rows use status `Draft`, version `0.1`, owner `Hoang Quy Nguyen`, approver `Hoang Quy Nguyen`, GitHub identity `frwkHoangQuy`, `approved_content_commit: TBD`, `sharepoint_url: TBD`, and SharePoint synchronization status/date `TBD`.

| Document ID | Git path | Title | Classification |
|---|---|---|---|
| `SAC-GOV-001` | `README.md` | SAC Documentation Repository Overview | Governance |
| `SAC-GOV-002` | `AGENTS.md` | Repository Agent Instructions | Governance |
| `SAC-GOV-003` | `docs/00-project-control/document-governance.md` | Document Governance | Governance |
| `SAC-GOV-004` | `docs/00-project-control/git-sharepoint-sync.md` | Git-SharePoint Synchronization Procedure | Governance |
| `SAC-REG-001` | `registers/document-register.md` | Document Register | Register |
| `SAC-REG-002` | `registers/raid-log.md` | RAID Log | Register |
| `SAC-REG-003` | `registers/decision-log.md` | Decision Log | Register |
| `SAC-TPL-001` | `templates/project-document-template.md` | Project Document Template | Template |
| `SAC-TPL-002` | `templates/current-state-brief-template.md` | Current-State Brief Template | Template |
| `SAC-TPL-003` | `templates/meeting-minutes-template.md` | Meeting Minutes Template | Template |
| `SAC-TPL-004` | `templates/handover-checklist-template.md` | Handover Checklist Template | Template |

These rows record control metadata only. They do not assert SharePoint publication, approval, synchronization, project facts, customer facts, or approved content commit SHAs.

Deferred:

- Contribution register: Git history and pull requests already provide contribution traceability; add only if a contractual reporting need appears.
- Requirements register: create when the first evidenced requirement exists.
- Stakeholder register: create when identities, roles, and permitted personal-data treatment are confirmed.
- Current-State Brief v0: do not create in Phase 2.
- All substantive project documents: require factual input.

## 12. Governance and approval workflow

### Lifecycle

- **Draft:** Active authoring; incomplete or unverified content is allowed only when clearly labeled.
- **In Review:** Content is stable enough for review; outstanding questions remain explicit.
- **Approved:** Designated human authority has approved the content for controlled publication. SharePoint publication status is tracked separately.
- **Superseded:** A later approved version replaces it; preserve Git history and link to the replacement.

Deletion should not be used to conceal superseded approved records.

### Ownership and approval

- `owner`: accountable for accuracy and maintenance.
- `approver`: person authorized to approve that document.
- The initial owner and approver is Hoang Quy Nguyen, mapped to GitHub identity `frwkHoangQuy`.
- Material scope, governance, or baseline changes require Hoang Quy Nguyen's approval unless delegation is recorded.
- Author and approver should be different where practicable; the human authority has explicitly assigned both initial roles to Hoang Quy Nguyen for this baseline.

### Naming and versioning

- Paths and filenames: lowercase `kebab-case`.
- Filenames remain stable and do not include version numbers.
- Dates: ISO `YYYY-MM-DD`.
- IDs: stable project-prefixed identifiers, for example `SAC-DEC-001`; the exact type-code list should remain small.
- Draft series: `0.1`, `0.2`, and so on.
- First approved release: `1.0`.
- Minor approved revision: `1.1`, `1.2`.
- Material restructuring or changed baseline: `2.0`.
- Ordinary commits do not automatically increment a document version; version changes correspond to controlled document releases.
- Initial Phase 2 governance, register, and template files use status `Draft` and version `0.1`.

### Documentation language

- English is the standard language for documents maintained in Git.
- Vietnamese or bilingual variants are created only when required for a defined audience or delivery obligation.
- A translation must preserve traceability to its authoritative English source.
- This decision does not add translation deliverables to the exact 11-file Phase 2 scope.

### Branch and PR workflow after bootstrap

1. Start from current `main`.
2. Use a short-lived branch such as `docs/<purpose>`.
3. Change only an explicitly approved file set.
4. Open a PR describing evidence, affected documents, sensitive-data review, and SharePoint impact.
5. Review links, metadata, facts/TBD markings, and diff scope.
6. Obtain explicit approval from the designated human authority.
7. Merge without bypassing required review.
8. Record the approved content commit and synchronize when publication is required.

### Phase 2 bootstrap topology

Phase 2 must use this sequence, without variation:

1. Identify the **approved plan commit**: the future plan revision SHA explicitly approved by the human authority.
2. Create `main` at exactly that approved plan commit.
3. Set `main` as the default branch.
4. Create `implementation/0001-repository-initialization` from `main`.
5. Create exactly the approved 11-file Phase 2 set in Section 10.
6. Validate and commit the implementation.
7. Push `implementation/0001-repository-initialization`.
8. Open a pull request targeting `main`.
9. Obtain human review and approval before merge.

In compact form:

```text
approved plan commit
-> create main at exactly the approved plan commit
-> set main as the default branch
-> create implementation/0001-repository-initialization from main
-> create exactly the approved 11-file Phase 2 set
-> validate and commit the implementation
-> push the implementation branch
-> open a pull request targeting main
-> obtain human review and approval before merge
```

"Approved plan commit" means the future plan revision SHA explicitly approved by the human authority. It does not automatically mean root commit `2fafae7f304ca5acdc675509da7f658f97a7903c`, and merely pushing v0.2 does not approve that revision. The plan branch must not be used as the implementation branch, and Phase 2 must not commit implementation content directly to the current default plan branch. Creating `main`, changing the default branch, creating implementation files, pushing an implementation branch, and opening a pull request all require separate Phase 2 authorization.

## 13. Git-SharePoint synchronization workflow

1. Complete the document in Git using evidence-backed content.
2. Obtain the required Git review and human approval.
3. Merge the controlled version to `main`.
4. Identify the exact content commit SHA to publish.
5. Export or copy the document from that exact commit--not from an uncommitted workspace.
6. The human authority uploads it to the authorized SharePoint location and runs the official approval/publication process.
7. Record in the document register:
   - Git path;
   - approved content commit SHA;
   - document version;
   - SharePoint URL;
   - SharePoint status;
   - SharePoint version/reference where available;
   - synchronization timestamp.
8. Add the register update through the normal Git review process.
9. Do not continue editing a document if SharePoint contains an un-reconciled correction.

### Corrections originating in SharePoint

1. Treat the SharePoint correction as a change request, not a second working source.
2. Temporarily stop parallel editing of the affected Git document.
3. Capture the exact SharePoint revision, approver, and rationale.
4. Reconcile the correction into Git on a branch.
5. Review and merge it using the standard approval gate.
6. Republish the new Git-controlled version to SharePoint.
7. Update the document register with the new content SHA, SharePoint revision, and synchronization date.

This restores Git as the sole working source while preserving SharePoint as the official corporate publication and approval repository.

## 14. Metadata recommendation

Recommended embedded document metadata:

```yaml
document_id:
title:
status:
version:
owner:
approver:
github_identity:
last_updated:
```

Recommended register-only synchronization fields:

```text
approved_content_commit
sharepoint_url
sharepoint_status
sharepoint_version
sharepoint_synced_at
```

### Field timing

Before commit:

- `document_id`
- `title`
- `status`
- `version`
- `owner`
- `approver`
- `github_identity`
- `last_updated`

For the initial Phase 2 baseline, `owner` and `approver` are `Hoang Quy Nguyen`, and `github_identity` is `frwkHoangQuy`. Other unknown values should be `TBD`, not blank or invented. `last_updated` is the document revision date, not an automatically changing build timestamp.

After merge:

- `approved_content_commit` is recorded in the document register.
- It should identify the commit containing the approved document content.

After SharePoint synchronization:

- `sharepoint_url`
- `sharepoint_status`
- `sharepoint_version`, if available
- `sharepoint_synced_at`

`git_commit` should not be embedded in the document itself. Doing so would require another commit, immediately making the embedded "current SHA" stale. The document register should instead record the content commit being controlled and published.

## 15. Current-State Brief v0 recommendation

Phase 2 should create **only `templates/current-state-brief-template.md`**.

It should prominently state:

> Discovery template. Any document created from this template remains a Discovery Draft until its claims are supported by cited evidence and formally approved.

A Current-State Brief v0 should be created only when the human supplies or identifies at least some usable evidence. At that point:

- status must be `Draft`;
- version should begin at `0.1`;
- unknown sections must say `TBD`;
- every substantive claim should identify its source;
- it must not be described as an approved current-state baseline.

Creating a v0 now would provide only headings and TBD markers, duplicating the template without adding project knowledge.

## 16. Verification and acceptance criteria

Before any Phase 2 edit:

- Reconfirm repository visibility and remote.
- Reconfirm the approved plan commit SHA and clean worktree.
- Re-read any newly introduced `AGENTS.md` or contribution instructions.
- Record the human decisions and exact authorization scope.
- Confirm separate authorization to create `main`, change the default branch, create the implementation branch and files, push, and open a pull request.
- Create `main` at exactly the human-approved plan commit, set it as default, and create `implementation/0001-repository-initialization` from `main` before editing implementation content.
- Confirm the approved plan commit is the explicitly approved future revision SHA, not merely the most recently pushed plan commit.

During Phase 2:

- Create only the 11 approved files.
- Populate no unsupported project facts.
- Validate all relative Markdown links.
- Check required headings and metadata fields.
- Search for credential patterns, tokens, private keys, customer identifiers, personal data, and accidental pasted logs.
- Use a dedicated secret scanner if already available; do not install one without authorization.
- Run Markdown linting if already available; otherwise perform deterministic structural checks.
- Run `git diff --check`.
- Review the entire staged diff, not only a summary.

Before the implementation commit:

- Compare `git diff --cached --name-only` against the exact 11-file allowlist.
- Review `git diff --cached`.
- Confirm no untracked or unrelated files exist with `git status --short`.
- Confirm every created directory contains an approved file.
- Confirm no project-content directory was created.
- Confirm English is used consistently and no unapproved translation deliverable was created.
- While the repository remains public, confirm the diff contains no secrets, credentials, customer-identifying data, sensitive handover details, non-public architecture details, or confidential operational information.
- Obtain the explicit bootstrap and material-scope approval.

After the commit, if authorized:

- Confirm the commit contains exactly the approved files.
- Confirm `git status` is clean.
- Confirm the resulting commit SHA.
- Do not push, open a PR, or alter settings unless separately authorized in Phase 2.

Acceptance requires both exact scope and absence of unsupported or sensitive content.

## 17. Risks and decision gates

### Resolved by human authority

- Documentation language: English is standard in Git; audience-required translations remain traceable to the English source.
- Initial lifecycle: `Draft`, version `0.1`.
- Initial owner and approver: Hoang Quy Nguyen; GitHub identity `frwkHoangQuy`.
- Exact Phase 2 scope: the unchanged 11 files in Section 10.
- Bootstrap topology: approved plan commit -> `main` -> implementation branch -> PR targeting `main`.
- Document-register initialization: rows for all 11 controlled governance, register, and template assets with the values specified in Section 11.
- Current public visibility: temporarily accepted; a deferred change to private is owned by the human authority.

### No longer active

- The empty-repository first-commit choice. The plan root commit and remote plan branch now exist.

### Still requires separate approval or authorization

- Approval of the complete revised plan by its reviewed commit SHA.
- Creation of `main` at the approved plan commit.
- Changing the default branch to `main`.
- Phase 2 implementation and its exact content.
- Opening the implementation pull request and merging it.
- Publication or synchronization to SharePoint.
- Private visibility and appropriate access controls before any sensitive or non-public project content is stored.

### May safely remain TBD during bootstrap

- SharePoint URL and library, provided the fields remain `TBD`.
- Software repository URL.
- Detailed branch-protection settings until `main` exists.
- Owners and approvers for future project-content documents beyond the initial baseline.
- Regulatory and retention details, provided no sensitive material is introduced.

### Future discovery questions that do not block bootstrap

- Customer identity and stakeholders.
- Hanoi/HCM team composition.
- Mandate, scope, deadlines, and resources.
- Software architecture and technical condition.
- Requirements, risks, dependencies, test status, deployment readiness, and support model.

These belong in discovery and must not be answered speculatively during initialization.

## 18. Questions requiring human decision

1. Is the future v0.2 plan commit approved as the controlling plan commit for Phase 2? A pushed commit is not approved until the human authority explicitly identifies and approves its SHA.
2. Is the separate Phase 2 authorization granted to create `main`, change the default branch, create and push the implementation branch, create the 11 files, and open a pull request? This plan revision does not grant that authorization.
3. Where is the authorized SharePoint site/library, and what SharePoint state constitutes official approval? This may remain `TBD` for governance-only bootstrap but must be resolved before the first synchronization.

## 19. Final statement confirming that no repository changes were made

Phase 1 used only file listing, Git inspection, and read-only GitHub metadata queries. No file or directory was created or modified during Phase 1. No branch, commit, tag, issue, pull request, or repository-setting change was made during Phase 1. No dependency was installed, and nothing was pushed during Phase 1.

Phase 1 plan completed. Implementation authorization: **NOT APPROVED**.
