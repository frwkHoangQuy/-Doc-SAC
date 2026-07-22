---
plan_id: SAC-PLAN-0001
title: Repository Initialization Plan
status: Proposed
version: 0.1
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

The repository is genuinely empty and suitable for controlled initialization, but Phase 2 should not begin until three material decisions are made:

1. Whether this public repository may remain public given its intended project/customer documentation.
2. How the first commit will be created, because an empty repository cannot use the normal branch-and-PR workflow.
3. The documentation language policy.

The candidate directory structure is too broad for the first baseline. The recommended initial baseline contains exactly 11 governance, register, and template files. Project-content directories should be created only when evidence-backed documents are ready.

No implementation was performed.

## 2. Verified repository checkpoint

Verification date: 2026-07-22, Asia/Bangkok.

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

The distinction between "configured default branch" and "actual branch" is important: GitHub is configured to use `main`, but no `refs/heads/main` exists until the first commit is created.

## 3. Authority and instruction files read

The following authority/instructions were considered:

- The complete Phase 1 instruction supplied by Hoang Quy Nguyen in this conversation.
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

### Repository-confirmed

- The exact repository is `frwkHoangQuy/-Doc-SAC`.
- It is public.
- Its configured default branch name is `main`.
- It has no commits, branch refs, tags, files, issues, or pull requests.
- The local checkout points to the stated GitHub repository.
- The local checkout is clean and has an unborn `main`.

### Confirmed by the task authority

- This repository is intended for SAC project documentation.
- Git is the working and version-history source.
- SharePoint is the company's official publication and approval repository.
- Hoang Quy Nguyen is the human authority for material scope and implementation gates.
- Synchronization of approved Git versions to SharePoint will be manual.
- Current-State Brief v0 must remain a discovery artifact and must not be represented as an approved current-state baseline.

No customer, software, team, schedule, scope, resource, or technical-condition facts were supplied.

## 5. Assumptions

These are planning assumptions only, not approved policy:

- Markdown will be the normal editable format in Git because the requested baseline uses `.md` files.
- Stable filenames without embedded version numbers will reduce broken links.
- The first baseline should contain operational governance and reusable structures, but no substantive project claims.
- Formal binaries or signed approval records may be linked from Git rather than duplicated into it.
- Hoang Quy Nguyen is the likely initial approver, but the exact approver identity and GitHub account must be confirmed.

## 6. Unknown/TBD items

The following remain unknown:

- Repository confidentiality/data-classification requirements.
- Whether public visibility is intentional.
- Customer identity and permitted level of identification.
- SAC mandate, business objectives, scope, exclusions, schedule, budget, and resources.
- Hanoi and Ho Chi Minh City team identities and responsibilities.
- Handover status and available evidence.
- Software/source-code repository URL and ownership.
- Current architecture, environments, integrations, data, security posture, and technical debt.
- SharePoint site, library, approval workflow, permissions, and link format.
- Required regulatory, retention, contractual, or records-management rules.
- Documentation language.
- Document owners and delegated approvers.
- Whether the initial governance baseline should be `Draft` or `Approved`.
- Branch-protection and required-review settings after `main` exists.

These must remain explicitly `TBD` until supported by evidence or human decision.

## 7. Conflicts or blockers

### Blocking conflicts

- **Public repository versus intended content:** Customer discovery, requirements, architecture, handover, risks, and operational support information commonly contain confidential or identifying material. A public repository is unsafe for such content unless the authority explicitly limits it to public-safe material.
- **PR workflow versus empty repository:** There is no base commit or branch ref against which a Phase 2 pull request can be opened. The first commit requires an explicitly approved bootstrap exception or a human-created seed commit.
- **Language policy:** The requested content cannot be authored consistently until English, Vietnamese, or bilingual usage is selected.

### Non-blocking observations

- The local branch tracks `origin/main`, but that remote ref does not yet exist. This is expected for an empty repository.
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
- Confidential customer identifiers unless explicitly authorized for the repository's classification.
- Signed originals where SharePoint is the controlled record.
- Large generated exports or duplicate working copies.
- Chat/email transcripts as authoritative records.
- Material prohibited by contract, privacy rules, or company policy.

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

Subject to resolution of the blocking decisions, Phase 2 should create exactly these 11 files:

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
| `docs/00-project-control/document-governance.md` | Lifecycle, roles, metadata, naming/versioning, review/approval, supersession, link rules, language policy placeholder, and sensitive-data handling | Central governance source avoids duplication | Governance only |
| `docs/00-project-control/git-sharepoint-sync.md` | Candidate preparation, Git approval, merge, export, SharePoint publication, register update, reconciliation, and correction workflow | Manual synchronization is a core operational boundary | Governance only |
| `registers/document-register.md` | Column definitions and an initially empty register for controlled documents, versions, content SHAs, and SharePoint status | Provides the cross-system control record | Governance structure; no project facts |
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
- Material scope, governance, or baseline changes require Hoang Quy Nguyen's approval unless delegation is recorded.
- Author and approver should be different where practicable.
- A GitHub approval identity must be mapped to the named human approver.

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

