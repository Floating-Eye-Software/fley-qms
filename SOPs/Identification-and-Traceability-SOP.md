# 🧾 **SOP: Identification and Traceability**

**Effective Date:** 2025-10-12
**Revision:** r2
**Title:** Identification and Traceability
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To establish and maintain a consistent method for identifying and tracing controlled documents, products, components, and records within the Quality Management System (QMS).
This ensures each item’s origin, revision, and status can be verified at any stage, supporting product quality, regulatory compliance, and audit readiness.

---

## **2. Scope**

This SOP applies to:

* All controlled documents managed in GitHub (SOPs, WIs, Templates, Policies, etc.)
* Electronic records, datasets, and configurations affecting quality or regulatory compliance
* Products, components, or materials requiring batch, lot, or configuration traceability
* Change records, CAPAs, and verification/validation outputs

---

## **3. Responsibilities**

| Role                                 | Responsibilities                                                                         |
| ------------------------------------ | ---------------------------------------------------------------------------------------- |
| **Quality Manager**                  | Ensures identification and traceability are maintained across all QMS elements.          |
| **Document Owners**                  | Maintain unique slugs and revision metadata for controlled documents.                    |
| **Process Owners**                   | Ensure traceability of records and data within their process area.                       |
| **Change Control Coordinator (CCC)** | Verifies that all controlled changes retain linkage between revisions, issues, and tags. |
| **All Employees**                    | Follow traceability requirements and report missing or inconsistent identifiers.         |

---

## **4. Definitions**

| Term             | Definition                                                                                                                                                                     |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Identifier**   | A unique tag, slug, or code that distinguishes a document, item, or record from all others.                                                                                    |
| **Slug**         | A standardized, unique identifier based on document type and title (e.g., `SOP_Identification-and-Traceability`). Used consistently in filenames and Git tags.                 |
| **Version**      | Any iteration of a document within the Git repository, including drafts and commits. Versions may or may not be approved.                                                      |
| **Revision**     | A formally approved and controlled version of a document, identified by a Git tag (e.g., `SOP_Identification-and-Traceability_r2`). Each revision supersedes the previous one. |
| **Traceability** | The ability to track the history, application, or location of an item through recorded identification.                                                                         |
| **Git Tag**      | A permanent, immutable label assigned to a specific commit in Git representing an approved revision.                                                                           |
| **Commit Hash**  | The cryptographic identifier (e.g., `a1b2c3d`) that uniquely represents a change event in Git history.                                                                         |

---

## **5. Procedure**

### **5.1 Document Identification**

All controlled documents must include the following header metadata:

```markdown
# SOP – Identification and Traceability
**Revision:** r2  
**Effective Date:** 2025-10-12  
**Approved By:** [Name]  
**Controlled Source:** https://github.com/<org>/<repo>/SOPs/SOP_Identification-and-Traceability.md
```

Each document shall:

* Use the **slug-based naming convention** defined in the Document Control SOP.
* Include a revision identifier in the header (`r#`).
* Be traceable to its corresponding Git tag (e.g., `SOP_Identification-and-Traceability_r2`).
* Maintain linkage to the related Pull Request and Change Request.

---

### **5.2 Product and Record Identification**

1. **Products and Materials**

   * Must be identified by unique batch, lot, or serial number.
   * Records must link this identifier to the corresponding production, inspection, and release documentation.

2. **Electronic Records**

   * Files, scripts, or configurations affecting quality must include identifiable metadata (e.g., version string, filename, or commit reference).
   * The Git commit hash provides the traceability record.

3. **Data Exports or Reports**

   * Must include the Git tag, revision number, and timestamp of generation to confirm source data integrity.

---

### **5.3 Revision and Tagging Control**

1. Every approved revision of a controlled document is associated with a Git tag matching the revision identifier, using the format:

   ```
   [Slug]_r#
   ```

   Example:

   ```
   SOP_Identification-and-Traceability_r2
   ```
2. Each Git tag must include:

   * Tag name (matching slug + revision)
   * Tagger (approver)
   * Date/time of approval
3. Tags serve as immutable references for auditors to retrieve specific approved revisions.

---

### **5.4 Linking Change Records**

Each controlled document or record must link to:

* The corresponding Change Request (Issue ID)
* The Pull Request implementing the change
* The Git tag representing the approved revision

Example reference section (at document end):

```
Change Request: CR-2025-014  
Pull Request: #45  
Approved Tag: SOP_Identification-and-Traceability_r2
```

---

### **5.5 Traceability Chain**

| Entity              | Identified By           | Traceability Link                               |
| ------------------- | ----------------------- | ----------------------------------------------- |
| Controlled Document | Slug, Revision, Git Tag | Linked to Change Request and Pull Request       |
| Product Batch       | Batch/Lot Number        | Linked to inspection and release records        |
| Configuration File  | Commit Hash             | Linked to software build or deployment          |
| CAPA Record         | CAPA ID                 | Linked to corrective actions and affected items |

---

### **5.6 Obsolete and Superseded Items**

1. Obsolete revisions are retained in the Git history and/or moved to an `/archive` directory.
2. Headers must include the note:

   > *“Obsolete – Superseded by SOP_Identification-and-Traceability_r3 (Effective 2025-11-01)”*
3. Obsolete revisions remain traceable but are not editable.

---

### **5.7 Verification and Audit**

1. During internal or external audits, traceability shall be demonstrated by showing:

   * The document header metadata
   * The Git tag and associated commit history
   * The linked Change Request and Pull Request records
2. The Change Control Coordinator verifies traceability quarterly or upon request by Quality Management.

---

## **6. References**

* SOP – Document Control
* SOP – Change Control
* WI – Git Version Control and Traceability
* ISO 9001:2015 §7.5.2–7.5.3
* ISO 13485:2016 §4.2.4, §7.5.9
* 21 CFR Part 11 – Electronic Records and Signatures

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                           | Approved By |
| -------- | ---------- | ------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating Git-based document and record traceability          | [Name]      |
| r2       | 2025-10-12 | Updated to align with slug-based identification and Git-native revision control | [Name]      |
