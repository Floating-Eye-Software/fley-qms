# PLAN - Repository-Native Workflow QMS Integration

**Slug:** Repository-Native-Workflow-Plan
**Revision:** draft
**Status:** draft
**Related SOPs:** Quality-Planning-SOP, Change-Control-SOP,
Document-Control-SOP, Management-Review-SOP
**Controlled Source:**
`/Plans/Repository-Native-Workflow-Plan.md`

## 1. Purpose

Define, approve, and validate a repository-native implementation methodology
that is equivalent to the GitHub Issues methodology for implementing
applicable FLEY QMS processes.

The plan does not replace GitHub Issues. It establishes a controlled basis for
using either methodology when the selected implementation profile satisfies the
same governing QMS requirements.

Equivalence means satisfying the same process requirements for authority,
planning, execution, traceability, verification, approval, records, retention,
and Management Review input. It does not require identical artifacts or user
interfaces.

## 2. Background

The original CSV workflow implementation note treated file-native workflow as
a possible Halfbaked-specific adapter. The repository-native workflow is now a
realized organization-level execution model owned by `fley-org` and adopted or
adapted by execution repositories.

Canonical organization-owned inputs:

```text
../fley-org/templates/repo-workflow.md
../fley-org/templates/org-process.md
../fley-org/docs/dashboard-policy-and-procedures.md
../fley-org/docs/repo-workflow-installation.md
```

Typical repo-local execution surfaces:

```text
AGENTS.md
_work/README.md
_work/repo-workflow.md
_work/local-workflow.md                 # optional local supplement
_work/plans/plans.csv
_work/plans/*.md
_work/todo.csv
_work/todo.md
_work/codex-log.md
```

The approved `SOPs/Quality-Planning-SOP.md` separates governing process
requirements from platform-specific execution methods and can support multiple
approved methodologies.

The approved `WIs/FLEY/FLEY-Planning-Workflow.md` remains GitHub-specific. It
requires Planning Issues and GitHub Issues for quality-related work. Until
controlled changes are approved, repository-native workflow is not a
replacement for GitHub artifacts required by that WI.

## 3. Objective

Approve a methodology-neutral FLEY planning model with:

- an approved GitHub-native implementation profile
- an approved repository-native implementation profile
- defined cross-methodology traceability
- validation evidence demonstrating that repository-native workflow satisfies
  applicable QMS process requirements

## 4. Scope

### In Scope

- define methodology-neutral planning and execution requirements
- preserve GitHub Issues, Projects, dependencies, and Pull Requests as an
  approved methodology
- define repo-native plans, todos, dashboards, validation, Git history, and
  controlled Pull Requests as an approved methodology
- classify repo-native QMS records and define retention requirements
- define required links to controlled Plans, risks, changes, objectives, CAPA,
  and Management Review
- define approval, closure, VoE, escalation, backup, and audit requirements
- define cross-repository and cross-methodology traceability
- pilot and validate the repository-native implementation profile

### Out Of Scope

- making every `_work/` artifact a controlled QMS record
- making `fley-org` the owner of controlled QMS execution
- replacing GitHub Issues or retiring the GitHub WIs
- treating organization-process reconciliation as QMS approval
- treating ordinary commits, todo closure, or plan closure as controlled
  approval when Change Control requires a reviewed Pull Request
- approving repository-native use without Change Control and validation

## 5. Authority Boundaries

- `fley-org` owns the canonical lightweight repository workflow, dashboard
  policy, organization process, adoption guidance, and cross-repository
  routing.
- execution repositories own local execution state, implementation decisions,
  verification evidence, and repo-specific workflow extensions.
- `fley-qms` owns controlled process requirements, approved implementation
  profiles, required records, approval semantics, retention, validation, and
  methodology approval.

The generic repository workflow is lightweight and uncontrolled by default. A
repo-native artifact becomes a QMS record only when a controlled process
requires it, an approved implementation profile designates it as such, or it is
intentionally routed into a controlled QMS record.

## 6. Methodology Equivalence Model

| QMS intent | GitHub-native methodology | Repository-native methodology |
| --- | --- | --- |
| Identify executable action | GitHub Issue | Todo dashboard row plus prose when needed |
| Define and govern a plan | Planning Issue, linked Issues, optional controlled Plan | Plan dashboard row plus plan file, with controlled Plan when required |
| Classify work | Issue type, labels, fields | `track`, `priority`, plan relationship, and approved local fields |
| Represent workflow state | Project fields and Issue state | Authoritative dashboard `status` |
| Sequence work | Blocks / blocked-by relationships | `depends_on` references |
| Define acceptance and evidence | Issue body, comments, links, attachments | Plan/todo prose, source changes, linked evidence, and logs |
| Verify completion | Issue review and closure criteria | Todo completion criteria and plan closure review |
| Verify effectiveness | Planning Issue or linked VoE record | Plan VoE section or linked controlled record |
| Approve controlled change | Pull Request review and merge under Change Control | Pull Request review and merge under Change Control |
| Preserve traceability | Issue, Project, PR, and Git history | Stable file IDs, Git history, linked records, and validation results |
| Feed Management Review | Linked Plans, Issues, VoE, and MR Issue | Routed plan/VoE summaries and controlled MR records |

Both methodologies may use Git and Pull Requests for controlled-document
approval. Repository-native local closure is not controlled approval unless the
governing controlled process explicitly authorizes it.

