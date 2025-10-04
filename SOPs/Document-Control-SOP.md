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
