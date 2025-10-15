# 🧾 **SOP: Document Control**

**Revision:** r4
**Title:** Document Control
**Controlled Source:** [Organization Wiki or Repository URL]

---

## **1. Purpose**

To ensure that all Quality Management System (QMS) documents and records are created, reviewed, approved, distributed, and maintained in a controlled manner that preserves their accuracy, integrity, and availability throughout their lifecycle.

This procedure defines how current, authorized versions are made available to users, how historical versions remain traceable, and how obsolete information is prevented from unintended use.

---

## **2. Scope**

This SOP applies to **all documented information** within the QMS, including:

* **Controlled documents:** Standard Operating Procedures (SOPs), Work Instructions (WIs), templates, policies, and controlled forms.
* **Records:** Logs, registers, the Master Planning Log (MPL), CAPA log, Risk Register, and other evidence of QMS activities.
* **All repositories, platforms, or wikis** used to store or publish QMS information.

> Controlled documents are subject to formal review and approval.
> Records are maintained by process owners as factual evidence of activities and may be updated continuously but remain under configuration and integrity control.

---

## **3. Responsibilities**

| Role                                                     | Responsibilities                                                                                                                                       |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Process Owners**                                       | Develop, maintain, and review documents within their process area; ensure records (MPL, CAPA log, Risk Register) are current, accurate, and traceable. |
| **Quality Manager / Document Control Coordinator (DCC)** | Administer the document control system; ensure appropriate approval, publication, access, and retention of documents and records.                      |
| **Management**                                           | Approve controlled documents that affect QMS governance and allocate resources for document and record management.                                     |
| **All Personnel**                                        | Use only current, approved documents published on the official wiki or repository; update records accurately and report discrepancies.                 |

---

## **4. Definitions**

| Term                    | Definition                                                                                                             |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Controlled Document** | A formally approved and version-controlled document made available for operational use.                                |
| **Record**              | Evidence of activities or compliance outcomes, maintained for traceability (e.g., logs, registers, meeting notes).     |
| **Slug**                | A standardized unique identifier for each document, typically combining type and title (e.g., `SOP_Document-Control`). |
| **Revision (`r#`)**     | The controlled, approved iteration of a document. Each revision supersedes the prior one.                              |
| **Version**             | Any iteration within the document repository, including drafts prior to approval.                                      |
| **Controlled Source**   | The authoritative location where the current approved revision is published (e.g., organization wiki or main branch).  |

---

## **5. Procedure**

### **5.1 Document Creation and Approval**

1. Documents are authored by Process Owners or designated contributors using approved templates and structure.
2. Each document must:

   * Include a **title**, **revision number**, and **controlled source link** in the header.
   * Have a unique **slug** for identification.
3. Documents undergo formal review and approval according to the Change Control SOP.
4. Once approved, the document is published to the **controlled source** (e.g., the wiki or main branch of the repository).
5. The published version represents the **current approved revision** available for use.

---

### **5.2 Review and Revision**

1. Controlled documents are reviewed:

   * At planned intervals (typically every two years), or
   * Whenever a process, regulatory, or organizational change occurs.
2. Proposed updates follow the Change Control process and are reviewed and approved prior to publication.
3. Each approved revision is uniquely identified by its **revision number** (`r#`) and published as the new active version.
4. Superseded revisions remain archived and traceable.

---

### **5.3 Control of Records**

1. Records document **what has occurred** within the QMS and are maintained as factual evidence of compliance.
2. Process owners update records in real time in their controlled repositories or logs.
3. Each record entry should include:

   * Date of entry
   * Responsible owner or contributor
   * Links to related changes, actions, or issues (if applicable)
4. Records are reviewed periodically (e.g., quarterly) to verify completeness and alignment with management review outputs.
5. Historical records are never deleted; version control or archival systems preserve their full audit trail.

---

### **5.4 Identification and Status**

1. Each controlled document includes in its header:

   * Title
   * Revision identifier (e.g., `r4`)
   * Controlled Source link (the official publication location)
2. Users can confirm they are viewing the current approved revision by verifying that the document is:

   * Published on the official wiki, or
   * Located at the **HEAD of the main branch** of the controlled repository.
3. Approval, effective date, and review metadata are maintained within the document control system (e.g., approval logs, PRs, or system history) and do not need to appear in the document itself.

> **Note:** The system’s change history, approval workflow, and tagging constitute the official record of review, approval, and effective date.

---

### **5.5 Control of Obsolete Documents**

1. When a new revision is approved, the previous revision becomes **obsolete**.
2. Obsolete documents remain available for reference but are clearly identified as superseded (e.g., moved to an archive area or labeled “Obsolete”).
3. Only the current approved revision is visible on the official wiki or active repository branch.
4. Records are never obsolete; they remain part of the permanent QMS evidence base.

---

### **5.6 Availability and Access**

1. The controlled source (wiki or main repository) serves as the **single source of truth** for all approved QMS documents.
2. All personnel have read-only access to controlled documents.
3. Editing rights are restricted to authorized roles (process owners, DCC, Quality Manager).
4. Access permissions and configuration controls ensure document integrity, traceability, and version authenticity.

---

### **5.7 Retention**

| Type                                     | Location                                                | Retention                                                         |
| ---------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------------------- |
| Controlled Documents                     | Controlled source (wiki or main repository)             | Current revision active; previous revisions archived indefinitely |
| Records (Logs, MPL, CAPA, Risk Register) | Controlled repositories or logs                         | Permanent                                                         |
| Approval and Change Metadata             | Within document control system (e.g., system logs, PRs) | Permanent                                                         |

---

## **6. References**

* ISO 9001:2015 — Clauses 7.5.2, 7.5.3
* ISO 13485:2016 — Clauses 4.2.4, 4.2.5
* SOP – Change Control
* SOP – Identification and Traceability
* WI – Documented Information and Repository Management

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                     | Approved By |
| -------- | ---------- | ----------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial Git-based document control procedure                                              | [Name]      |
| r2       | 2025-10-12 | Added slug-based identification and clarified version control                             | [Name]      |
| r3       | 2025-10-14 | Clarified distinction between controlled documents and records                            | [Name]      |
| **r4**   | 2025-10-15 | Streamlined for system-maintained approvals; minimal header; wiki-based publication model | [Name]      |
