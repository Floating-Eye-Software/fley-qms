# 🧾 **SOP: Change Control**

**Effective Date:** 2025-10-12
**Revision:** r2
**Title:** Change Control
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To ensure all changes affecting the Quality Management System (QMS), processes, documents, software, or products are identified, reviewed, approved, implemented, and recorded in a controlled manner that maintains compliance, traceability, and quality integrity.

---

## **2. Scope**

This procedure applies to all planned and unplanned changes affecting:

* QMS processes, procedures, and controlled documents
* Software repositories, scripts, or configurations
* Equipment, materials, or production/service processes
* Organizational structure, roles, or responsibilities
* Any activity that could impact regulatory compliance or product quality

---

## **3. Responsibilities**

| Role                                 | Responsibilities                                                                                                                     |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Process Owners**                   | Initiate, document, and assess the impact of proposed changes. Ensure appropriate review and implementation.                         |
| **Change Control Coordinator (CCC)** | Manage and track change requests, verify adherence to this SOP, and ensure all change records are properly maintained and traceable. |
| **Reviewers/Approvers**              | Evaluate proposed changes for adequacy, risk, and compliance with QMS and regulatory requirements.                                   |
| **Quality Manager**                  | Oversees the change control process and ensures all records are complete and compliant.                                              |
| **All Employees**                    | Follow approved changes and report unintended or unauthorized modifications.                                                         |

---

## **4. Definitions**

| Term                    | Definition                                                                                                                                                 |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Change Request (CR)** | A documented proposal for modification to any controlled element of the QMS. Typically represented as a GitHub Issue.                                      |
| **Planned Change**      | A proposed, reviewed, and approved change implemented through the formal process.                                                                          |
| **Unintended Change**   | An unapproved or unscheduled modification requiring immediate review and corrective action.                                                                |
| **Pull Request (PR)**   | A GitHub mechanism for submitting proposed changes for review and approval. Serves as the formal approval record.                                          |
| **Slug**                | A standardized identifier combining the document type and title (e.g., `SOP_Change-Control`). Used consistently in filenames and Git tags.                 |
| **Revision**            | A formally approved and controlled version of a document, identified by a Git tag (e.g., `SOP_Change-Control_r2`). Each revision supersedes the prior one. |
| **Version**             | Any iteration of a document in the Git repository, including drafts or commits that are not yet approved.                                                  |
| **CAPA**                | Corrective and Preventive Action — a structured process for addressing unintended changes or adverse effects.                                              |

---

## **5. Procedure**

### **5.1 Initiating a Change**

1. The initiator creates a **Change Request (CR)** using a GitHub Issue or approved form that includes:

   * Description and justification for the change
   * Assessment of impact on quality, compliance, or operations
   * Related documents or systems affected
   * Proposed effective date

2. Assign a unique CR identifier (e.g., `CR-2025-014`).

3. Link the CR to any associated Pull Requests, CAPAs, or other relevant records.

---

### **5.2 Review and Approval**

1. All changes must be reviewed and approved prior to implementation to ensure:

   * Risks and unintended consequences are evaluated.
   * Impacts to product conformity or QMS integrity are identified.
   * Necessary updates to documentation or training are planned.

2. Review and approval occur via **Pull Request (PR)** in GitHub:

   * The PR serves as the formal change record.
   * Approvals provided through GitHub review count as digital signatures.

3. The **CCC** ensures that each PR includes:

   * A link to the associated CR Issue (e.g., `Fixes #XX`).
   * Updated document metadata (revision, effective date, approver).
   * A Git tag reflecting the approved revision (see 5.3).

---

### **5.3 Implementation**

1. Upon approval, the PR is merged into the `main` branch.
2. A **Git tag** is created for the approved revision, using the format:

   ```
   [Slug]_r#
   ```

   Example:

   ```
   SOP_Change-Control_r2
   ```
3. The tag represents the official approved revision of the document or configuration.
4. The effective date is updated in the document header.
5. Affected personnel are notified of the approved change, and related training or process updates are initiated.

---

### **5.4 Documentation and Records**

All changes must maintain a full audit trail containing the following records:

| Record Type          | Description                                            | Location                        |
| -------------------- | ------------------------------------------------------ | ------------------------------- |
| Change Request (CR)  | Description, justification, and impact analysis        | GitHub Issues or CR Register    |
| Review & Approval    | PR discussion, comments, and approval records          | GitHub Pull Request             |
| Implementation       | Merge commit and Git tag                               | GitHub Repository               |
| Superseded Documents | Archived or replaced revisions retained in Git history | Git history / archive directory |

---

### **5.5 Control of Unintended Changes**

1. If an unintended change occurs (e.g., direct commit to `main`, unauthorized update), it must be:

   * Documented as a **CAPA** in GitHub Issues.
   * Reviewed to assess impact, cause, and required corrective actions.
   * Linked to a corrective Pull Request implementing the approved fix.

2. Preventive actions may include:

   * Adjusting branch protection rules.
   * Enforcing required PR approvals.
   * Updating access control or review checklists.

---

### **5.6 Closure**

Before closing a Change Request, the **CCC** verifies that:

* All affected documents and records have been updated, approved, and tagged.
* The CR Issue is linked to all associated PRs and Git tags.
* Evidence of approval and implementation is complete and traceable.
* Superseded revisions are marked as obsolete but remain accessible via Git history.

---

## **6. References**

* ISO 9001:2015 — Clauses 6.3, 7.5, 8.1, 8.3.6, 8.5.6
* SOP – Document Control
* SOP – Identification and Traceability
* WI – GitHub Pull Request and Branch Management
* WI – Git Version Control and Traceability
* CAPA Procedure

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                                                      | Approved By |
| -------- | ---------- | -------------------------------------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating GitHub-based change tracking and approval                                                      | [Name]      |
| r2       | 2025-10-12 | Updated for slug-based identification and Git-native revision control; aligned with Document Control and Traceability SOPs | [Name]      |
