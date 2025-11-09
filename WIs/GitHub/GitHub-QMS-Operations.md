# **WI – Operate the QMS in GitHub – Single FLEY Board**

**Slug:** GitHub-QMS-Operations  
**Revision:** r2 **DRAFT**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Change-Control-SOP, Document-Control-SOP, Identification-and-Traceability-SOP, Quality-Planning-SOP, Leadership-SOP, Management-Review-SOP, Risk-and-Opportunity-Management-SOP, Project-Management-SOP, Design-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Operations.md  

---

## **1. Purpose**

To define how FLEY operates and maintains its **Quality Management System (QMS)** in GitHub using a single **Project (“FLEY QMS”)** that integrates both **Development** and **Operations** Issue Types and QMS Label categories.

This instruction ensures consistent operation and continual improvement of the QMS through a **unified digital workflow** accessible to all process owners.

---

## **2. Scope**

Applies to all operational QMS activities and quality records managed in GitHub, including:

* CAPA and Nonconformance management
* Risk and Opportunity tracking
* Change Requests and Change implementation
* Quality Objectives and Management Reviews
* Internal Audits and Improvement actions

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* WI – GitHub–Document–Control
* WI – GitHub–Change–Control
* WI – GitHub–Version–Control
* [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)

---

## **4. Responsibilities and Authorities**

| Role                            | Responsibilities                                            | Authority / Decision Rights        |
| ------------------------------- | ----------------------------------------------------------- | ---------------------------------- |
| **Quality Manager / QMS Admin** | Maintain board and automations; verify record completeness. | Approve closure of QMS records.    |
| **Top Management**              | Conduct and approve Management Reviews and key changes.     | Approve QMS direction and policy.  |
| **Process Owners**              | Manage assigned CAPAs, Risks, and Objectives.               | Approve closure of related Issues. |
| **Contributors / SMEs**         | Provide input, data, and recommendations.                   | May open or comment on Issues.     |

---

## **5. QMS Operations in GitHub**

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
| **Development** | Creation or improvement of products, processes, or systems. | New document, automation, or template. |
| **Operations**  | Execution or monitoring of QMS processes and records.       | CAPA, Risk, Audit, Objective, MR.      |

---

### **5.4 QMS Label Definitions**

| Label                 | Definition                                | Typical Usage                       |
| --------------------- | ----------------------------------------- | ----------------------------------- |
| **Audit**             | Record of internal/external audit.        | Audit plan or report.               |
| **CAPA**              | Corrective or Preventive Action.          | Linked to NC or Risk.               |
| **Change**            | Approved change implementation.           | Executing updates.                  |
| **Change Request**    | Proposed controlled change.               | Requesting a QMS update.            |
| **Improvement**       | Continual improvement initiative.         | Minor optimizations.                |
| **Management Review** | QMS review meeting record.                | Quarterly MR.                       |
| **Nonconformance**    | Requirement not fulfilled.                | Deviations or failures.             |
| **Objective**         | Quality KPI or goal.                      | Planning and review.                |
| **Opportunity**       | Positive potential for improvement.       | Linked to MR or Risk.               |
| **Risk**              | Potential negative impact or uncertainty. | Risk identification and mitigation. |

Each Label corresponds to a GitHub Issue Template for consistent metadata and traceability.

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

### **5.6 Milestone-Based MR Workflow**

The Management Review (MR) cycle in GitHub ensures that leadership oversight, performance review, and strategic actions are structured, traceable, and auditable. Each MR cycle corresponds to a **GitHub milestone** that ties together related quality records.

#### **1. MR Issue Creation**

1. Create a **Management Review (MR) issue** documenting decisions, outputs, and links to related issues.
2. This MR issue is **the source of truth** for the cycle.

#### **2. Milestone Creation**

1. Create a **milestone** corresponding to the MR issue (e.g., `MR-1: QMS Launch`).
2. Assign **Objectives, Risks, Improvements, and Opportunities** issues to this milestone.
3. Keep the milestone open until all assigned issues are completed.

#### **3. Sub-Issues & Linking**

* Create sub-issues under Objectives or Improvements for actionable tasks.
* Link each issue back to the originating MR issue for traceability.

#### **4. Progress Tracking**

* Use GitHub milestone progress bars to track completion of all assigned issues.
* Sub-issue progress rolls up to parent issue completion.

#### **5. Event-Driven Cycle Updates**

* For a new MR, create a new MR issue and milestone.
* Incomplete issues from prior cycles may be reassigned to the new milestone.
* Milestone names should remain consistent across repositories.

---

### **5.7 Change Control and Approvals**

* Controlled documents updated through Pull Requests linked to `Change Request` issues.
* Merge approval = official change approval.
* Old versions retained in Git history.

---

### **5.8 Integration and Traceability**

* All repos use same Issue Types and Label scheme.
* QMS Project serves as the traceability hub.
* Use “Linked Issues” for cross-repo connections.

---

### **5.9 Backup and Export**

Backups preserve the long-term integrity of the QMS record set and provide a disaster-recovery measure aligned with Document Control retention requirements.

Follow WI – GitHub-QMS-Setup (quarterly manual export until automated).

---

## **6. Records**

| Record                    | Location                           | Retention |
| ------------------------- | ---------------------------------- | --------- |
| QMS Issues (all)          | GitHub Project                     | Permanent |
| Management Review Records | GitHub Project                     | Permanent |
| Audit Reports & CAPAs     | GitHub Project                     | Permanent |
| Repository Exports        | `/records/github-exports/YYYY-MM/` | 5 years   |
