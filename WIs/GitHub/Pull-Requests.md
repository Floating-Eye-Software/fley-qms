# **WI – GitHub Pull Request Procedure**

**WI Number:** WI-DOC-PR-001
**Title:** GitHub Pull Request Procedure
**Effective Date:** ____
**Owner:** Project Manager / Developer Lead

---

## **1. Purpose**

To implement **SOP-DOC-002 – Change & Version Control**, this WI defines the standardized process for creating, reviewing, and merging pull requests (PRs) in GitHub repositories to ensure:

* Code quality
* Traceability to requirements
* Compliance with the project Quality Plan

---

## **2. Scope**

Applies to all contributors working on any GitHub repository managed under FLEY’s QMS.

---

## **3. Procedure**

### **3.1 Pre-Requisites**

* Link your work to a **GitHub Issue** or documented requirement.
* Ensure local changes pass **unit tests and linters**.
* Update **documentation** if relevant (wiki, README, API docs).

---

### **3.2 Creating a Pull Request**

1. Create a feature or bugfix branch from `main` (naming convention: `feature/<short-description>` or `bugfix/<short-description>`).
2. Commit changes with clear messages referencing the related issue (e.g., `Fixes #42: corrected input validation`).
3. Push the branch to GitHub.
4. Open a pull request against the `main` branch.
5. Complete the PR template (if available), including:

   * Summary of changes
   * Related issue(s)
   * Testing performed
   * Impact analysis (dependencies, risks, documentation updates)

---

### **3.3 Review Process**

* At least **one reviewer** approval is required (two for high-risk or regulatory-impact changes).
* Reviewers check:

  * Code quality and adherence to coding standards
  * Test coverage and passing results
  * Traceability to requirements or design inputs
  * Security, privacy, and GDPR impact (if applicable)
* Reviewers may request changes; **merging is not allowed until approval is granted**.

---

### **3.4 Merging the Pull Request**

* Confirm that CI/CD pipelines pass (tests, lint, build).
* Merge using **Squash and Merge** (preferred for cleaner history).
* Delete the feature branch after merge.
* Tag the release if the change corresponds to a milestone or version increment.

---

### **3.5 Post-Merge Activities**

* Update linked issue(s) or milestone status.
* Update project board (e.g., move task from *In Progress* → *Done*).
* Update traceability matrix if requirements or design inputs were implemented or changed.

---

## **4. Recordkeeping**

* PRs, approvals, and CI/CD test results in GitHub serve as **official records**.
* Merge commit references issue/requirement → provides **traceability evidence**.
* Any exported reports or snapshots are stored in `/Records/` if required for regulatory or audit purposes.

---

## **5. Responsibilities**

| Role               | Responsibility                                                                 |
| ------------------ | ------------------------------------------------------------------------------ |
| Developer          | Create PRs, link to requirements/issues, respond to review feedback            |
| Reviewer(s)        | Conduct review, ensure compliance with SOP-DOC-002, approve or request changes |
| Project Maintainer | Ensure PRs meet quality requirements before merging                            |

---

# QP-08.05.06 — Pull Request Change Control Procedure
**Title:** Control of Design, Development, and QMS Document Changes via Pull Requests
**Revision:** 1.0
**Effective Date:** 2025-10-04
**Process Owner:** Quality Manager / DevOps Lead

---

## 1. Purpose
This procedure defines how changes to controlled work outputs, designs, and quality management system (QMS) documents are proposed, reviewed, approved, and recorded using GitHub Pull Requests (PRs).
The goal is to ensure all changes are evaluated for adequacy, correctness, and impact before release or implementation.

---

## 2. Scope
This procedure applies to:
- All software design and development work performed under the QMS
- Controlled documents such as SOPs, policies, templates, and records stored in the GitHub Wiki or QMS repositories
- Any other item designated as controlled information under the QMS

---

## 3. References
- **ISO 9001:2015**
  - Clause 7.5 – Documented Information
  - Clause 8.3.6 – Design and Development Changes
  - Clause 8.5.6 – Control of Changes
  - Clause 9.1 – Performance Evaluation
- SOP-07 Configuration Management
- WI-03 Work Unit Design Output Template

---

