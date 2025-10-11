## 🧾 **SOP: Change Control**

**Document Number:** SOP-004
**Effective Date:** 2025-10-11
**Revision:** r1
**Title:** Change Control
**Controlled Source:** [GitHub Repository URL]

---

### **1. Purpose**

To ensure all changes affecting the Quality Management System (QMS), processes, documents, software, or products are identified, reviewed, approved, and implemented in a controlled manner that preserves compliance and traceability.

---

### **2. Scope**

This procedure applies to all planned and unplanned changes affecting:

* QMS processes and procedures
* Controlled documents and records
* Software or configuration repositories
* Equipment, materials, or production/service processes
* Organizational structure and responsibilities

---

### **3. Responsibilities**

| Role                                 | Responsibilities                                                                                                |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| **Process Owners**                   | Initiate, document, and assess the impact of proposed changes. Ensure appropriate review and implementation.    |
| **Change Control Coordinator (CCC)** | Manage and track change requests, ensure adherence to this SOP, and verify all records are properly maintained. |
| **Reviewers/Approvers**              | Evaluate changes for adequacy, impact, and compliance with regulatory and QMS requirements.                     |
| **Management**                       | Approve significant or cross-functional changes and allocate resources as needed.                               |
| **All Employees**                    | Follow approved changes and report unintended or unauthorized changes.                                          |

---

### **4. Definitions**

| Term                    | Definition                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------- |
| **Change Request (CR)** | A documented proposal for modification to any controlled element of the QMS.              |
| **Planned Change**      | A proposed, reviewed, and approved change prior to implementation.                        |
| **Unintended Change**   | An unapproved modification or deviation requiring immediate review and corrective action. |
| **Pull Request (PR)**   | A GitHub mechanism for submitting proposed changes for review and approval.               |
| **CAPA**                | Corrective and Preventive Action; used to manage unintended or adverse changes.           |

---

### **5. Procedure**

#### **5.1 Initiating a Change**

1. The initiator creates a **Change Request (CR)** using a GitHub Issue or designated form.
   Include:

   * Description and justification for the change
   * Impact assessment (on quality, compliance, or operations)
   * Related documents or systems affected
   * Proposed effective date

2. Assign a unique identifier to the CR (e.g., `CR-2025-014`).

3. Link the CR to associated Pull Requests or CAPA records where applicable.

---

#### **5.2 Review and Approval**

1. All changes must be reviewed before implementation to assess:

   * Potential risks or unintended consequences
   * Impact on product conformity or QMS integrity
   * Required updates to documentation or training

2. Reviews and approvals occur via **Pull Request review and approval in GitHub**, which serves as an authenticated digital signature.

3. The **CCC** ensures the PR includes:

   * Reference to the CR Issue number (`Fixes #XX`)
   * Updated metadata (revision, effective date, approver)
   * Git tag matching the revision after merge

---

#### **5.3 Implementation**

1. After approval, merge the PR into the `main` branch.
2. Create a Git tag corresponding to the approved revision (e.g., `SOP-004_r2`).
3. Notify relevant personnel of the approved change and its effective date.
4. Update training, documentation, or linked systems as required.

---

#### **5.4 Documentation and Records**

All changes must have the following records:

| Record Type        | Description                                     | Location                      |
| ------------------ | ----------------------------------------------- | ----------------------------- |
| Change Request     | Description, justification, and impact analysis | GitHub Issues or CR log       |
| Review & Approval  | Pull Request discussion and approval records    | GitHub                        |
| Implementation     | Git tag and merge commit                        | GitHub                        |
| Obsolete Documents | Archived or superseded files with tags          | Git history/archive directory |

---

#### **5.5 Control of Unintended Changes**

1. If an unintended change occurs (e.g., direct commit to `main` or unreviewed update), the issue must be:

   * Documented as a **CAPA** in GitHub Issues.
   * Reviewed to determine cause, impact, and corrective actions.
   * Linked to a corrective Pull Request implementing the fix.

2. Preventive actions may include updates to permissions, branch protection, or review requirements.

---

#### **5.6 Closure**

The CCC verifies that:

* All affected documents and records have been updated and tagged.
* The CR Issue is linked to all related PRs and Git tags.
* Evidence of approval and implementation is complete before closing the CR.

---

### **6. References**

* ISO 9001:2015, Clauses 6.3, 7.5, 8.1, 8.3.6, 8.5.6
* SOP – Document Control
* SOP – Identification and Traceability
* WI – GitHub Pull Request and Branch Management
* WI – Git Version Control and Traceability

---

### **7. Revision History**

| Revision | Date       | Description of Change                                                 | Approved By |
| -------- | ---------- | --------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating GitHub-based change tracking and approval | [Name]      |
