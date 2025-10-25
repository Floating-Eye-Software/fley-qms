# **WI – GitHub Document Control**

**Slug:** GitHub-Document-Control  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Document-Control-SOP, Identification-and-Traceability-SOP  
**Controlled Source:** https://github.com/mlehotay/fley-qms/blob/main/WIs/GitHub/GitHub-Document-Control.md  

---

## **1. Purpose**

To define the method for creating, revising, approving, and maintaining controlled QMS documents within GitHub, in alignment with the Document Control SOP.
This Work Instruction (WI) specifies how GitHub’s native version control, pull request, and tagging functions fulfill document control requirements.

---

## **2. Scope**

This WI applies to all controlled QMS documents maintained in the GitHub repository, including SOPs, WIs, Templates (TPLs), and controlled Records (RECs).
It describes *how* document control is implemented within GitHub. The SOP defines *what* must be achieved.

---

## **3. References**

* SOP – Document Control
* WI – GitHub–QMS–Setup
* TPL – Standard-Operating-Procedure-Template
* TPL – Work-Instruction-Template
* TPL – Header-Template
* ISO 9001:2015 §§7.5.2–7.5.3
* 21 CFR Part 11

---

## **4. Responsibilities**

| Role                            | Responsibilities                                                                                                  |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Authors / Process Owners**    | Draft and maintain controlled documents using the correct slug and revision formatting.                           |
| **Reviewers / Approvers**       | Review proposed changes in Pull Requests (PRs) and provide formal approval comments.                              |
| **Quality Manager / DCC / CCC** | Verify correct structure, header format, and tagging. Ensure only approved content appears at the HEAD of `main`. |
| **All Users**                   | Use only the approved versions visible in the wiki or `main` branch.                                              |

---

## **5. Procedure**

### **5.1 Document Identification and Naming**

1. Each controlled document resides in the appropriate folder (`/SOPs`, `/WIs`, `/Templates`, `/Records`, etc.).
2. The **document slug** serves as the unique identifier and is derived from the filename.
   *Example:*
   `Document-Control-SOP.md` → **Slug:** Document-Control-SOP
3. Documents are referenced in text using double brackets, e.g., `[[Document Control SOP]]`.
   This links directly to the file in the GitHub wiki.
4. Document prefixes are shown below.

| Type                           | Prefix   | Example                           | Notes                         |
| ------------------------------ | -------- | --------------------------------- | ----------------------------- |
| Quality Management System Core | **QMS**  | `QMS-Quality-Manual.md`           | Foundational documents        |
| Standard Operating Procedure   | **SOP**  | `SOP-Document-Control.md`         | Process-level control         |
| Work Instruction               | **WI**   | `WI-GitHub-Document-Control.md`   | Detailed procedural steps     |
| Template                       | **TPL**  | `TPL-Design-Control-Plan.md`      | Controlled templates or forms |
| Reference / Overview           | **REF**  | `REF-GitHub-QMS-Overview.md`      | Context or guidance           |
| Compliance Mapping             | **MAP**  | `MAP-ISO-13485.md`                | Standards mapping             |
| Corrective & Preventive Action | **CAPA** | `CAPA-0001-Nonconformance.md`     | Issue and resolution tracking |
| Complaint                      | **CMPL** | `CMPL-0001-Customer-Complaint.md` | Complaint records             |
| Record / Evidence              | **REC**  | `REC-Design-Review.md`            | Controlled evidence outputs   |
| Plan                           | **PLAN** | `PLAN-Continuous-Improvement.md`  | Project or system plans       |

5. Where used, document numbers are sequential and unique within each type. Authors propose the next number; the reviewer or DCC confirms uniqueness.

---

### **5.2 Document Header Format**

Each controlled Markdown file begins with the following header:

```markdown
# **[TYPE] – [Title]**

**Slug:** [Slug-Name]  
**Revision:** r[#]  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** [Linked SOP] _(optional)_  
**Controlled Source:** https://github.com/[org]/[repo]/[path]/[file].md
```

**Notes:**

* “Approved By” is not required; approvals are recorded in the GitHub Pull Request history.
* The “Effective Date” is retained for clarity, though not required by the SOP.
* The header is updated only when a new revision is approved and merged.

---

### **5.3 Drafting and Review Workflow**

1. Authors create a new branch for each draft or revision:

   ```bash
   git checkout -b update/Document-Control-SOP_r5
   ```

2. Edit the Markdown file following the header template.

3. Commit with a clear, descriptive message.

4. Push the branch and open a **Pull Request (PR)** for review and approval.

5. Reviewers add comments or approve directly in GitHub.

6. When all approvals are complete, merge the PR into `main`.

> The merged commit represents the official approved revision and serves as the formal approval record.

---

### **5.4 Tagging Approved Revisions**

After merging, the DCC or Quality Manager tags the new approved revision:

```bash
git tag Document-Control-SOP_r5
git push origin Document-Control-SOP_r5
```

**Rules:**

* Tag names must match the slug and revision exactly.
* Each tag represents one approved revision.
* Tags are immutable — do **not** delete or reuse tags.

> The tag, merge commit, and PR together form the complete approval and effective-date record.

---

### **5.5 Publication and Controlled Source**

1. The **HEAD of `main`** branch represents the **current approved revision**.
2. The repository **wiki** displays this same content for user access.
3. Users confirm document currency by comparing the wiki version to the HEAD of `main`.

---

### **5.6 Managing Obsolete or Superseded Documents**

1. When a new revision is approved:

   * The previous version remains accessible through its tag.
   * Do **not** delete historical files or tags.
2. When a document is retired:

   * Add `**Status:** Obsolete` in the header.
   * Move the file to `/archive/` or mark it clearly as obsolete.
   * Reference the superseding document, if applicable.
3. The tag of the last active revision remains the official record of its approval.

---

### **5.7 Traceability and Audit History**

GitHub provides a full audit trail of all document activity.

**Commands:**

*View revision history for a document:*

```bash
git log --follow -- SOPs/Document-Control-SOP.md
```

*List revision tags:*

```bash
git tag --list | grep Document-Control-SOP
```

*View approval record:*
Open the tagged commit in GitHub → click **Pull Request** to view reviews and approvals.

These controls demonstrate compliance with ISO 9001 §7.5.2–7.5.3 and ISO 13485 §4.2.4.

---

## **6. Records and Retention**

| Record Type                      | Location                   | Retention  |
| -------------------------------- | -------------------------- | ---------- |
| Controlled Markdown Files        | GitHub `main` branch       | Indefinite |
| Tags (approved revisions)        | GitHub repository          | Indefinite |
| Pull Requests (approval records) | GitHub                     | Indefinite |
| Commit history (traceability)    | Git repository             | Indefinite |
| Archived/Obsolete Files          | `/archive/` or Git history | Indefinite |

All GitHub metadata serves as the official QMS record of document control activities.
