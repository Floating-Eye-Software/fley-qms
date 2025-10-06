# **Work Instruction — Document Control in GitHub**

**WI ID:** WI-GIT-DC-001
**Project:** Red Witch
**References:** SOP-DOC-001 – Document & Record Control

---

## 1. **Purpose**

This Work Instruction defines *how* the Red Witch Project implements **document and record control** within GitHub repositories and wiki. It ensures compliance with:

* **SOP-DOC-001 – Document & Record Control**
* ISO 9001:2015 §7.5
* ISO 13485:2016 §4.2
* 21 CFR 820.40

It also specifies management of **external documents and licensing constraints**, ensuring that copyrighted standards (e.g., ISO, IEC) are **not stored in full** in GitHub.

---

## 2. **Scope**

Applies to all QMS and project documentation maintained in GitHub:

* SOPs, WIs, Plans, Quality Manual, Compliance pages (`redwitch.wiki`)
* Design docs, requirements, code, test artifacts (`redwitch`)
* Records of approvals, reviews, and sign-offs (via Pull Requests, Issues, Wiki edits)
* External document metadata summaries (no full copyrighted content unless licensed)

---

## 3. **Roles & Responsibilities**

| Role                | Responsibility                                                                 |
| ------------------- | ------------------------------------------------------------------------------ |
| **Author**          | Drafts or updates documents in feature branches; summarizes external docs.     |
| **Reviewer**        | Reviews PRs for compliance, formatting, and SOP conformance.                   |
| **Approver**        | Project Lead or Quality Representative; approves PRs before merge.             |
| **Repo Maintainer** | Ensures repo protections, access control, and compliance with branch policies. |
| **Document Owner**  | Maintains currency of documents; ensures external metadata is updated.         |

---

## 4. **Repositories & Folder Structure**

| Repo / Folder              | Contents                                               | Notes                                    |
| -------------------------- | ------------------------------------------------------ | ---------------------------------------- |
| `redwitch.wiki`            | SOPs, WIs, Plans, Quality Manual, Compliance pages     | Controlled documents                     |
| `redwitch`                 | Design docs, requirements, code, tests                 | Controlled project artifacts             |
| `/Records/`                | Finalized plans, reports, PMS logs, validation results | Immutable records                        |
| `/Templates/`              | Document templates                                     | Controlled documents                     |
| `/External-Docs-Metadata/` | Metadata and summaries of third-party documents        | No copyrighted full text unless licensed |

---

## 5. **Process**

### 5.1 Document Creation

1. Create new documents in the appropriate repo/folder.
2. Filename convention: `Title-With-Dashes.md`.
3. Include:

   * Title
   * Version/Revision History
   * References to SOPs, standards, or related issues

### 5.2 Version Control

1. Commit all changes via **feature branches**.
2. Branch naming:

   * `doc/<short-title>` → new documents
   * `update/<short-title>` → revisions
3. Submit **Pull Request (PR)** into `main`.

### 5.3 Review & Approval

1. At least **one Reviewer** per PR.
2. **Approver** (Project Lead / Quality Rep) must approve before merge.
3. PR approval history serves as **formal document approval record**.
4. PR may reference an Issue capturing rationale, CAPA linkage, or external document updates.

### 5.4 External Documents & Metadata

1. Store only **metadata and summaries** of external/copyrighted documents.
2. Include in metadata file:

   * Document ID
   * Title, author, year
   * Source / link
   * Type (Standard, Article, Report, Guidance)
   * Summary / Notes
   * License status
3. If license allows, full PDFs may be stored in a **restricted, access-controlled repo**.
4. Link metadata to internal documents (SOPs, WIs, Risk Assessments).

### 5.5 Publication & Access

1. Merged `redwitch.wiki` pages are **controlled documents**.
2. Merged `redwitch` repo artifacts are **controlled design/project documents**.
3. Repos are access-controlled; only authorized personnel may edit or approve.

### 5.6 Obsolete Documents

1. Mark superseded docs with **“Obsolete”** at the top.
2. Add link to replacement document.
3. Preserve full history in GitHub.

---

## 6. **Records**

* **Pull Requests** → approvals and change rationale
* **Issues** → change requests, CAPA linkage, external document updates
* **Git commit history** → version history
* **Wiki edit logs** → document change history
* **External metadata files** → evidence of external document review and summary

---

## 7. **Traceability & Audit**

* PR approvals, Issues, and Git commit logs provide full audit trail.
* External document summaries link to original source and internal references.
* Records are immutable; new versions are created for updates.
* Annual review by Document Owner to ensure currency and compliance.

