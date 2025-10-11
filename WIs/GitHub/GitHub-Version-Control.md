## ⚙️ **WI: Git Version Control and Traceability**

**Document Number:** WI-007
**Effective Date:** 2025-10-11
**Revision:** r1
**Related SOPs:** Document Control, Change Control, Identification and Traceability
**Controlled Source:** [GitHub Repository URL]

---

### **1. Purpose**

To define the standardized use of Git and GitHub for ensuring identification, version control, and traceability of QMS-controlled documents and records.

---

### **2. Scope**

Applies to all repositories, documents, and configurations managed under QMS control that utilize Git for version management and approval tracking.

---

### **3. Responsibilities**

| Role                                 | Responsibilities                                                       |
| ------------------------------------ | ---------------------------------------------------------------------- |
| **Document Authors**                 | Commit and tag changes according to approved SOPs.                     |
| **Reviewers/Approvers**              | Verify traceability between commits, tags, and CRs.                    |
| **Change Control Coordinator (CCC)** | Ensure traceability data is complete and consistent before PR closure. |
| **Quality Manager**                  | Audit version control compliance.                                      |

---

### **4. Procedure**

#### **4.1 Viewing Revision History for a Single File**

```bash
git log --follow --pretty=format:"%h %ad %an %s" --date=iso path/to/document.md
```

* `--follow` tracks renames and moves.
* Output provides commit hash, author, date, and message.
* Use this log to demonstrate traceability for audits.

---

#### **4.2 Viewing Repository-Wide History**

```bash
git log main --pretty=format:"%h %ad %an %s" --date=iso
```

Shows all repository commits in chronological order.
Can be filtered by branch or directory to isolate specific changes.

---

#### **4.3 Viewing Approved Versions**

```bash
git for-each-ref --format="%(refname:short) %(taggerdate:iso)" refs/tags
```

Lists all tags (approved revisions) with their approval timestamps.
Auditors can use this list to identify all released versions.

---

#### **4.4 Linking Changes to CRs and PRs**

Each approved change must include:

* Commit message referencing the Change Request (e.g., `Fixes #23`)
* Merge via approved PR with review signatures
* Tag matching the document number and revision (e.g., `SOP-006_r2`)

---

#### **4.5 Retrieving a Specific Approved Version**

To access an approved revision:

```bash
git checkout tags/SOP-006_r1
```

The working directory will reflect the exact approved version for audit or distribution.

---

#### **4.6 Verifying Integrity**

```bash
git show SOP-006_r1
```

Displays metadata (author, date, commit hash) proving the record’s integrity and authenticity.

---

#### **4.7 Archiving and Retention**

1. No manual deletion of historical tags or branches is permitted.
2. Repositories are backed up regularly and mirrored as read-only archives for record retention.
3. Tags and commit history serve as permanent traceability records.

---

### **5. Audit Demonstration Checklist**

| Verification Step         | Git Command                       | Output                               |
| ------------------------- | --------------------------------- | ------------------------------------ |
| Identify current version  | `git describe --tags`             | Shows current tag (e.g., SOP-006_r2) |
| View revision log         | `git log --follow path/to/doc.md` | Displays file-specific history       |
| Confirm approved revision | `git tag -l`                      | Lists all released versions          |
| Verify approver and date  | `git show <tag>`                  | Displays approval metadata           |

---

### **6. References**

* SOP – Document Control
* SOP – Change Control
* SOP – Identification and Traceability
* ISO 9001:2015 §7.5.2–7.5.3
* ISO 13485:2016 §4.2.4
* 21 CFR Part 11 – Electronic Records and Signatures

---

### **7. Revision History**

| Revision | Date       | Description of Change                                              | Approved By |
| -------- | ---------- | ------------------------------------------------------------------ | ----------- |
| r1       | 2025-10-11 | Initial release defining Git-based traceability and audit commands | [Name]      |
