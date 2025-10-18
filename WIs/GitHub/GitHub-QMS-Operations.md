# **WI - Operate the QMS in GitHub – Single FLEY Board**

**Slug:** GitHub-QMS-Operations  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Change-Control-SOP, Document-Control-SOP, Quality-Planning-SOP, Leadership-SOP, Project-Management-SOP, Risk-and-Opportunity-Management-SOP   
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-QMS-Operations  

---

## **1. Purpose**

To define how the organization operates and maintains its Quality Management System (QMS) in GitHub using a single integrated Kanban board (**FLEY QMS**) within the `redwitch.wiki` repository.

This instruction ensures that:

* All QMS records (e.g., CAPAs, risks, objectives, reviews, changes, improvements) are managed in a consistent, auditable workflow.
* All required ISO 9001:2015 actions — determine, implement, review, and improve — are traceable.
* Digital evidence is retained as permanent quality records.

---

## **2. Scope**

Applies to all operational QMS activities, including:

* Risk and opportunity management
* CAPA and continual improvement
* Quality objectives planning and monitoring
* Management review and leadership activities
* Change control and document management
* Record control and periodic export

---

## **3. References**

* ISO 9001:2015 – Clauses 4 through 10
* ISO 9004:2018 – Clauses 4 through 9
* QMS-SOP-03 – Documented Information Control
* QMS-SOP-04 – Change Control
* QMS-SOP-05 – Leadership
* QMS-SOP-06 – Planning
* QMS-SOP-08 – Risk & Opportunity Management
* WI-QMS-10-02 – QMS Setup in GitHub

---

## **4. Responsibilities and Authorities**

| Role                            | Responsibilities                                                        | Authority / Decision Rights                   |
| ------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------- |
| **Quality Manager / QMS Admin** | Maintain the QMS board, monitor issues, and oversee Management Reviews. | Approve closure of QMS issues.                |
| **Top Management**              | Lead Management Reviews and approve outputs.                            | Final approval of review records and actions. |
| **Process Owners**              | Manage CAPAs, risks, and objectives in their process areas.             | Close related issues upon completion.         |
| **Contributors / SMEs**         | Provide data, context, and inputs for reviews and improvements.         | Propose and comment on QMS issues.            |

---

## **5. GitHub Components and QMS Roles**

| GitHub Area                      | QMS Function                                             |
| -------------------------------- | -------------------------------------------------------- |
| **Repository (`redwitch.wiki`)** | Controlled home for QMS documentation and records.       |
| **Wiki**                         | User-friendly access to policies, SOPs, and WIs.         |
| **Issues**                       | Primary mechanism for QMS records and actions.           |
| **Pull Requests**                | Formal approvals and document control.                   |
| **Projects → FLEY QMS Board**    | Workflow management for all QMS issues.                  |
| **Discussions**                  | Optional collaboration and feedback.                     |
| **Actions**                      | Optional automation for reminders, exports, and metrics. |

---

## **6. FLEY QMS Board Workflow**

**Columns:**

```
Backlog → In Progress → In Test → Closed
```

| Column          | Description                                             | Example Activities                                               |
| --------------- | ------------------------------------------------------- | ---------------------------------------------------------------- |
| **Backlog**     | New or planned QMS items awaiting assignment.           | New objective, identified risk, audit finding, improvement idea. |
| **In Progress** | Active work or implementation in progress.              | Implementing CAPA, mitigating a risk, executing an objective.    |
| **In Test**     | Awaiting validation, approval, or effectiveness review. | CAPA verification, risk monitoring, objective review.            |
| **Closed**      | Fully approved, verified, or completed.                 | CAPA effective, risk closed, audit complete, objective achieved. |

---

## **7. Typical Issue Lifecycles**

### 5.1 CAPA (Corrective or Preventive Action)

1. **Backlog:** Nonconformance or issue recorded.
2. **In Progress:** Root cause and actions defined and implemented.
3. **In Test:** Effectiveness verified.
4. **Closed:** Action confirmed effective; evidence attached.

### 5.2 Risk or Opportunity

1. **Backlog:** Risk or opportunity identified.
2. **In Progress:** Evaluation, mitigation, or implementation.
3. **In Test:** Results monitored.
4. **Closed:** Effectiveness confirmed or residual risk accepted.

### 5.3 Objective

1. **Backlog:** New objective proposed.
2. **In Progress:** Target and plan defined; implementation underway.
3. **In Test:** Results under review.
4. **Closed:** Objective achieved or concluded with justification.

### 5.4 Audit or Management Review

1. **Backlog:** Audit or review scheduled.
2. **In Progress:** Conducted; data and evidence gathered.
3. **In Test:** Findings analyzed, actions assigned.
4. **Closed:** Records and conclusions approved and filed.

---

## **8. Labels and Templates**

The following labels are used for operational QMS management:

| Category                 | Labels                                                                                                    | Description                                                                |
| ------------------------ | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| **Operational Records**  | `Audit`, `CAPA`, `Change Request`, `Improvement`, `Management Review`, `Objective`, `Opportunity`, `Risk` | Used for all ongoing QMS activities and ISO 9001 records.                  |
| **Setup Phase (legacy)** | `Setup`                                                                                                   | Used only for issues created during the initial establishment of the QMS.  |
| **Planning (optional)**  | `Plan`                                                                                                    | *(Optional)* Used if specific plans or initiatives are tracked separately. |

Each label corresponds to an Issue Template under `.github/ISSUE_TEMPLATE/` to ensure metadata consistency.

---

## **9. Leadership and Management Review**

* Quality Policy and Objectives are defined in `/QMS/Quality-Policy.md` and `/QMS/Quality-Manual.md`.

* Management Reviews are initiated quarterly using an issue labeled `Management Review`.

* Each review includes:

  * Status of previous MR actions
  * QMS performance and effectiveness
  * Internal/external issues and interested parties
  * Risks, opportunities, and objectives
  * CAPA status and audit results
  * Continual improvement actions
  * Customer satisfaction and feedback results
  * Adequacy of resources

* Minutes and supporting records are stored in `/records/management-reviews/`.

**Outputs and Follow-Up Actions:**

* New or revised **Quality Objectives** are created as GitHub issues labeled `Objective`.
* Each objective issue includes:

  * A clear measurable target or KPI
  * Assigned owner and due date
  * Links to the originating Management Review issue
* Objectives are tracked on the QMS Project Board and reviewed at the next Management Review.

---

## **10. Change Control and Documented Information**

* All controlled document updates occur through Pull Requests.
* Each Pull Request must reference its originating `Change Request` issue.
* Merge completion constitutes formal approval.
* Obsolete information remains preserved in repository history for audit traceability.

---

## **11. Records and Traceability**

* All Issues, Pull Requests, and comments are official QMS records.
* Closed issues remain permanently accessible in GitHub for audit purposes.
* Files under `/QMS/`, `/SOPs/`, `/WIs/`, and `/records/` constitute documented information.
* Manual exports per WI-QMS-10-02 ensure offline backup and long-term retention.

---

## **12. Continual Improvement Cycle**

At least quarterly (or during each Management Review):

1. Reassess context and interested parties.
2. Update risks, opportunities, and objectives.
3. Review CAPA status and verify effectiveness.
4. Identify and record new improvement opportunities.
5. Update relevant issues and QMS documents.
