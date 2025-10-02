# **Work Instruction — Document Control in GitHub**

**WI ID:** WI-GIT-DC-001
**Project:** Red Witch
**References:** SOP-DOC-001 – Document & Record Control

---

## 1. **Purpose**

This Work Instruction defines *how* the Red Witch Project implements **document and record control** within GitHub repositories and wiki. It ensures compliance with:

* **SOP-DOC-001 – Document & Record Control**
* ISO 9001:2015 §7.5
* ISO 13485:2016 §4.2
* 21 CFR 820.40

It also specifies management of **external documents and licensing constraints**, ensuring that copyrighted standards (e.g., ISO, IEC) are **not stored in full** in GitHub.

---

## 2. **Scope**

Applies to all QMS and project documentation maintained in GitHub:

* SOPs, WIs, Plans, Quality Manual, Compliance pages (`redwitch.wiki`)
* Design docs, requirements, code, test artifacts (`redwitch`)
* Records of approvals, reviews, and sign-offs (via Pull Requests, Issues, Wiki edits)
* External document metadata summaries (no full copyrighted content unless licensed)

---

## 3. **Roles & Responsibilities**

| Role                | Responsibility                                                                 |
| ------------------- | ------------------------------------------------------------------------------ |
| **Author**          | Drafts or updates documents in feature branches; summarizes external docs.     |
| **Reviewer**        | Reviews PRs for compliance, formatting, and SOP conformance.                   |
| **Approver**        | Project Lead or Quality Representative; approves PRs before merge.             |
| **Repo Maintainer** | Ensures repo protections, access control, and compliance with branch policies. |
| **Document Owner**  | Maintains currency of documents; ensures external metadata is updated.         |

---

## 4. **Repositories & Folder Structure**

| Repo / Folder              | Contents                                               | Notes                                    |
| -------------------------- | ------------------------------------------------------ | ---------------------------------------- |
| `redwitch.wiki`            | SOPs, WIs, Plans, Quality Manual, Compliance pages     | Controlled documents                     |
| `redwitch`                 | Design docs, requirements, code, tests                 | Controlled project artifacts             |
| `/Records/`                | Finalized plans, reports, PMS logs, validation results | Immutable records                        |
| `/Templates/`              | Document templates                                     | Controlled documents                     |
| `/External-Docs-Metadata/` | Metadata and summaries of third-party documents        | No copyrighted full text unless licensed |

---

## 5. **Process**

### 5.1 Document Creation

1. Create new documents in the appropriate repo/folder.
2. Filename convention: `Title-With-Dashes.md`.
3. Include:

   * Title
   * Version/Revision History
   * References to SOPs, standards, or related issues

### 5.2 Version Control

1. Commit all changes via **feature branches**.
2. Branch naming:

   * `doc/<short-title>` → new documents
   * `update/<short-title>` → revisions
3. Submit **Pull Request (PR)** into `main`.

### 5.3 Review & Approval

1. At least **one Reviewer** per PR.
2. **Approver** (Project Lead / Quality Rep) must approve before merge.
3. PR approval history serves as **formal document approval record**.
4. PR may reference an Issue capturing rationale, CAPA linkage, or external document updates.

### 5.4 External Documents & Metadata

1. Store only **metadata and summaries** of external/copyrighted documents.
2. Include in metadata file:

   * Document ID
   * Title, author, year
   * Source / link
   * Type (Standard, Article, Report, Guidance)
   * Summary / Notes
   * License status
3. If license allows, full PDFs may be stored in a **restricted, access-controlled repo**.
4. Link metadata to internal documents (SOPs, WIs, Risk Assessments).

### 5.5 Publication & Access

1. Merged `redwitch.wiki` pages are **controlled documents**.
2. Merged `redwitch` repo artifacts are **controlled design/project documents**.
3. Repos are access-controlled; only authorized personnel may edit or approve.

### 5.6 Obsolete Documents

1. Mark superseded docs with **“Obsolete”** at the top.
2. Add link to replacement document.
3. Preserve full history in GitHub.

---

## 6. **Records**

* **Pull Requests** → approvals and change rationale
* **Issues** → change requests, CAPA linkage, external document updates
* **Git commit history** → version history
* **Wiki edit logs** → document change history
* **External metadata files** → evidence of external document review and summary

---

## 7. **Traceability & Audit**

* PR approvals, Issues, and Git commit logs provide full audit trail.
* External document summaries link to original source and internal references.
* Records are immutable; new versions are created for updates.
* Annual review by Document Owner to ensure currency and compliance.

---

## 8. **References**

* SOP-DOC-001 – Document & Record Control
* ISO 9001:2015 §7.5
* ISO 13485:2016 §4.2
* 21 CFR 820.40

---

## 9. **Revision History**

| Rev | Date       | Author | Change Description |
| --- | ---------- | ------ | ------------------ |
| 0.1 | YYYY-MM-DD | Name   | Initial Draft      |

---