---

## 8. **References**

* SOP-DOC-001 – Document & Record Control
* ISO 9001:2015 §7.5
* ISO 13485:2016 §4.2
* 21 CFR 820.40

---

## 9. **Revision History**

| Rev | Date       | Author | Change Description |
| --- | ---------- | ------ | ------------------ |
| 0.1 | YYYY-MM-DD | Name   | Initial Draft      |

---

# QP-07.05 — Document Control Procedure
**Title:** Control of Documents and Electronic Records
**Revision:** 1.0
**Effective Date:** 2025-10-04
**Process Owner:** Quality Manager

---

## 1. Purpose
To define the controls necessary to ensure that all documents and electronic records required by the Quality Management System (QMS) are reviewed, approved, distributed, and maintained using the GitHub platform as the system of record.
This procedure also defines how electronic reviews and approvals performed through GitHub Pull Requests (PRs) are recognized as compliant electronic signatures in accordance with ISO 9001:2015 and 21 CFR Part 11.

---

## 2. Scope
This procedure applies to:
- All controlled QMS documents (SOPs, work instructions, templates, forms, policies).
- Product-related documentation maintained in the *redwitch* repository.
- Software design, development, and verification records generated within GitHub.

---

## 3. References
- **ISO 9001:2015** – Clause 7.5 Documented Information
- **21 CFR Part 11** – Electronic Records; Electronic Signatures
- **QP-08.05.06** – Pull Request Change Control Procedure
- **SOP-07** – Configuration Management

---

## 4. Definitions
| Term | Definition |
|------|-------------|
| **Controlled Document** | Any document subject to review and approval prior to use. |
| **Pull Request (PR)** | GitHub mechanism used to propose, review, and approve a change. |
| **Electronic Signature** | GitHub user identity and approval action recorded within a PR, including username, timestamp, and intent (approve/reject). |
| **Main Branch** | Repository branch containing current, approved versions of controlled documents. |
| **Draft Branch** | Temporary branch used to prepare document updates prior to approval. |

---

## 5. Procedure

### 5.1 Document Creation and Identification
1. All controlled documents shall include:
   - Document ID, title, revision, effective date, and owner.
   - Unique filename and clear folder structure (e.g., `/SOPs/`, `/Policies/`).
2. New or revised documents are created on a dedicated branch (e.g., `draft/update-SOP07`).

---

### 5.2 Review and Approval
1. Drafts are submitted for review via a **Pull Request**.
2. The PR description shall include:
   - Purpose of change
   - Summary of revisions
   - Related issues, audits, or corrective actions
3. Reviewers (Process Owners or Quality Manager) provide feedback directly in the PR.
4. When reviewers select **“Approve”** in GitHub, the system records:
   - Authenticated user ID
   - Date and time stamp
   - Meaning of signature (“Approved for release”)
   These actions constitute *electronic signatures* under **21 CFR Part 11 §§ 11.50–11.70**.
5. After approval, the PR is merged into the `main` branch by an authorized user.
   - The merged version becomes the controlled document.
   - Prior versions remain retrievable in GitHub history.

---

### 5.3 Access and Distribution
1. The `main` branch of the `redwitch.wiki` repository represents the official QMS documentation available to all employees.
2. Read access is provided to all users; write access is restricted to authorized maintainers.
3. Automated notifications (or release tags) may be used to announce new document versions.

---

### 5.4 Change Control
1. Revisions follow the **Pull Request Change Control Procedure (QP-08.05.06)**.
2. Each change must be linked to the relevant issue, CAR, or improvement request.
3. GitHub commit history and PR metadata serve as the official revision log.

---

### 5.5 Document Retention and Archiving
1. Superseded versions are retained in GitHub history (immutable).
2. If required, an archival branch (e.g., `archive/*`) or export to PDF may be used for long-term retention.
3. Retention period: minimum three (3) years or as required by regulation or contract.

---

### 5.6 External Documents
External standards, customer specifications, and supplier documents referenced by the QMS are maintained in read-only form with current-version verification at least annually.

---

### 5.7 Security and Authorization
1. Only authorized users with GitHub accounts and two-factor authentication may access controlled repositories.
2. Branch protection rules enforce review and approval before merge.
3. Access rights are reviewed annually by the Quality Manager.

---

