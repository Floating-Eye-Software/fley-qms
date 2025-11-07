# **WI – Operate the QMS in GitHub – Single FLEY Board**

**Slug:** GitHub-QMS-Operations  
**Revision:** r2 **Draft**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Change-Control-SOP, Document-Control-SOP, Identification-and-Traceability-SOP, Quality-Planning-SOP, Leadership-SOP, Management-Review-SOP, Risk-and-Opportunity-Management-SOP, Project-Management-SOP, Design-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Operations.md  

---

## **1. Purpose**

To define how FLEY operates and maintains its **Quality Management System (QMS)** in GitHub using a single **Project (“FLEY QMS”)** that integrates both **Development** and **Operations** Issue Types and QMS Label categories.

This ensures:

* Unified management of QMS operations, improvement, and records.
* Full traceability of ISO 9001:2015 activities from creation to closure.
* Controlled, auditable digital records for all QMS functions.


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

## **5. FLEY QMS Workflow**

```
Backlog → In Progress → In Test → Closed
```

| Column      | Purpose                                     | Examples                         |
| ----------- | ------------------------------------------- | -------------------------------- |
| Backlog     | New or proposed records awaiting triage.    | New Risk, Objective, CAPA.       |
| In Progress | Active investigation or execution.          | Implementing corrective actions. |
| In Test     | Awaiting verification, review, or approval. | Effectiveness checks, PR review. |
| Closed      | Record verified complete.                   | MR approved, CAPA effective.     |

---

## **6. Issue Types**

| Type            | Definition                                                  | Use                                    |
| --------------- | ----------------------------------------------------------- | -------------------------------------- |
| **Development** | Creation or improvement of products, processes, or systems. | New document, automation, or template. |
| **Operations**  | Execution or monitoring of QMS processes and records.       | CAPA, Risk, Audit, Objective, MR.      |

---

## **7. QMS Label Definitions**

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

## **8. Project Views**

| View                  | Filter                                 | Purpose                                  |
| --------------------- | -------------------------------------- | ---------------------------------------- |
| Development           | `type:Development`                     | Track QMS framework creation or updates. |
| QMS Actions           | `label:"Management Review", Objective` | Plan and track leadership actions.       |
| Change Log            | `label:"Change Request", Change`       | Full lifecycle of changes.               |
| Risks & Opportunities | `label:Risk, Opportunity`              | Risk-based thinking dashboard.           |
| CAPAs                 | `label:CAPA`                           | Corrective/Preventive Actions.           |
| Audits                | `label:Audit`                          | Internal and external audits.            |
| Nonconformances       | `label:Nonconformance`                 | Track deviations.                        |
| Improvements          | `label:Improvement`                    | Continual improvement.                   |
| Missing Label         | `no:label -type:Development`           | Classification completeness check.       |

---

## **9. Issue Lifecycle Examples**

### **9.1 Change Request**

1. **Backlog:** Issue created with summary and justification.
2. **In Progress:** PR opened; work implemented.
3. **In Test:** Changes reviewed and verified.
4. **Closed:** PR merged and approved.

### **9.2 CAPA / Nonconformance**

1. **Backlog:** Nonconformance recorded (Operation Issue + `CAPA`).
2. **In Progress:** Root cause and actions defined and implemented.
3. **In Test:** Effectiveness review conducted.
4. **Closed:** Verified as effective; evidence attached.

### **9.3 Objective**

1. **Backlog:** Objective defined from MR or planning.
2. **In Progress:** Plan executed; data collected.
3. **In Test:** KPI results evaluated.
4. **Closed:** Objective achieved or redefined.

### **9.4 Audit or Management Review**

1. **Backlog:** Review scheduled or triggered.
2. **In Progress:** Execution and data collection.
3. **In Test:** Findings analyzed, actions assigned.
4. **Closed:** Records completed; outputs tracked as new issues.

---

## **10. Change Control and Approvals**

* Controlled documents updated through Pull Requests linked to `Change Request` issues.
* Merge approval = official change approval.
* Old versions retained in Git history.

---

## **11. Records and Evidence**

| Record                    | Location                           | Retention |
| ------------------------- | ---------------------------------- | --------- |
| QMS Issues (all)          | GitHub Project                     | Permanent |
| Management Review Minutes | `/records/management-reviews/`     | Permanent |
| Audit Reports & CAPAs     | `/records/`                        | Permanent |
| Repository Exports        | `/records/github-exports/YYYY-MM/` | 5 years   |

---

## **12. Continual Improvement**

Quarterly:

1. Review context and interested parties.
2. Evaluate risks, opportunities, and objectives.
3. Assess CAPA and improvement results.
4. Record new actions as Issues.

---

## **13. Integration and Traceability**

* All repos use same Issue Types and Label scheme.
* QMS Project serves as the traceability hub.
* Use “Linked Issues” for cross-repo connections.

---

## **14. Backup and Export**

Follow WI – GitHub-QMS-Setup (quarterly manual export until automated).

---

## **15. Legacy Note**

Old GitHub issue types (`Task`, `Feature`, `Bug`) are **deprecated** and replaced with standardized `Development` and `Operations`.
