# ✅ **Cross-Document Alignment Summary (Batch 1)**

The three documents already align well conceptually, but there are **inconsistencies, missing linkages, and terminology gaps** that should be addressed to ensure that:

* The **SOP (Change Control)** defines the high-level process
* The **WI – GitHub Change Control** implements the SOP within GitHub
* The **WI – GitHub Configuration Verification** cleanly supports configuration-specific changes but does not conflict with the primary change-control flow

Below is a structured analysis:

---

# 1. **Role and Responsibility Alignment**

### ✔ Strong alignment

* All three documents reference:

  * Change Requestor / Author
  * Reviewer / Approver
  * Quality Manager
  * CCC (Change Control Coordinator) — appears only in Change Control SOP + GitHub Change Control WI

### ⚠ Minor inconsistency

**GitHub Config Verification WI does not reference the CCC role** even though the Change Control SOP assigns them responsibility for “administering the change control system.”

**Recommendation:**
Add CCC to GitHub-Config-Verification §4, at least to acknowledge their oversight role (e.g., verifying that configuration changes are routed through correct CRs and documented accordingly).

---

# 2. **Definition Alignment**

### ✔ Strong alignment

* “Change Request (CR)” concept is used consistently across documents.
* “CR Issue” in GitHub WI clearly maps to CR in SOP.

### ⚠ Missing / inconsistent terminology

1. **Unintended change**

   * Defined in SOP
   * **Not mentioned at all in the GitHub WIs**

2. **Record of Change** vs GitHub artifacts

   * SOP uses generalized terminology; GitHub WI uses Issues/PRs/merge commits/tags.
   * Conceptually aligned but not explicitly mapped.

**Recommendation:**
Add cross-references or a table mapping:

| SOP Term                 | GitHub Implementation                |
| ------------------------ | ------------------------------------ |
| Change Request (CR)      | GitHub Issue                         |
| Review & Approval Record | Pull Request + GitHub review actions |
| Implementation Evidence  | Commits + PR description             |
| Record of Change         | Tag + Merge Commit + PR              |

---

# 3. **Process Alignment**

### 3.1 **Initiation**

✔ Fully aligned.

* SOP: CR is required for any change.
* GitHub WI: Requires CR Issue using template.

### 3.2 **Review and Approval**

✔ Good alignment.
GitHub WI provides implementation-level detail for the SOP’s approval phase.

### ⚠ Gaps

**SOP requires risk assessment for each CR.**
GitHub WI requires it implicitly via templates but does not explicitly say “risk assessment is required for all CRs.”

**Recommendation:**
Add explicit language in GitHub WI §5.1 referencing SOP §6.2 requirements for risk analysis.

---

# 4. **Metadata & Revision Control Alignment**

### ✔ Strong alignment

GitHub WI §5.6 specifies how revision, status, and effective date are finalized.

### ⚠ Gap

**SOP does not mention metadata or GitHub-specific record tags.**

**Recommendation:**
SOP should state:

> “When controlled documents are stored in Git-based systems, revision metadata and effective dates are controlled per the applicable work instructions."

This keeps SOP technology-agnostic but aligned.

---

# 5. **Unintended / Unauthorized Change Handling**

### ✔ GitHub WI section exists (§5.11), referencing CAPA.

### ⚠ SOP and GitHub WI terminology mismatch

SOP uses **Unintended Change** → CAPA.
GitHub WI uses **Unauthorized Change** → CAPA + revert PR.
The meanings are equivalent but inconsistent.

**Recommendation:**
Normalize terminology to “Unintended or Unauthorized Change” across all GitHub WIs.

---

# 6. **Scope Delineation**

### ✔ Clear boundaries

* SOP covers all QMS changes.
* GitHub Change Control WI covers document/config changes managed in Git.
* GitHub Config Verification WI covers configuration testing only.

### ⚠ Small misalignment

GitHub Config Verification WI claims:

> “This WI does not determine whether the QMS configuration is fit for purpose (validation).”

This is correct, but **SOP does require verification/validation where applicable.**
This may cause confusion unless explicitly linked.

**Recommendation:**
Add a sentence in GitHub-Config-Verification §1:

> “Verification performed under this WI satisfies the verification requirement of the Change Control SOP but does not constitute validation.”

---

# 7. **Recordkeeping**

### ✔ All three documents maintain permanent records in GitHub for controlled environments.

### ⚠ Small inconsistencies

