# ✅ **GITHUB-QMS WI ALIGNMENT CHANGE PLAN (DRAFT)**

**Applies to:**

* GitHub-QMS-Setup (r3 draft exists)
* GitHub-Document-Control (r2)
* GitHub-Change-Control (existing but needs alignment)
* GitHub-QMS-Operations (r2)
* FLEY-Action-Management (r3)

**Objective:**
To harmonize structure, terminology, workflow logic, and compliance behavior across all GitHub-based QMS Work Instructions.

---

# 1. **GLOBAL CHANGES (APPLY TO ALL WIs)**

## 1.1 Role Harmonization

All WIs will use the following core roles:

* **Authors** — create or update QMS content
* **Approvers** — approve and merge pull requests
* **Quality Manager** — owns the QMS and document control rules
* **Top Management** — only when a process requires escalation or formal management review

Additional roles allowed where needed:

* **Project Owner** (for project-specific Issues/Plans)
* **Process Owner** (for functional procedure ownership)

Roles to remove globally:

* Change Control Coordinator (CCC)
* Document Control Coordinator (DCC)
* QMS Admin
* Design Lead
* Any redundancy between Reviewers and Approvers (Approvers cover both)

---

# 2. **GITHUB-QMS-SETUP (r3) — ALIGNMENT CHANGES**

Setup WI is mostly complete; changes are minimal:

### 2.1 Add references to other WIs

Setup WI will reference:

* GitHub-Document-Control
* GitHub-Change-Control
* GitHub-QMS-Operations

### 2.2 Add unified terminology section

For consistency (e.g., “Controlled Source,” “Revision Tag”).

### 2.3 Add role-specific expectations

Clarify:

* Only Approvers may configure protected branches, tags, CODEOWNERS.

### 2.4 Confirm tag protection patterns match Document-Control

Ensure `*_r*` and `FLEY-QMS_*` are listed identically in Document-Control.

---

# 3. **GITHUB-DOCUMENT-CONTROL (r2 → r3) — MAJOR CHANGES**

This WI needs the most restructuring.

## 3.1 Remove contradictions

Your current Document-Control WI predates the new Setup and Ops logic and describes:

* older tag conventions
* incomplete approval semantics
* role descriptions that don’t match Option A
* inconsistent record lifecycle (draft → controlled → superseded)

## 3.2 Add formal “Document Lifecycle Model”

The revised WI will define:

1. Draft
2. In Review
3. Approved (merged into main)
4. Released (revision tag created)
5. Superseded
6. Obsolete

## 3.3 Align PR and Tag Steps with Setup WI

Document-Control will explicitly state:

* PR merge = formal approval
* Tag = release event
* Tags are immutable due to tag protection rules
* Only Approvers can create tags

## 3.4 Standardize file header requirements

Every controlled document will include:

* Title
* Document ID
* Revision
* Effective Date
* Owner
* Links to PR and Plan/Issue
* Controlled Source URL

## 3.5 Remove legacy roles (DCC/CCC/etc.)

---

# 4. **GITHUB-CHANGE-CONTROL (→ r3) — MAJOR CHANGES**

This WI will become the **authoritative definition** of:

* how changes are proposed
* how changes are reviewed
* how changes are approved
* how changes are released
* how records of change are maintained

## 4.1 Replace old approval model with PR-based model

All approvals will flow through Pull Requests with:

* Review comments
* Required Approver sign-off
* Resolution of all conversations
* Merge commit required

## 4.2 Describe change types

Include:

* Minor editorial changes
* Major technical changes
* New document creation
* Document retirement
* Emergency changes (if you want this category)

## 4.3 Define the “Controlled Source” concept clearly

Align with Setup WI and Document-Control.

## 4.4 Remove deprecated roles and steps

Remove:

* CCC
* DCC
* Multi-role approval sequences
* Manual approval signatures outside GitHub

## 4.5 Include required integration with Issues or Plans

Every change must link to:

* A governing Issue (problem, request, deviation, improvement), or
* A Plan (action management)

## 4.6 Standardize tagging logic

Make Change-Control the canonical source for revision tags.

---

# 5. **GITHUB-QMS-OPERATIONS (r2 → r3)**

## 5.1 Align terminology with Document-Control

Replace “linked PRs,” “MR Milestones,” etc. with consistent definitions.

## 5.2 Clarify when Issues vs. Plans are used

This WI will define:

* Issues = atomic units of work
* Plans = multi-step actions or corrective/preventive programs
* PRs = implementation of solutions
* Tags = final release identifiers (for documents only)

## 5.3 Clarify process roles

Minimal roles unless project ownership is needed.

## 5.4 Formalize operational recordkeeping

Ensure alignment with Document-Control requirements for:

* traceability
* record ownership
* completion criteria
* archival

---

# 6. **FLEY-ACTION-MANAGEMENT (r3 → r4)**

This WI is well-structured but needs harmonization.

## 6.1 Replace DCC/CCC terminology