## 7. Deliverables

1. Revised methodology-neutral FLEY Planning Workflow.
2. Confirmed GitHub-native implementation profile using the existing GitHub
   WIs, with required harmonization changes identified.
3. Approved repository-native workflow profile or WI.
4. Cross-methodology traceability and stable-ID linking procedure.
5. Repository-native templates, schemas, or controlled references where
   required.
6. Pilot validation protocol and completed validation report.
7. Training, adoption, and controlled rollout records where required.
8. Management Review input summarizing approval, evidence, residual risks, and
   rollout decision.

## 8. Work Plan

### Phase 1 - Requirements And Gap Analysis

1. Identify QMS processes that permit multiple implementation methodologies.
2. Extract mandatory requirements from applicable SOPs and approved WIs.
3. Compare GitHub-native and repository-native capabilities against those
   requirements.
4. Identify gaps involving approval, record classification, retention,
   traceability, backup, escalation, VoE, and Management Review.
5. Determine which controlled documents require revision or creation.

### Phase 2 - Controlled Design

1. Revise the FLEY Planning Workflow to define methodology-neutral core
   requirements and reference approved implementation profiles.
2. Preserve and harmonize the GitHub WIs as the GitHub-native profile.
3. Create the repository-native implementation profile or WI defining:
   - applicability and adoption approval
   - minimum surfaces and schemas
   - QMS record classification and retention
   - required controlled-record links
   - approval and closure authority
   - evidence and VoE requirements
   - validation, backup, and audit requirements
   - escalation into controlled QMS processes
4. Define cross-methodology linking without duplicating execution state.
5. Process controlled document changes through Change Control.

### Phase 3 - Pilot And Validation

1. Select a representative repository-native pilot.
2. Define a validation protocol covering normal work, plans, dependencies,
   controlled-change escalation, evidence, closure, VoE, and Management Review
   routing.
3. Execute the pilot using the proposed repository-native profile.
4. Verify deterministic validation and reconstruct traceability from retained
   records.
5. Record deviations, limitations, residual risks, and required changes.

### Phase 4 - Approval And Rollout

1. Resolve pilot findings through Change Control.
2. Approve the methodology-neutral planning model and implementation profiles.
3. Define repository adoption and periodic review requirements.
4. Train affected maintainers or process owners where required.
5. Route validation results, residual risks, and rollout decisions into
   Management Review.

## 9. Acceptance Criteria

The plan is complete when:

- methodology-neutral requirements are approved
- GitHub-native and repository-native profiles are both defined and approved
- the repository-native profile identifies applicable QMS activities and
  required controlled records
- responsibilities, approval authorities, and closure authorities are explicit
- dependencies, status, acceptance criteria, evidence, and VoE are traceable
- required controlled Plans, risks, changes, objectives, CAPA, and Management
  Review records are created or linked
- required reviews and approvals cannot be bypassed by ordinary local closure
- significant changes use the approved Change Control process
- records are readable, protected, backed up, retained, and auditable
- deterministic checks detect the defined invalid workflow states
- cross-repository and cross-methodology links can be reconstructed
- a representative repository-native pilot is completed and validated
- residual risks and rollout decisions are dispositioned through the
  applicable controlled process

## 10. Verification And Validation

### Verification

- review controlled documents against the approved requirements and
  equivalence model
- inspect schemas, templates, validation rules, approval gates, and records
- verify traceability from plan to actions, evidence, change records, VoE, and
  Management Review input
- verify GitHub-native requirements remain supported

### Validation

- execute representative QMS-related work through the repository-native profile
- confirm that process owners can plan, execute, review, approve, close, and
  reconstruct the work as intended
- confirm that controlled approvals and escalations cannot be bypassed
- confirm that retained records support audit and Management Review needs

## 11. Risks And Controls

| Risk | Control |
| --- | --- |
| Dual methodologies create inconsistent process outcomes | One methodology-neutral requirements baseline and approved profiles |
| Repo-local closure is mistaken for controlled approval | Explicit approval boundaries and Change Control gates |
| QMS records are not retained or protected | Approved classification, retention, backup, and access requirements |
| Execution state is duplicated and diverges | Stable cross-methodology links without duplicate authoritative state |
| Workflow drift changes required behavior | Canonical workflow ownership, drift checks, and controlled profile review |
| Pilot evidence is insufficient | Approved validation protocol and documented acceptance criteria |

## 12. Records

Expected records include:

- governing Change Request and linked implementation actions
- approved revised WIs or implementation profiles
- requirements and gap-analysis evidence
- pilot validation protocol, results, deviations, and disposition
- approval and rollout records
- VoE results, residual risks, lessons learned, and follow-up actions
- Management Review inputs and decisions

Retention and controlled locations shall be defined by the approved
implementation profile and applicable QMS procedures.

## 13. Verification Of Effectiveness

At plan closure, assess:

- whether both methodologies produce equivalent compliant process outcomes
- whether repository-native work remains traceable and auditable over time
- whether controlled approvals and required escalations function as intended
- whether users can select and operate the correct methodology
- whether validation findings and residual risks were effectively addressed

Record evidence, residual risks, lessons learned, follow-up actions, and an
Effective / Partially Effective / Ineffective assessment.

## 14. Status

Draft. Pending controlled planning, Change Control, and assignment of governing
QMS records.
