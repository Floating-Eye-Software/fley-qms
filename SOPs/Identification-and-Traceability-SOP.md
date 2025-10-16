# **SOP – Identification and Traceability**

**Slug:** Identification-and-Traceability-SOP
**Revision:** r1
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Identification-and-Traceability-SOP
**Process Owner:** Quality Manager
**Effective Date:** [YYYY-MM-DD]

---

## **1. Purpose**

To define consistent methods for identifying and tracing all controlled documents, records, products, and configurations within the Quality Management System (QMS).

This SOP ensures that each item’s origin, revision, and status are verifiable at any time, supporting **product quality, regulatory compliance, and audit readiness**.

---

## **2. Scope**

This SOP applies to all QMS elements requiring **unique identification or traceability**, including:

* Controlled documents (SOPs, WIs, forms, templates, policies)
* Quality records and logs (CAPA, Risk Register, Master Planning Log)
* Products, components, materials, and configurations
* Change records, approvals, and verification/validation outputs

It applies across all systems and repositories used to create, store, or publish QMS information.

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* ISO 9001:2015 — Clauses 7.5.2–7.5.3
* ISO 13485:2016 — Clauses 4.2.4, 7.5.9
* 21 CFR Part 11 — Electronic Records and Signatures

---

## **4. Definitions**

| Term                         | Definition                                                                                                        |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Identifier**               | A unique code, name, or label distinguishing a document, record, product, or configuration.                       |
| **Slug**                     | A standardized identifier derived from document type and title (e.g., `SOP_Identification-and-Traceability`).     |
| **Revision (`r#`)**          | The approved and published iteration of a controlled document.                                                    |
| **Version**                  | Any iteration or draft recorded prior to formal approval.                                                         |
| **Traceability**             | The ability to follow the history, application, or location of an item through recorded identification.           |
| **Controlled Source**        | The authoritative system location containing the current approved revision (e.g., DMS, wiki, repository).         |
| **Configuration Identifier** | A unique reference used to trace digital assets, code, or datasets (e.g., checksum, timestamp, configuration ID). |

---

## **5. Resources**

* Document and record repository (controlled source)
* Approved templates and forms
* Change Control workflow
* Access control and permissions management
* Trained personnel responsible for document and record handling

---

## **6. Responsibilities and Authorities**

| Role                                   | Responsibilities                                                                                                      | Authorities                                                         |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Quality Manager**                    | Ensures consistent identification and traceability practices across the QMS.                                          | Authorizes process improvements or updates to identification rules. |
| **Document Control Coordinator (DCC)** | Maintains identifiers for controlled documents and ensures approved revisions are published at the controlled source. | Maintains document registry and approves document metadata.         |
| **Process Owners**                     | Maintain traceability of records and process outputs; link records, changes, and affected documents.                  | Approve traceability entries within their process scope.            |
| **Change Control Coordinator (CCC)**   | Ensures traceability is preserved through change implementation.                                                      | Assigns and validates CR identifiers and trace links.               |
| **All Personnel**                      | Follow traceability rules and report missing or inconsistent identifiers.                                             | None beyond assigned responsibilities.                              |

---

## **7. Process Description**

### **7.1 Identification of Controlled Documents**

1. Each controlled document includes in its header:

   * Title
   * Revision (e.g., `r3`)
   * Controlled Source link
2. Each document has a **unique slug** identifier displayed in:

   * Filename or title
   * Controlled source listing
   * Related change or approval records
3. The **current approved revision** is the one published at the controlled source or system of record.
4. Approval, effective date, and reviewer metadata are maintained in the document control system and are **not repeated in the document body**.

---

### **7.2 Identification of Records**

1. Each record or dataset must be traceable to:

   * Responsible owner
   * Date or timestamp
   * Related process, document, or change identifier
2. Modifications are logged automatically by the repository or record system.
3. Records are identified using stable IDs, e.g.:

   * CAPA ID (`CAPA-2025-003`)
   * Change Request ID (`CR-2025-014`)
   * Log entry number or timestamp

---

### **7.3 Identification of Products and Configurations**

1. Physical products, components, or materials are uniquely identified by **lot, batch, or serial numbers**.
2. Digital assets or configurations include:

   * Configuration identifier (checksum, timestamp, or version string)
   * Reference to associated documentation or test records
3. Product and configuration identifiers are linked to inspection, release, and change records to maintain full traceability.

---

### **7.4 Traceability Relationships**

| Entity                    | Identified By     | Traceability Links                                         |
| ------------------------- | ----------------- | ---------------------------------------------------------- |
| Controlled Document       | Slug + Revision   | Linked to CR, approval record, or change history           |
| Record (e.g., CAPA, Risk) | Record ID         | Linked to related documents or actions                     |
| Product or Material       | Lot/Serial Number | Linked to inspection and release data                      |
| Configuration Item        | Configuration ID  | Linked to associated tests, validation, or deployment logs |

> All items must be traceable **backward** to their origin and **forward** to their use or outcome.

---

### **7.5 Control of Obsolete and Superseded Items**

1. Superseded document revisions become **obsolete**.
2. Obsolete documents are retained in the archive or historical view of the controlled source, clearly marked as superseded.
3. Header note example:

   > *“Obsolete – Superseded by Revision r4 (Effective YYYY-MM-DD)”*
4. Records are never considered obsolete; they remain part of the permanent QMS evidence base.

---

### **7.6 Verification of Traceability**

1. Traceability is verified during audits or management review by confirming:

   * Identifier and revision in document headers
   * Document location in the controlled source
   * Corresponding approval or change records in the system
2. The DCC and CCC verify traceability periodically (e.g., quarterly).
3. Missing or broken links are corrected through Change Control or CAPA procedures.

---

## **8. Records / Documented Information**

| Record / Artifact         | Responsible Owner            | Storage Location        | Retention | Control Method           |
| ------------------------- | ---------------------------- | ----------------------- | --------- | ------------------------ |
| Approved SOPs             | Document Control Coordinator | Controlled repository   | Permanent | Revision control         |
| Change Logs / CRs         | Quality Manager / CCC        | Change control system   | Permanent | Unique IDs & trace links |
| Records (CAPA, Risk, MPL) | Process Owners               | Controlled repositories | Permanent | Version-controlled       |
