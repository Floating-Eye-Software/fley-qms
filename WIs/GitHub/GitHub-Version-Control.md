# **WI - GitHub Version Control and Traceability**

**Slug:** GitHub-Version-Control  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Identification-and-Traceability-SOP   
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-Version-Control  

---

## **1. Purpose**

To define the standardized use of Git and GitHub for maintaining identification, version control, and traceability of all controlled QMS documents and records.

This WI implements the requirements of the SOPs through specific Git and GitHub actions.

---

## **2. Scope**

Applies to all controlled repositories, documents, configurations, and records under QMS control that use Git for version management, approval tracking, and audit traceability.

---

## **3. References**

* SOP – Identification and Traceability
* WI – GitHub–QMS–Setup
* 21 CFR Part 11

---

## **4. Responsibilities**

| Role                                 | Responsibilities                                                                                                                       |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Authors / Process Owners**         | Commit and tag updates according to approved QMS processes. Ensure commits and branches reference the appropriate Change Request (CR). |
| **Reviewers / Approvers**            | Review Pull Requests (PRs) and verify complete traceability between CRs, commits, and tags.                                            |
| **Change Control Coordinator (CCC)** | Confirm traceability data is complete before PR closure and tag creation.                                                              |
| **Quality Manager**                  | Audit repository structure, tag integrity, and traceability compliance.                                                                |

---

## **5. Procedure**

### **5.1 Version Control Model**

1. Each controlled repository must include:

   * A protected `main` branch representing **current approved revisions**.
   * Branch protection rules requiring review and approval before merging.
   * Tags representing **approved revisions** (immutable identifiers).

2. All controlled changes must be made through a **Pull Request (PR)** linked to a **Change Request (CR)**.

3. The **merged commit** and corresponding **Git tag** together serve as the official approval record.

---

### **5.2 Commit Standards**

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

### **5.3 Viewing Revision History for a Single File**

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

> **Audit Tip:** This command demonstrates version changes for a specific document, linking commits to CRs and PRs.

---

### **5.4 Viewing Repository-Wide History**

To view all commits in chronological order:

```bash
git log main --pretty=format:"%h %ad %an %s" --date=iso
```

Use filters to isolate specific branches or folders as needed.

> **Audit Tip:** Repository-wide history shows all changes, approvals, and commit authors.

---

### **5.5 Approved Revisions (Tags)**

Tags represent **formally approved revisions**. To list all approved versions:

```bash
git for-each-ref --format="%(refname:short)  %(taggerdate:iso)" refs/tags
```

Each tag is:

* Named to match the document and revision (e.g., `Change-Control-SOP_r2`)
* Created only after PR approval and merge
* Immutable once pushed

> **Audit Tip:** Tags serve as evidence of official approval. Use `git show <tag>` to view approver identity, date, and linked commit.

---

### **5.6 Retrieving an Approved Revision**

To view or restore a specific approved revision:

```bash
git checkout tags/Change-Control-SOP_r2
```

This provides the exact approved content for audit, review, or controlled reproduction.

> **Audit Tip:** Demonstrates obsolete or superseded revisions for historical comparison.

---

### **5.7 Verifying Approval and Integrity**

To view tag metadata:

```bash
git show Change-Control-SOP_r2
```

Displays:

* Tagger (approver)
* Tag date (effective date)
* Linked commit hash
* Commit message

> **Audit Tip:** This proves the identity of the approver, the timestamp of approval, and the immutable link between the document and its approval.

---

### **5.8 Linking Commits, PRs, and CRs**

Each approved change must maintain traceability between:

* **Change Request (Issue ID)** – reason for change
* **Pull Request (PR)** – review and approval discussion
* **Git Tag** – official approved revision

These links are established automatically when PR descriptions reference Issues (e.g., `Fixes #23`) and tags are created on the merged commit.

> **Audit Tip:** This shows a full, auditable trail from intent → implementation → approval.

---

### **5.9 Integrity and Retention**

1. Git history and tags are **permanent and immutable**; never delete or rewrite.

2. Repository settings must:

   * Enforce branch protection on `main`
   * Restrict force-pushes and tag deletions

3. Repositories are backed up and mirrored for redundancy.

4. Git metadata (commits, tags, PRs) serves as the **official QMS record** of document approval and revision history.

---

### **5.10 Audit Demonstration**

The following commands demonstrate that documents are **controlled, approved, traceable, and current**:

| Audit Objective                | Command / Git Evidence                                              | Notes                                            |
| ------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------ |
| Current approved version       | `git checkout main`<br>`git describe --tags`<br>`git show <tag>`    | Verify the latest approved revision              |
| Revision history               | `git log --follow <file>`<br>`git log --merges <file>`              | Show version changes and approvals               |
| Change / ECO log               | `git log --grep="CR-"`                                              | Demonstrate CR → PR → commit → tag traceability  |
| Master Document List           | `ls SOP-*; ls WI-*`<br>`git tag --list "SOP_*"`                     | Confirm all documents are under revision control |
| Traceability of changes        | `git show <commit>`<br>`git show <tag>`                             | Show links between CRs, PRs, and tags            |
| Obsolete / superseded versions | `git checkout <old-tag>`<br>`git diff <old-tag> main`               | Demonstrate historical version and replacement   |
| CAPA / corrective actions      | `git log --grep="CAPA-"`<br>`git show <commit>`                     | Show resolution of unintended changes            |
| Retention & backup             | `git tag --list`<br>`git log --all --pretty=format:"%h %ad %an %s"` | Prove history is complete and permanent          |

> **Tip:** Include PR discussion in GitHub as evidence of reviewer/approver actions.

---

## **6. Records and Retention**

| Record Type                        | Location          | Retention |
| ---------------------------------- | ----------------- | --------- |
| Commits and commit history         | Git repository    | Permanent |
| Tags (approved revisions)          | GitHub repository | Permanent |
| Pull Requests (reviews, approvals) | GitHub            | Permanent |
| Change Requests (Issues)           | GitHub            | Permanent |
| Repository backups                 | Mirrored archive  | Permanent |

GitHub and Git history together form the immutable audit trail of document approval and control.
