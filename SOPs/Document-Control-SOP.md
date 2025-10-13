# 🧾 **SOP: Document Control**

**Effective Date:** [To be assigned]
**Revision:** r2
**Title:** Document Control
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To ensure all QMS documents are identified, approved, maintained, and controlled so that only current, authorized revisions are available for use and obsolete or draft material is not used unintentionally.

---

## **2. Scope**

This procedure applies to all documented information that forms part of the Quality Management System (QMS), including policies, procedures, work instructions, templates, and records, regardless of medium or format.
It covers all repositories, systems, and locations where such documents are created, stored, or used.

---

## **3. Responsibilities**

| Role                                               | Responsibilities                                                                                                                             |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Process Owners**                                 | Develop, maintain, and review documents related to their processes. Ensure accuracy, relevance, and compliance with applicable requirements. |
| **Quality Manager / Document Control Coordinator** | Maintain the controlled repository, ensure appropriate document identification, revision control, approval, and access management.           |
| **Management**                                     | Approve new or revised documents that affect the QMS.                                                                                        |
| **All Employees**                                  | Use only approved and current revisions of controlled documents. Report obsolete or inconsistent content.                                    |

---

## **4. Definitions**

| Term                    | Definition                                                                                                                                                      |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Controlled Document** | A document maintained under version control, approved for use, and accessible to authorized personnel.                                                          |
| **Slug**                | A standardized, unique identifier based on document type and title (e.g., `SOP_Document-Control`). Used consistently in filenames and Git tags.                 |
| **Version**             | Any iteration of a document within the Git repository, including drafts and commits. Versions may or may not be approved.                                       |
| **Revision**            | A formally approved and controlled version of a document, identified by a Git tag (e.g., `SOP_Document-Control_r2`). Each revision supersedes the previous one. |
| **Git Tag**             | A permanent marker in Git identifying an approved revision of a controlled document.                                                                            |
| **GitHub Repository**   | The official controlled source of QMS documents and their full revision history.                                                                                |

---

## **5. Procedure**

### **5.1 Creation and Approval of Documents**

1. New documents shall be authored by the responsible Process Owner or delegate.
2. Each new document shall:

   * Use the approved template and metadata header.
   * Be assigned a unique **slug** (see Section 5.6).
   * Be submitted via a GitHub Pull Request (PR) for review and approval.
3. Documents must be **reviewed and approved** prior to merging to the `main` branch.

   * Approval is provided through GitHub PR approval.
   * The merged and tagged revision represents the official approved document.

---

### **5.2 Review and Revision**

1. Controlled documents shall be reviewed periodically—typically every two years—or sooner if a change in process, regulation, or requirement occurs.
2. Revisions are proposed via Pull Request in accordance with the **Change Control SOP**.
3. Upon approval and merge, a new Git tag shall be created to identify the approved revision, using the format:

   ```
   SOP_Document-Control_r2
   ```

   where the **slug** identifies the document and the **r#** identifies the approved revision.

---

### **5.3 Control of Obsolete Documents**

1. Superseded or obsolete revisions remain in the repository’s history but are not accessible as the default revision.
2. Obsolete documents may be moved to an `/archive/` directory or clearly marked as **OBSOLETE** in the file header.
3. Only the **main branch** and latest Git tag represent current, controlled revisions.

---

### **5.4 Availability and Access**

1. Approved documents are available in read-only form through the GitHub repository or published GitHub Pages site.
2. Editing rights are restricted to authorized personnel with designated access.
3. Public or internal read access is determined by management and repository settings.

---

### **5.5 Control of External Documents**

Documents of external origin that are necessary for the QMS (e.g., standards, supplier manuals) shall be:

* Listed in an external document register or referenced within applicable SOPs.
* Verified as current and relevant.
* Stored or linked within the controlled repository or document management system.

---

### **5.6 Document Identification**

1. Each controlled document shall have a **unique slug** constructed as:

   ```
   [Type]_[Descriptive-Title]
   ```

   Examples:

   * `SOP_Document-Control.md`
   * `WI_Pull-Request-Workflow.md`
   * `TPL_Corrective-Action-Form.md`
2. The document header shall include the following metadata fields:

   ```markdown
   # SOP – Document Control  
   **Revision:** r2  
   **Effective Date:** 2025-10-12  
   **Approved By:** [Name / Title]  
   **Controlled Source:** https://github.com/[org]/[repo]/SOPs/SOP_Document-Control.md  
   ```
3. **Revisions** are identified using the `r#` notation, matching the Git tag (e.g., `SOP_Document-Control_r2`).
4. The **GitHub repository** and associated **Git tags** constitute the single source of truth for document identification and revision history.

---

### **5.7 Records and Retention**

| Record Type              | Location          | Retention                                                                      |
| ------------------------ | ----------------- | ------------------------------------------------------------------------------ |
| Document files           | GitHub Repository | Current revision: active; prior revisions retained indefinitely in Git history |
| Pull Request approvals   | GitHub            | Permanent                                                                      |
| Git tags and releases    | GitHub            | Permanent                                                                      |
| Metadata (header fields) | Within document   | Permanent                                                                      |

---

## **6. References**

* ISO 9001:2015 – Clauses 7.5, 6.3, and 8.5.6
* SOP – Change Control
* SOP – Identification and Traceability
* WI – GitHub Document Control
* WI – GitHub Pull Request and Branch Management
* WI – Git Version Control and Traceability

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                        | Approved By |
| -------- | ---------- | -------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating Git-based document control                                       | [Name]      |
| r2       | 2025-10-12 | Updated to slug-based identification; clarified Version definition; removed document numbers | [Name]      |
