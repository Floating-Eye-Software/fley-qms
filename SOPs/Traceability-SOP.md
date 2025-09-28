# **Standard Operating Procedure (SOP)**

**Title:** Regulatory Traceability (Standard → Evidence)
**Document Number:** SOP-QMS-TRC-001
**Version:** 1.0
**Effective Date:** [Insert Date]
**Approved By:** [Insert Approver]

---

## **1. Purpose**

This SOP defines how Floating Eye Software (FLEY) ensures **bidirectional traceability** between regulatory and standards requirements (ISO 9001, ISO 13485, 21 CFR 820, Ontario Digital Service Standard) and project/organizational quality evidence. The process guarantees that each regulatory clause can be traced to documented **SOPs, Work Instructions (WIs), Project Quality Plans (PQPs), and project artifacts**.

---

## **2. Scope**

This SOP applies to:

* All quality standards and regulatory frameworks adopted by FLEY.
* All organizational SOPs, WIs, PQPs, and project-level artifacts subject to audit or inspection.
* All projects executed under the Red Witch QMS.

---

## **3. Responsibilities**

* **Quality Manager (QM):** Owns the Traceability Matrix; ensures it is current, reviewed, and auditable.
* **Process Owners:** Ensure SOPs/WIs map to applicable regulatory clauses.
* **Project Managers (PMs):** Ensure project-level evidence (artifacts/records) is linked in the PQP.
* **All Staff:** Follow WI-defined traceability practices (e.g., tagging artifacts with requirement IDs).

---

## **4. Definitions**

* **Standard/Regulation:** A clause from ISO 9001, ISO 13485, 21 CFR 820, or DSS.
* **Evidence:** A controlled document, record, or artifact that demonstrates compliance.
* **Traceability Matrix (TM):** A controlled document (Excel/CSV or database) that lists each clause → mapped QMS element(s) → linked SOP/WI → evidence location.

---

## **5. Procedure**

### 5.1 Establish Traceability Matrix

1. Maintain a **master Traceability Matrix (TM)** at the organization level.

   * Columns: *Standard/Reg Clause → QMS Element → SOP/WI Reference → PQP Reference → Artifact/Record Example → Status (OK/GAP)*.
   * The TM must include **all clauses**, not only those currently addressed, so that **gaps are visible**.
2. Quality Manager updates the TM:

   * When adopting new standards.
   * When revising SOPs/WIs.
   * At least **annually** during Management Review.

---

### 5.2 Map Standards to QMS Elements

1. For each clause, identify the applicable **QMS Quality Element** (e.g., Risk Management, Document Control).
2. Record the mapping in the TM.
3. If no element applies → mark as **Gap** and escalate to Quality Manager for remediation (new SOP/WI).

---

### 5.3 Map QMS Elements to SOPs and WIs

1. For each QMS element, record:

   * The controlling **SOP** (mandatory).
   * The implementing **WI(s)** (optional; may vary by project/toolchain).
2. Ensure all SOPs/WIs have version control and approval signatures.

---

### 5.4 Link to Project Quality Plans (PQP)

1. Each PQP must reference the **SOP/WI mappings** from the TM.
2. The PQP must link the clause to **actual project artifacts** (e.g., GitHub PRs, Jira tickets, Confluence pages, spreadsheets).
3. Artifacts must be **uniquely identifiable** (e.g., PR #, file path, Confluence link).

---

### 5.5 Evidence Collection

1. Artifacts/records must be stored in controlled repositories (GitHub, Confluence, file share).
2. Evidence must include metadata:

   * Standard clause reference ID.
   * SOP/WI reference.
   * Approval status (draft, approved, released).
3. Evidence must be **auditable and retrievable within 24 hours** of request.

---

### 5.6 Review & Audit

1. The Quality Manager reviews the TM quarterly.
2. Internal audits include spot-checks:

   * Select clause → trace to SOP/WI → trace to PQP → trace to artifact.
   * Verify bidirectionality (Standard → Evidence, Evidence → Standard).
3. Audit findings feed into CAPA if traceability is broken or evidence missing.

---

## **6. Records**

* **Traceability Matrix (controlled spreadsheet or database).**
* **Project Quality Plans (PQP).**
* **Audit Reports (internal/external).**
* **CAPA records (if gaps identified).**

---

## **7. References**

* ISO 9001:2015 — Quality management systems.
* ISO 13485:2016 — Medical devices — QMS requirements.
* 21 CFR Part 820 — Quality System Regulation.
* Ontario Digital Service Standard.
* SOP-QMS-DC-001 — Document Control.
* SOP-QMS-CAPA-001 — CAPA.

---

## **8. Revision History**

| Version | Date     | Description     | Author | Approver |
| ------- | -------- | --------------- | ------ | -------- |
| 1.0     | [Insert] | Initial release | [Name] | [Name]   |