Replace all references with Option A equivalents:

* Owner (Issue/Plan)
* Approvers (if needed)
* Quality Manager for escalations

## 6.2 Align the “Plan” concept with Ops WI

Ensure Plans behave consistently across both WIs.

## 6.3 Clarify the relationship between Actions and Documents

Provide consistent statements such as:

* “Actions may result in changes to controlled documents, which then follow GitHub-Change-Control.”

## 6.4 Standardize definition of “Controlled Source”

Same as Setup + Document-Control.

## 6.5 Ensure headers match Document-Control

Every controlled template or form will follow the same header structure.

---

# 7. **CROSS-DOCUMENT CONSISTENCY PACKAGE**

Final step after revising the WIs:

## 7.1 Unified front-matter for all WIs

* Standard Purpose / Scope / Responsibilities / Definitions sections
* Standard revision table
* Standard header format

## 7.2 Cross-reference matrix

Shows how each WI connects to others.

## 7.3 Compliance mapping

Shows how combined GitHub WIs satisfy:

* ISO 9001
* ISO 13485
* FDA 21 CFR 820.40
* Internal Document-Control-SOP

---

# 8. **DELIVERABLES**

### **Phase 1 (You are here)**

✔ Change Plan (this document)

### **Phase 2**

**Draft revised WIs:**

* GitHub-Document-Control r3
* GitHub-Change-Control r3
* GitHub-QMS-Operations r3
* FLEY-Action-Management r4

### **Phase 3**

* Unified Governance Package
* Cross-WI consistency table
* Compliance mapping
* Optional: Repo templates, header prototypes, file stubs

---

# ✅ Unified Formatting & Style Guide (Recommended for All GitHub WIs)

These rules bring the suite into a single, professional, audit-ready style.

## **1. Headings**

Use:

```
# WI – Title
## 1. Purpose
## 2. Scope
## 3. References
## 4. Responsibilities / Responsibilities and Authorities
## 5. Procedure / Operations / Setup
## 6. Records
```

**Never use Level 1 headers inside the body**.

Use **Title Case** for section headers.

---

## **2. Writing Style**

* Use **imperative mood** (“Configure…”, “Create…”, “Update…”).
* Use **short, direct sentences**.
* Avoid phrases like “This WI ensures…” unless absolutely needed.
* Use “QMS” consistently, not switching among “quality system”, “system”, “framework”, etc.
* Use “Issue” / “Pull Request (PR)” capitalization consistently.
* Refer to the controlled repository as **`fley-qms`** everywhere.

---

## **3. Table Formatting**

Use consistent table structure:

* Bold column headings
* Wrap long definitions
* Keep column order consistent (Definition → Use / Purpose)

Example:

| **Label** | **Definition** | **Typical Use** |
| --------- | -------------- | --------------- |

---

## **4. Code Blocks & Lists**

* Use triple backticks for directory structures.
* Use numbered lists for procedural steps.
* Use bullets only for unordered concepts.

---

## **5. Terminology Consistency**

Standardize:

| Term               | Use This                                 | Avoid                    |
| ------------------ | ---------------------------------------- | ------------------------ |
| QMS roles          | Quality Manager / QMS Admin              | QMS Manager, Admin alone |
| Issue Types        | Development / Operations                 | Dev, Ops                 |
| Board Columns      | Backlog → In Progress → In Test → Closed | Todo / Doing / Completed |
| Change terminology | Change Request (CR), Change              | CR, Change Ticket        |
| MR                 | Management Review                        | Mgmt Review, M.R.        |
| Risk & Opportunity | Use the phrase exactly                   | Risks/Opportunities, RoO |

---

## **6. Cross-Document References**

Always reference other WIs and SOPs as:

> **WI – GitHub–Document–Control**

not:

> GitHub-Document-Control WI
> Document Control WI

---

## **7. Record Retention**

Ensure all WIs use:

* **Permanent**
* **5 years**
* **Current + 1 revision**

No other retention terms.

---

# ✔ WI – GitHub-Project-Management (r2 draft)

### **Required Consistency Adjustments**

1. **Convert Section 5 to imperative WI style**
   Currently reads like guidance.
   Rewrite steps as actionable instructions.

2. **Reduce narrative descriptions**
   Tables such as “Overview of GitHub Project Environment” include long explanatory paragraphs.
   Condense to the concise style used in QMS-Operations.

4. **Match Issue Types and Label Definitions**
   Do not introduce `Task`, `Review`, `Testing` unless these are official labels.
   Use only the globally defined QMS labels.

5. **Project planning**
   Align to QMS language:

* Objectives = Issues labeled `Objective`
* Milestones = Management Review alignment (if applicable)
* Risk = Issue Type: Operations + Label: Risk

6. **Project Closure**
   Ensure steps reference:

* Verification of effectiveness
* PR-based approval for final documentation
* Preservation of records according to WI – GitHub-Document-Control

7. **Improve integration section**
   Use same format as Setup and Operations.

---
