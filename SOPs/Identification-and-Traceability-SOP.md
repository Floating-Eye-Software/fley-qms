# 🧾 **SOP: Identification and Traceability**

**Revision:** r3
**Title:** Identification and Traceability
**Controlled Source:** [Organization Wiki or Repository URL]

---

## **1. Purpose**

To define consistent methods for identifying and tracing all controlled documents, records, products, and configurations within the Quality Management System (QMS), ensuring each item’s origin, revision, and status are verifiable at any time.
Traceability supports product quality, regulatory compliance, and audit readiness.

---

## **2. Scope**

This SOP applies to all QMS elements that require unique identification or traceability, including:

* Controlled documents (SOPs, WIs, forms, templates, policies)
* Quality records and logs (CAPA, Risk Register, Master Planning Log)
* Products, components, materials, and configurations
* Change records, approvals, and verification/validation outputs

It applies across all systems used to create, store, or publish QMS information.

---

## **3. Responsibilities**

| Role                                   | Responsibilities                                                                                                                           |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Quality Manager**                    | Ensures consistent application of identification and traceability practices across the QMS.                                                |
| **Document Control Coordinator (DCC)** | Maintains identifiers for controlled documents and ensures that current approved revisions are clearly published at the controlled source. |
| **Process Owners**                     | Maintain traceability of records and process data; ensure links between records, changes, and affected documents.                          |
| **Change Control Coordinator (CCC)**   | Verifies that identification and traceability are preserved through change implementation.                                                 |
| **All Personnel**                      | Follow traceability rules and report any missing or inconsistent identifiers.                                                              |

---

## **4. Definitions**

| Term                         | Definition                                                                                                                                |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Identifier**               | A unique code, name, or label that distinguishes a document, item, or record from all others.                                             |
| **Slug**                     | A standardized identifier derived from document type and title (e.g., `SOP_Identification-and-Traceability`).                             |
| **Revision (`r#`)**          | The approved and published iteration of a controlled document.                                                                            |
| **Version**                  | Any iteration within a repository or document system, including drafts.                                                                   |
| **Traceability**             | The ability to follow the history, application, or location of an item through recorded identification.                                   |
| **Controlled Source**        | The authoritative system location (e.g., wiki, controlled repository, DMS) that contains the current approved revision.                   |
| **Configuration Identifier** | A unique reference used to trace specific versions of digital assets, code, or datasets (e.g., checksum, timestamp, or configuration ID). |

---

## **5. Procedure**

### **5.1 Identification of Controlled Documents**

1. Each controlled document shall include the following header fields:

   * Title
   * Revision (e.g., `r3`)
   * Controlled Source link

2. Each document has a unique **slug** identifier (e.g., `SOP_Identification-and-Traceability`) that appears in:

   * The filename and/or title
   * The controlled source listing
   * Related change or approval records

3. The **current approved revision** is the version published at the **HEAD of the main branch** or its equivalent within the controlled source.

4. Document approval, effective date, and reviewer metadata are maintained by the document control system, not repeated within the document itself.

---

### **5.2 Identification of Records**

1. Each record entry or dataset must be traceable to:

   * A responsible owner
   * A date or timestamp
   * Related process, document, or change identifier

2. Records may be continuously updated, but each modification is logged automatically by the record system or repository to preserve traceability.

3. Records are identified by stable names or identifiers such as:

   * CAPA ID (e.g., `CAPA-2025-003`)
   * Change Request ID (e.g., `CR-2025-014`)
   * Log Entry Number or Timestamp

---

### **5.3 Identification of Products and Configurations**

1. Physical products, components, and materials shall be identified by unique lot, batch, or serial numbers.
2. Electronic configurations or digital assets shall include:

   * A configuration identifier (checksum, timestamp, or version string)
   * Reference to associated documentation or test records
3. Product and configuration identifiers must be linked to corresponding inspection, release, and change records to maintain full traceability.

---

### **5.4 Traceability Relationships**

Every controlled item should be traceable along a chain linking its origin, approval, and effect:

| Entity                    | Identified By     | Traceability Links                             |
| ------------------------- | ----------------- | ---------------------------------------------- |
| Controlled Document       | Slug + Revision   | Linked to Change Request, Approval Record      |
| Record (e.g., CAPA, Risk) | Record ID         | Linked to related documents or actions         |
| Product or Material       | Lot/Serial Number | Linked to inspection and release data          |
| Configuration Item        | Configuration ID  | Linked to associated tests and deployment logs |

These relationships ensure that any document, product, or record can be traced backward to its source and forward to its use or outcome.

---

### **5.5 Control of Obsolete and Superseded Items**

1. When a new revision of a controlled document is published, the previous revision becomes **obsolete**.
2. Obsolete documents are retained in the archive or historical view of the controlled source but clearly marked as superseded.
3. The header of an obsolete document should include a note such as:

   > *“Obsolete – Superseded by Revision r4 (Effective 2025-11-01)”*
4. Records are not obsolete; they remain part of the permanent QMS evidence base.

---

### **5.6 Verification of Traceability**

1. During audits or reviews, traceability shall be demonstrated by showing:

   * The identifier and revision visible in the document header.
   * The document’s location at the controlled source.
   * The corresponding approval or change record maintained in the system.
2. The DCC and CCC verify traceability quarterly or as part of management review.
3. Missing or broken traceability links must be corrected promptly through the Change Control or CAPA process.

---

## **6. References**

* SOP – Document Control
* SOP – Change Control
* ISO 9001:2015 §7.5.2–7.5.3
* ISO 13485:2016 §4.2.4, §7.5.9
* 21 CFR Part 11 – Electronic Records and Signatures

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                         | Approved By |
| -------- | ---------- | --------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release defining Git-based document and record traceability                           | [Name]      |
| r2       | 2025-10-12 | Aligned with slug-based identification and digital revision control                           | [Name]      |
| **r3**   | 2025-10-15 | Updated for system-maintained approvals, minimal header, and tool-agnostic traceability model | [Name]      |
