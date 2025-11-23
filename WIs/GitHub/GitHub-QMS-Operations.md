---
slug: GitHub-QMS-Operations
revision: r3
type: WI
status: approved
effective: 2025-11-23
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Operations.md
---

# **WI – Operate the QMS in GitHub**

## **1. Purpose**

To define how the Floating Eye Software (FLEY) Quality Management System (QMS) operates within GitHub.

This work instruction ensures consistent operation and continual improvement of the QMS through a **unified digital workflow** accessible to all process owners. It provides the operational foundation used by FLEY-Action-Management and GitHub-Project-Management.

---

## **2. Scope**

Applies to all QMS-related records and activities maintained in GitHub repositories, including:

* CAPA and Nonconformance management
* Risk and Opportunity tracking
* Change Requests and Change implementation
* Quality Objectives and Management Reviews
* Internal Audits and Improvement actions

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* SOP – Quality-Planning
* WI – FLEY-Action-Management
* WI – GitHub–Document–Control
* WI – GitHub–Change–Control
* WI – GitHub–Version–Control
* [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)

---

## **4. Responsibilities and Authorities**

| **Role**                        | **Responsibilities**                                                                                                                                                                                                      | **Authorities**                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Quality Manager / QMS Admin** |  Oversees repository configuration and structure; Ensures all QMS artifacts are properly linked and controlled; Maintains traceability across repositories and ensures linkage to governing FLEY Actions; Maintains cross-repository traceability. |  Approve QMS-level Issues, Plans, and Milestones; Create and close MR milestones. |
| **Process Owners**              |  Maintain Issues and Plans relevant to their processes; Link work to the correct MR milestone; Provide inputs for MR records.                                                                                  |  Approve Issue closure for their process areas.                                        |
| **Contributors / Team Members** |  Execute assigned actions and attach evidence; Use GitHub’s dependency and linking features to maintain traceability; Participate in MR-related actions.                                                       |  Close low-risk Issues with peer review.                                               |

---

## **5. Procedure**

Day-to-day QMS activity is driven through GitHub Issues, Projects, and Pull Requests. These tools together ensure that every quality record - whether a Risk, CAPA, or Audit - is **visible, traceable, and closed through a controlled workflow**.

### **5.1 GitHub Components and QMS Roles**

| GitHub Area                      | QMS Function                                             |
| -------------------------------- | -------------------------------------------------------- |
| **Repository (`fley-qms`)**      | Controlled home for QMS documentation and records.       |
| **Issues**                       | Primary mechanism for QMS records and actions.           |
| **Pull Requests**                | Formal approvals and document control.                   |
| **Projects → FLEY QMS Board**    | Workflow management for all QMS issues.                  |
| **Discussions**                  | Optional collaboration and feedback.                     |
| **Actions**                      | Optional automation for reminders, exports, and metrics. |
| **Wiki**                         | Optional user-friendly access to documentation.          |

---

### **5.2 FLEY QMS Workflow**

```
Backlog (GREY) → In Progress (GREEN) → In Test (YELLOW) → Closed (BLUE)
```

| Column      | Purpose                                     | Examples                         |
| ----------- | ------------------------------------------- | -------------------------------- |
| Backlog     | New or proposed records awaiting triage.    | New Risk, Objective, CAPA.       |
| In Progress | Active investigation or execution.          | Implementing corrective actions. |
| In Test     | Awaiting verification, review, or approval. | Effectiveness checks, PR review. |
| Closed      | Record verified complete.                   | MR approved, CAPA effective.     |

---

### **5.3 Issue Types**

| Type            | Definition                                                  | Use                                    |
| --------------- | ----------------------------------------------------------- | -------------------------------------- |
| **Development** | Activities that create or improve products, processes, or systems. | QMS framework setup, automation, template design. |
| **Operations**  | Activities that manage, maintain, or monitor processes and systems. |CAPA, Audit, Objective, Risk, Management Review.   |

---

### **5.4 QMS Label Definitions**

| Label             | | Definition                                    |
| ----------------- | ----------------------------------------------- |
| Audit             | Internal/external audit records                 |
| CAPA              | Corrective and preventive actions               |
| Change Request    | Proposed change for review and approval         |
| Change            | Implementation of a Change Request              |
| Improvement       | General improvement actions                     |
| Management Review | MR records and outputs                          |
| Nonconformance    | Record of non-fulfilment of a requirement       |
| Objective         | Quality objectives and performance tracking     |
| Opportunity       | Positive improvement opportunities              |
| Risk              | Risk identification, evaluation, and mitigation |

---

### **5.5 Project Views**

| View                  | Filter                                 | Purpose                                  |
| --------------------- | -------------------------------------- | ---------------------------------------- |
| Development           | `type:Development`                     | Track QMS framework creation or updates. |
| QMS Actions           | `label:"Management Review", Objective` | Plan and track leadership actions.       |
| Changes               | `label:"Change Request", Change`       | Full lifecycle of changes.               |
| Improvements          | `label:Improvement`                    | Continual improvement.                   |
| Risks & Opportunities | `label:Risk, Opportunity`              | Risk-based thinking dashboard.           |
| Audits                | `label:Audit`                          | Internal and external audits.            |
| CAPAs                 | `label:CAPA`                           | Corrective/Preventive Actions.           |
| Nonconformances       | `label:Nonconformance`                 | Track deviations.                        |
| Missing Label         | `no:label -type:Development`           | Classification completeness check.       |
| All Issues            | *(no filter)*                          | Complete record view.                    |

---

### **5.6 Document Status and Approval**

All QMS documents and templates follow the controlled workflows defined in
GitHub-Document-Control and GitHub-Change-Control.

* Drafts are created in **feature branches** off `main`.
* When ready for formal review, create a **Pull Request (PR)** targeting `main`.
* Link all PRs to the corresponding Change Request Issue.
* Required reviewers provide approvals within the PR; review comments serve as audit evidence.
* PR merge is the **formal approval event** for controlled content.
* Feature branches may be deleted after merge; Git history preserves prior drafts.
* `main` always reflects the **current approved version**.
* Git tags capture the **official revision identifier** for the approved content.

---

### **5.7 Backup and Export**

Backups preserve the long-term integrity of the QMS record set and provide a disaster-recovery measure aligned with Document Control retention requirements.

Follow WI – GitHub-QMS-Setup (quarterly manual export until automated).

---

## **6. Records**

| **Record / Artifact**       | **Responsible Owner** | **Storage Location**  | **Retention**        |
| --------------------------- | --------------------- | --------------------- | -------------------- |
| Issues                      | Quality Manager       | QMS GitHub repository | 5 years              |
| Milestones                  | Quality Manager       | GitHub Milestones     | 5 years              |
| Linked Issues               | Process Owners        | Respective repos      | 5 years              |
| Configuration and templates | QMS Admin             | `/Templates/`         | Current + 1 revision |
| Repository Exports          | QMS Admin             | `/Records/github-exports/`| 5 years          |
