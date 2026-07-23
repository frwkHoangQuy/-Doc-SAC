# Issue #5 Gate 1 Corrected Inventory and Proposed Implementation Plan

## 8.1 Document control

| Field | Value |
|---|---|
| Artifact status | **Proposed — not approved** |
| Related issue | Issue #5, `[Governance] Project Information Update Workflow` |
| Issue URL | https://github.com/frwkHoangQuy/-Doc-SAC/issues/5 |
| Gate | Gate 1 correction only |
| Correction prompt ID | `SAC-GOV-PIUW-GATE1-CORRECTION-PROMPT-v1` |
| Objective | Preserve the verified v1 inventory and proposal while correcting six material governance findings and presenting a complete successor for independent review. |
| Authorization boundary | Read-only preparation plus this one new review artifact, one new immutable commit, and one normal push to the existing review branch. No canonical APPLY or later gate is authorized. |
| Canonical source branch | `main` |
| Canonical immutable base | `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Review branch | `review/agent-artifacts` |
| Artifact path | `agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v2.md` |
| Inspection timestamp | `2026-07-24T02:43:05+07:00` (`Asia/Ho_Chi_Minh`) |
| Repository visibility | Public |
| Public-safety classification | Public-safe governance proposal using only the permitted public governance identity; restricted identifiers and non-public content remain prohibited |

### Immutable predecessor

| Predecessor field | Exact value |
|---|---|
| Gate 1 prompt ID | `SAC-GOV-PIUW-GATE1-PROMPT-v1` |
| Gate 1 prompt SHA-256 | `0553b5643963f06bcf065ade1871fb4b47e48a81f85b519fadf458ba9c095739` |
| Review commit | `19197b84e3364a2ffb73eeea44e5a0e9bc329997` |
| Artifact path | `agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v1.md` |
| Artifact blob SHA | `81cf1c3e5f278207e9b3923d7463b7aacc564c23` |
| Review branch | `review/agent-artifacts` |
| Parent/canonical base | `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Review disposition | Gate 1 execution Passed; Gate 1 Plan v1 Correction required; Gate 2 implementation authorization not recommended and not granted |

V1 remains immutable and reviewable. V2 does not replace or rewrite v1. V2
becomes the current proposal only if the Human Authority accepts its immutable
commit after independent review.

### Correction traceability

| Finding | Corrected in v2 |
|---|---|
| Publication/synchronization authorization state omitted | Section 8.8 defines the full state, including inputs, decision/execution authority, evidence, success/failure/not-applicable paths, and prohibited implied transitions. |
| Gate 2 and Gate 3 semantics conflated | Sections 8.8–8.16 define Gate 2 as review plus Human Authority implementation authorization and Gate 3 as canonical APPLY, execution reporting, and independent verification. |
| Checkpoint could not record its own SHA | Sections 8.9–8.14 define four non-self-referential identifiers and two ordered implementation commits. |
| Gate 3 execution-report artifact contract absent | Sections 8.9–8.16 define an exact review-channel report transaction and proposed exact report path. |
| Public-safety criterion rejected every personal identifier | Sections 8.3, 8.7, 8.11, 8.13, and 8.15 permit only the necessary public governance identity and prohibit other identifiers unless separately classified and authorized. |
| Future canonical transaction lacked fixed commits/pushes/order | Sections 8.10–8.12 define exactly three commits, two pushes, one new branch, zero PRs, zero Issue/PR mutations, and failure handling at every boundary. |

This artifact is a non-canonical review object. It cannot approve itself,
authorize implementation, or become canonical through commit or branch
presence.

The Agent inspected local immutable Git objects and live GitHub state. The Agent
did not inspect SharePoint, private corporate sources, administrative audit
logs, or substantive project evidence. The Lead PM/SA Reviewer remains
read-only. Only Hoang Quy Nguyen (`frwkHoangQuy`) may instruct the Agent and
approve gates or state transitions.

No approved SharePoint location, Mandate source, substantive Discovery fact,
delivery ownership, delivery strategy, architecture, schedule, resource, or
readiness evidence was available. GitHub state is time-bounded and must be
re-read at each gate.

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

The URLs and public-safe pause content were read back. They authorize no
continuation, closure, migration, supersession, Discovery, or later gate.

### Live checkpoint

