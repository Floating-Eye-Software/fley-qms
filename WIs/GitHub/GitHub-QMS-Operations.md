# **WI – Operate the QMS in GitHub – Single FLEY Board**

**Slug:** GitHub-QMS-Operations  
**Revision:** r2 **Draft**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Change-Control-SOP, Document-Control-SOP, Identification-and-Traceability-SOP, Quality-Planning-SOP, Leadership-SOP, Management-Review-SOP, Risk-and-Opportunity-Management-SOP, Project-Management-SOP, Design-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Operations.md  

---

## **1. Purpose**

To define how the organization **operates and maintains its Quality Management System (QMS)** in GitHub using a single integrated Kanban board (**FLEY QMS**) that supports both **Development** and **Operation** issue types.

This ensures:

* Unified management of QMS setup, improvement, and records.
* Full traceability of ISO 9001:2015 activities from creation to closure.
* Controlled, auditable digital records for all QMS functions.

---

## **2. Scope**

Applies to all operational QMS activities and quality records managed in GitHub, including:

* CAPA and Nonconformances
* Risk and Opportunity management
* Change Control and Document Management
* Quality Objectives and Management Reviews
* Internal Audits and Continual Improvement

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* SOP – Leadership
* SOP – Management Review
* SOP – Risk and Opportunity Management
* WI – GitHub–QMS–Setup
* WI – GitHub–Change–Control
* WI – GitHub–Document–Control
* WI – GitHub–Version–Control

---

## **4. Responsibilities and Authorities**

| Role                            | Responsibilities                                             | Authority / Decision Rights               |
| ------------------------------- | ------------------------------------------------------------ | ----------------------------------------- |
| **Quality Manager / QMS Admin** | Maintain board, monitor issues, ensure records completeness. | Approve closure of QMS issues.            |
| **Top Management**              | Conduct Management Reviews, approve outputs.                 | Approve final records and policy changes. |
| **Process Owners**              | Manage assigned CAPAs, risks, and objectives.                | Approve closure of their process issues.  |
| **Contributors / SMEs**         | Provide data, evidence, and recommendations.                 | May open or comment on issues.            |

---

## **5. FLEY QMS Board Workflow**

**Columns**

```
Backlog → In Progress → In Test → Closed
```

| Column          | Description                            | Examples                                          |
| --------------- | -------------------------------------- | ------------------------------------------------- |
| **Backlog**     | New or proposed items awaiting triage. | New objective, identified risk, improvement idea. |
| **In Progress** | Active work or investigation.          | CAPA implementation, document update.             |
| **In Test**     | Awaiting verification or approval.     | Effectiveness check, PR review.                   |
| **Closed**      | Verified and complete.                 | CAPA effective, audit approved.                   |

---

## **6. Issue Types and QMS Roles**

| Issue Type      | Purpose                                                                       | Typical Usage                                              |
| --------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Development** | Used for creating, modifying, or configuring systems, documents, or software. | New WI, automation workflow, system setup.                 |
| **Operation**   | Used for QMS process records and actions under ISO 9001.                      | Audit, CAPA, Risk, Opportunity, Objective, Change Request. |

All issues of either type flow through the same four status columns.

---

## **7. Operational Record Labels**

| Label               | Description                                                 |
| ------------------- | ----------------------------------------------------------- |
| `Audit`             | Internal or supplier audit activity.                        |
| `CAPA`              | Corrective or Preventive Action, including Nonconformances. |
| `Change Request`    | Proposed modification to documents, procedures, or systems. |
| `Improvement`       | Opportunities or ideas for continual improvement.           |
| `Management Review` | Quarterly or ad hoc review of QMS effectiveness.            |
| `Objective`         | Measurable quality goal or KPI.                             |
| `Opportunity`       | Positive factor to enhance QMS or performance.              |
| `Risk`              | Identified threat to QMS performance or compliance.         |

Each label aligns with a GitHub Issue Template for metadata consistency.

---

## **8. Issue Lifecycle Examples**

### **8.1 Change Request**

1. **Backlog:** Issue created with summary and justification.
2. **In Progress:** PR opened; work implemented.
3. **In Test:** Changes reviewed and verified.
4. **Closed:** PR merged and approved.

### **8.2 CAPA / Nonconformance**

1. **Backlog:** Nonconformance recorded (Operation Issue + `CAPA`).
2. **In Progress:** Root cause and actions defined and implemented.
3. **In Test:** Effectiveness review conducted.
4. **Closed:** Verified as effective; evidence attached.

### **8.3 Objective**

1. **Backlog:** Objective defined from MR or planning.
2. **In Progress:** Plan executed; data collected.
3. **In Test:** KPI results evaluated.
4. **Closed:** Objective achieved or redefined.

### **8.4 Audit or Management Review**

1. **Backlog:** Review scheduled or triggered.
2. **In Progress:** Execution and data collection.
3. **In Test:** Findings analyzed, actions assigned.
4. **Closed:** Records completed; outputs tracked as new issues.

---

## **9. Change Control and Approvals**

* All QMS documents are updated via Pull Requests linked to their `Change Request` issue.
* PR merge = approval.
* Obsolete information remains in repo history for audit traceability.

---

## **10. Records and Evidence**

| Record                                   | Location                           | Retention |
| ---------------------------------------- | ---------------------------------- | --------- |
| All QMS Issues (Development + Operation) | GitHub Project                     | Permanent |
| Management Review Minutes                | `/records/management-reviews/`     | Permanent |
| Audit Reports and CAPAs                  | `/records/`                        | Permanent |
| Repository Exports                       | `/records/github-exports/YYYY-MM/` | 5 years   |

All comments, linked PRs, and attachments are part of the auditable record.

---

## **11. Continual Improvement Cycle**

Quarterly or as needed:

1. Review context and interested parties.
2. Evaluate risks, opportunities, and objectives.
3. Assess CAPA effectiveness and improvement results.
4. Identify new improvement or development actions.
5. Record all updates via new or linked Issues.

---

## **12. Integration with Other Repositories**

* Each product repository uses the same two issue types (`Development`, `Operation`) for consistency.
* Issues related to QMS compliance or actions are linked back to the FLEY QMS Project.
* This linkage maintains traceability between quality system and development work.

---

## **13. Backup and Export**

Follow the schedule defined in WI – GitHub-QMS-Setup.
Quarterly manual export until automation is implemented.

---

## **14. Legacy Note**

The previous Issue types (`Task`, `Feature`, `Bug`) are **deprecated** and replaced by `Development` and `Operation`.
Existing issues may retain historical type for reference but should not be reused.