## 4. Definitions
| Term | Definition |
|------|-------------|
| **Pull Request (PR)** | GitHub mechanism for proposing a change from one branch to another. |
| **Change Originator** | Individual initiating the PR. |
| **Reviewer / Approver** | Authorized person verifying and approving the change before merge. |
| **Controlled Repository** | Any GitHub repository or wiki folder subject to QMS change control. |

---

## 5. Procedure

### 5.1 Initiation
1. All proposed changes to controlled items must be initiated through a Pull Request.
2. The PR description must include:
   - Purpose and scope of the change
   - Reference to related issue, requirement, or audit finding
   - Summary of verification or testing performed
3. Each PR must reference any related **Work Unit Design Output Record**.

---

### 5.2 Review and Approval
1. Every PR must be reviewed by at least one qualified **Reviewer** not directly responsible for the original change.
2. Reviewers confirm that:
   - The change meets input requirements or objectives.
   - No adverse or unintended effects are introduced.
   - Verification or testing has been completed successfully.
   - Relevant documentation (code comments, wiki, SOPs) has been updated.
3. Review comments are resolved before approval.
4. Formal approval is granted by the reviewer using GitHub’s **Approve Pull Request** action.
5. Only individuals designated as approvers in the **CODEOWNERS** file or authority matrix may approve merges to controlled branches.

---

### 5.3 Merge and Record Retention
1. Approved PRs are merged into the target branch (e.g., `main`).
2. The merge commit, review comments, and linked issues form the permanent change record.
3. Artifacts such as CI/CD results or verification reports are linked within the PR.
4. All PRs remain stored in GitHub and constitute objective evidence of change control.

---

### 5.4 Post-Implementation Verification
1. After merge, automated or manual verification confirms intended performance.
2. If any issues arise, a new corrective-action issue is opened and linked to the PR.

---

### 5.5 Emergency / Hotfix Changes
1. Urgent changes required to restore service or integrity may be merged with expedited review.
2. The justification must be documented in the PR description.
3. A retrospective review and approval are performed within 5 working days.

---

### 5.6 Metrics and Monitoring
- Number of PRs created, reviewed, and approved
- Average lead time from PR creation to merge
- Frequency of re-opened issues or rollback events
- Review of metrics occurs during Management Review (ISO 9001 § 9.3)

---

### 5.7 Application to QMS and Quality Documents
1. This PR process also applies to controlled **QMS documents**, including:
   - Standard Operating Procedures (SOPs)
   - Work Instructions (WIs)
   - Policies, manuals, templates, and forms
   - Wiki-based QMS pages or Markdown documentation
2. Changes to QMS documentation must be initiated via a Pull Request that includes:
   - Summary of proposed change and justification
   - References to related audit findings, CARs/PARs, or improvement requests
3. Review and approval must be performed by the **Process Owner** and/or **Quality Manager** as defined in the authority matrix or CODEOWNERS file.
4. The GitHub PR approval and merge history constitute the formal record of review and approval required by ISO 9001 § 7.5.2.
5. When merged:
   - The updated version becomes the current controlled document.
   - Previous versions remain accessible via GitHub history.
   - The merge commit or PR link may be noted in the QMS revision log if required.
6. Major procedural or policy changes that affect multiple processes should be referenced in a **QMS Change Notice** or **Management Review** record.

---

## 6. Records
| Record | Storage Location | Retention |
|--------|------------------|-----------|
| Pull Request (including approvals, comments, merge history) | GitHub repository | Permanent |
| Linked Work Unit Design Output Record | `/qms/design-outputs/` | 3 years minimum |
| CI/CD Verification Logs | Build system | 1 year minimum |

---

## 7. Roles and Responsibilities
| Role | Responsibility |
|------|----------------|
| **Change Originator** | Initiates PR, ensures completeness of description and evidence. |
| **Reviewer / Approver** | Reviews and approves changes for adequacy and impact. |
| **Quality Manager** | Audits PR process and ensures documentation integrity. |
| **DevOps Lead** | Maintains branch protection, CODEOWNERS, and access control settings. |

---

## 8. Related Documents
- WI-03 Work Unit Design Output Template
- SOP-07 Configuration Management
- QP-08.07 Corrective and Preventive Action Procedure

---

**End of Procedure**

---

# **SOP – Change & Version Control (FLEY)**