### Branch and PR workflow after bootstrap

1. Start from current `main`.
2. Use a short-lived branch such as `docs/<purpose>`.
3. Change only an explicitly approved file set.
4. Open a PR describing evidence, affected documents, sensitive-data review, and SharePoint impact.
5. Review links, metadata, facts/TBD markings, and diff scope.
6. Obtain explicit approval from the designated human authority.
7. Merge without bypassing required review.
8. Record the approved content commit and synchronize when publication is required.

### First-commit exception

Because `main` has no commit, Phase 2 requires one of these explicit choices:

- Authorize one exact, reviewed bootstrap commit directly to `main`; normal PR governance begins immediately afterward.
- Have the human create a seed commit, after which Phase 2 uses a branch and PR.

The first option is simpler, but it must be explicitly authorized as a one-time exception.

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
- `last_updated`

Unknown values should be `TBD`, not blank or invented. `last_updated` is the document revision date, not an automatically changing build timestamp.

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
- Reconfirm the repository is still empty and the worktree is clean.
- Re-read any newly introduced `AGENTS.md` or contribution instructions.
- Record the human decisions and exact authorization scope.

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

Before the initial commit:

- Compare `git diff --cached --name-only` against the exact 11-file allowlist.
- Review `git diff --cached`.
- Confirm no untracked or unrelated files exist with `git status --short`.
- Confirm every created directory contains an approved file.
- Confirm no project-content directory was created.
- Confirm the chosen language policy is applied consistently.
- Confirm the visibility/data-classification decision permits the content.
- Obtain the explicit bootstrap and material-scope approval.

After the commit, if authorized:

- Confirm the commit contains exactly the approved files.
- Confirm `git status` is clean.
- Confirm the resulting commit SHA.
- Do not push, open a PR, or alter settings unless separately authorized in Phase 2.

Acceptance requires both exact scope and absence of unsupported or sensitive content.

## 17. Risks and decision gates

### Blocking before Phase 2

- Repository visibility and permitted data classification.
- One-time first-commit mechanism.
- Documentation language.
- Exact 11-file baseline approval.
- Named approver and the meaning of `Approved` versus SharePoint approval status.

### May safely remain TBD during bootstrap

- SharePoint URL and library, provided the fields remain `TBD`.
- Software repository URL.
- Detailed branch-protection settings until `main` exists.
- Document owners for future project-content documents.
- Regulatory and retention details, provided no sensitive material is introduced.

### Future discovery questions that do not block bootstrap

- Customer identity and stakeholders.
- Hanoi/HCM team composition.
- Mandate, scope, deadlines, and resources.
- Software architecture and technical condition.
- Requirements, risks, dependencies, test status, deployment readiness, and support model.

These belong in discovery and must not be answered speculatively during initialization.

## 18. Questions requiring human decision

1. May `frwkHoangQuy/-Doc-SAC` remain public, and exactly what information classification is permitted? Recommended: make it private before adding any customer, architecture, handover, risk, or operational material.
2. For the empty-repository bootstrap, do you authorize one reviewed initial commit directly to `main`, or will you create a seed commit so Phase 2 can use a PR?
3. Should repository documents be English, Vietnamese, or bilingual? Recommended: choose one primary language and translate only documents with a defined audience need; avoid maintaining duplicate bilingual copies without ownership.
4. Should the Phase 2 governance baseline be committed as `Draft` pending operational trial, or approved as version `1.0`? Recommended: `Draft`/`0.1` until the workflow and SharePoint mapping are validated.
5. Who is the named document approver, and which GitHub identity represents that approval?
6. Do you approve the exact 11-file Phase 2 scope proposed above?
7. Where is the authorized SharePoint site/library, and what SharePoint state constitutes official approval? This may remain TBD for initial creation but must be resolved before the first synchronization.

## 19. Final statement confirming that no repository changes were made

Phase 1 used only file listing, Git inspection, and read-only GitHub metadata queries. No file or directory was created or modified during Phase 1. No branch, commit, tag, issue, pull request, or repository-setting change was made during Phase 1. No dependency was installed, and nothing was pushed during Phase 1.

Phase 1 plan completed. Implementation authorization: **NOT APPROVED**.
