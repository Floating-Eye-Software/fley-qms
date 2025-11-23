---
slug: Change-Control-SOP
revision: r2
type: SOP
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/SOPs/Change-Control-SOP.md
---

# **SOP – Change Control**

## **1. Purpose**

To ensure that all changes affecting the Quality Management System (QMS), processes, documents, software, or products are identified, reviewed, approved, implemented, and recorded in a **controlled** manner that preserves compliance, traceability, and quality integrity throughout the change lifecycle.

This procedure also governs the implementation of improvement actions arising from Management Review, Risk & Opportunity evaluation, effectiveness verification, or quality planning activities.

---

## **2. Scope**

This procedure applies to **all changes** that could affect the QMS or regulated activities, including but not limited to:

* QMS processes, procedures, or controlled documents
* Software, digital configurations, or data used in production or support
* Equipment, materials, or operational methods
* Organizational structure, roles, or resource assignments
* Product conformity, safety, or regulatory compliance

This SOP governs both **planned** and **unintended** changes.

---

## **3. References**

* ISO 9001:2015 § 6.3
* ISO 9001:2015 § 8.5.6
* WI – GitHub–Change–Control

---

## **4. Definitions**

| Term                    | Definition                                                                                                  |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Change Request (CR)** | A documented proposal to modify any controlled element of the QMS or related system.                        |
| **Planned Change**      | A proposed change that undergoes formal review and approval before implementation.                          |
| **Unintended Change**   | An unapproved or unscheduled modification that must be investigated and corrected through the CAPA process. |
| **Revision (`r#`)**     | A formally approved and published iteration of a controlled document or configuration.                      |
| **Version**             | Any interim draft or working iteration within the control system prior to formal approval.                  |
| **Record of Change**    | The documented evidence of review, approval, and implementation of a change within the control system.      |

---

## **5. Responsibilities and Authorities**

| Role                                 | Responsibilities                                                                                                     | Authorities                                                                    |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Change Requestor**                 | Proposes changes and provides justification         | Initiate CRs.                               |
| **Process Owners**                   | Evaluate impact of change requests and ensure proper review, implementation, and documentation. Ensure that improvement actions implemented through this procedure achieve their intended outcomes. | Approve technical and process-related changes within their domain.             |
| **Change Control Coordinator (CCC)** | Administers the change control system; ensures compliance with this procedure and maintains traceability of records. | Assign reviewers and control CR workflow status.                               |
| **Reviewers / Approvers**            | Evaluate proposed changes for adequacy, risk, and compliance; approve, reject, or request revisions.                 | Authorize change approval within assigned scope.                               |
| **Quality Manager**                  | Oversees the change control process and ensures alignment with QMS and regulatory requirements.                      | Final authority for release of changes impacting QMS governance or compliance. |
| **All Personnel**                    | Use only approved, published documents and report any unauthorized or unintended changes.                            | None beyond authorized document use.                                           |

---

## **6. Process Description**

### **6.1 Initiating a Change**

1. Any individual may propose a change by submitting a **Change Request (CR)** using the approved form or digital system.
2. Each CR must include:

   * Description and justification for the change
   * Assessment of impact on quality, compliance, or operations
   * Affected documents, systems, or processes
   * Proposed effective date (if applicable)
3. The CR is assigned a unique identifier (e.g., `fley-qms#42`).
4. The **Change Control Coordinator (CCC)** registers the CR and routes it for review.

---

### **6.2 Review and Approval**

1. The CCC assigns reviewers and approvers based on scope, risk, and potential impact.
2. Reviewers evaluate the proposal for:

   * Adequacy and completeness
   * Risks, dependencies, or unintended effects
   * Need for verification, validation, or training
   * Effects on compliance, quality, or operations
3. Approvals are recorded in the change control system. Digital approvals or equivalent acknowledgments constitute formal authorization.
4. Once approved, the change is cleared for implementation.

> **Note:** Approval metadata (e.g., reviewer, approver, date) are stored in the control system; they do not need to appear in the controlled document itself.

---

### **6.3 Implementation**

1. Approved changes are implemented by the responsible Process Owner or designated personnel.
2. Controlled documents impacted by the change are revised and reissued under the **Document Control SOP**.
3. The current approved revision is published at the designated **controlled source**.
4. When applicable, training, communication, or validation activities are performed to ensure awareness and compliance.

---

### **6.4 Control of Unintended Changes**

1. Any unintended or unauthorized change must be documented immediately as a **Corrective and Preventive Action (CAPA)**.
2. The CAPA record must include:

   * Identification of affected items
   * Description and assessment of the unintended change
   * Defined corrective and preventive actions
3. The CAPA is reviewed and verified prior to closure.
4. The CAPA record and resulting approved change together provide full traceability of the event.

---

### **6.5 Closure**

1. The CCC verifies that:

   * All affected items and documents are updated and published
   * Approvals are complete and traceable
   * Related training, communication, or validation activities are closed
   * The change record reflects the final status and outcomes
2. Once verified, the CR is formally closed and retained as part of the permanent change history.

---

### **6.6 Verification and Audit**

1. The change control process is reviewed periodically (e.g., annually) for compliance and effectiveness.
2. During audits, traceability of a change is demonstrated by linking the CR, review records, and resulting document revisions.
3. Deficiencies or nonconformities are addressed through the CAPA process.
4. The effectiveness of improvement-related changes shall be evaluated after implementation and reported during Management Review.

---

## **7. Records**

| Record / Artifact            | Description                                                | Responsible Owner          | Retention | Control Method                      |
| ---------------------------- | ---------------------------------------------------------- | -------------------------- | --------- | ----------------------------------- |
| **Change Request (CR)**      | Description, justification, and impact assessment          | Change Control Coordinator | Permanent | Unique ID and tracking log          |
| **Review & Approval Record** | Approval decisions, reviewer notes, and risk assessment    | Quality Manager            | Permanent | Stored in control system            |
| **Implementation Evidence**  | Updated documents, validation reports, or training records | Process Owners             | Permanent | Linked to CR or CAPA                |
| **Obsolete Documents**       | Superseded versions retained for reference                 | DCC / Quality Manager      | Permanent | Archived under Document Control SOP |
