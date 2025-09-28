# **Work Instruction — Records Management in GitHub**

**WI ID:** WI-GIT-RC-001
**Project:** Red Witch
**Repo(s):**

* `redwitch` → design & development records (code, commits, test results, design history)
* `redwitch.wiki` → QMS process records (approvals, meeting notes, compliance evidence)

---

## 1. **Purpose**

This Work Instruction defines *how records are created, approved, stored, and retrieved* in GitHub for the Red Witch Project, ensuring compliance with the Records SOP (`SOP-QMS-RC-001`) and regulatory requirements (ISO 9001:7.5.3, ISO 13485:4.2.5, 21 CFR 820.180).

---

## 2. **Scope**

Covers all **quality records** associated with Red Witch, including but not limited to:

* **Design & Development Records** → requirements, designs, commits, test logs
* **Review & Approval Records** → Pull Request approvals, Issue discussions, Wiki edit logs
* **Change Control Records** → Issues and PRs documenting rationale and approvals
* **Training & Meeting Records** → meeting notes, decision logs in Wiki
* **Compliance Records** → traceability matrices, QMS coverage, standards mappings

---

## 3. **Roles & Responsibilities**

* **Author** → Creates records (commits, Issues, PRs, Wiki entries).
* **Reviewer** → Confirms completeness and accuracy of records.
* **Approver** → Provides documented approval (via PR review or Wiki edit approval).
* **Repo Maintainer** → Ensures repositories are access-controlled, retention rules are enforced, and backups are maintained.

---

## 4. **Process**

### 4.1 Record Creation

1. **Code & Design Records**

   * Created automatically by Git commits in the `redwitch` repo.
   * Each commit must reference the related Issue or requirement when applicable.

2. **Review & Approval Records**

   * Created through GitHub Pull Requests.
   * Approvals and comments captured in the PR discussion thread.

3. **Change Control Records**

   * Created as Issues (describing change request, rationale).
   * Linked to Pull Requests implementing the change.

4. **Meeting & Decision Records**

   * Documented in `redwitch.wiki` under `/Records/`.
   * Linked to related Issues or PRs when relevant.

---

### 4.2 Record Approval

1. Approvals are provided electronically in GitHub (via PR approval).
2. Wiki records (e.g., meeting notes) must be reviewed by at least one other team member.
3. Approval is documented in GitHub history as part of the permanent record.

---

### 4.3 Record Storage

1. All records are stored in GitHub repositories:

   * `redwitch` → engineering/design records
   * `redwitch.wiki` → QMS/process records
2. GitHub automatically retains full history of commits, Issues, PRs, and Wiki edits.
3. Backups are maintained via GitHub and periodic local clones.

---

### 4.4 Record Retrieval

1. Records may be retrieved directly from GitHub web interface or via Git CLI.
2. Search functionality (Issues, PRs, commits) must be used to locate specific records.
3. For audits, records must be exported to PDF/Markdown and stored in `/Records/` as needed.

---

### 4.5 Record Retention

1. Records must be retained for a minimum of **10 years after product discontinuation** (ISO 13485:4.2.5, 21 CFR 820.180).
2. GitHub repositories must remain accessible during this retention period.
3. If repositories are migrated, all commit history, Issues, PRs, and Wiki content must be preserved.

---

## 5. **Records**

* **Commits** → design/development history
* **Pull Requests** → approvals, review history
* **Issues** → change requests, CAPAs, bug reports, risk logs
* **Wiki Pages** → meeting minutes, compliance evidence
* **Exported Records** → copies in `/Records/` for audits

---

## 6. **References**

* SOP-QMS-RC-001 — Records Management SOP
* SOP-QMS-DC-001 — Document Control SOP
* ISO 9001:2015 §7.5.3 (Control of documented information)
* ISO 13485:2016 §4.2.5 (Control of records)
* 21 CFR 820.180 (General requirements for records)