* SOP lists “Obsolete Documents” as a record; GitHub WI does not explicitly state how obsolete docs are archived.
* GitHub-Config-Verification WI:

  * Correctly states test-repo records are not controlled.
  * Should explicitly state that only fley-qms records are governed by SOP retention.

**Recommendation:**
Add mapping table showing which repository holds which type of record and why.

---

# 8. **Document-to-Document Reference Consistency**

### ✔ Good

All WIs reference the Change Control SOP.

### ⚠ Missing cross link

SOP references “WI – GitHub–Change–Control” only.
It does **not** reference GitHub Config Verification WI.

**Recommendation:**
Add it to SOP §3 as a supporting reference for cases where configuration changes occur.

---

# 9. **Overall Observations**

Your system already has:

✔ Clear hierarchy (SOP → WI → templates → GitHub actions)
✔ Strong alignment of core change control logic
✔ Good compliance posture for ISO 9001 and Part 11

The main gaps are:

* terminology mismatches (“unintended” vs “unauthorized”)
* missing CCC role in GitHub Config Verification WI
* SOP not acknowledging GitHub metadata controls
* GitHub WI not explicitly referencing all SOP risk/verification requirements
* explicit mapping tables missing between SOP constructs and GitHub artifacts
* inconsistent definitions and cross-references

All of these are easy to fix with small edits.

---

# ✅ **Cross-Document Consistency & Alignment Analysis (Batch 2)**

## **1. Relationship Hierarchy (SOP → WI)**

**Strong alignment:**

* Document Control SOP establishes “what must be controlled.”
* GitHub Document Control WI establishes “how control is implemented in GitHub.”
* FLEY Planning Workflow WI references document control only indirectly (via traceability).

**Minor gaps:**

* Planning Workflow WI introduces controlled documents (Plans, PQPs, DCPs), but **does not explicitly reference the Document Control SOP**, only the GitHub Document Control WI.
* Document Control SOP does **not reference Planning artifacts (Plans, PQPs, DCPs)** even though they are controlled documents.

**Recommendation:**

* Add Plans/PQPs/DCPs to the Document Control SOP as controlled document types.
* Add a reference explicitly:

  > Controlled planning documents follow SOP–Document Control and WI–GitHub–Document–Control.

---

# 2. **Definitions Alignment**

## ✔ Well-aligned terms:

* Controlled document
* Revision
* Controlled source
* Records

## ⚠ Misalignments / Missing Definitions:

1. **The Planning Workflow introduces many unique artifacts**, none of which appear in the Document Control SOP:

| Term (Planning WI)      | Missing From      | Comments                                                          |
| ----------------------- | ----------------- | ----------------------------------------------------------------- |
| Plan Issue              | SOP, GitHub DC WI | Should clarify whether these are controlled documents or records  |
| Phase Issue             | SOP, GitHub DC WI | Treated as planning records                                       |
| Quality Plan (Document) | SOP               | Should be categorized formally (likely SOP “Controlled Document”) |
| PQP / DCP               | SOP               | Should be added as controlled planning documents                  |
| Management Review Issue | SOP               | Should be categorized as records                                  |

2. **Document Control SOP defines “Record” broadly**, but Planning WI imposes a 5–10 year retention schedule—**potential conflict** (SOP says permanent).

**Recommendation:**
Define:

* Plan Issues, Phase Issues, MR Issues → **Records**, not controlled documents
* Quality Plans, PQPs, DCPs → **Controlled Documents**

And cross-reference them.

---

# 3. **Roles & Authorities**

## ✔ Good alignment:

* SOP roles: Process Owners, DCC, QM, Management
* GitHub DC WI: Authors, Reviewers, QM/DCC/CCC
* Planning Workflow: Top Management, Quality Manager, Project Manager, Process Owner

## ⚠ Inconsistencies:

1. **Document Control SOP uses “Document Control Coordinator (DCC)”**
   GitHub DC WI uses “Quality Manager / DCC / CCC” (CCC appears only here).
   Planning Workflow uses “Quality Manager / QMS Admin” but **not DCC**.

2. The Planning Workflow WI grants the Quality Manager final approval of Plans/PQPs/DCPs, but the Document Control SOP says **Process Owners → QM final approval**.

3. For Plans/PQPs/DCPs, **who is the approving authority?**

   * The Document Control SOP never addresses planning documents.
   * The Planning Workflow WI assigns authorities locally.

This should be aligned globally.

**Recommendation:**
Add a unified statement in the Document Control SOP:

> “Controlled planning documents (Quality Plans, PQPs, DCPs) follow the Document Control SOP. Approval authority is defined in the Planning Workflow WI and recorded via GitHub PR approval.”