### 5.8 Electronic Records and Signatures (21 CFR Part 11)
1. GitHub user authentication, audit logs, and immutable commit records satisfy the requirements of **§11.10(a–k)** for secure electronic records.
2. Reviewer approvals recorded in Pull Requests meet the intent of **§11.50** and **§11.70** for electronic signatures, as they:
   - Are linked to a unique user ID and verified login.
   - Capture the printed name (GitHub username), date/time, and meaning (approval).
   - Are permanently associated with the record and cannot be repudiated.
3. Users are responsible for maintaining the security of their GitHub credentials.

---

### 5.9 Periodic Review
1. Each controlled document shall be reviewed at least once every 24 months or as specified by the Process Owner.
2. Reviews are conducted through the same PR approval workflow and recorded in GitHub.

---

## 6. Records
| Record | Storage | Retention |
|--------|----------|-----------|
| Approved documents | GitHub `main` branch | Active |
| Superseded versions | GitHub history | ≥ 3 years |
| PR approval history | GitHub PR database | Permanent |
| Access control list | GitHub admin console | Annual review |

---

## 7. Roles and Responsibilities
| Role | Responsibility |
|------|----------------|
| **Document Author** | Drafts new or revised documents. |
| **Reviewer / Approver** | Verifies adequacy and approves via PR. |
| **Quality Manager** | Ensures control system integrity and compliance. |
| **System Administrator** | Maintains access controls and branch protections. |

---

**End of Procedure**

---


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
* **ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 7.3.10** – Documented information, design & development files

The SOP ensures all QMS, project-level, and regulatory documents and records are **controlled, accessible, traceable, and preserved appropriately**.

<!--
Compliance
==========
Document Control SOP
ISO 9001 7.5, 4.4, 6.1
Controlled Document Registers, Version Histories, Retention Logs, Evidence of Risk Mitigation
==========
6 Planning
6.1 Actions to address risks and opportunities

7 Support
7.5 Documented information
7.5.1 General
7.5.2 Creating and updating
7.5.3 Control of documented information

4 Context of the organization
4.4 Quality management system and its processes
==========

4.4.2 To the extent necessary, the organization shall:
a) maintain documented information to support the operation of its processes;
b) retain documented information to have confidence that the processes are being carried out as
planned.

7.5 Documented information
7.5.1 General
The organization’s quality management system shall include:
a) documented information required by this International Standard;
b) documented information determined by the organization as being necessary for the effectiveness
of the quality management system.
NOTE The extent of documented information for a quality management system can differ from one
organization to another due to:
— the size of organization and its type of activities, processes, products and services;
— the complexity of processes and their interactions;
— the competence of persons.
7.5.2 Creating and updating
When creating and updating documented information, the organization shall ensure appropriate:
a) identification and description (e.g. a title, date, author, or reference number);
b) format (e.g. language, software version, graphics) and media (e.g. paper, electronic);
c) review and approval for suitability and adequacy.
7.5.3 Control of documented information
7.5.3.1 Documented information required by the quality management system and by this International
Standard shall be controlled to ensure:
a) it is available and suitable for use, where and when it is needed;
b) it is adequately protected (e.g. from loss of confidentiality, improper use, or loss of integrity).
7.5.3.2 For the control of documented information, the organization shall address the following
activities, as applicable:
a) distribution, access, retrieval and use;
b) storage and preservation, including preservation of legibility;
c) control of changes (e.g. version control);
d) retention and disposition.
Documented information of external origin determined by the organization to be necessary for the
planning and operation of the quality management system shall be identified as appropriate, and
be controlled.
Documented information retained as evidence of conformity shall be protected from unintended
alterations.
NOTE Access can imply a decision regarding the permission to view the documented information only, or
the permission and authority to view and change the documented information.

-->

---

## **2. Scope**

This SOP applies to all FLEY documentation related to QMS and regulated product development, including:

* **Controlled Documents:** SOPs, Work Instructions (WIs), Quality Manuals, Templates, Design & Development documents (requirements, risk analyses, design docs, traceability matrices).
* **Records:** Approved plans, test reports, validation results, CAPA logs, audit logs, meeting minutes, training records, CI/CD execution results.

It applies to all employees, contractors, and collaborators involved in QMS or product development activities.

---

## **3. Responsibilities**

| Role                                     | Responsibility                                                                                                      |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Quality Manager / QMS Owner**          | Maintains SOP; approves controlled documents; ensures proper classification of documents vs. records.               |
| **Project Manager**                      | Ensures project-level documents follow this SOP; ensures records are stored appropriately.                          |
| **Developers / Team Members**            | Use only approved controlled documents; submit changes via change control; generate and file records of activities. |
| **Privacy Officer / Compliance Officer** | Ensures regulatory content (e.g., GDPR, ISO standards) remains current and referenced correctly.                    |

