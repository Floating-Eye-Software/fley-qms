# 🧭 **Work Instruction (WI): GitHub Document Control**

**Document Number:** WI-004
**Revision:** r2
**Related SOP:** Document Control SOP
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To define the practical method for creating, revising, approving, and maintaining controlled QMS documents within GitHub, consistent with the Document Control SOP.
This WI specifies how GitHub’s built-in version control, tagging, and pull-request workflows implement document control requirements.

---

## **2. Scope**

Applies to all controlled QMS documents managed in the GitHub repository, including SOPs, WIs, Policies (POLs), Templates (TPLs), and controlled Records (REC).
This WI describes *how* to perform document control in GitHub — the SOP defines *what* must be achieved.

---

## **3. Responsibilities**

| Role                            | Responsibilities                                                                                                          |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Authors / Process Owners**    | Draft and maintain controlled documents in the designated folders and ensure correct identifiers and revision formatting. |
| **Reviewers / Approvers**       | Review proposed changes in Pull Requests (PRs) and provide formal approval comments.                                      |
| **Quality Manager / DCC / CCC** | Verify correct structure, numbering, and tagging; ensure that only approved content appears at the HEAD of `main`.        |
| **All Users**                   | Use only the approved revisions visible on the wiki or in the `main` branch.                                              |

---

## **4. Procedure**

### **4.1 Document Identification and Naming**

1. Each controlled document is stored in the relevant folder (`/SOPs`, `/WIs`, `/TPLs`, `/POLs`, `/RECs`).

2. File naming convention:

   ```
   [PREFIX]-[###]_[Title].md
   ```

   Example:
   `SOP-003_Document-Control.md`

3. Prefix conventions:

   | Type                         | Prefix |
   | ---------------------------- | ------ |
   | Standard Operating Procedure | SOP    |
   | Work Instruction             | WI     |
   | Policy                       | POL    |
   | Template                     | TPL    |
   | Record                       | REC    |

4. Document numbers are sequential and unique within each type.
   *Authors propose the next number; the reviewer or DCC confirms uniqueness.*

---

### **4.2 Document Header Format**

Each controlled Markdown file begins with a minimal header aligned with the Document Control SOP:

```markdown
# SOP-003 – Document Control
**Revision:** r4  
**Controlled Source:** https://github.com/[org]/[repo]/SOPs/SOP-003_Document-Control.md
```

**Notes:**

* *No “Approved By” or “Effective Date” fields are included.*
  Approvals, effective dates, and reviewers are maintained automatically in GitHub PRs and history.
* This header must be updated only when a new revision is approved and merged.

---

### **4.3 Drafting and Review Workflow**

1. Authors create a new branch for the draft or revision:

   ```bash
   git checkout -b update/SOP-003_r5
   ```

2. Update the Markdown file following the minimal header structure.

3. Commit changes with a clear message describing the update.

4. Push the branch and open a **Pull Request (PR)** for review and approval.

5. Reviewers provide comments and approvals directly in GitHub.

6. Once all required approvals are complete, the PR is merged into `main`.

> The merged commit represents the *approved revision* and is traceable through GitHub’s system metadata.

---

### **4.4 Tagging Approved Revisions**

After the PR is merged, the DCC or Quality Manager creates a tag to mark the official revision:

```bash
git tag SOP-003_r5
git push origin SOP-003_r5
```

**Rules:**

* Tag names must match the document ID and revision number exactly.
* Each tag marks a controlled, approved revision.
* Tags must be immutable — do **not** reuse or delete tags.

> The tag, associated PR, and merge commit together form the *approval and effective-date record*.

---

### **4.5 Publication and Controlled Source**

1. The **HEAD of `main`** branch represents the **current approved revision** of every controlled document.
2. The repository’s **wiki or published documentation site** displays the same content for user access.
3. Users verify document currency by checking that the version on the wiki matches the HEAD of `main`.

---

### **4.6 Managing Obsolete or Superseded Documents**

1. When a new revision is approved:

   * The old revision remains accessible through its tag.
   * Do **not** delete old files or tags — they serve as permanent historical records.
2. If a document is intentionally retired:

   * Update the file header to include `**Status:** Obsolete` and reference the superseding document (if any).
   * Move the file to `/archive/` or mark it clearly within the repository.
3. The tag for the last active revision remains the authoritative record of its approval.

---

### **4.7 Traceability and Audit History**

GitHub inherently records all changes and approvals.
Key commands:

*View revision history for a document:*

```bash
git log --follow -- path/to/SOP-003_Document-Control.md
```

*View approval and tagging history:*

```bash
git tag --list | grep SOP-003
```

*View the approving Pull Request:*

* Open the tagged commit in GitHub → click “Pull Request” link to see review and approval metadata.

These records demonstrate full compliance with ISO 9001 §7.5.2–7.5.3 and ISO 13485 §4.2.4.

---

## **5. Records and Retention**

| Record Type                             | Location                   | Retention  |
| --------------------------------------- | -------------------------- | ---------- |
| Controlled Markdown Files               | GitHub main branch         | Indefinite |
| Tags (approved revisions)               | GitHub repository          | Indefinite |
| Pull Requests (review/approval records) | GitHub                     | Indefinite |
| Commit history (traceability)           | Git repository             | Indefinite |
| Archived/Obsolete Files                 | `/archive/` or Git history | Indefinite |

All Git metadata serves as the official QMS record of document control activities.

---

## **6. References**

* SOP – Document Control (r4)
* SOP – Identification and Traceability (r3)
* SOP – Change Control (r3)
* WI – GitHub Branch & Pull Request Management
* ISO 9001:2015, Clauses 7.5.2 & 7.5.3
* ISO 13485:2016, Clauses 4.2.4 & 4.2.5

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                            | Approved By |
| -------- | ---------- | ------------------------------------------------------------------------------------------------ | ----------- |
| r1       | 2025-10-11 | Initial release implementing Git-based numbering and revision control                            | [Name]      |
| **r2**   | 2025-10-15 | Updated to align with new tool-agnostic SOPs; minimal header; approvals managed via PRs and tags | [Name]      |