---

# 4. **Control of Documents (SOP) vs GitHub Implementation (WI)**

## ✔ Good alignment:

* SOP: revision, archiving, controlled source
* GitHub DC WI: header metadata, tags, PR review, `main` as source of truth

## ⚠ Missing mapping between SOP requirements and GitHub mechanisms

Examples:

| SOP Requirement                         | GitHub Implementation | Gap                                               |
| --------------------------------------- | --------------------- | ------------------------------------------------- |
| “Current version available to users”    | `main` branch         | Well documented                                   |
| “Archive obsolete versions”             | Git tags              | SOP should explicitly reference tags              |
| “Approval and change metadata retained” | PR + commit history   | SOP doesn’t state PRs are formal records          |
| “Controlled Source”                     | GitHub repo           | Aligned but SOP doesn’t mention Git-based systems |

**Recommendation:**
Add a clause in SOP §6.1:

> “When documents are maintained in Git-based systems, GitHub commit history, pull requests, and tags serve as the approval and archival record per WI–GitHub–Document–Control.”

---

# 5. **Record Retention Differences**

This is the **most significant misalignment**.

### SOP Retention (§6.7)

| Type                      | Retention  |
| ------------------------- | ---------- |
| Controlled Documents      | Indefinite |
| Records (CAPA, Risk, MPL) | Permanent  |
| Metadata                  | Permanent  |

### GitHub DC WI Retention

All GitHub metadata: **Indefinite**

### Planning Workflow WI Retention (§12)

| Artifact    | Retention        |
| ----------- | ---------------- |
| Issues      | 5 years          |
| Plan Issues | 5 years          |
| PQPs        | 10 years         |
| DCP         | 10 years or life |
| MR Cycles   | 5 years          |

### ⚠ Conflicts:

* Document Control SOP says “Records are permanent.”
* Planning Workflow WI says “5 years” for many records.
* PQPs and DCPs are not accounted for in SOP retention rules.

This will cause nonconformance unless harmonized.

**Recommendation:**
Either:

### Option A (Common)

* Change Document Control SOP to specify retention **according to document category**, allowing shorter periods:

  > “Records are retained according to their governing procedure.”

### Option B (Strict)

* Update Planning Workflow retention to “Permanent” for Issues that contribute to QMS evidence.

I can generate harmonized retention tables if desired.

---

# 6. **Traceability Requirements**

## ✔ Document Control WI clearly uses slug + revision + controlled source.

## ⚠ Planning Workflow WI references “traceability to controlled documents” but:

* Does not define required metadata
* Does not require a controlled header
* Does not state if Plan Issues or documents need slugs/revisions

**Recommendation:**

Add to Planning Workflow WI:

* Plan Documents must include standard QMS header per Document Control SOP
* Plan Issues must reference:

  * slug of controlled Plan Document
  * revision number
  * controlled source link

This protects traceability during audits.

---

# 7. **Cross-Referencing Consistency**

## Missing from Planning Workflow WI:

* Reference to **Document Control SOP** as the governing document for controlled Plans/PQPs/DCPs.

## Missing from Document Control SOP:

* Reference to **Planning Workflow WI** as the governing procedure for planning document lifecycle.

**Recommendation:**
Add explicit cross-references in both documents for bi-directional coverage.

---

# 8. **Terminology Consistency**

## Issues identified:

| Term Inconsistency        | Documents Affected       |
| ------------------------- | ------------------------ |
| DCC vs CCC vs QMS Admin   | All three                |
| Approver vs Reviewer      | GitHub DC WI vs SOP      |
| Effective date usage      | SOP vs GitHub DC WI      |
| Record retention policies | SOP vs Planning Workflow |

**Recommendation:**
Create a unified glossary and enforce its usage across all SOPs and WIs.

---

# Summary of Key Misalignments to Fix

| Category                      | Issue                                                           |
| ----------------------------- | --------------------------------------------------------------- |
| **Retention**                 | Major conflict: SOP says permanent; Planning WI uses 5–10 years |
| **Roles**                     | DCC, CCC, QMS Admin inconsistently referenced                   |
| **Controlled Document Types** | SOP does not recognize Plans/PQPs/DCPs                          |
| **Traceability**              | Plan Docs and Plan Issues lack formal metadata requirements     |
| **Approval Authority**        | Planning WI assigns approvals not described in SOP              |
| **Cross references**          | Missing references between SOP and Planning WI                  |
| **Definitions**               | Planning workflow introduces artifacts not acknowledged in SOP  |
