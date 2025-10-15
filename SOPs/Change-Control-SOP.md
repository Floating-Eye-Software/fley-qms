# 🧾 **SOP: Change Control**

**Revision:** r3
**Title:** Change Control
**Controlled Source:** [Organization Wiki or Repository URL]

---

## **1. Purpose**

To ensure that all changes affecting the Quality Management System (QMS), processes, documents, software, or products are identified, reviewed, approved, implemented, and recorded in a controlled manner that maintains compliance, traceability, and quality integrity.

---

## **2. Scope**

This procedure applies to all changes that could impact:

* QMS processes, procedures, or controlled documents
* Software, digital configurations, or datasets used in regulated activities
* Equipment, materials, or production/service methods
* Organizational structure, responsibilities, or resources
* Product conformity or regulatory compliance

The procedure applies to both planned and unintended changes.

---

## **3. Responsibilities**

| Role                                 | Responsibilities                                                                                                              |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Process Owners**                   | Initiate change requests, evaluate impact, and ensure appropriate review, implementation, and documentation.                  |
| **Change Control Coordinator (CCC)** | Administers the change control system; ensures changes follow this procedure and that all records are traceable and complete. |
| **Reviewers / Approvers**            | Evaluate proposed changes for adequacy, risk, and compliance; approve or reject as appropriate.                               |
| **Quality Manager**                  | Oversees the change control process and ensures compliance with QMS and regulatory requirements.                              |
| **All Personnel**                    | Follow only approved, published versions of controlled documents and report any unauthorized changes.                         |

---

## **4. Definitions**

| Term                    | Definition                                                                                    |
| ----------------------- | --------------------------------------------------------------------------------------------- |
| **Change Request (CR)** | A documented proposal to modify any controlled element of the QMS.                            |
| **Planned Change**      | A proposed change that undergoes formal review and approval prior to implementation.          |
| **Unintended Change**   | An unapproved or unscheduled modification requiring immediate review and corrective action.   |
| **Revision (`r#`)**     | A formally approved and published iteration of a controlled document or configuration.        |
| **Version**             | Any draft or iteration recorded in the control system prior to approval.                      |
| **Record of Change**    | Evidence of review, approval, and implementation maintained within the change control system. |

---

## **5. Procedure**

### **5.1 Initiating a Change**

1. Any individual may propose a change by creating a **Change Request (CR)** using the approved form or system entry.
2. Each CR shall include:

   * Description and justification for the change
   * Assessment of impact on quality, compliance, or operations
   * Affected documents, systems, or processes
   * Proposed effective date (if applicable)
3. The CR is assigned a unique identifier (e.g., `CR-2025-014`).
4. The CR is submitted to the **Change Control Coordinator (CCC)** for registration and routing for review.

---

### **5.2 Review and Approval**

1. The CCC assigns reviewers and approvers based on the change scope and impact.
2. Reviewers evaluate:

   * The adequacy and completeness of the change proposal
   * Potential risks or unintended consequences
   * Need for verification, validation, or training updates
3. Approvals are recorded within the change control system; digital reviews, signatures, or equivalent acknowledgments constitute formal approval.
4. Once approved, the change is authorized for implementation.

> **Note:** Approval details and effective dates are maintained automatically by the system and do not need to appear in the controlled document.

---

### **5.3 Implementation**

1. The approved change is implemented by the responsible Process Owner or delegated personnel.
2. Controlled documents affected by the change are revised and reissued under the **Document Control SOP**.
3. The current approved revision of each affected document is published at the controlled source (wiki or main branch).
4. Where applicable, related training, process updates, or communications are executed to ensure awareness and compliance.

---

### **5.4 Documentation and Records**

All change activities must be documented and traceable. Minimum records include:

| Record Type                    | Description                                              | Retention |
| ------------------------------ | -------------------------------------------------------- | --------- |
| **Change Request (CR)**        | Description, justification, and impact assessment        | Permanent |
| **Review and Approval Record** | Approvals, comments, and risk assessments                | Permanent |
| **Implementation Evidence**    | Updated documents, configurations, or validation outputs | Permanent |
| **Obsolete Documents**         | Retained as historical records of superseded revisions   | Permanent |

All change records are maintained in the digital QMS or repository with appropriate access control.

---

### **5.5 Control of Unintended Changes**

1. Any unintended or unauthorized change (e.g., modification outside the approved process) must be documented immediately as a **Corrective and Preventive Action (CAPA)**.
2. The CAPA record must:

   * Identify the affected item(s)
   * Describe the nature and impact of the unintended change
   * Define corrective and preventive measures
3. The CAPA process ensures the change is formally reviewed, corrected, and verified prior to closure.
4. The incident, CAPA, and resulting approved change form a single, traceable chain of records.

---

### **5.6 Closure**

Before a CR is closed, the CCC verifies that:

* All affected items and documents have been updated and published.
* Approvals are complete and traceable within the system.
* Associated training, communication, or validation actions are complete.
* The change record reflects the final status and outcomes.

Once verified, the CR is closed and retained as part of the permanent change history.

---

### **5.7 Verification and Audit**

1. The change control process is reviewed periodically (e.g., annually) to confirm adherence to this SOP.
2. During audits, traceability of a change is demonstrated by linking the CR, review record, and the resulting approved document revision.
3. Any deficiencies are addressed through the CAPA process.

---

## **6. References**

* SOP – Document Control
* SOP – Identification and Traceability
* CAPA Procedure
* ISO 9001:2015 — Clauses 6.3, 7.5, 8.1, 8.5.6
* ISO 13485:2016 — Clauses 4.2.4, 4.2.5, 7.5.6
* 21 CFR Part 11 — Electronic Records and Signatures

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                      | Approved By |
| -------- | ---------- | ------------------------------------------------------------------------------------------ | ----------- |
| r1       | 2025-10-11 | Initial release integrating digital change tracking                                        | [Name]      |
| r2       | 2025-10-12 | Updated for slug-based identification and revision control                                 | [Name]      |
| **r3**   | 2025-10-15 | Converted to tool-agnostic model; minimal header; system-maintained approvals and metadata | [Name]      |
