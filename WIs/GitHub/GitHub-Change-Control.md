# **WI – GitHub Pull Request and Branch Management**

**Slug:** GitHub-Change-Control
**Revision:** r1
**Effective Date:** [YYYY-MM-DD]
**Related SOP:** Change-Control-SOP
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-Change-Control

---

## **1. Purpose**

To define the standardized method for proposing, reviewing, approving, and implementing changes to QMS-controlled documents and configurations using GitHub Issues, branches, and Pull Requests (PRs).

This Work Instruction implements the Change Control SOP within a Git-based environment.

---

## **2. Scope**

This WI applies to all repositories containing QMS-controlled documentation or configuration data managed in GitHub, including Standard Operating Procedures (SOPs), Work Instructions (WIs), Templates (TPLs), and Records (RECs).

---

## **3. References**

* SOP – Change Control
* SOP – Document Control
* WI – GitHub–QMS–Setup
* ISO 9001:2015 §§6.3, 7.5.3
* 21 CFR Part 11

---

## **4. Responsibilities**

| Role                                 | Responsibilities                                                                          |
| ------------------------------------ | ----------------------------------------------------------------------------------------- |
| **Change Requestor (Author)**        | Initiates the change through a GitHub Issue and implements updates in a dedicated branch. |
| **Reviewer / Approver**              | Reviews and approves PRs for completeness, accuracy, and compliance before merge.         |
| **Change Control Coordinator (CCC)** | Verifies correct Issue linkage, approvals, and tags before merging.                       |
| **Quality Manager**                  | Ensures adherence to the change control process and maintains record integrity in GitHub. |

---

## **5. Procedure**

### **5.1 Initiating a Change**

1. Open a **GitHub Issue** to serve as the Change Request (CR).
   Include:

   * Purpose and justification for change
   * Impact and risk assessment
   * References to affected SOPs, WIs, or CAPAs

2. Create a new **branch** from the protected `main` branch to implement the change:

   ```bash
   git checkout -b change/update-document-control
   ```

3. Implement and test changes as needed.

4. Commit with a descriptive message referencing the Issue number:

   ```bash
   git commit -m "Fixes #42 – Updated document identification process"
   ```

> Each commit referencing an Issue provides traceability and establishes a record of implementation activity.

---

### **5.2 Submitting for Review**

1. Open a **Pull Request (PR)** to merge the change branch into `main`.
2. The PR title must clearly identify the document and revision, for example:

   ```
   WI-GitHub-Change-Control_r2 – Revised PR procedure
   ```
3. The PR description must include:

   * A link to the related Issue (CR), e.g. `Fixes #42`
   * A concise summary of the proposed changes
   * Any relevant testing, verification, or validation notes
4. The PR serves as the **formal review and approval record** for the change.

---

### **5.3 Review and Approval**

1. Reviewers provide comments or approvals directly in GitHub using the review tools:

   * **“Approve”** = electronic approval
   * **“Request changes”** = return to author for correction

2. Required reviewers are designated in the repository’s `CODEOWNERS` file.

3. GitHub approval actions constitute **electronic signatures** under 21 CFR Part 11 and ISO 13485 §4.2.4.

4. Once all required approvals are complete, the PR is ready for merge.

---

### **5.4 Merging and Tagging Approved Changes**

1. After approval, the **Change Control Coordinator (CCC)** performs the merge:

   * Confirm all required approvals are present.
   * Merge the PR into the protected `main` branch using **“Squash and Merge”** or **“Merge Commit”** (per repository policy).

2. Create a Git **tag** to mark the approved and effective revision:

   ```bash
   git tag GitHub-Change-Control_r2
   git push origin GitHub-Change-Control_r2
   ```

3. The tag must match the document slug and revision exactly (e.g., `Document-Control-SOP_r5`).

4. Each tag represents a controlled, approved, and effective revision.

5. Tags are **immutable** — do **not** delete or reuse them.

6. The **HEAD of `main`** always represents the **current approved version** displayed on the QMS Wiki.

> The PR, merge commit, and associated tag together form the complete electronic approval and effective-date record.

---

### **5.5 Branch and Access Control**

1. The `main` branch must be **protected** to ensure data integrity:

   * Require PR reviews before merging
   * Disallow direct commits
   * Disallow force pushes and branch deletions
   * Require passing status checks (if configured)

2. Branch naming conventions promote traceability:

   ```
   change/update-sop-004
   fix/typo-wi-002
   feature/new-qms-template
   ```

3. After merge, branches may be deleted to maintain repository hygiene.
   All history remains traceable in Git logs and the closed PR.

---

### **5.6 Handling Unauthorized or Noncompliant Changes**

1. If an unapproved or incorrect change is discovered in `main`:

   * Immediately open a **CAPA Issue** referencing the affected commit or PR.
   * Document the event, impact, and corrective action.

2. Revert the unauthorized change using a new PR that references the CAPA:

   ```bash
   git revert <commit-hash>
   ```

3. After verification and approval, merge the corrective PR and create a new tag (e.g., `_r3`).

4. Close the CAPA when corrective actions are verified as effective.

---

## **6. Integration with Related Procedures**

This WI interfaces with and supports:

* **SOP – Change Control:** Defines evaluation and approval requirements for controlled changes.
* **SOP – Document Control:** Establishes that `main` and its tags represent approved source records.
* **WI – GitHub Version Control** Provides commands and audit methods for historical review.

---

## **7. Records and Retention**

| Record Type             | Description                                                | Location            | Retention  |
| ----------------------- | ---------------------------------------------------------- | ------------------- | ---------- |
| GitHub Issues           | Change Requests (CRs), CAPAs, and related records          | GitHub              | Indefinite |
| Pull Requests           | Review, approval, and merge record (electronic signatures) | GitHub              | Indefinite |
| Commits                 | Implementation history and traceability                    | Git repository      | Indefinite |
| Tags                    | Approved and effective revision identifiers                | GitHub              | Indefinite |
| Branch Protection Rules | Configuration record of repository controls                | Repository Settings | Indefinite |

> All GitHub metadata and configuration serve as the official QMS record of change control and approval.