| Object | Verified state |
|---|---|
| Repository | `frwkHoangQuy/-Doc-SAC`; public; default branch `main` |
| Remote | `origin` fetch/push: `https://github.com/frwkHoangQuy/-Doc-SAC` |
| Live `main` | `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Issue #5 | Open; exact controlling title |
| Issue #2 | Open and paused by the Gate 0 comment |
| Draft PR #3 | Open/Draft; base `main`; head branch `implementation/0002-current-state-discovery-readiness`; head `4bc090137d5843c975159ecd2b3b98f4cebf52a5` |
| PR #3 divergence | Two commits ahead and one behind live `main`; merge base `4ce275b0ecb3cd297636bade6168407de4e3b2d0` |
| PR #4 | Merged at `53479ad5694071555cbb97bdea5bbe3316271d45` |
| Review branch before correction | Local and remote head `19197b84e3364a2ffb73eeea44e5a0e9bc329997`; no Pull Request |
| V1 predecessor | One direct child of canonical base; one added regular Markdown path; blob unchanged |
| V2 path before correction | Absent locally and at the remote review head |
| Local repository | Clean worktree and index; no untracked paths |

Active work is Gate 1 correction only. The last completed repository action was
the immutable v1 review artifact. Pending decisions include acceptance,
correction, or rejection of v2; a possible Gate 2 implementation authorization;
and later migration treatment. The only permitted next action after v2 is
independent read-only Gate 2 review. Canonical implementation, PR actions,
merge, baseline, publication, Discovery, architecture, and software remain
prohibited.

## 8.3 Evidence and classification method

### Sources inspected

1. Canonical source tree at
   `53479ad5694071555cbb97bdea5bbe3316271d45`.
2. Complete predecessor at
   `19197b84e3364a2ffb73eeea44e5a0e9bc329997` and blob
   `81cf1c3e5f278207e9b3923d7463b7aacc564c23`.
3. PR #3 head tree at
   `4bc090137d5843c975159ecd2b3b98f4cebf52a5`.
4. Commit topology and diffs for the baseline, PR #3, PR #4, and v1.
5. Live repository, branch, Issue, comment, and Pull Request reads.
6. Issue #5 and the applicable `SAC-GOV-002`, `SAC-GOV-003`, and
   `SAC-GOV-004` governance at the canonical base.
7. The correction prompt with SHA-256
   `0a0f913f44616ef13e0542b9ce1ba649046470e95c45c291a3c84baecf522bc3`.

### Classifications

| Classification | Meaning |
|---|---|
| Source | Identified input; source existence alone does not establish authority or truth. |
| Evidence | Inspectable support with immutable SHA/path or live URL where practical. |
| Verified repository fact | Reproduced from an immutable Git object. |
| Verified live state | Read from GitHub at the inspection time and subject to drift. |
| Human Authority decision | Explicit bounded choice personally transmitted by Hoang Quy Nguyen (`frwkHoangQuy`). |
| Instruction | Binding rule within its scope; not a project fact. |
| Proposal | Future design/action requiring approval. |
| Assumption | Working proposition requiring validation. |
| Unknown/unresolved | Evidence or an authorized choice is absent. |
| Approval | Explicit Human Authority acceptance identifying object, action, and boundary. |
| Canonical record | Explicitly designated working source under governance; Git presence alone is insufficient. |
| Review artifact | Immutable non-canonical evidence on `review/agent-artifacts`, never merged. |
| Historical record | Retained evidence that does not automatically control current authority. |

Conflicts are incompatible assertions of status, authority, sequence, scope, or
identity. Staleness is a recorded mutable state or base that no longer matches
live evidence. Authority leakage is any transition that appears to grant a
Human-Authority-only permission.

Git facts at named SHAs have high reproducibility. Live GitHub facts are
time-bounded. Uninspected private evidence receives no confidence claim.
Unsupported project statements remain unknown.

### Public-safety identity classes

Permitted public governance identity is limited to:

- `Hoang Quy Nguyen`;
- GitHub identity `frwkHoangQuy`; and
- necessary public repository ownership, authorship, approver, or authority
  references already required by the public governance records.

Prohibited unless separately classified, evidenced as necessary, minimized,
and explicitly authorized:

- customer, employee, stakeholder, or other personal identifiers;
- private contact details;
- credentials, secrets, tokens, private endpoints;
- production or confidential operational details;
- private corporate or SharePoint content; and
- sensitive or special-category personal data.

The permitted governance identity alone does not fail validation. Any newly
introduced identifier outside that class stops the transaction.

## 8.4 Complete relevant inventory

Every tracked file at the canonical base was inspected. Blob SHAs make the
inventory reproducible.

| Path | Purpose/status | Relationship | Gap/conflict | Blob at canonical base |
|---|---|---|---|---|
| `AGENTS.md` | Repository instructions; Draft 0.1 | Human Authority, exact allowlists, evidence rules | No reusable Issue #5 lifecycle, review protocol, or checkpoint model | `6a7af21eda66ece78efbef8b0e93150c3bacc980` |
| `README.md` | Repository overview/navigation; Draft 0.1 | Links 11 baseline files | No update workflow, context journal, or review channel navigation | `1a361d2c6560d3d13e4c697dc6c0015ab0d1ac3a` |
| `docs/00-project-control/document-governance.md` | Lifecycle/authority governance; Draft 0.1 | Draft/In Review/Approved/Superseded | No intake, impact map, PLAN/APPLY, or non-self-referential checkpoint | `7488f35f594b4d9fed0aaca471fcabf489639182` |
| `docs/00-project-control/git-sharepoint-sync.md` | Git/SharePoint reconciliation; Draft 0.1 | Separate manual publication gate | Destination/mechanics unresolved; already supplies essential separation | `863ae60a4a57deb078eb7bdb780ee6314ec7a992` |
| `docs/plans/0001-repository-initialization-plan.md` | Historical bootstrap plan | Origin of 11-file baseline | Historical state must not control current execution | `077b37a7288c47ebcb687822dfcf27294fe14f19` |
| `docs/plans/0002-current-state-discovery-and-decision-readiness-plan.md` | SAC-PLAN-0002; Proposed/Not Approved on `main` | PR #4 introduced it | PR #3 head says Approved/executed; Issue #5 pauses resolution | `1836c30f534ff0c0a1702b977e27e0f763333614` |
| `registers/decision-log.md` | Decision register; Draft 0.1 | `SAC-DEC-001`–`006` | PR #3 adds 007/008 only on retained branch | `d322e099df1fe78609fa81ff5abd9c6e56301054` |
| `registers/document-register.md` | Document catalog; Draft 0.1 | Exactly 11 baseline rows | No workflow/context records; PR #3 has unmerged rows | `185baa3f5e1f4ede3a9bf2ebc821ab4fcc0381fb` |
| `registers/raid-log.md` | RAID register; Draft 0.1; empty | Evidence-backed risks | Cannot replace update/impact/checkpoint records | `262990bae92ee02794007e807f60841a2c27004d` |
| `templates/current-state-brief-template.md` | Discovery template; Draft 0.1 | Evidence/unknown classifications | Not an intake or PLAN structure | `78897fca889b3be991148bab615a75abb8e7a1cb` |
| `templates/handover-checklist-template.md` | Handover template; Draft 0.1 | Receipt versus verification | No update lifecycle or impact map | `28f7d4dea35475e420f912d8c3a07db8aff698f1` |
| `templates/meeting-minutes-template.md` | Meeting template; Draft 0.1 | Minutes do not approve decisions | Cannot create canonical decisions/authorization | `7ae1acd0ba4479f181efb566ea9c3f3951653961` |
| `templates/project-document-template.md` | General document template; Draft 0.1 | Metadata/classification/review | Too general for deterministic transaction control | `e7bb0d0e40be5ecc45def20a6b923f3106cadb09` |

No canonical context/work journal, update register, or `agent-artifacts` path
exists at the canonical base.

### Retained PR #3 content

| PR #3 path | Role | Blob at `4bc090137d5843c975159ecd2b3b98f4cebf52a5` | Classification |
|---|---|---|---|
| `docs/02-handover-and-discovery/confirmation-register.md` | Discovery confirmation inventory | `743ed8b2740656933c7d4e867494d0020ac6d5e5` | Draft/Not Approved; retained evidence |
| `docs/02-handover-and-discovery/current-state-brief.md` | Discovery questions/gaps | `00780bd8cd9f0438ebeb7248445ae66251fc634f` | Draft/Not Approved; retained evidence |
| `docs/02-handover-and-discovery/handover-checklist.md` | Handover verification structure | `419010f743bce43d76399e88078b2619fcbc5fc8` | Draft/Not Approved; retained evidence |
| `docs/plans/0002-current-state-discovery-and-decision-readiness-plan.md` | Marks plan Approved/executed | `c10f2eb37f14cf7f16c85478f11ddc9dbc1ac320` | Conflicts with current `main` copy |
| `registers/decision-log.md` | Adds `SAC-DEC-007`/`008` | `e7134953a3344ae0e34d318dcd38b5d4b307f7e7` | Unmerged retained branch record |
| `registers/document-register.md` | Adds three Draft rows | `7240090afa3c8ad1900af5ffa4c50be8bcc5c10c` | Unmerged retained branch record |

### GitHub and branch inventory

| Object | State and authority interpretation |
|---|---|
| Issue #5 | Open controlling governance Issue; https://github.com/frwkHoangQuy/-Doc-SAC/issues/5 |
| Issue #2 | Open and paused; retained Phase 3 plan history |
| Draft PR #3 | Open/Draft, six paths; retained evidence with no transition authority |
| PR #4 | Merged historical provenance; merge did not itself approve the plan |
| `main` | Canonical checkpoint `53479ad5694071555cbb97bdea5bbe3316271d45` |
| `plan/0001-repository-initialization` | Historical plan branch at `270c85c1f114ef903275b0663eb70497eb5fa3ff` |
| `implementation/0001-repository-initialization` | Historical implementation branch at `19d0daa52387172a679aab72d47dad8767f06278` |
| `plan/0002-current-state-discovery-readiness` | Retained plan branch at `4ce275b0ecb3cd297636bade6168407de4e3b2d0` |
| `implementation/0002-current-state-discovery-readiness` | Paused PR #3 branch at `4bc090137d5843c975159ecd2b3b98f4cebf52a5` |
| `review/agent-artifacts` | Non-merge review channel; v1 head before this correction |

Relevant commits remain:

- `970c7f092a99cc31dfdc3cba2de6ff23dd815035`: add SAC-PLAN-0002;
- `4ce275b0ecb3cd297636bade6168407de4e3b2d0`: correct plan controls;
- `53479ad5694071555cbb97bdea5bbe3316271d45`: PR #4 merge/current `main`;
- `602aa2a28248295a0586fa0e6406ef7da532cbfb`: add Discovery package;
- `4bc090137d5843c975159ecd2b3b98f4cebf52a5`: correct PR #3 traceability;
- `19197b84e3364a2ffb73eeea44e5a0e9bc329997`: immutable Gate 1 v1 review.

### Authority and current lifecycle inventory

| Role | Permitted | Prohibited |
|---|---|---|
| Human Authority | Personally instruct Agent; explicitly decide gates, SHAs, paths, branches, transitions, merge, baseline, publication, migration | Inference or silent scope transfer |
| Lead PM/SA Reviewer | Read-only inspection and immutable-SHA recommendation | Writes, Agent instruction, approval, execution |
| Repository Agent | Exact approved reads/writes and evidence return | Self-authorization, scope expansion, invented facts |
| Record owner/approver | Maintain/review within recorded authority | Treat receipt/commit/PR as approval |
| Source/submitter | Supply evidence/request | Self-confirm authority or force adoption |

Current canonical governance supports drafting, evidence classification, review,
explicit approval, merge, content-commit recording, and separate SharePoint
synchronization. It lacks a stable update ID, intake, source-authority
assessment, complete impact map, reusable PLAN/APPLY contract, execution-report
channel contract, and non-self-referential recoverable checkpoint.

## 8.5 Current information and approval flows

The actual flow remains fragmented:

1. Information enters through conversation, Issues, plans, or documents.
2. Evidence classification is required, but no canonical intake captures source
   authority, confidentiality, requested change, affected records, or owner.
3. Plans may propose allowlists and the decision log may record approvals, but
   no stable update ID connects intake, PLAN, authorization, APPLY, validation,
   report, checkpoint, baseline, and publication.
4. Impact mapping is ad hoc and may omit navigation, registers, templates,
   lifecycle records, migration, or downstream phases.
5. PLAN/APPLY separation exists in prior plan-specific workflows but is not a
   reusable canonical state machine.
6. Review uses branches, commits, Issues, and PRs. The review branch exists but
   lacks a canonical Gate 3 execution-report contract.
7. Canonical state changes through authorized implementation and later merge;
   document approval, baseline, and SharePoint publication remain separate.
8. No canonical checkpoint can yet let a fresh reviewer correlate content,
   checkpoint, branch-head, and execution-report SHAs.

Unsafe transitions include discussion-to-fact, receipt-to-confirmation,
commit-to-approval, plan-to-APPLY, implementation-to-PR/merge/baseline,
baseline-to-publication, review-branch-to-canonical, stale-record-to-current,
and silent history removal. Every such transition must fail closed without a
separate explicit authority record.

## 8.6 Conflict analysis

### Issue #2

Issue #2 is open historical Phase 3 plan work. Its body requires plan-SHA and
allowlist approval; later execution produced PR #3. Gate 0 now pauses it.
Immediate continuation violates Issue #5 sequencing; immediate closure risks
unapproved migration. **Recommendation:** retain open, paused, and unchanged
until the workflow pilot and explicit migration decision.

### Draft PR #3

PR #3 is open/Draft. Its head marks SAC-PLAN-0002 Approved/executed and adds
decision records 007/008, while current `main` contains Proposed/Not Approved.
It is two commits ahead and one behind `main`. Rebase, update, merge, or close
is not authorized. **Recommendation:** retain Draft and byte-for-byte unchanged;
later choose closure-unmerged or a new non-destructive migration plan.

### PR #4

PR #4 is merged and introduced the Proposed/Not Approved plan to `main`. Its
merge is immutable history, not plan approval. **Recommendation:** retain
unchanged; use new records for any later supersession.

### SAC-PLAN-0002

The `main` copy is Proposed/Not Approved; PR #3 has a different branch state.
Issue #5 makes the phase-order and authority conflict explicit.
**Recommendation:** retain the `main` copy unchanged as historical proposed
planning; preserve the PR branch state as evidence; resolve only through a new
Human Authority migration/supersession decision.

### Joint recommendation

Keep Issue #2 and PR #3 paused and unchanged; retain PR #4 and both plan branch
histories; treat `main` SAC-PLAN-0002 as Proposed/Not Approved; reserve
`SAC-DEC-007` and `SAC-DEC-008` because retained PR #3 already uses them; and
defer continuation, closure, or supersession until workflow implementation,
pilot, independent review, and explicit Human Authority decision.

## 8.7 Gap and risk analysis

| Risk | Likelihood | Impact | Evidence | Proposed control | Residual risk | Owner/authority | Stop condition |
|---|---|---|---|---|---|---|---|
| Source-to-fact traceability breaks | Medium | High | No update register | Stable ID, source assessment, classification history | External authenticity | Record owner/Human Authority | Source/authority unidentified |
| Approval is inferred | Medium | Critical | Branch/status conflicts | SHA-bound explicit state decisions | Ambiguous wording | Human Authority | Gate/SHA/scope absent |
| PLAN self-authorizes APPLY | Medium | Critical | Controls are plan-specific | Gate 2 authorization distinct from Gate 3 execution | Operator error | Human Authority/Agent | Authorization incomplete |
| Impact scope is incomplete | High | High | No impact-map template | Direct/indirect paths and validations | Novel dependencies | Plan author/reviewer | Scope open-ended |
| Registers/documents diverge | Medium | High | PR #3 needed coordinated edits | Per-file intent and consistency validation | Manual error | Owner/approver | IDs/status/rows disagree |
| Checkpoint self-reference is impossible | High | Critical | A containing commit cannot know its own SHA | Two implementation commits plus later report SHA | Mis-recorded parent | Agent/reviewer | Journal subject != checkpoint parent |
| Gate 3 report is missing or ambiguous | Medium | Critical | V1 lacked review transaction | Gate 2 binds exact absent report path and parent; one report commit | Ambiguous remote state | Agent/Human Authority | Path/parent not exact |
| Context cannot be recovered | High | High | No canonical journal | Four-SHA comparison and fresh-context test | Stale journal | Checkpoint owner | Test mismatch |
| Review artifact is merged/canonicalized | Medium | Critical | Dedicated branch is non-canonical | No PR/merge; immutable versioning | Admin bypass | Human Authority | Review PR/merge exists |
| Stale/conflicting state is used | High | High | Plan states differ | Live checks and fail-closed conflict handling | Post-read drift | Agent/reviewer | Base/object differs |
| Transaction partially succeeds | Medium | Critical | Future work spans two branches | Fixed commit/push order and boundary reporting | Network ambiguity | Agent/Human Authority | Remote state ambiguous |
| History is silently erased | Medium | High | Paused objects need migration | Retain commits; new supersession records | Open-state confusion | Human Authority | Rewrite/deletion proposed |
| Public repository exposes restricted identity/content | Low–Medium | Critical | Public repository | Permit only necessary public governance identity; minimize and scan all other classes | Human error | Author/Human Authority | New non-permitted identifier/content |
| Reviewed SHA is rewritten | Low | Critical | Immutable review requirement | Ban amend/rebase/force; verify ancestry | Admin override | Agent/Human Authority | Submitted SHA missing/rewritten |
| PR/merge/baseline/publication gates collapse | Medium | Critical | Capability can be mistaken for authority | Independent states and decisions | Process fatigue | Human Authority | One gate used for another |
| Phase advances before Mandate | Medium | High | Issue #5 identifies conflict | Mandate pilot before Discovery continuation | Evidence unavailable | Human Authority | Pilot source unsafe/unavailable |

## 8.8 Proposed target workflow

Each update receives a stable `SAC-UPD-NNN` identifier. The required Issue #5
lifecycle has thirteen connected states. A context checkpoint is a mandatory
cross-cutting record after every approved transition, not a state that grants
authority. Migration/supersession is a separately authorized handling path
after an accepted state or when retained work must be reconciled.

| State | Entry/input | Required output | Responsible role / decision authority | Success, failure, correction, and stop |
|---|---|---|---|---|
| 1. `INTAKE` | Public-safe request/source | ID, submitter role, date/timezone, source, requested change, phase, provisional classes, confidentiality, owner, approver, urgency, conflicts, questions, outcome | Agent under prompt or authorized record owner; no approval | Unsafe source stops; receipt does not accept |
| 2. `SOURCE CLASSIFICATION` | Intake/source | Authority, provenance, mutability, verification need | Owner/reviewer; Human Authority if authority itself is a decision | Unverified remains unverified; false authority stops |
| 3. `INFORMATION CLASSIFICATION` | Atomic statements | Confirmed, Assumption, Unknown, or Decision required plus evidence | Owner/verifier; Human Authority for decisions | Unsupported claims demote to Unknown |
| 4. `IMPACT MAP` | Classified proposed change | Direct/indirect paths, registers, links, lifecycle, migration, phases, safety, exact candidate scope, validation, rollback | Plan author; reviewer tests completeness | Open-ended or unsafe scope stops |
| 5. `PLAN` | Intake/classifications/impact | Immutable proposal with base, branch, exact paths, intent, validations, rollback, exclusions | Agent under bounded prompt | Cannot self-approve |
| 6. `PLAN REVIEW` | Full plan SHA/path | Independent findings/recommendation | Lead PM/SA read-only; Human Authority later decides | Correction uses new review commit |
| 7. `APPLY AUTHORIZATION` | Accepted plan/review | Gate 2 decision naming exact Gate 1 SHA/path, Gate 3 branch/base, paths, commit roles, report path/parent, counts, validations, migration, safety, rollback, stops | Human Authority only | Missing field or drift stops |
| 8. `APPLY` | Complete Gate 2 authorization | Gate 3 canonical content commit then checkpoint-record commit, within exact transaction | Repository Agent | Extra path/commit/action stops; no implied PR |
| 9. `VERIFY` | Both implementation SHAs and remote branch | Automated/manual evidence, ancestry/path equality, remote read-back, Gate 3 report commit on review branch | Agent reports; Lead PM/SA verifies read-only; Human Authority decides outcome | Correction uses new authorization/commit; no amend |
| 10. `PR AUTHORIZATION` | Accepted implementation/report SHAs | Explicit permission for a named PR action | Human Authority | No PR by default; head drift stops |
| 11. `MERGE AUTHORIZATION` | Reviewed PR head/checks, when PR used | Explicit target/method/head authorization | Human Authority | Failed/drifted checks stop; PR presence is not approval |
| 12. `BASELINE DECISION` | Verified canonical content/merge state | Explicit accepted/rejected baseline and exact content SHA | Human Authority | Merge does not imply baseline; rejection preserves history |
| 13. `PUBLICATION / SYNCHRONIZATION AUTHORIZATION` | Accepted baseline, exact approved content SHA, classified publication copy, verified destination/workflow, public/private boundary, successful safety review | Separate Human Authority authorization record naming content, destination, executor, validation, and register update scope | Human Authority decides; authorized human performs external SharePoint action; Agent may only execute separately authorized Git record changes | Authorization is not publication. Success requires external evidence and later authorized register update. Failure leaves publication fields unchanged and records no false success. Correction regenerates from exact Git content. Not applicable requires explicit recorded decision. Missing destination, approval, safety, or exact SHA stops. Merge, baseline, capability, workflow completion, or this state itself cannot imply authorization or external completion. |

After every approved transition, a separately allowlisted checkpoint update
records the active update, gate, last authorized action, immutable subjects,
pending decisions, and next/prohibited actions. It grants no permission.

Migration/supersession requires an explicit Human Authority decision mapping
each predecessor to continue, migrate, supersede, retain, or close. History is
preserved. Corrections return to PLAN or a newly bounded Gate 3 transaction.
Publication failure never changes the accepted Git baseline and never imports
private SharePoint content into this public repository.

## 8.9 Proposed document topology and controls

### Canonical topology

| Information class | Source of truth | Trigger |
|---|---|---|
| Execution rules | `AGENTS.md` | Approved governance change |
| Navigation | `README.md` | Canonical add/move/supersession |
| Lifecycle | `docs/00-project-control/document-governance.md` | Lifecycle/authority change |
| Update workflow | `docs/00-project-control/project-information-update-workflow.md` | Workflow acceptance/revision |
| Intake/state history | `registers/information-update-register.md` | Intake or authorized transition |
| Current checkpoint/history | `registers/context-and-work-journal.md` | Gate transition, pause, migration, baseline, or publication decision |
| Document catalog | `registers/document-register.md` | Controlled artifact/status change |
| Decisions | `registers/decision-log.md` | Explicit Human Authority decision |
| PLAN template | `templates/information-update-plan-template.md` | Workflow field change |
| Impact template | `templates/information-impact-map-template.md` | Coverage change |
| Review template | `templates/review-artifact-template.md` | Review protocol change |
| Review artifacts | Exact paths on `review/agent-artifacts` | Explicit review-artifact authorization only |

Canonical metadata and register rows must agree. Approval SHAs belong in
registers/decisions, not in self-referential document metadata. Review artifacts
remain non-canonical: no PR, no merge, no Document Register row, explicit
Proposed status, immutable commits, and versioned corrections.

### Four non-self-referential Gate 3 identifiers

1. **Implementation content SHA:** Gate 3 Commit 1 implementing the exact
   eleven canonical paths; parent is canonical base.
2. **Checkpoint-record commit SHA:** Gate 3 Commit 2; only parent is the
   implementation content SHA; only changed path is
   `registers/context-and-work-journal.md`; its content records Commit 1, not
   its own SHA.
3. **Current implementation branch-head SHA:** after the two-commit
   implementation transaction, equals the checkpoint-record commit SHA.
4. **Gate 3 execution-report review SHA:** later review-branch commit recording
   both implementation SHAs, branch head, validations, and exact report path;
   its SHA is returned after commit and is not embedded in its own file.

The checkpoint journal records its subject/parent implementation content SHA.
The reviewer verifies that the live checkpoint-record commit has exactly that
SHA as its only parent, changes only the journal, and is the live implementation
branch head. The Gate 3 report records Commit 1, Commit 2, branch head, paths,
and evidence. No file self-records its containing commit SHA.

### Review-artifact naming and retention

Convention:

`agent-artifacts/issue-<issue>/gate-<gate>/<literal-authorized-date>-<lowercase-kebab-purpose>-v<integer>.md`

The full path is literal in the authorizing prompt; the Agent never substitutes
a date, chooses an alternate path, or uses a wildcard. Versions start at v1;
corrections use a new path/version and new commit. Case-only duplicates,
amend/rebase/force-push/deletion, PRs, and merges are prohibited.

Proposed exact Gate 3 report path for the later Gate 2 decision:

`agent-artifacts/issue-5/gate-3/2026-07-24-canonical-implementation-execution-report-v1.md`

The literal date is the path reservation date for this proposal, not a claim
about the future execution timestamp. Gate 2 must explicitly accept this exact
previously absent path or authorize no Gate 3 transaction.

### Gate 3 execution-report contract

The report is a complete public-safe Markdown artifact recording:

- Issue #5, Gate 3, and Gate 2 authorization evidence;
- final corrected Gate 1 review SHA/path;
- implementation branch and canonical base;
- exact eleven canonical paths;
- implementation content SHA;
- checkpoint-record commit SHA;
- current implementation branch-head SHA;
- parent relationships and per-commit changed paths;
- validation and remote read-back evidence;
- worktree state and live Issue/PR state;
- absence of unauthorized actions;
- limitations, drift, partial state, stops, and exact next decision.

The report commit is one new non-amended commit on existing
`review/agent-artifacts`; changes only the exact new report path; has the final
corrected Gate 1 review head authorized at Gate 2 as its only parent; occurs
after implementation remote verification; is pushed once without force; has no
PR and is never merged. Its full review SHA is returned and sent by the Human
Authority to the Lead PM/SA for read-only verification of the report and both
implementation commits.

## 8.10 Proposed canonical implementation plan

This is a proposed **Gate 3 canonical APPLY authorized by a future Gate 2
decision**. Gate 2 itself performs independent plan review and records the
Human Authority implementation authorization; it does not execute canonical
changes.

### Exact branch, base, scope, and limits

- Implementation branch:
  `implementation/0005-project-information-update-workflow`
- Exact base: `53479ad5694071555cbb97bdea5bbe3316271d45`
- New implementation branches: exactly 1, only if absent at Gate 3 preflight
- Canonical implementation commits: exactly 2
- Implementation-branch pushes: exactly 1
- Review-artifact commits: exactly 1
- Review-branch pushes: exactly 1
- Whole Gate 3 new commits: exactly 3
- Whole Gate 3 pushes: exactly 2
- Pull Requests: 0
- Issue/PR mutations: 0

### Unchanged exact eleven-path canonical allowlist

| Order | Path | Operation and intent |
|---|---|---|
| 1 | `docs/00-project-control/project-information-update-workflow.md` | Add `SAC-GOV-005`, Draft 0.1: lifecycle, authority, states, review protocol, correction, migration, publication, and stops |
| 2 | `registers/information-update-register.md` | Add `SAC-REG-005`, Draft 0.1: stable IDs, intake, classifications, state/evidence history |
| 3 | `registers/context-and-work-journal.md` | Add `SAC-REG-006`, Draft 0.1 in Commit 1; update only this path in Commit 2 to record Commit 1 and checkpoint state |
| 4 | `templates/information-update-plan-template.md` | Add `SAC-TPL-005`, Draft 0.1: exact PLAN/authorization structure |
| 5 | `templates/information-impact-map-template.md` | Add `SAC-TPL-006`, Draft 0.1: direct/indirect impact coverage |
| 6 | `templates/review-artifact-template.md` | Add `SAC-TPL-007`, Draft 0.1: review/evidence/report structure |
| 7 | `AGENTS.md` | Modify: workflow lookup, ID/PLAN/APPLY checks, review non-merge rule, checkpoint/recovery, stops |
| 8 | `docs/00-project-control/document-governance.md` | Modify: source classification, update lifecycle, review artifacts, checkpoint, supersession |
| 9 | `README.md` | Modify: six new canonical links and canonical/review distinction |
| 10 | `registers/document-register.md` | Modify: exact rows/IDs for six new canonical files; review artifacts excluded |
| 11 | `registers/decision-log.md` | Modify: reserve 007/008; add 009 for final Gate 1 approval and 010 for exact Gate 2 authorization only when explicitly decided |

No wildcard, implicit path, generated file, alternate checkpoint path, or
additional canonical path is allowed.

### Exact Gate 3 implementation-branch transaction

**Commit 1 — implementation content**

- only parent: canonical base
  `53479ad5694071555cbb97bdea5bbe3316271d45`;
- implements the approved eleven-path scope;
- changes only those eleven paths;
- initializes the context/work journal without its own SHA;
- contains no placeholder for its own SHA.

**Commit 2 — checkpoint record**

- only parent: Commit 1;
- modifies exactly
  `registers/context-and-work-journal.md`;
- records Commit 1 as the implementation content SHA;
- records approved branch, base, allowlist, active gate, pending decisions,
  permitted next action, prohibited actions, and exact planned Gate 3 report
  path;
- contains no placeholder or claim for Commit 2's own SHA.

After both local commits and validation, the Agent performs exactly one normal
non-force implementation-branch push. Remote head must equal Commit 2; Commit 2
must have Commit 1 as only parent; Commit 1 must have the canonical base as only
parent.

### Exact Gate 3 review-branch report transaction

Only after successful implementation remote read-back:

- start from the exact final corrected Gate 1 review head named in Gate 2;
- add exactly
  `agent-artifacts/issue-5/gate-3/2026-07-24-canonical-implementation-execution-report-v1.md`;
- create exactly one review commit;
- push exactly once, normally and without force, to
  `review/agent-artifacts`;
- create no branch or PR.

### Partial-state handling

| Boundary | Required response |
|---|---|
| Preflight fails before Commit 1 | No write; report blocker |
| Commit 1 exists but Commit 2 cannot be created | Preserve local Commit 1; no push, amendment, compensation, or extra commit; report SHA |
| Commit 2 exists but validation fails | Preserve both local commits; no push or correction; report both SHAs |
| Implementation push fails unambiguously | Stop; inspect remote read-only; no automatic retry if duplication/ambiguity is possible |
| Implementation remote state ambiguous | Stop before report commit; preserve state; Human Authority decision required |
| Implementation remote verified but report creation fails | Preserve remote implementation; no alternate report path or compensating write |
| Report commit exists locally but pre-push validation fails | Preserve local report commit; do not amend/push/create another |
| Report push ambiguous | Stop; do not retry automatically; report local/observed remote SHAs |

Hidden third canonical commits, extra checkpoint commits, alternate report
paths, automatic compensation, amend, rebase, reset, force-push, deletion, or
continuation after ambiguous remote state are prohibited.

### Dependencies, exclusions, and retained work

Gate 2 authorization must name the final v2 SHA/path, implementation branch,
base, eleven paths and intent, two implementation commit roles, checkpoint-only
path, exact report path and parent, validations, safety class, migration,
partial-state/rollback/stops, and all counts.

The Gate 3 transaction excludes `git-sharepoint-sync.md`, both existing plans,
RAID log, existing Discovery/handover templates, all Issue/PR mutations,
existing branches, settings, SharePoint, project facts, Discovery,
architecture, and software.

Issue #2 remains open/paused; PR #3 remains open/Draft and unchanged; PR #4
history remains unchanged; `main` SAC-PLAN-0002 remains Proposed/Not Approved;
decision IDs 007/008 remain reserved. Later migration is a separate Human
Authority decision.

## 8.11 Validation plan

| Validation | Method and acceptance |
|---|---|
| Gate 2 authority | Exact final v2 SHA/path, branch/base, eleven paths, two commit roles, checkpoint path, report path/parent, counts, safety, migration, rollback, and stops all explicitly named |
| Base/branch | Live repository/base exact; implementation branch absent before creation |
| Commit 1 | Only parent is canonical base; only eleven allowlisted paths; approved add/modify types; no self-SHA placeholder |
| Commit 2 | Only parent is Commit 1; only journal modified; journal records Commit 1; no self-SHA placeholder |
| Implementation remote | One push; remote head equals Commit 2; exact two-commit ancestry |
| Four identifiers | Journal subject = Commit 1; Commit 2 parent = Commit 1; implementation head = Commit 2; report records both and head |
| Review report | Exact previously absent path; parent exact final corrected Gate 1 head; one added regular Markdown path; one commit/push; no PR |
| Staged paths | Ordinal equality to the applicable commit allowlist: eleven for Commit 1, journal only for Commit 2, report only for review commit |
| Modes/operations | No rename/delete/mode-only/symlink/submodule/hidden tree change |
| Metadata | Unique IDs, Draft 0.1, owner/approver/identity/date consistent with register |
| Structure | Workflow, state table, authority, PLAN/APPLY, report, checkpoint, correction, migration, publication, and stops substantive |
| Links/navigation | Every relative Markdown link resolves from source; README/register include all six new canonical files |
| Register consistency | File metadata matches Document Register; review artifacts excluded |
| Decisions | No inference or ID collision; 007/008 reserved; 009/010 match explicit Human decisions |
| Public safety | Permit only necessary `Hoang Quy Nguyen`/`frwkHoangQuy` governance references; minimize them; stop on any newly introduced non-permitted identifier; scan credentials, secrets, endpoints, private sources, production/confidential content; inspect full diffs |
| PLAN/APPLY | Gate 2 authorizes; Gate 3 executes; no state self-authorizes |
| Publication | Separate Human Authority decision after accepted baseline; authorization distinguished from actual external completion |
| Drift/conflicts | Base/object/checkpoint mismatch fails closed |
| Fresh-context | Section 8.14 output reproduced without chat |
| Git quality | `git diff --check`, exact commit counts, remote ancestry, clean worktrees |
| Unauthorized actions | Zero PRs and Issue/PR mutations; no merge, baseline, SharePoint, Discovery, architecture, or software action |

Automated checks cover paths, modes, metadata, links, IDs, headings, signatures,
diffs, counts, ancestry, refs, and cleanliness. Manual checks cover evidence
meaning, identity necessity/minimization, public safety, authority, migration,
and plan adequacy. Only the Human Authority accepts decisions and transitions.

## 8.12 Rollback and correction plan

- Rejected v2: retain v1 and v2 commits; correction uses new version/path and
  commit.
- Stale base/branch/report path before Gate 3: stop before writes; obtain new
  explicit authorization.
- Commit 1 local failure state: preserve Commit 1 if created; no Commit 2
  workaround, amendment, or push.
- Commit 2 local failure state: preserve both commits; no push or third commit.
- Partial/ambiguous implementation push: read remote only, stop, and report;
  never compensate or auto-retry.
- Verified implementation but failed report transaction: preserve remote
  canonical commits; do not invent alternate path/parent or imply review.
- Report commit failure before push: preserve local report commit if created;
  do not amend or create another.
- Ambiguous report push: stop and report exact local/observed remote state.
- Incorrect evidence/checkpoint: new authorized correction records the prior
  assertion and successor; no rewrite.
- Superseded artifact: new version and predecessor/successor links; retain all.
- PR/baseline/publication rejection: preserve Git history and external state;
  use a new bounded plan.

No rollback uses amend, rebase, force-push, hard reset, deletion, review-branch
merge, hidden commits, or automatic compensation.

## 8.13 Mandate pilot plan

After canonical workflow acceptance for pilot use, a real public-safe Mandate
statement must be supplied with a sanitized authoritative source. The permitted
public governance identity may be used only when necessary. Any customer,
employee, stakeholder, contact, sensitive personal, private, credential,
endpoint, production, or confidential content stops the public-repository
pilot unless separately classified and explicitly authorized.

### Pilot PLAN

1. Create `SAC-UPD-001`.
2. Classify source/authority and every statement.
3. Map exact proposed pilot APPLY scope:
   - `docs/01-mandate-and-stakeholders/mandate.md` — add;
   - `registers/information-update-register.md` — modify;
   - `registers/context-and-work-journal.md` — modify;
   - `registers/document-register.md` — modify.
4. Produce an exact Gate 4 review path/commit under the convention.
5. Stop for independent review and Human Authority decision.

PLAN success requires safe source authority, exact scope, validation, rollback,
and no canonical change. Gate 4 does not authorize pilot APPLY.

Pilot APPLY requires separate approval of its SHA/path, branch/base, paths,
commit/checkpoint/report transaction, validation, safety, rollback, and stops.
Success requires source-to-fact traceability and immutable review. Baseline and
publication/synchronization remain separate decisions. Publication
authorization, when applicable, requires the full State 13 inputs and never
follows automatically from pilot success. No substantive Discovery occurs.

## 8.14 Fresh-context recovery test

### Inputs

A fresh authorized reviewer receives only repository URL, `AGENTS.md`,
`README.md`, canonical workflow, information-update register, context/work
journal, controlling Issue, exact review/implementation SHAs and paths, and live
branch/PR reads. No chat or unstored memory is allowed.

### Procedure

1. Verify repository identity, visibility, default branch, live SHA, and clean
   local state.
2. Read instructions/workflow at the recorded baseline.
3. Locate active `SAC-UPD-NNN`, controlling Issue, current gate, last approved
   action, baseline, and pending decisions.
4. Resolve source branch/SHA, final Gate 1 review SHA/path, implementation
   branch, implementation content SHA, checkpoint-record commit SHA, current
   implementation head, and Gate 3 execution-report review SHA/path.
5. Verify journal subject SHA equals the only parent of checkpoint-record
   commit.
6. Verify live implementation branch head equals checkpoint-record commit SHA.
7. Verify the report records both implementation SHAs, the same branch head,
   exact per-commit paths, and final Gate 1 parent.
8. Compare all values with live immutable Git objects and exact allowlists.
9. List Issue #2, PR #3, SAC-PLAN-0002, pending decisions, permitted next
   action, and prohibited actions.
10. Fail closed on any mismatch.

### Acceptance

The reviewer reproduces current phase/baseline, Issue/gate, last action, four
non-self-referential identifiers, branches/paths, exact allowlists, retained
work, decisions, and next/prohibited actions without chat. Journal subject,
checkpoint parent, live head, and report must agree exactly. Any mismatch
freezes progression and requires a new authorized correction; no value is
guessed.

## 8.15 Explicit exclusions and stop conditions

This Gate 1 correction does not authorize canonical files, implementation
branches, Issues, PRs, settings, Gate 2/3/4/5, pilot work, merge, baseline,
publication, SharePoint, Discovery, architecture, software, migration,
supersession, closure, or phase transition.

A later Agent stops if Human Authority transmission is absent; prompt/hash/base,
branch/head/path/allowlist/report path/count differs; worktree is dirty; live
state drifts; evidence is inaccessible; scope is open-ended; a reviewed SHA
would be rewritten; or validation/remote state is failed or ambiguous.

Public-safety stops include any newly introduced personal identifier other than
the necessary, minimized public governance identity `Hoang Quy Nguyen`
(`frwkHoangQuy`), or any private contact, customer/stakeholder/employee
identifier, sensitive personal data, credential, secret, token, private
endpoint, production/confidential detail, or private corporate/SharePoint
content without separate classification and explicit authorization.

No state, commit, branch, report, review, merge, baseline, technical capability,
or successful workflow step authorizes the next state by itself.

## 8.16 Exact authorization requested from Human Authority

The object requested for independent Gate 2 review is the full correction
commit SHA that adds exactly:

`agent-artifacts/issue-5/gate-1/2026-07-24-inventory-and-proposed-implementation-plan-v2.md`

The Agent returns that SHA after remote read-back. It cannot be embedded in this
file without self-reference.

After independent read-only review, the bounded Gate 2 decision requested is to
accept, correct, or reject the exact v2 SHA/path and, if accepted, explicitly
authorize or decline the following proposed Gate 3 contract:

- implementation branch
  `implementation/0005-project-information-update-workflow`;
- base `53479ad5694071555cbb97bdea5bbe3316271d45`;
- unchanged exact eleven canonical paths and per-file intent in Section 8.10;
- exactly two implementation commits: content then journal-only checkpoint;
- exactly one implementation-branch push;
- exact checkpoint-only path
  `registers/context-and-work-journal.md`;
- exact Gate 3 report path
  `agent-artifacts/issue-5/gate-3/2026-07-24-canonical-implementation-execution-report-v1.md`;
- report commit parent equal to the final corrected Gate 1 review head;
- exactly one report commit and one review-branch push;
- exactly three total commits, two pushes, one new branch, zero PRs, and zero
  Issue/PR mutations;
- four non-self-referential identifier rules;
- validation and public-safety rules;
- unchanged retained treatment of Issue #2, PR #3, PR #4, SAC-PLAN-0002, and
  reserved `SAC-DEC-007`/`008`;
- partial-state, rollback, and stop rules.

Gate 2 is independent plan review plus the Human Authority authorization
decision. Any authorized canonical execution occurs only in Gate 3. PR
creation, Ready transition, merge, baseline, publication/synchronization,
pilot, migration/closure, Discovery, architecture, software, and later gates
remain prohibited unless separately authorized.

V2 is a proposal, is not approved, is not canonical, does not authorize
implementation, and cannot authorize itself.