**SOP Number:** SOP-DOC-002
**Title:** Change & Version Control
**Effective Date:** ____
**Owner:** Quality Manager
**Review Cycle:** Annual

---

## **1. Purpose**

This SOP defines the policies and responsibilities for managing changes and version control of:

* Controlled documents (SOPs, WIs, Plans, Templates, Project Documentation)
* Records (approved plans, test reports, validation evidence, CI/CD logs)
* Software source code (Red Witch project repository)

It ensures that all changes are:

* Reviewed and approved before implementation
* Traceable to requirements, milestones, or issues
* Preserved as an immutable record when finalized

This SOP ensures compliance with:

* 21 CFR 820.40 – Document Controls
* 21 CFR 820.30(j) – Design History File
* ISO 13485:2016 Clauses 4.2.3, 4.2.4, 7.3.10

<!--
Compliance
==========
Change Control SOP
ISO 9001 6.3, 8.1, 7.5
Change Requests, Impact Assessments, Approval Records, Updated Procedures, Revision Logs
==========
6 Planning
6.3 Planning of changes

8 Operation
8.1 Operational planning and control

7 Support
7.5 Documented information
7.5.1 General
7.5.2 Creating and updating
7.5.3 Control of documented information
==========

6 Planning
6.3 Planning of changes
When the organization determines the need for changes to the quality management system, the changes
shall be carried out in a planned manner (see 4.4).
The organization shall consider:
a) the purpose of the changes and their potential consequences;
b) the integrity of the quality management system;
c) the availability of resources;
d) the allocation or reallocation of responsibilities and authorities.


-->

---

## **2. Scope**

Applies to all FLEY employees, contractors, and collaborators making changes to controlled documents, records, or source code in the Red Witch project.

---

## **3. Responsibilities**

| Role                            | Responsibility                                                                                       |
| ------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **Quality Manager / QMS Owner** | Approve changes to controlled documents; ensure versioning and change control compliance.            |
| **Project Manager**             | Ensure project-level changes follow SOP; confirm traceability to requirements/milestones.            |
| **Developers / Team Members**   | Submit changes via PRs or document revisions; link changes to issues, plans, or design inputs.       |
| **Reviewer(s)**                 | Review, approve, or reject changes; ensure compliance with SOPs, coding standards, and traceability. |

---

## **4. Definitions**

* **Change Control:** Process to propose, review, approve, and implement changes.
* **Revision / Version:** Sequential identifier for a document or software release (e.g., 0.1 → 1.0 → 1.1).
* **Controlled Document:** Living document defining procedures, requirements, or specifications.
* **Record:** Evidence that an action has been completed; immutable once approved.
* **Pull Request (PR):** GitHub mechanism for proposing code changes subject to review and approval.

---

## **5. Change & Version Control Policy**

1. **All changes to controlled documents or code must follow this SOP.**
2. **Documents:**

   * Revision number updated with each change.
   * GitHub wiki tracks version history; major revisions labeled in the Revision History table.
3. **Records:**

   * Once finalized/approved, records are immutable.
   * New records created for subsequent updates (e.g., Quality Plan v1.1).
4. **Source Code:**

   * Changes implemented via feature/bugfix branches, merged only after PR approval.
   * Commit messages must reference GitHub issues, requirements, or design inputs.
5. **Traceability:**

   * Each change must link to an issue, milestone, or plan.
   * Evidence (CI/CD test reports, approval records) retained in `/Records/`.

---

## **6. Versioning Rules**

* **Documents:** Major revisions (1.0, 2.0), minor revisions (1.1, 1.2)
* **Records:** Use version + approval date in filename (e.g., `PLAN-QMS-001_v1.0_2025-09-30`)
* **Software:** Semantic versioning (MAJOR.MINOR.PATCH), tied to milestones/releases

---

## **7. Approval & Review**

* Controlled documents or source code changes require review/approval prior to implementation.
* PR approval or documented review in the wiki serves as the official record of approval.
* High-risk or regulatory-impact changes may require additional sign-off by the Quality Manager.

---

## **8. Recordkeeping**

* GitHub PRs, commit history, CI/CD test results → source code records
* Wiki version history → document change records
* `/Records/` folder → immutable evidence (approved plans, reports, test results)
