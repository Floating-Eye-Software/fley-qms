# 🧾 **SOP: Document Control**

**Effective Date:** [To be assigned]
**Revision:** r3
**Title:** Document Control
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To ensure all QMS documents and records are identified, maintained, and controlled so that:

* Only current, authorized revisions of controlled documents are used.
* Records accurately capture what has occurred in the QMS and remain auditable.
* Obsolete or draft material is not used unintentionally.

---

## **2. Scope**

Applies to **all documented information** within the QMS, including:

* Controlled documents: SOPs, WIs, templates, policies
* Records: logs, registers, the Master Planning Log (MPL), CAPA log, Risk Register
* All repositories, systems, and locations where such documents or records are created, stored, or used

> **Note:** Controlled documents require formal approval and revision control.
> Records are maintained in a structured, version-controlled system (e.g., Git) and updated by process owners without formal approval for each entry, but are subject to traceability, integrity, and periodic review.

---

## **3. Responsibilities**

| Role                                               | Responsibilities                                                                                                                                    |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Process Owners**                                 | Develop, maintain, and review documents; update records (MPL, CAPA log, Risk Register) as part of their process; ensure accuracy and traceability.  |
| **Quality Manager / Document Control Coordinator** | Maintain controlled repository, oversee document approval, revision, and access; ensure records are complete, traceable, and reviewed periodically. |
| **Management**                                     | Approve controlled documents that affect the QMS; support governance and resource allocation.                                                       |
| **All Employees**                                  | Use only approved and current revisions of controlled documents; update records as required; report discrepancies.                                  |

---

## **4. Definitions**

| Term                          | Definition                                                                                                                                      |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Controlled Document**       | A document maintained under version control, approved for use, and accessible to authorized personnel.                                          |
| **Record**                    | Information created, received, and maintained as evidence of activities or compliance; includes MPL, CAPA Log, Risk Register, audit records.    |
| **Slug**                      | A standardized, unique identifier based on document type and title (e.g., `SOP_Document-Control`). Used consistently in filenames and Git tags. |
| **Version / Revision**        | Version is any iteration of a document in Git; revision (`r#`) is a formally approved version.                                                  |
| **Git Tag**                   | Permanent marker identifying an approved revision in Git.                                                                                       |
| **Master Planning Log (MPL)** | A record capturing planning activities, decisions, and QMS changes; maintained in Markdown in the wiki and updated by process owners.           |

---

## **5. Procedure**

### **5.1 Creation and Approval of Controlled Documents**

1. Authoring is done by Process Owners or delegates.
2. Each document must:

   * Use an approved template and header
   * Have a unique **slug**
   * Be submitted via GitHub Pull Request (PR) for review and approval
3. Approved PRs are merged to `main` and tagged; this constitutes the official revision.

---

### **5.2 Review and Revision of Controlled Documents**

1. Periodic review (typically every two years) or upon regulatory/process change.
2. Revision proposed via PR per **Change Control SOP**.
3. Approved revisions tagged with the format:

   ```
   SOP_Document-Control_r3
   ```

---

### **5.3 Control of Records (MPL, CAPA Log, Risk Register, etc.)**

1. Records **document what has happened**, not what should happen.
2. **Updates are made by process owners** or designated personnel in real time.
3. Records must include:

   * Date of entry
   * Responsible owner
   * Links to related GitHub Issues, PRs, or Milestones
4. Records are **version-controlled** via Git and/or stored in the QMS Wiki.
5. Records are **reviewed periodically** (quarterly) for completeness, integrity, and alignment with Management Review.
6. Historical entries are **never deleted**; audit trails are preserved automatically by Git.

---

### **5.4 Control of Obsolete Documents**

1. Superseded or obsolete controlled documents remain in Git history but are not the default version.
2. Obsolete documents may be archived or marked `OBSOLETE`.
3. Records are never considered obsolete; they remain accessible for audit and traceability.

---

### **5.5 Availability and Access**

1. Controlled documents are available in read-only form to all relevant personnel.
2. Editing privileges are restricted to authorized personnel.
3. Records are updated in their structured repository by assigned owners.
4. Access permissions in GitHub ensure integrity and traceability.

---

### **5.6 Document Identification**

1. Controlled documents have a **slug**: `[Type]_[Descriptive-Title]`
   Examples:

   * `SOP_Document-Control.md`
   * `WI_Pull-Request-Workflow.md`
   * `TPL_Corrective-Action-Form.md`
2. Header metadata includes:

   ```markdown
   # SOP – Document Control  
   **Revision:** r3  
   **Effective Date:** 2025-10-14  
   **Approved By:** [Name / Title]  
   **Controlled Source:** https://github.com/[org]/[repo]/SOPs/SOP_Document-Control.md
   ```
3. **Revisions** identified by `r#` and Git tag.

---

### **5.7 Retention**

| Record/Document Type         | Location          | Retention                                                                     |
| ---------------------------- | ----------------- | ----------------------------------------------------------------------------- |
| Controlled Documents         | GitHub Repository | Current revision active; prior revisions retained indefinitely in Git history |
| Pull Request approvals       | GitHub            | Permanent                                                                     |
| Git tags / releases          | GitHub            | Permanent                                                                     |
| Metadata (headers)           | Within document   | Permanent                                                                     |
| MPL, CAPA Log, Risk Register | GitHub / Wiki     | Permanent; updated continuously by process owners                             |

---

## **6. References**

* ISO 9001:2015 – Clauses 7.5, 6.3, 8.5.6
* ISO 13485:2016 – Clauses 4–8, document & record control
* SOP – Change Control
* SOP – Identification and Traceability
* WI – GitHub Document Control
* WI – GitHub Pull Request and Branch Management
* WI – Git Version Control and Traceability

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                        | Approved By |
| -------- | ---------- | -------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial Git-based document control                                                           | [Name]      |
| r2       | 2025-10-12 | Updated to slug-based identification; clarified Version definition                           | [Name]      |
| r3       | 2025-10-14 | Added guidance for **records** (MPL, CAPA Log, Risk Register) and distinction from documents | [Name]      |
