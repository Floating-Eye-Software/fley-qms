# **Work Instruction: QMS Operations in GitHub**

**Document No.:** WI-QMS-09-01
**Title:** QMS Operations in GitHub
**Revision:** 1.0
**Effective Date:** [Insert Date]
**Approved by:** [Top Management]

---

## **1. Purpose**

To define how the organization operates its Quality Management System (QMS) within **GitHub**, ensuring leadership, planning, risk management, objectives, and continuous improvement are effectively implemented and traceable in compliance with **ISO 9001:2015 Clauses 4–10**.

---

## **2. Scope**

This WI applies to all QMS activities conducted in GitHub, including:

* Leadership and management review
* Quality planning and objective management
* Risk and opportunity management
* Change control and continual improvement
* Documentation and records management

It supports implementation of:

* **QMS-SOP-05 – Leadership**
* **QMS-SOP-06 – Planning**
* **QMS-SOP-08 – Risk & Opportunity Management**
* **QMS-SOP-04 – Change Control**
* **QMS-SOP-03 – Documented Information Control**

---

## **3. Responsibilities**

| Role                                    | Responsibilities                                                                                                                         |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Top Management**                      | Demonstrates leadership and commitment to the QMS, approves objectives, reviews QMS performance, and provides resources.                 |
| **Quality Manager / QMS Administrator** | Maintains repositories, Projects, and records in GitHub; coordinates Management Review; monitors risk and objectives.                    |
| **Process Owners**                      | Create and maintain Issues and Projects related to their processes; manage risks, opportunities, and objectives.                         |
| **All Employees**                       | Follow GitHub-based procedures, update Issues and Projects relevant to their responsibilities, and participate in continual improvement. |

---

## **4. GitHub Structure for the QMS**

| GitHub Area                          | Function in the QMS                                                                                                |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| **Repository (`QMS` or equivalent)** | Central home for all controlled QMS documentation (SOPs, WIs, templates, records).                                 |
| **Wiki**                             | User-facing documentation: SOPs, WIs, policies, reference materials.                                               |
| **Issues**                           | Records for risks, opportunities, nonconformities, corrective actions, improvements, and management review inputs. |
| **Pull Requests**                    | Formal mechanism for approving document or process changes (supports Change Control SOP).                          |
| **Projects**                         | Boards for tracking QMS objectives, risk actions, improvement projects, and management review tasks.               |
| **Discussions**                      | Collaborative communication and brainstorming (optional).                                                          |
| **Actions (CI/CD)**                  | Automation (e.g., backups, notifications, record archiving).                                                       |
| **Security**                         | Access control and audit of contributor permissions.                                                               |
| **Insights**                         | Analytics and history of participation, commits, and repository metrics.                                           |
| **Settings**                         | Configuration of branches, permissions, and repository policies.                                                   |

---

## **5. Procedure**

### **5.1 Leadership and QMS Governance**

1. **Quality Policy**

   * Stored in the Wiki under `/Quality-Policy`.
   * Reviewed annually via a GitHub Issue labeled `Management Review`.

2. **Roles & Responsibilities**

   * Documented in `/docs/OrganizationChart.md`.
   * Updated via Pull Request; approved by Top Management.

3. **Management Review**

   * Initiated as a GitHub Issue with label `Management Review`.
   * Links to:

     * Risk Register Project
     * Objectives Project
     * Audit results (Issues labeled `Audit`)
     * Feedback and customer satisfaction data
   * Minutes are captured in the Issue body or attached as a PDF.
   * On completion, the Issue is closed and archived under `/records/management-reviews/`.

---

### **5.2 Quality Planning and Objectives**

1. **Setting Objectives**

   * Each **Quality Objective** is created as a **GitHub Issue** labeled `Objective`.
   * The Issue includes:

     * Objective title and description
     * Metric / target value
     * Responsible owner
     * Due date and milestones
     * Links to related processes or SOPs

