## 🧭 **Work Instruction (WI): GitHub Pull Request and Branch Management**

**Document Number:** WI-005
**Effective Date:** 2025-10-11
**Revision:** r1
**Related SOP:** Change Control
**Controlled Source:** [GitHub Repository URL]

---

### **1. Purpose**

To define the standardized method for proposing, reviewing, approving, and implementing changes to controlled QMS documents and records using GitHub branches and Pull Requests (PRs).

---

### **2. Scope**

Applies to all repositories containing QMS-controlled documentation or configuration data managed through GitHub.

---

### **3. Responsibilities**

| Role                                 | Responsibilities                                                                |
| ------------------------------------ | ------------------------------------------------------------------------------- |
| **Change Requestor**                 | Create and document proposed changes using a GitHub Issue and corresponding PR. |
| **Reviewer/Approver**                | Evaluate changes for completeness, accuracy, and compliance before approval.    |
| **Change Control Coordinator (CCC)** | Verify the PR includes appropriate links, approvals, and tags before merging.   |
| **Quality Manager**                  | Ensure adherence to approval requirements and retention of all records.         |

---

### **4. Procedure**

#### **4.1 Initiating a Change**

1. Create a **GitHub Issue** to describe the proposed change, including:

   * Change reason and summary
   * Impact assessment
   * Related SOPs, WIs, or CAPAs

2. Create a **branch** from `main`:

   ```
   git checkout -b change/update-document-control
   ```

3. Implement changes in the branch.

4. Commit updates with a clear message referencing the CR Issue:

   ```
   git commit -m "Fixes #42 – Updated numbering and revision control section"
   ```

---

#### **4.2 Submitting for Review**

1. Open a **Pull Request** (PR) to merge the branch into `main`.
2. PR title should summarize the change, e.g.:

   ```
   SOP-004_r2 – Updated review and tagging section
   ```
3. PR description must include:

   * Link to CR Issue (e.g., `Fixes #42`)
   * Summary of changes
   * Any validation or verification results (if applicable)

---

#### **4.3 Review and Approval**

1. Reviewers evaluate the PR using GitHub’s review features:

   * “Approve” = formal approval
   * “Request changes” = return to author for updates

2. Required reviewers are determined by the repository’s `CODEOWNERS` or approval matrix.

3. Approval in GitHub constitutes an **electronic signature** in compliance with 21 CFR Part 11 and ISO 13485 requirements.

---

#### **4.4 Merging and Tagging**

1. Once approved:

   * Merge the PR into the `main` branch.
   * Create a Git tag corresponding to the new revision (e.g., `SOP-004_r2`).
   * Push the tag:

     ```bash
     git push origin SOP-004_r2
     ```
2. The tag represents the official approved version.
3. Update the document header to reflect the new revision and effective date.

---

#### **4.5 Branch and Access Control**

1. The `main` branch is **protected**:

   * Requires PR review before merge
   * Prevents direct commits
   * Restricts deletion or force-push operations

2. All draft work occurs in feature branches:

   ```
   feature/update-sop-004
   ```

3. Obsolete branches may be deleted after the PR is merged.

---

#### **4.6 Handling Unintended Changes**

1. If an unapproved commit appears in `main`, open a CAPA Issue immediately.
2. Document:

   * Nature of the unintended change
   * Root cause analysis
   * Corrective and preventive actions
3. Revert the change via corrective PR and tag the corrected revision.

---

#### **4.7 Records and Retention**

| Record Type    | Description                  | Location   | Retention |
| -------------- | ---------------------------- | ---------- | --------- |
| GitHub Issues  | Change requests and CAPAs    | GitHub     | Permanent |
| Pull Requests  | Change review and approval   | GitHub     | Permanent |
| Commit history | Complete change log          | Repository | Permanent |
| Tags/releases  | Approved version identifiers | GitHub     | Permanent |

---

### **5. References**

* SOP – Change Control
* SOP – Document Control
* SOP – Identification and Traceability
* WI – Git Version Control and Traceability
* ISO 9001:2015, Clauses 6.3, 7.5, 8.5.6
* 21 CFR Part 11 – Electronic Records and Signatures

---

### **6. Revision History**

| Revision | Date       | Description of Change                                              | Approved By |
| -------- | ---------- | ------------------------------------------------------------------ | ----------- |
| r1       | 2025-10-11 | Initial release integrating Git-based change and approval workflow | [Name]      |
