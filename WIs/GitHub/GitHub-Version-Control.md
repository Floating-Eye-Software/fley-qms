# ⚙️ **WI: GitHub Version Control and Traceability**

**Document Number:** WI-007
**Revision:** r2
**Related SOPs:** Document Control, Change Control, Identification and Traceability
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To define the standardized use of Git and GitHub for maintaining identification, version control, and traceability of all controlled QMS documents and records.
This WI implements the requirements of the SOPs through specific Git and GitHub actions.

---

## **2. Scope**

Applies to all controlled repositories, documents, configurations, and records under QMS control that use Git for version management, approval tracking, and audit traceability.

---

## **3. Responsibilities**

| Role                                 | Responsibilities                                                                                                                       |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Authors / Process Owners**         | Commit and tag updates according to approved QMS processes. Ensure commits and branches reference the appropriate Change Request (CR). |
| **Reviewers / Approvers**            | Review Pull Requests (PRs) and verify complete traceability between CRs, commits, and tags.                                            |
| **Change Control Coordinator (CCC)** | Confirm traceability data is complete before PR closure and tag creation.                                                              |
| **Quality Manager**                  | Audit repository structure, tag integrity, and traceability compliance.                                                                |

---

## **4. Procedure**

### **4.1 Version Control Model**

1. Each controlled repository must include:

   * A protected `main` branch representing **current approved revisions**.
   * Branch protection rules requiring review and approval before merging.
   * Tags representing **approved revisions** (immutable identifiers).

2. All controlled changes must be made through a **Pull Request (PR)** linked to a **Change Request (CR)**.

3. The **merged commit** and corresponding **Git tag** together serve as the official approval record.

---

### **4.2 Commit Standards**

Each commit should:

* Use descriptive messages summarizing the change.
* Reference related records:

  ```
  Fixes #23  # (Change Request or Issue)
  Related: CAPA-2025-004
  ```
* Contain only approved content relevant to the scope of the CR.

Commit history provides traceability of who made each change, when, and why.

---

### **4.3 Viewing Revision History for a Single File**

To demonstrate document-level traceability:

```bash
git log --follow --pretty=format:"%h %ad %an %s" --date=iso path/to/document.md
```

This shows:

* Commit hash (unique ID)
* Author
* Date/time
* Commit message

The `--follow` flag ensures full history even across file renames or moves.

---

### **4.4 Viewing Repository-Wide History**

To view all commits in chronological order:

```bash
git log main --pretty=format:"%h %ad %an %s" --date=iso
```

Use filters to isolate specific branches or folders as needed.

---

### **4.5 Approved Revisions (Tags)**

Tags represent **formally approved revisions**.
To list all approved versions:

```bash
git for-each-ref --format="%(refname:short)  %(taggerdate:iso)" refs/tags
```

Each tag is:

* Named to match the document and revision (e.g., `SOP-006_r2`)
* Created only after PR approval and merge
* Immutable once pushed

---

### **4.6 Retrieving an Approved Revision**

To view or restore a specific approved revision:

```bash
git checkout tags/SOP-006_r2
```

This provides the exact approved content for audit, review, or controlled reproduction.

---

### **4.7 Verifying Approval and Integrity**

To view the tag metadata:

```bash
git show SOP-006_r2
```

Displays:

* Tagger (approver)
* Tag date (effective date)
* Linked commit hash
* Commit message (summary of change)

Together, this demonstrates:

* Identity of approver (GitHub account / PR approver)
* Approval timestamp
* Immutable cryptographic link between document and approval

---

### **4.8 Linking Commits, PRs, and CRs**

Each approved change must maintain traceability between:

* **Change Request (Issue ID)** – why the change occurred
* **Pull Request (PR)** – review and approval discussion
* **Git Tag** – the official approved revision

These links are established automatically when:

* PR descriptions reference Issues (e.g., `Fixes #23`)
* Tags are created on the merged commit of the PR

This chain provides full, auditable traceability from intent → implementation → approval.

---

### **4.9 Integrity and Retention**

1. Git history and tags are **permanent and immutable**; they must never be deleted or rewritten.
2. Repository settings must:

   * Enforce branch protection on `main`
   * Restrict force-pushes and tag deletions
3. Repositories are backed up and mirrored for redundancy.
4. Git metadata (commits, tags, PRs) serves as the **official QMS record** of document approval and revision history.

---

### **4.10 Audit Demonstration Commands**

| Purpose                     | Command                               | Example Output                 |
| --------------------------- | ------------------------------------- | ------------------------------ |
| Show current version        | `git describe --tags`                 | `SOP-006_r2`                   |
| List all approved revisions | `git tag -l`                          | `SOP-006_r1`, `SOP-006_r2`     |
| Show approval details       | `git show SOP-006_r2`                 | Tagger, date, commit hash      |
| Show file history           | `git log --follow path/to/SOP-006.md` | Commit-by-commit audit trail   |
| Confirm links               | PR → Tag → CR                         | Linked automatically in GitHub |

---

## **5. Records and Retention**

| Record Type                        | Location          | Retention |
| ---------------------------------- | ----------------- | --------- |
| Commits and commit history         | Git repository    | Permanent |
| Tags (approved revisions)          | GitHub repository | Permanent |
| Pull Requests (reviews, approvals) | GitHub            | Permanent |
| Change Requests (Issues)           | GitHub            | Permanent |
| Repository backups                 | Mirrored archive  | Permanent |

GitHub and Git history together form the immutable audit trail of document approval and control.

---

## **6. References**

* SOP – Document Control (r4)
* SOP – Change Control (r3)
* SOP – Identification and Traceability (r3)
* WI – GitHub Document Control
* ISO 9001:2015 §§7.5.2–7.5.3
* ISO 13485:2016 §§4.2.4–4.2.5
* 21 CFR Part 11 – Electronic Records and Signatures

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                                                   | Approved By |
| -------- | ---------- | ----------------------------------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release defining Git-based traceability and audit commands                                                      | [Name]      |
| **r2**   | 2025-10-15 | Updated to align with tool-agnostic SOPs; clarified system-managed approvals, HEAD=approved version, and immutable tags | [Name]      |