2. **Tracking Objectives**

   * Objectives are tracked using a **Project Board** named **“QMS Objectives”**, with columns:

     * Planned
     * In Progress
     * Achieved
     * Reviewed
   * Each Objective Issue is moved across columns as progress is made.

3. **Review**

   * Reviewed quarterly or during Management Review.
   * Objective effectiveness is noted in the corresponding Issue comments.

---

### **5.3 Risk and Opportunity Management**

1. **Creating Risks or Opportunities**

   * Each identified risk or opportunity is a **GitHub Issue** labeled `Risk` or `Opportunity`.
   * Include:

     * Description
     * Source (e.g., audit, feedback, process change)
     * Likelihood (Low / Medium / High)
     * Impact (Low / Medium / High)
     * Mitigation or enhancement plan
     * Owner and due date

2. **Tracking**

   * Risks and opportunities are maintained on a **Project Board** titled **“QMS Risk Register”**, with columns:

     * Identified
     * Action Planned
     * Mitigation in Progress
     * Closed / Controlled

3. **Actions**

   * Mitigation or improvement actions are tracked as linked Issues (labeled `Action` or `CAPA`).
   * Progress and closure are recorded in comments.

4. **Review**

   * Quality Manager reviews open risks quarterly.
   * Major items are included in the next Management Review.

5. **Records**

   * Closed risk Issues are retained indefinitely as QMS records.
   * Optionally exported quarterly to `/records/risk-register/YYYY-MM/`.

---

### **5.4 Change Control and Continual Improvement**

1. **Initiating a Change**

   * Changes to processes, documentation, or the QMS are made through **Pull Requests**.
   * Each PR must:

     * Reference the related Change Control Issue (label `Change Request`).
     * Describe the change and justification.
     * Be reviewed and approved by the Quality Manager and Process Owner.

2. **Approval**

   * Approval is documented through GitHub’s PR review system (electronic signature).
   * Merge = authorized implementation.

3. **Post-Implementation Review**

   * Linked Change Request Issue is updated with the implementation result and closed.

4. **Continual Improvement**

   * Improvements, suggestions, and CAPAs are logged as Issues labeled `Improvement`.
   * Reviewed and prioritized in the **QMS Improvement Project Board**.

---

### **5.5 Document Control and Record Retention**

* Follows the **Documented Information Control SOP (QMS-SOP-03)**.
* All controlled documents are stored in `/docs` or the Wiki.
* Obsolete revisions are archived automatically by Git version control.
* Records (closed Issues, PRs, and exports) are backed up regularly.

---

## **6. Backup and Record Export**

1. Use a GitHub Action or external tool to:

   * Export all open and closed Issues (including comments and attachments) quarterly.
   * Save under `/records/github-exports/YYYY-MM/`.
2. The export serves as the **official QMS record backup**.
3. For redundancy, repositories should also be cloned to an offline backup location.

---

## **7. References**

* ISO 9001:2015 – Clauses 4, 5, 6, 8, 9, 10
* QMS-SOP-03 – Documented Information Control
* QMS-SOP-05 – Leadership
* QMS-SOP-06 – Planning
* QMS-SOP-08 – Risk & Opportunity Management
* QMS-SOP-04 – Change Control

---

## **8. Revision History**

| Revision | Date   | Description of Change                                                                      | Approved By |
| -------- | ------ | ------------------------------------------------------------------------------------------ | ----------- |
| 1.0      | [Date] | Initial release – implements Leadership, Planning, and Risk-based QMS operations in GitHub | [Name]      |

---

## 💡 **Implementation Notes**

* GitHub repositories and Projects act as **living QMS records**, fully traceable through commits, Issues, and pull request history.
* This WI provides a complete implementation framework for ISO 9001 risk-based thinking, leadership accountability, and continual improvement — entirely within GitHub.
* If your organization later uses other tools (e.g., Confluence, Jira), this WI can reference external procedures while keeping GitHub as the master control system.
