# **SOP – Document & Record Control (FLEY)**

**SOP Number:** SOP-DOC-001
**Title:** Document & Record Control
**Effective Date:** ____
**Owner:** Quality Manager
**Review Cycle:** Annual

---

## **1. Purpose**

This SOP establishes the requirements for creating, approving, revising, storing, distributing, and retiring controlled documents and records at Floating Eye Software (FLEY). It ensures compliance with:

* **21 CFR 820.40** – Document Controls
* **21 CFR 820.180** – Device History Record
* **21 CFR 820.30(j)** – Design History File
* **ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 7.3.10** – Documented information, design & development file

The SOP ensures all QMS, project-level, and regulatory documents and records are **controlled, accessible, traceable, and preserved appropriately**.

---

## **2. Scope**

This SOP applies to all FLEY documentation related to the QMS and regulated product development, including:

* **Controlled Documents:**

  * Standard Operating Procedures (SOPs)
  * Work Instructions (WIs)
  * Quality Manuals and Quality Plans (org-level and project-level)
  * Templates
  * Design & development documentation (requirements, risk analyses, design docs, traceability matrices)

* **Records:**

  * Completed Quality Plans (approved versions)
  * Test reports, validation reports
  * CAPA logs, audit logs, meeting minutes
  * Training records
  * CI/CD execution results linked as evidence

This SOP applies to all FLEY employees, contractors, and collaborators involved in QMS or product development activities.

---

## **3. Responsibilities**

| Role                                     | Responsibility                                                                                                   |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Quality Manager / QMS Owner**          | Maintains SOP; approves controlled documents; ensures proper classification of documents vs. records.            |
| **Project Manager**                      | Ensures project-level documents follow this SOP; ensures that completed plans and reports are stored as records. |
| **Developers / Team Members**            | Use only approved controlled documents; submit changes via PR; generate and file records of activities.          |
| **Privacy Officer / Compliance Officer** | Ensures regulatory content (e.g., GDPR) remains current and referenced correctly.                                |

---

## **4. Definitions**

* **Controlled Document** – A living document that defines processes, procedures, requirements, or specifications. It can be revised, but only under change control.
* **Record** – Evidence that a process has been carried out. Records are immutable after approval and may not be altered.
* **Uncontrolled Copy** – Any exported or printed version; reference must point to the controlled wiki version.
* **Document Owner** – The individual responsible for maintaining and ensuring a document is current.
* **Change Control** – Formal process for proposing, reviewing, approving, and implementing revisions.

---

## **5. Document & Record Lifecycle**

### **5.1 Creation**

1. Use approved templates from `redwitch.wiki/Templates/`.
2. Assign a **Document Owner**.
3. Create the new page or file in the appropriate wiki or repo folder:

   * `/SOPs/`, `/WIs/`, `/Plans/`, `/Project-Docs/` → Controlled Documents
   * `/Records/` → Records

### **5.2 Review & Approval**

1. Submit changes to controlled documents via **GitHub Pull Request (PR)**.
2. Reference related issues, milestones, or project boards in the PR.
3. Review by at least one approver (QM or Project Manager).
4. Merge PR only after approval → merged version becomes the **controlled document of record**.
5. Records (e.g., a completed Quality Plan, test report) are generated, approved, and then stored in `/Records/` without later modification.

### **5.3 Revision (Controlled Documents Only)**

1. Add/Update a **Revision History** table:

   ```markdown
   | Rev | Date       | Author      | Change Description |
   |-----|------------|-------------|--------------------|
   | 0.1 | 2025-09-25 | M. Lehotay  | Initial Draft      |
   ```

2. Update cross-references to milestones/issues as needed.

3. Retain prior versions in GitHub history.

### **5.4 Distribution**

* The **GitHub wiki is the single source of truth** for controlled documents.
* Exported/printed copies are uncontrolled and must cite the canonical wiki link.

### **5.5 Obsolete / Retired Documents**

* Mark retired controlled documents with **“Obsolete”** in the title.
* Add reason and retirement date.
* Preserve prior versions in GitHub history for traceability.

### **5.6 Records Management**

* Records are finalized versions of documents (e.g., “Quality Plan v1.0 – Approved 2025-01-15”).
* Once approved, records are stored in `/Records/` and **must not be modified**.
* If changes are required, a **new record** is generated (e.g., v1.1), leaving the old one intact.

---

## **6. Document Identification & Versioning**

* Controlled document IDs:

  * `SOP-XXX` for SOPs
  * `WI-XXX` for WIs
  * `PLAN-XXX` for Quality Plans

* Records are identified with document type, title, version, and approval date (e.g., `PLAN-QMS-001_v1.0_2025-01-15`).

* Revisions:

  * Draft/minor changes: 0.1 → 0.2
  * Approved major versions: 1.0 → 1.1 → 2.0

---

## **7. Access & Control**

* Wiki holds **controlled documents**.
* `/Records/` repo/folder holds **immutable records**.
* Pull request approval serves as the **formal review log**.
* GitHub history provides full traceability.
* Links to Issues, Milestones, and CI/CD reports establish **execution evidence**.

---

## **8. Record of Changes / Revision History**

* All controlled documents contain a **Revision History** table.
* All prior versions preserved in **GitHub history**.
* Records are immutable — once finalized, they are never changed.

---

## **9. References**

* 21 CFR 820.40 – Document Controls
* 21 CFR 820.180 – Device History Record
* 21 CFR 820.30(j) – Design History File
* ISO 13485:2016 – Clauses 4.2, 4.2.3, 4.2.4, 7.3.10
* SOP-Quality-Planning
* WI-GitHub-Project-Management

---

## **10. Appendices**

### Appendix A – GitHub Integration

* Controlled documents live in the **wiki**.
* Records live in the `/Records/` directory (or separate repo).
* All document PRs reference governing **milestones** and **issues**.
* The “Linkage to Execution” section on wiki pages connects to relevant milestones, boards, and issues.
* CI/CD and automated test reports are linked from Records.
