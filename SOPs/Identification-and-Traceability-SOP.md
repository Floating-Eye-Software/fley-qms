## 🧾 **SOP: Identification and Traceability**

**Document Number:** SOP-006
**Effective Date:** 2025-10-11
**Revision:** r1
**Title:** Identification and Traceability
**Controlled Source:** [GitHub Repository URL]

---

### **1. Purpose**

To establish and maintain a consistent method for identifying and tracing controlled documents, products, components, and records within the Quality Management System (QMS).
This ensures each item’s origin, version, and status can be verified at any stage, supporting product quality, regulatory compliance, and audit readiness.

---

### **2. Scope**

This SOP applies to:

* All controlled documents managed in GitHub (SOPs, WIs, Forms, Templates, Policies, etc.)
* Electronic records, datasets, and configurations affecting quality or regulatory compliance
* Products, components, or materials requiring batch, lot, or configuration traceability
* Change records, CAPAs, and verification/validation outputs

---

### **3. Responsibilities**

| Role                                 | Responsibilities                                                                         |
| ------------------------------------ | ---------------------------------------------------------------------------------------- |
| **Quality Manager**                  | Ensures identification and traceability are maintained across all QMS elements.          |
| **Document Owners**                  | Maintain unique identifiers and revision metadata for controlled files.                  |
| **Process Owners**                   | Ensure traceability of records and data within their process area.                       |
| **Change Control Coordinator (CCC)** | Verifies that all controlled changes retain linkage between revisions, issues, and tags. |
| **All Employees**                    | Follow traceability requirements and report missing or inconsistent identifiers.         |

---

### **4. Definitions**

| Term             | Definition                                                                                             |
| ---------------- | ------------------------------------------------------------------------------------------------------ |
| **Identifier**   | A unique tag, code, or number that distinguishes a document, item, or record from all others.          |
| **Traceability** | The ability to track the history, application, or location of an item through recorded identification. |
| **Git Tag**      | A permanent, immutable label assigned to a specific commit in Git representing an approved revision.   |
| **Commit Hash**  | The cryptographic identifier (e.g., `a1b2c3d`) that uniquely represents a change event in Git history. |

---

### **5. Procedure**

#### **5.1 Document Identification**

All controlled documents must include the following header metadata:

```markdown
# SOP-006 – Identification and Traceability
**Revision:** r1  
**Effective Date:** 2025-10-11  
**Approved By:** [Name]  
**Controlled Source:** https://github.com/<org>/<repo>/path/to/SOP-006_Identification-and-Traceability.md
```

Each document shall:

* Use the defined numbering convention from SOP-001 (Document Control)
* Include a revision number (`r#`)
* Reference the official Git tag (`SOP-006_r1`)
* Be traceable to its corresponding PR and Change Request

---

#### **5.2 Product and Record Identification**

1. **Products and Materials**

   * Must be identified by unique batch, lot, or serial number.
   * Records must link this identifier to the corresponding production, inspection, and release documentation.

2. **Electronic Records**

   * Files, scripts, or configurations affecting quality must include version identifiers in filenames or metadata.
   * The Git commit hash provides the traceability record.

3. **Data Exports or Reports**

   * Must include the Git tag, revision number, and timestamp of generation.

---

#### **5.3 Revision and Tagging Control**

1. Every approved revision is associated with a Git tag matching the revision identifier (e.g., `SOP-006_r2`).
2. The Git tag includes:

   * Tag name (e.g., `SOP-006_r1`)
   * Tagger (approver)
   * Date/time of approval
3. Tags serve as immutable references for auditors to retrieve specific approved versions.

---

#### **5.4 Linking Change Records**

Each controlled document or record must link to:

* The corresponding Change Request (Issue ID)
* The Pull Request implementing the change
* The Git tag representing the approved version

Example reference section (at document end):

```
Change Request: CR-2025-014
Pull Request: #45
Approved Tag: SOP-006_r1
```

---

#### **5.5 Traceability Chain**

| Entity              | Identified By                      | Traceability Link                               |
| ------------------- | ---------------------------------- | ----------------------------------------------- |
| Controlled Document | Document Number, Revision, Git Tag | Linked to CR and PR                             |
| Product Batch       | Batch/Lot Number                   | Linked to inspection and release records        |
| Configuration File  | Commit Hash                        | Linked to software build or deployment          |
| CAPA Record         | CAPA ID                            | Linked to corrective actions and affected items |

---

#### **5.6 Obsolete and Superseded Items**

1. Obsolete versions are maintained in Git history and/or moved to an `/archive` directory.
2. Headers must include the note:

   > *“Obsolete – Superseded by SOP-006_r2 (Effective 2025-11-01)”*
3. Obsolete versions remain traceable but are not editable.

---

#### **5.7 Verification and Audit**

1. During internal or external audits, traceability can be demonstrated by showing:

   * The document header
   * The Git tag and commit history
   * The linked Issue and PR records
2. The CCC verifies traceability quarterly or when requested by Quality Management.

---

### **6. References**

* SOP – Document Control
* SOP – Change Control
* WI – Git Version Control and Traceability
* ISO 9001:2015 §7.5.2–7.5.3
* ISO 13485:2016 §4.2.4, §7.5.9
* 21 CFR Part 11 – Electronic Records and Signatures

---

### **7. Revision History**

| Revision | Date       | Description of Change                                                  | Approved By |
| -------- | ---------- | ---------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating Git-based document and record traceability | [Name]      |
