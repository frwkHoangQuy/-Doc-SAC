# Issue #5 Gate 1 Inventory and Proposed Implementation Plan

## 8.1 Document control

| Field | Value |
|---|---|
| Artifact status | **Proposed — not approved** |
| Related issue | Issue #5, `[Governance] Project Information Update Workflow` |
| Issue URL | https://github.com/frwkHoangQuy/-Doc-SAC/issues/5 |
| Gate | Gate 1 |
| Prompt ID | `SAC-GOV-PIUW-GATE1-PROMPT-v1` |
| Task objective | Re-verify the repository and GitHub checkpoint; inventory the current information-update and approval system; analyze conflicts; and propose a bounded canonical implementation for independent review. |
| Authorization boundary | Read-only inspection plus one new review branch, this one new review artifact, one immutable commit, and one normal push. No canonical APPLY work is authorized. |
| Source branch | `main` |
| Immutable source SHA | `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Review branch | `review/agent-artifacts` |
| Artifact path | `agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v1.md` |
| Inspection timestamp | `2026-07-24T02:08:36+07:00` (`Asia/Ho_Chi_Minh`) |
| Repository visibility | Public |
| Public-safety classification | Public-safe governance proposal; no customer-identifying, personal, credential, private-endpoint, production, confidential architecture, or sensitive operational content |

This artifact is a non-canonical review object. It records verified facts, live
state, analysis, and proposals; its existence, commit, or push does not approve
its content or authorize implementation.

The inspection used local Git commit-addressed reads and live GitHub REST reads.
The Agent could inspect public repository content and authenticated repository
metadata but did not inspect SharePoint, private corporate evidence, repository
administrative audit logs, or facts outside the supplied public sources. The
Lead PM/SA Reviewer did not participate in execution and retains read-only
authority. The Human Authority remains the only instruction and approval
authority.

Evidence limitations are explicit:

- No approved SharePoint location or synchronization record was available.
- No project Mandate evidence was inspected.
- No evidence supports substantive Discovery facts, delivery ownership,
  delivery strategy, architecture, schedule, resources, or readiness.
- GitHub Issue and Pull Request state is mutable and must be re-read at every
  later gate.
- A commit cannot contain its own final SHA without changing that SHA. The full
  review SHA is therefore the SHA of the immutable commit that adds this exact
  path and is returned in the Agent's Gate 1 execution report.

## 8.2 Gate 0 traceability and current checkpoint

### Gate 0 provenance

| Item | Verified value |
|---|---|
| Gate 0 prompt ID | `SAC-GOV-PIUW-GATE0-PROMPT-v4` |
| Gate 0 package ID | `SAC-GOV-PIUW-GATE0-PACKAGE-v1` |
| Package byte length | `29182` |
| Package SHA-256 | `1f72d89dd47470696a89b10387ada1d59ecfda3111c9eef6b1976183a5b98ae8` |
| Controlling Issue | https://github.com/frwkHoangQuy/-Doc-SAC/issues/5 |
| Issue #2 pause comment | https://github.com/frwkHoangQuy/-Doc-SAC/issues/2#issuecomment-5062178601 |
| Draft PR #3 pause comment | https://github.com/frwkHoangQuy/-Doc-SAC/pull/3#issuecomment-5062178818 |

All three URLs were read back. The two comments state linkage and pause
boundaries without authorizing continuation, closure, migration, supersession,
Discovery, or a later gate.

### Live checkpoint

| Object | Verified state at inspection |
|---|---|
| Repository | `frwkHoangQuy/-Doc-SAC`; public; default branch `main` |
| Remote | `origin` fetch/push: `https://github.com/frwkHoangQuy/-Doc-SAC` |
| Live `main` | `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Local pre-write state | Branch `implementation/0002-current-state-discovery-readiness`, HEAD `4bc090137d5843c975159ecd2b3b98f4cebf52a5`, clean index and worktree |
| Issue #5 | Open; exact title `[Governance] Project Information Update Workflow`; controlling governance Issue |
| Issue #2 | Open; `[Plan] SAC-PLAN-0002 — Phase 3 Current-State Discovery and Decision Readiness`; paused by the Gate 0 comment |
| Draft PR #3 | Open and Draft; base `main`; head `implementation/0002-current-state-discovery-readiness`; head `4bc090137d5843c975159ecd2b3b98f4cebf52a5` |
| PR #3 divergence | Diverged from live `main`: 2 commits ahead, 1 behind; merge base `4ce275b0ecb3cd297636bade6168407de4e3b2d0` |
| PR #4 | Closed and merged; merge commit `53479ad5694071555cbb97bdea5bbe3316271d45`; introduced SAC-PLAN-0002 into `main` |
| Review branch before Gate 1 | `review/agent-artifacts` absent locally and remotely |
| Gate 1 artifact at base | Exact allowlisted path absent at the approved base |

Active gate is Gate 1. The last approved action was Gate 0 creation of Issue #5
and the two pause comments. Pending Human Authority decisions include Gate 2
review disposition, any canonical implementation authorization, and the later
treatment of Issue #2, PR #3, PR #4, and SAC-PLAN-0002. The only permitted next
action after this Gate 1 push is independent read-only review of the immutable
artifact. Gate 2 execution, canonical implementation, Issue/PR mutation, merge,
baseline, SharePoint, Discovery, architecture, and software work remain
prohibited.

## 8.3 Evidence and classification method

### Sources inspected

1. Exact source tree at commit
   `53479ad5694071555cbb97bdea5bbe3316271d45`.
2. Exact PR #3 head tree at
   `4bc090137d5843c975159ecd2b3b98f4cebf52a5`.
3. Git commit topology and diffs for the baseline, PR #3, and PR #4.
4. Live GitHub repository metadata, branches, Issues #2 and #5, PRs #3 and #4,
   the Gate 0 comments, PR commits, and changed paths.
5. The Human Authority-transmitted Gate 1 prompt whose SHA-256 is
   `0553b5643963f06bcf065ade1871fb4b47e48a81f85b519fadf458ba9c095739`.

### Classification vocabulary

| Classification | Meaning in this artifact |
|---|---|
| Source | An identified input whose content can be inspected; source status alone does not make every statement authoritative. |
| Evidence | Inspectable material supporting a claim, with an immutable SHA/path or live URL where practical. |
| Verified repository fact | A result reproduced from the immutable Git object graph. |
| Verified live GitHub state | A result read from GitHub at the inspection time; mutable and subject to drift. |
| Human Authority decision | An explicit, bounded choice personally transmitted by Hoang Quy Nguyen (`frwkHoangQuy`). |
| Instruction | A binding rule within its authority and scope; it is not a project fact. |
| Proposal | A recommended future design or action requiring approval. |
| Assumption | A working proposition requiring validation. |
| Unknown or unresolved | Evidence is unavailable or a Human Authority choice remains outstanding. |
| Approval | An explicit Human Authority acceptance identifying the controlled object and scope. |
| Canonical record | A repository record explicitly designated as the working source under governance; presence in Git alone is insufficient. |
| Review artifact | Immutable non-canonical material on `review/agent-artifacts`, never a merge candidate. |
| Historical record | Retained evidence of prior work or authority state; it does not automatically control current work. |

Immutable evidence is cited by a full commit SHA and path or Git blob SHA.
GitHub state is cited by URL and inspection timestamp. A conflict exists when
two records assert incompatible status, authority, sequence, or scope. Staleness
exists when a mutable object's state or referenced base no longer matches the
current checkpoint. Authority leakage exists when an artifact or state
transition appears to grant a permission that only the Human Authority can
grant.

Confidence is high for Git object contents and topology at an identified SHA.
Confidence is time-bounded for live GitHub state. Confidence is not assigned to
uninspected private evidence. Any unsupported project statement remains unknown
or unresolved. Public-safety controls require sanitized references, credential
value-pattern scanning, complete diff inspection, and stopping if non-public
content would be necessary.

## 8.4 Complete relevant inventory

### Repository instructions, governance, canonical navigation, plans, registers, and templates

Every tracked file at the approved base was inspected. Blob SHAs make the
inventory reproducible.

| Path | Purpose and current authority/status | Relevant relationship | Observed gap or conflict | Blob at approved base |
|---|---|---|---|---|
| `AGENTS.md` | Repository instructions; Draft 0.1; binding within repository execution | Defers to Human Authority, exact allowlists, evidence classifications, and document governance | Does not define the Issue #5 lifecycle, review branch protocol, or fresh-context checkpoint | `6a7af21eda66ece78efbef8b0e93150c3bacc980` |
| `README.md` | Canonical repository overview/navigation; Draft 0.1 | Links 11 Phase 2 baseline files | No navigation for information-update workflow, context journal, or review controls | `1a361d2c6560d3d13e4c697dc6c0015ab0d1ac3a` |
| `docs/00-project-control/document-governance.md` | Canonical document lifecycle and authority rules; Draft 0.1 | Controls Draft/In Review/Approved/Superseded and evidence rules | Does not distinguish intake/PLAN/APPLY or define update impact mapping | `7488f35f594b4d9fed0aaca471fcabf489639182` |
| `docs/00-project-control/git-sharepoint-sync.md` | Canonical Git/SharePoint reconciliation procedure; Draft 0.1 | Separate manual publication gate | SharePoint destination and mechanics remain unknown; no change is required for the proposed Gate 2 workflow implementation | `863ae60a4a57deb078eb7bdb780ee6314ec7a992` |
| `docs/plans/0001-repository-initialization-plan.md` | Historical bootstrap plan; Proposed plan record | Origin of the 11-file baseline design and authority boundaries | Contains time-bounded historical repository facts; must not control current state | `077b37a7288c47ebcb687822dfcf27294fe14f19` |
| `docs/plans/0002-current-state-discovery-and-decision-readiness-plan.md` | Current `main` copy of SAC-PLAN-0002; **Proposed / Not Approved** | PR #4 introduced it; PR #3 later changes its status | Conflicts with PR #3 head, which records it as Approved and executed; Issue #5 pauses resolution | `1836c30f534ff0c0a1702b977e27e0f763333614` |
| `registers/decision-log.md` | Canonical decision register; Draft 0.1 | Contains `SAC-DEC-001` through `SAC-DEC-006` | No current canonical decision for Issue #5; PR #3 branch adds 007/008 but those are not in `main` | `d322e099df1fe78609fa81ff5abd9c6e56301054` |
| `registers/document-register.md` | Canonical document-control register; Draft 0.1 | Registers exactly 11 baseline files; plans intentionally excluded | No information-update, context, or review-control records; PR #3 branch has additional non-canonical rows | `185baa3f5e1f4ede3a9bf2ebc821ab4fcc0381fb` |
| `registers/raid-log.md` | Canonical RAID structure; Draft 0.1; no entries | Supports evidence-backed risk tracking | Does not replace an update/impact register; no current entry authorizes Issue #5 decisions | `262990bae92ee02794007e807f60841a2c27004d` |
| `templates/current-state-brief-template.md` | Reusable Discovery template; Draft 0.1 | Requires evidence and explicit unknowns | Discovery-specific; cannot serve as update intake or PLAN template | `78897fca889b3be991148bab615a75abb8e7a1cb` |
| `templates/handover-checklist-template.md` | Reusable handover verification template; Draft 0.1 | Separates receipt from verification | Handover-specific; no update lifecycle or impact-map structure | `28f7d4dea35475e420f912d8c3a07db8aff698f1` |
| `templates/meeting-minutes-template.md` | Reusable meeting record; Draft 0.1 | States that minutes do not approve decisions | Does not create canonical decisions or update authorization | `7ae1acd0ba4479f181efb566ea9c3f3951653961` |
| `templates/project-document-template.md` | General controlled-document template; Draft 0.1 | Provides metadata, classification, review, and supersession sections | Too general for deterministic intake, impact mapping, PLAN/APPLY, and checkpoint recovery | `e7bb0d0e40be5ecc45def20a6b923f3106cadb09` |

No tracked context record or work journal exists at the approved base. No
tracked `agent-artifacts` path exists there. The absence is a verified inventory
finding, not an instruction to create canonical files during Gate 1.

### Retained PR #3 content

PR #3 proposes six changed paths. Its three new Discovery Draft files and three
modified files are historical/review evidence while the PR is paused.

| PR #3 head path | Role at PR head | Blob at `4bc090137d5843c975159ecd2b3b98f4cebf52a5` | Current classification |
|---|---|---|---|
| `docs/02-handover-and-discovery/confirmation-register.md` | Consolidated Discovery confirmation inventory | `743ed8b2740656933c7d4e867494d0020ac6d5e5` | Draft / Not Approved; retained PR evidence |
| `docs/02-handover-and-discovery/current-state-brief.md` | Discovery current-state questions and gaps | `00780bd8cd9f0438ebeb7248445ae66251fc634f` | Draft / Not Approved; retained PR evidence |
| `docs/02-handover-and-discovery/handover-checklist.md` | Discovery handover verification structure | `419010f743bce43d76399e88078b2619fcbc5fc8` | Draft / Not Approved; retained PR evidence |
| `docs/plans/0002-current-state-discovery-and-decision-readiness-plan.md` | Changes plan status to Approved and records execution | `c10f2eb37f14cf7f16c85478f11ddc9dbc1ac320` | Conflicts with Proposed/Not Approved `main` copy and current Issue #5 sequencing |
| `registers/decision-log.md` | Adds `SAC-DEC-007` and `SAC-DEC-008` | `e7134953a3344ae0e34d318dcd38b5d4b307f7e7` | Unmerged branch record; retain without treating as current canonical register |
| `registers/document-register.md` | Adds three Draft rows and Project Document classification | `7240090afa3c8ad1900af5ffa4c50be8bcc5c10c` | Unmerged branch record; retain without treating as current canonical register |

### Issues, Pull Requests, branches, and commits

| Object | Evidence and state | Authority/status interpretation |
|---|---|---|
| Issue #5 | https://github.com/frwkHoangQuy/-Doc-SAC/issues/5; open | Current controlling governance Issue by Human Authority Gate 0 action |
| Issue #2 | https://github.com/frwkHoangQuy/-Doc-SAC/issues/2; open and paused | Historical Phase 3 plan work; no continuation, closure, migration, or supersession authority |
| Draft PR #3 | https://github.com/frwkHoangQuy/-Doc-SAC/pull/3; open/Draft; six paths | Retained review evidence; no update, Ready, merge, close, rebase, or force-push authority |
| PR #4 | https://github.com/frwkHoangQuy/-Doc-SAC/pull/4; merged | Historical merge introducing the Proposed/Not Approved plan into `main`; merge does not itself approve it |
| `main` | `53479ad5694071555cbb97bdea5bbe3316271d45` | Current source checkpoint |
| `plan/0001-repository-initialization` | `270c85c1f114ef903275b0663eb70497eb5fa3ff` | Retained historical plan branch |
| `implementation/0001-repository-initialization` | `19d0daa52387172a679aab72d47dad8767f06278` | Retained historical implementation branch |
| `plan/0002-current-state-discovery-readiness` | `4ce275b0ecb3cd297636bade6168407de4e3b2d0` | Retained plan branch; merged by PR #4 |
| `implementation/0002-current-state-discovery-readiness` | `4bc090137d5843c975159ecd2b3b98f4cebf52a5` | Paused PR #3 head |
| `review/agent-artifacts` | Absent before Gate 1 | Gate 1 alone authorizes creation from the exact approved base |

Relevant commit sequence:

- `970c7f092a99cc31dfdc3cba2de6ff23dd815035` added SAC-PLAN-0002.
- `4ce275b0ecb3cd297636bade6168407de4e3b2d0` corrected its controls.
- `53479ad5694071555cbb97bdea5bbe3316271d45` merged PR #4 and is live `main`.
- `602aa2a28248295a0586fa0e6406ef7da532cbfb` added the six-file Discovery
  Draft package from the approved-plan branch line.
- `4bc090137d5843c975159ecd2b3b98f4cebf52a5` corrected four PR #3 files and
  is the paused head.

### Authority inventory

| Role | Permitted | Prohibited |
|---|---|---|
| Human Authority: Hoang Quy Nguyen (`frwkHoangQuy`) | Personally instruct Agent; explicitly approve gates, SHAs, paths, branches, transitions, merges, baselines, publication, migration, and supersession | Approval cannot be inferred; one approval cannot silently expand another |
| Lead PM/SA Reviewer | Read-only inspection, analysis, immutable-SHA review, and recommendations to Human Authority | Repository/GitHub writes; direct Agent instruction; approval or execution |
| Repository Agent | Read and perform only exact Human-Authority-approved writes; return evidence | Self-authorization, scope expansion, inferred facts, or prohibited transitions |
| Document owner/approver | Maintain and explicitly decide controlled document state within recorded authority | Treat receipt, commit, or PR as approval |
| Information source/submitter | Supply source material and requested update | Confirm its own authority or force canonical adoption |

### Current information-update and approval lifecycle

The existing canonical documents provide document drafting, review, explicit
approval, merge, content-commit recording, and separate SharePoint
synchronization. Templates distinguish confirmed facts, assumptions, unknowns,
and decisions. The decision register records explicit choices. However, there
is no canonical intake record, source-authority assessment, impact map,
immutable PLAN protocol, APPLY authorization record, context checkpoint, or
end-to-end update identifier connecting those pieces.

## 8.5 Current information and approval flows

The actual current flow is fragmented:

1. Information or an instruction enters through chat, an Issue, a plan, or a
   repository document.
2. Existing governance requires evidence classification, but no single intake
   record captures the submitter, source authority, confidentiality, requested
   change, and affected records.
3. Plans may propose an allowlist, while the decision log can record approval.
   No canonical rule requires one stable update ID across intake, plan,
   authorization, APPLY, validation, checkpoint, and baseline.
4. Impact mapping is performed ad hoc in plan prose. Indirectly affected
   navigation, registers, templates, lifecycle records, and retained work can
   be missed.
5. PLAN and APPLY were separated in SAC-PLAN-0001 and SAC-PLAN-0002 execution,
   but that separation is plan-specific rather than a reusable canonical
   workflow.
6. Review occurs through branches, commits, Issues, and PRs. Issue #5 now adds
   a dedicated non-merge artifact branch, but no canonical file yet defines its
   naming, correction, and retention rules.
7. Canonical state becomes current through authorized changes and merge to
   `main`; document approval and SharePoint publication remain separate. The
   repository lacks a compact context checkpoint that states the active gate,
   last approved action, exact SHAs, pending decisions, and permitted next
   action for a fresh session.

Missing or unsafe transitions include:

- discussion or Agent output to fact, without source and authority assessment;
- received evidence to Confirmed, without verification and acceptance;
- committed plan to approved plan, without an explicit SHA-bound decision;
- approved plan to APPLY, without a separate exact allowlist and base;
- successful APPLY to PR, merge, baseline, or publication, without independent
  gates;
- review branch presence to canonical or merge-candidate status;
- stale plan or PR state to current authority without reconciliation;
- branch deletion, history rewriting, or silent supersession that removes
  review evidence;
- context loss causing a fresh Agent to repeat or exceed an already bounded
  action.

## 8.6 Conflict analysis

### Issue #2

Issue #2 is an open plan work item whose body says implementation awaits
approval of a pushed plan SHA and exact allowlist. Historical execution then
created PR #3. The Gate 0 comment now pauses Issue #2. It remains evidence of
the earlier Phase 3 sequence but does not control current continuation.

Options:

1. Continue it now: preserves prior momentum but violates the Issue #5 pause
   and Mandate-first sequencing. Not viable without later explicit authority.
2. Close it immediately: simplifies the open-work list but could imply an
   unapproved migration or destroy context. Not recommended during workflow
   design.
3. Retain it paused until the workflow and Mandate pilot produce a migration
   decision: preserves evidence and prevents authority leakage. **Recommended.**

### Draft PR #3

PR #3 is open/Draft and contains a coherent six-file Discovery Draft package.
Its head records SAC-PLAN-0002 as Approved and adds decision entries 007/008,
while live `main` contains the plan as Proposed/Not Approved. It is two commits
ahead and one behind `main`. Its content is public-safe, but its phase sequence
is paused by Issue #5.

Options:

1. Rebase or update it now: would alter reviewed evidence and is prohibited.
2. Merge it: would promote paused Discovery work and conflicting status into
   `main`; prohibited and not recommended.
3. Close it now without a migration record: risks losing the operational
   meaning of its retained history; not recommended at Gate 1.
4. Leave it Draft and unchanged until a later Human Authority migration
   decision. Then either close it unmerged as retained evidence or authorize a
   new, non-destructive migration plan. **Recommended.**

### PR #4

PR #4 is merged. Its merge commit introduced SAC-PLAN-0002 into `main` but did
not approve the plan merely by merging it. The merge is immutable history and
must not be reverted or rewritten as a side effect of Issue #5.

Options are limited to interpreting and, if later authorized, superseding the
plan through new records. **Recommendation:** retain PR #4 and its merge
unchanged as historical provenance.

### SAC-PLAN-0002

At live `main`, SAC-PLAN-0002 is Proposed/Not Approved. At PR #3 head, it is
Approved with an execution record. Those are different branch states with
different authority implications. Issue #5 explicitly says presence in `main`
does not resolve approval or phase order.

Options:

1. Treat the PR #3 copy as canonical: conflicts with current `main` and Issue
   #5; not viable.
2. Delete or rewrite the `main` plan: loses provenance and is unnecessary.
3. Keep the `main` plan unchanged as a Proposed historical planning record,
   reserve its PR #3 state as retained evidence, and later create an explicit
   supersession/migration decision after the workflow pilot. **Recommended.**

### Joint recommendation

Keep Issue #2 and PR #3 paused and unchanged; retain PR #4 and both plan branch
histories; treat the `main` SAC-PLAN-0002 copy as Proposed/Not Approved; reserve
decision IDs `SAC-DEC-007` and `SAC-DEC-008` because they already exist in
retained PR #3 history; and defer continuation, closure, or supersession until
the canonical workflow is implemented, piloted, independently reviewed, and
the Human Authority makes an explicit migration decision.

## 8.7 Gap and risk analysis

| Risk | Likelihood | Impact | Evidence | Proposed control | Residual risk | Owner / decision authority | Stop condition |
|---|---|---|---|---|---|---|---|
| Source-to-fact traceability breaks | Medium | High | No canonical intake/update register | Stable update ID, source assessment, evidence reference, verifier, and classification history | Source authenticity may remain external | Record owner; Human Authority for acceptance | Source or authority cannot be identified |
| Decision or approval is inferred | Medium | Critical | Branch/plan/PR status differs across current objects | SHA-bound approval record and transition table | Human wording may still be ambiguous | Human Authority | Approval omits gate, SHA, scope, or action |
| PLAN authorizes APPLY | Medium | Critical | Plan-specific controls exist but no reusable workflow | Separate PLAN REVIEW and APPLY AUTHORIZATION states | Operator error | Human Authority and Agent | APPLY authorization is absent or incomplete |
| Impact map omits related records | High | High | No canonical impact-map structure | Required direct/indirect path, register, link, lifecycle, migration, and validation mapping | Novel relationships may be missed | Plan author; reviewer | Exact allowlist cannot be justified |
| Document/register inconsistency | Medium | High | PR #3 modifies documents and registers together, but ad hoc | Per-file intent table and consistency validation | Manual review remains necessary | Document owner/approver | IDs, status, or rows disagree |
| Context cannot be recovered | High | High | No context/work-journal record at base | Canonical current checkpoint plus immutable history entries | Checkpoint can become stale | Checkpoint owner; Human Authority for transitions | Fresh-context test fails |
| Review artifact becomes canonical or merged | Medium | Critical | Dedicated branch is new and not yet governed canonically | Non-merge branch rule, no PR, explicit banner, retention convention | GitHub admin could bypass process | Human Authority; repository admin | PR/merge target exists for review branch |
| Stale or contradictory state is used | High | High | SAC-PLAN-0002 differs between `main` and PR #3 | Live drift checks, conflict register fields, supersession links | Mutable GitHub state can change after inspection | Agent and reviewer | Base or object state differs from approval |
| Migration silently erases history | Medium | High | Paused Issue/PR need future treatment | Preserve branches/commits; new decision and supersession links only | Open objects may create confusion | Human Authority | Proposed action deletes or rewrites evidence |
| Public repository exposes restricted data | Low to Medium | Critical | Repository is public | Classification gate, sanitized references, value-pattern scan, manual complete-diff review | Human error remains | Author and Human Authority | Any non-public detail is required or detected |
| Reviewed SHA is rewritten | Low | Critical | Corrections historically use new commits; rule not yet centralized | Ban amend/rebase/force-push; verify remote ancestry | Admin override possible | Agent; Human Authority | Submitted SHA disappears or branch is rewritten |
| Branch/PR/merge/baseline gates collapse | Medium | Critical | Existing workflows are plan-specific | Independent explicit authorization states and checkpoint records | Process fatigue | Human Authority | One approval is used for another state |
| SharePoint state is inferred from Git | Low | High | Existing sync procedure already separates them | Retain separate publication authorization and register fields | External state unavailable to Agent | Human Authority | No verified destination/approval evidence |
| Phase transition precedes Mandate control | Medium | High | Issue #5 identifies Discovery-before-Mandate conflict | Mandate pilot before any Discovery continuation decision | Mandate evidence may be unavailable | Human Authority | Pilot evidence is unavailable or unsafe |

## 8.8 Proposed target workflow

Every update receives an immutable identifier `SAC-UPD-NNN`. State changes are
recorded without deleting prior state. A state records required inputs,
outputs, role, decision evidence, failure path, and stop condition.

| State | Required input | Required output | Responsible role | Approval point | Failure path / stop |
|---|---|---|---|---|---|
| 1. `INTAKE` | Public-safe request and source reference | Update-register entry with ID, submitter role, date/timezone, requested change, affected phase, confidentiality assessment, owner, approver, urgency, conflicts, questions, and expected outcome | Agent under bounded prompt or authorized record owner | None; receipt is not acceptance | Reject unsafe content; stop if source cannot be referenced safely |
| 2. `SOURCE CLASSIFICATION` | Intake entry and source | Source type, authority, provenance, mutability, and verification need | Plan author/reviewer | Human Authority only if source authority is itself a decision | Keep unverified; stop if authority is falsely implied |
| 3. `INFORMATION CLASSIFICATION` | Individual statements | Confirmed, Assumption, Unknown, or Decision required with evidence | Record owner and verifier | Human Authority for decisions/acceptance | Demote unsupported claims to Unknown |
| 4. `IMPACT MAP` | Classified proposed change | Direct/indirect paths, records, links, lifecycle, security, migration, downstream phases, exact candidate scope | Plan author | Reviewer assesses completeness | Stop if affected scope is open-ended |
| 5. `PLAN` | Intake, classifications, impact map | Immutable proposed plan with base, branch, exact paths, per-file intent, validations, rollback, exclusions | Agent under Human prompt | None; plan cannot approve itself | Return evidence gaps or bounded alternatives |
| 6. `PLAN REVIEW` | Full plan SHA/path | Independent findings and recommendation | Lead PM/SA Reviewer, read-only | Human Authority decides accept/correct/reject | Correction uses a new immutable review commit |
| 7. `APPLY AUTHORIZATION` | Accepted plan SHA and review | Explicit gate, implementation branch, exact base, exact allowlist, intent, validations, rollback, prohibited actions | Human Authority | Required | Stop on omitted SHA/scope/base or drift |
| 8. `APPLY` | Complete authorization | Only allowlisted changes and one or more explicitly bounded commits | Repository Agent | No additional implied authority | Stop before extra path/action |
| 9. `VERIFY` | Implementation SHA and authorization | Automated and manual results; exact path equality; traceability; clean state | Agent then independent reviewer | Human Authority accepts/corrects/rejects result | Correction uses new commit; never amend reviewed SHA |
| 10. `PR AUTHORIZATION` | Accepted implementation SHA | Explicit permission to create/update one named PR | Human Authority | Required when a PR is used | No PR without separate approval |
| 11. `MERGE AUTHORIZATION` | Reviewed PR head and checks | Explicit merge method/target authorization | Human Authority | Required | Stop on head drift, failed checks, or changed scope |
| 12. `BASELINE DECISION` | Verified merged/current content | Explicit accepted/rejected baseline and exact content SHA | Human Authority | Required | Merge alone remains non-baseline |
| 13. `CONTEXT CHECKPOINT` | Results of each gate/transition | Current phase, baseline, Issue, gate, SHAs, paths, decisions, paused work, next/prohibited actions | Agent under exact scope or record owner | Human Authority for decision fields | Stop if checkpoint conflicts with live state |
| 14. `MIGRATION / SUPERSESSION` | Approved new baseline and retained records | Explicit mapping of continue/migrate/supersede/close plus immutable links | Human Authority decision; Agent executes bounded changes | Required | Preserve history; stop on rewrite/deletion request |

Publication/synchronization remains a separate authorization after baseline.
Corrections return to PLAN or bounded APPLY as appropriate and always produce
new commits. Any state may fail closed: preserve the last verified state,
record the exact blocker, and require a new bounded Human Authority decision.

## 8.9 Proposed document topology and controls

### Minimum coherent canonical topology

| Information class | Proposed source of truth | Owner/update trigger |
|---|---|---|
| Repository execution rules | `AGENTS.md` | Human Authority-approved governance change |
| Repository navigation | `README.md` | Any canonical add/move/supersession |
| Document lifecycle | `docs/00-project-control/document-governance.md` | Lifecycle or authority rule change |
| Information-update workflow | `docs/00-project-control/project-information-update-workflow.md` | Workflow acceptance or revision |
| Intake and state history | `registers/information-update-register.md` | Intake or approved state transition |
| Current recoverable checkpoint and history | `registers/context-and-work-journal.md` | Every approved gate, transition, pause, migration, or baseline |
| Document catalog | `registers/document-register.md` | Controlled document/template/register add or status change |
| Decisions | `registers/decision-log.md` | Explicit Human Authority decision |
| PLAN structure | `templates/information-update-plan-template.md` | Workflow field change |
| Impact-map structure | `templates/information-impact-map-template.md` | Impact/validation coverage change |
| Review artifact structure | `templates/review-artifact-template.md` | Review protocol change |
| Non-canonical review outputs | `agent-artifacts/issue-<issue>/gate-<gate>/...` on `review/agent-artifacts` | Explicit review-artifact gate only |

Cross-references use stable IDs and repository-relative paths in canonical
files. A register row must match file metadata. Canonical documents use stable
paths, lifecycle status, version, owner, approver, GitHub identity, and
`last_updated`. Approval SHAs belong in registers/decisions, not self-referential
document metadata.

Review artifacts remain non-canonical because:

- they live only on `review/agent-artifacts`;
- no PR is created from that branch;
- the branch is never merged into `main` or an implementation branch;
- every artifact states Proposed/Not Approved;
- the Document Register does not register review artifacts;
- corrections create new commits and, when content changes materially, a new
  artifact version path.

Stale records are detected by comparing recorded base/head SHAs, live object
state, the current checkpoint, and supersession links. A stale record is
retained and marked historical/superseded through a new authorized record; it
is not rewritten.

Fresh-context recovery starts with `AGENTS.md`, `README.md`, the workflow,
information-update register, context/work journal, controlling Issue, and exact
immutable artifact/implementation SHAs. Current plans are identified by
`Proposed` or `In Review`; approved plans require a SHA-bound Human Authority
decision; implemented baselines require separate verification and baseline
decisions.

### Deterministic review-artifact convention

Use:

`agent-artifacts/issue-<decimal-issue-number>/gate-<decimal-gate-number>/<YYYY-MM-DD>-<lowercase-kebab-purpose>-v<positive-integer>.md`

Rules:

- issue and gate numbers are unpadded decimal values;
- the date is the Agent execution date in `Asia/Ho_Chi_Minh`;
- purpose is lowercase kebab-case;
- version starts at `v1` for a distinct artifact purpose;
- a content correction uses `v2`, `v3`, and so on at a new path and in a new
  non-amended commit;
- an execution retry that did not create a commit reuses no remote object and
  may use the same path only if no submitted artifact exists;
- paths are unique on the branch; case-only variants are prohibited;
- every submitted commit is retained; no amend, rebase, force-push, deletion,
  or history rewrite;
- branch commits are never merged and no PR is created from the branch.

This Gate 1 bootstrap path remains valid under the convention.

## 8.10 Proposed canonical implementation plan

### Recommended branch and base

- Branch: `implementation/0005-project-information-update-workflow`
- Exact immutable base:
  `53479ad5694071555cbb97bdea5bbe3316271d45`
- Base rule: create directly from that commit only after Gate 2 authorization.
  If live `main` differs or the branch exists, stop and request a new bounded
  decision; do not silently choose a newer base or alternate branch.

### Exact proposed canonical changed-file allowlist

| Order | Path | Operation | Purpose and intended change | Inputs/dependencies |
|---|---|---|---|---|
| 1 | `docs/00-project-control/project-information-update-workflow.md` | Add | Create `SAC-GOV-005`, Draft 0.1: canonical end-to-end lifecycle, authority matrix, state transitions, review branch protocol, correction, migration, publication, and stop rules | Issue #5, approved Gate 1 SHA, existing governance |
| 2 | `registers/information-update-register.md` | Add | Create `SAC-REG-005`, Draft 0.1: stable intake/update IDs, source/information classifications, impact/plan/apply/verify state, evidence, and history fields | Workflow |
| 3 | `registers/context-and-work-journal.md` | Add | Create `SAC-REG-006`, Draft 0.1: single current checkpoint plus append-only gate/transition history for fresh-context recovery | Workflow and update register |
| 4 | `templates/information-update-plan-template.md` | Add | Create `SAC-TPL-005`, Draft 0.1: exact PLAN structure covering source assessment, classifications, base/branch, allowlist, per-file intent, validation, rollback, exclusions, and authorization request | Workflow |
| 5 | `templates/information-impact-map-template.md` | Add | Create `SAC-TPL-006`, Draft 0.1: direct/indirect document, register, link, lifecycle, migration, phase, safety, validation, and rollback mapping | Workflow |
| 6 | `templates/review-artifact-template.md` | Add | Create `SAC-TPL-007`, Draft 0.1: non-canonical artifact banner, evidence inventory, findings, risks, exact request, limitations, and immutable-review fields | Review convention |
| 7 | `AGENTS.md` | Modify | Add binding workflow lookup, update-ID/PLAN/APPLY checks, review-branch non-merge rule, fresh-context check, and exact stop conditions | New workflow |
| 8 | `docs/00-project-control/document-governance.md` | Modify | Integrate source classification, update lifecycle, non-canonical review artifacts, context checkpoints, and supersession traceability | New workflow |
| 9 | `README.md` | Modify | Add navigation for the six new controlled artifacts and explain canonical versus review paths | Added paths |
| 10 | `registers/document-register.md` | Modify | Register the six new canonical files with exact IDs/statuses; keep review artifacts excluded | Added files and metadata |
| 11 | `registers/decision-log.md` | Modify | Reserve `SAC-DEC-007`/`008` due to retained PR #3 history; add `SAC-DEC-009` only for explicit Human Authority approval of the final Gate 1 SHA and `SAC-DEC-010` only for explicit Gate 2 authorization of this exact implementation branch, base, eleven-path scope, validation, migration treatment, rollback, and stops | Human Authority Gate 2 decision |

The allowlist is exact and contains eleven paths. No wildcard, generated file,
or implicit path is permitted.

### Ordered dependency gates

1. Lead PM/SA reads this artifact at its immutable commit and verifies every
   live-state claim read-only.
2. Human Authority accepts, corrects, or rejects this proposal.
3. Gate 2 authorization identifies the exact review SHA/path, branch, base,
   eleven paths, per-file intent, validations, migration treatment, and stops.
4. Agent re-verifies live state and creates the branch from the exact base.
5. Agent adds core workflow, registers, and templates.
6. Agent updates instructions, governance, navigation, document register, and
   decision log without changing unrelated content.
7. Agent performs deterministic validation and commits/pushes only the approved
   scope.
8. Independent read-only review occurs at the implementation SHA.
9. PR creation, merge, baseline, pilot, and migration remain later independent
   decisions.

### Explicit exclusions

The proposed Gate 2 APPLY must not modify:

- `docs/00-project-control/git-sharepoint-sync.md`;
- either existing plan;
- `registers/raid-log.md`;
- existing Discovery/handover templates;
- Issue #2, Issue #5, PR #3, or PR #4;
- any existing plan or implementation branch;
- repository settings, SharePoint, project facts, Discovery content,
  architecture, or software.

### Treatment of retained work

- Issue #2: remain open and paused.
- PR #3: remain open/Draft and byte-for-byte unchanged.
- PR #4: retain merged history unchanged.
- SAC-PLAN-0002: retain the `main` Proposed/Not Approved copy unchanged.
- `SAC-DEC-007`/`008`: reserve identifiers in the new design because the
  retained PR #3 branch already uses them; a later migration decision will
  reconcile canonical numbering without rewriting history.

After the workflow pilot and independent review, the Human Authority should
choose one bounded migration option: continue under a new compatible plan,
close Issue #2 and PR #3 unmerged while retaining links, or supersede
SAC-PLAN-0002 through a new plan/decision. This recommendation does not execute
that choice.

## 8.11 Validation plan

| Validation | Method | Acceptance criteria | Acceptance authority |
|---|---|---|---|
| Approved-base identity | Live GitHub ref plus local commit object | Exact authorized 40-character SHA and repository identity | Agent evidence; Human Authority accepts |
| Staged-path equality | Sort staged paths and approved allowlist using ordinal comparison | Exactly eleven paths; no missing/extra path | Agent; independent reviewer verifies |
| Operations | `git diff --cached --name-status`, raw tree modes, base existence | Six adds and five modifies exactly as listed; no rename/delete/mode-only/symlink/submodule | Agent/reviewer |
| Metadata | Parse front matter for all controlled new files | Unique IDs, titles, Draft status, version, owner, approver, identity, date match design | Document owner/approver |
| Structure | Required-heading scan plus manual inspection | Workflow states, authority, PLAN/APPLY, correction, migration, review, and checkpoint sections substantive | Lead PM/SA recommends; Human Authority accepts |
| Links/navigation | Resolve every relative Markdown link from its source directory at staged tree | Every target exists; README and register include all six new files | Agent/reviewer |
| Register consistency | Compare file metadata to Document Register rows and IDs | Exact one-to-one match; review artifacts excluded | Agent/reviewer |
| Decision traceability | Compare decision rows with Human authorization and reviewed SHA | No inferred decision; exact scope/evidence; no ID collision | Human Authority |
| Source/fact classification | Inspect examples and required fields | No statement can become Confirmed without evidence/verifier/authority | Lead PM/SA |
| PLAN/APPLY separation | Rule/state-machine checks | PLAN has no self-authorization; APPLY requires separate Human approval | Human Authority |
| Public safety | Credential/value signature scan and full manual diff | No secret value, personal/customer identifier, private endpoint, production or confidential content | Agent then Human Authority |
| Stale/conflict detection | Simulate changed base/object and conflicting checkpoint | Workflow stops and records drift without repair | Lead PM/SA |
| Immutable review | Verify commit ancestry and remote SHA; prohibit amend/rebase/force | Reviewed SHA remains addressable and corrections are new commits | Agent/reviewer |
| Review-branch isolation | Branch/PR reads | No PR from or merge of `review/agent-artifacts` | Human Authority |
| Fresh-context recovery | Execute Section 8.14 test | Fresh reviewer produces exact expected checkpoint without chat | Lead PM/SA |
| Migration/supersession | Trace retained Issue/PR/plan links and new decision | No history loss; explicit authority and successor/predecessor mapping | Human Authority |
| Unauthorized-action absence | Compare GitHub objects, branches, refs, and worktree before/after | No Issue/PR/merge/baseline/SharePoint/Discovery/architecture/software action outside scope | Agent/reviewer |
| Markdown/diff quality | `git diff --check`; complete staged diff | Pass with no whitespace error or hidden change | Agent |

Automated checks support path, mode, metadata, link, ID, heading, signature,
diff, ancestry, and clean-tree validation. Manual review is mandatory for
evidence meaning, authority, public safety, conflict resolution, and plan
adequacy. Only the Human Authority can accept decisions, scope, implementation,
merge, baseline, migration, or publication.

## 8.12 Rollback and correction plan

- Rejected Gate 1 plan: retain this immutable commit; record rejection outside
  the artifact only through a separately authorized object; a correction uses a
  new versioned artifact and new commit.
- Implementation validation failure before commit: leave changes uncommitted,
  report exact paths/blocker, and await direction. Do not create a partial
  commit merely to continue.
- Validation failure after commit but before push: preserve the local commit,
  do not amend or create a second commit under the same authorization, and
  report the local SHA and failure.
- Partial future APPLY after push: preserve the remote commit and branch; do
  not force-push or compensate automatically. A new correction authorization
  must identify the submitted SHA and exact corrective scope.
- Stale base: stop before branch/file writes. Human Authority must approve a
  refreshed plan or explicitly retain the old base.
- Incorrect or incomplete evidence: reclassify through a new authorized change;
  preserve the prior assertion and evidence history.
- Superseded artifact: add a new artifact/commit with predecessor/successor
  references; never delete the predecessor.
- PR rejection: retain PR and commits; Human Authority chooses correction or
  closure. No rebase, amend, force-push, or deletion.
- Baseline rejection: keep merged/current Git history distinct from baseline
  status; create an authorized corrective plan rather than rewriting history.

The review branch is never merged. No rollback method may use amend, rebase,
force-push, hard reset, history deletion, or branch deletion.

## 8.13 Mandate pilot plan

The pilot should use one real, public-safe Mandate statement supplied with a
sanitized authoritative source identifier by the Human Authority. If the source
cannot be referenced safely in this public repository, the pilot stops without
substituting invented content.

### Pilot PLAN

1. Create `SAC-UPD-001` intake and source classification.
2. Map impact against the exact proposed pilot APPLY scope:
   - `docs/01-mandate-and-stakeholders/mandate.md` — add;
   - `registers/information-update-register.md` — modify;
   - `registers/context-and-work-journal.md` — modify;
   - `registers/document-register.md` — modify.
3. Produce the Gate 4 review artifact under the deterministic convention.
4. Stop after commit/push and independent review.

Pilot PLAN success means source authority and public safety are verified,
statements are classified, the exact four-path scope is justified, validation
and rollback are defined, and no canonical path changes. Failure means any
evidence, authority, classification, or scope is unresolved.

### Independent approval and pilot APPLY

The Human Authority must separately approve the Gate 4 artifact SHA/path,
implementation branch, exact base, four paths, per-file intent, validation,
rollback, and stops. Pilot APPLY creates no PR, merge, baseline, or SharePoint
action unless separately authorized.

Pilot APPLY success means the four-path diff exactly implements the approved
Mandate information, maintains source-to-fact traceability, updates the
checkpoint, passes public-safety and link/register validation, and is reviewed
at its immutable SHA. Failure preserves the submitted commit and returns to a
new correction PLAN.

Final baseline acceptance is a separate Human Authority decision after
independent verification. Rejection keeps the content non-baseline and requires
a new corrective or supersession plan. The pilot performs no substantive
Discovery.

## 8.14 Fresh-context recovery test

### Inputs

A fresh authorized Agent or reviewer receives only:

1. repository URL and `AGENTS.md`;
2. `README.md`;
3. the canonical information-update workflow;
4. information-update register;
5. context/work journal;
6. controlling Issue URL;
7. recorded immutable review and implementation SHAs/paths;
8. live branch/PR reads.

No prior chat history or unstored Agent memory is permitted.

### Procedure

1. Verify repository identity, visibility, default branch, live SHA, and clean
   local state.
2. Read instructions and workflow from the recorded baseline SHA.
3. Locate the current checkpoint and active `SAC-UPD-NNN` record.
4. Resolve the controlling Issue, active gate, last approved action, baseline,
   source branch/SHA, review branch/SHA/path, and implementation branch/SHA.
5. List pending Human decisions and all paused, retained, or superseded work.
6. Compare the recorded exact allowlist with immutable diffs and live state.
7. State one permitted next action and all prohibited actions.
8. Stop on any mismatch rather than choosing a new state.

### Expected output and acceptance

The reviewer must reproduce, without ambiguity:

- current phase and approved baseline or explicit absence of one;
- Issue #5 and active gate;
- last approved action;
- exact source, review, and implementation branches/SHAs/paths;
- pending Human decisions;
- paused Issue #2, PR #3, and retained SAC-PLAN-0002 state;
- exact current allowlist;
- permitted next action and prohibited actions.

Acceptance requires exact SHA/path equality, no reliance on chat, no inferred
approval, and agreement between canonical checkpoint, registers, immutable
objects, and live GitHub state. Failure freezes progression, records the exact
conflict through a separately authorized correction, and returns to Human
Authority.

## 8.15 Explicit exclusions and stop conditions

Gate 1 does not authorize:

- any canonical file modification;
- any Issue or Pull Request mutation;
- implementation branch mutation;
- a PR for the review branch;
- merge, rebase, amend, force-push, tag, release, setting, label, milestone, or
  deployment;
- Gate 2, Gate 3, Gate 4, Gate 5, pilot PLAN, pilot APPLY, canonical
  implementation, baseline, SharePoint, Discovery, architecture, or software;
- approval, migration, supersession, closure, or phase transition;
- treating this artifact as canonical or self-authorizing.

A later Agent must stop if prompt authority is not personally transmitted by
the Human Authority; the prompt/hash/base/branch/path/allowlist differs; live
state drifts; the worktree is dirty; evidence is inaccessible; scope becomes
open-ended; sensitive content is required; a reviewed SHA would be rewritten;
an Issue/PR/branch action is not explicit; validation fails; or remote write
state is ambiguous.

## 8.16 Exact authorization requested from Human Authority

The object requested for independent Gate 2 review is the full 40-character
commit SHA that adds this exact artifact path:

`agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v1.md`

The Agent reports that immutable SHA after committing and remote read-back.
The SHA cannot be embedded in this file because doing so would change the file
and therefore the commit SHA.

After independent read-only review, the bounded Human Authority decision
requested is to approve, correct, or reject:

- this exact Gate 1 commit SHA and artifact path;
- proposed implementation branch
  `implementation/0005-project-information-update-workflow`;
- exact base `53479ad5694071555cbb97bdea5bbe3316271d45`;
- the exact eleven-path allowlist and per-file intent in Section 8.10;
- all validation requirements in Section 8.11;
- the retained, paused, unchanged treatment of Issue #2 and PR #3, unchanged
  PR #4 history, unchanged Proposed/Not Approved SAC-PLAN-0002, and reservation
  of `SAC-DEC-007`/`008`;
- non-destructive rollback and stop boundaries.

Even if the proposal is accepted, PR creation, Ready transition, merge,
baseline, SharePoint, pilot PLAN/APPLY, Issue/PR migration or closure,
Discovery, architecture, software, and every later gate remain prohibited
unless separately authorized.

This artifact is a proposal. It is not approved, is not canonical, does not
authorize implementation, and cannot authorize itself.