---

## **4. Definitions**

* **Controlled Document:** Living document defining processes, procedures, requirements, or specifications; revised only under change control.
* **Record:** Evidence that a process has been carried out; immutable after approval.
* **Uncontrolled Copy:** Exported or printed version; reference must cite the controlled document.
* **Document Owner:** Individual responsible for maintaining currency of the document.
* **Change Control:** Formal process for proposing, reviewing, approving, and implementing revisions.
* **External Document:** Document authored by a third party (standards, journal articles, regulatory guidance, market reports).

---

## **5. Document & Record Lifecycle**

### **5.1 Creation**

1. Use approved templates.
2. Assign a **Document Owner**.
3. Store the new document in a controlled location accessible only to authorized personnel.

### **5.2 Review & Approval**

1. Submit changes through the formal change control process.
2. Review by at least one approver (QM or Project Manager).
3. Document approval must be recorded in a revision history log.
4. Once approved, the document becomes the **controlled version of record**.

### **5.3 Revision (Controlled Documents Only)**

1. Update **Revision History**:

   | Rev | Date       | Author | Change Description |
   | --- | ---------- | ------ | ------------------ |
   | 0.1 | YYYY-MM-DD | Name   | Initial Draft      |

2. Update cross-references to related documents, issues, or project milestones.

3. Retain prior versions for traceability.

### **5.4 Distribution**

* Controlled documents must be accessible to all authorized users.
* Exported or printed copies are **uncontrolled**; must reference the canonical controlled document.

### **5.5 Obsolete / Retired Documents**

* Mark as **“Obsolete”** with reason and retirement date.
* Preserve prior versions for audit purposes.

### **5.6 Records Management**

* Records are finalized, approved documents.
* Store in a secure, access-controlled repository.
* Records **must not be modified**; updates require a new version.

### **5.7 Handling External Documents**

1. **Scope:** Applies to all third-party references used in QMS, PMS, SRS, or design activities.

2. **Storage:**

   * Do not store copyrighted materials (e.g., ISO standards, paid journal PDFs) in shared repositories.
   * Open-access or licensed materials may be stored locally under controlled access.

3. **Metadata Requirements:** Maintain for each external document:

   | Field           | Description                                           |
   | --------------- | ----------------------------------------------------- |
   | Document ID     | Unique identifier                                     |
   | Title           | Official document title                               |
   | Source / Link   | URL or publisher reference                            |
   | Type            | Standard, Article, Market Report, Regulatory Guidance |
   | Summary / Notes | Internal paraphrased summary relevant to QMS/PMS      |
   | Local Copy      | Location if allowed; otherwise “None”                 |

4. **Internal Summaries:** Include only key findings relevant to product safety, design, or regulatory compliance.

5. **Integration:** Reference Document ID in controlled documents (SRS, RMF, SOPs, PMS logs).

6. **Review:** Annually, or upon new edition release, create a new Document ID.

7. **Audit Compliance:** Metadata, summaries, and links suffice for auditors; original document can be accessed externally if required.

---

## **6. Document Identification & Versioning**

* Controlled documents: `SOP-XXX`, `WI-XXX`, `PLAN-XXX`.
* Records: Document type, title, version, approval date (e.g., `PLAN-QMS-001_v1.0_YYYY-MM-DD`).
* Revisions: Draft/minor 0.1 → 0.2; Major 1.0 → 1.1 → 2.0.

---

## **7. Access & Control**

* Controlled documents: accessible to authorized users only.
* Records: stored in a secure, immutable repository.
* Revision history must be maintained for traceability.
* External documents are linked via metadata; PDFs stored only if permitted.

---

## **8. Audit & Review**

* All controlled documents and records are reviewed annually.
* Document Owners are responsible for review and ensuring updates are applied under change control.
* External documents reviewed annually; updates generate new entries.

---

## **9. References**

* 21 CFR 820.40 – Document Controls
* 21 CFR 820.180 – Device History Record
* 21 CFR 820.30(j) – Design History File
* ISO 13485:2016 – Clauses 4.2, 4.2.3, 4.2.4, 7.3.10
* SOP-Quality-Planning
* WI-Document Management

---

## **10. Revision History**

| Rev | Date       | Author | Change Description |
| --- | ---------- | ------ | ------------------ |
| 0.1 | YYYY-MM-DD | Name   | Initial Draft      |
