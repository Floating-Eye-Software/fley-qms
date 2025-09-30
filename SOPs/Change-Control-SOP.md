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
