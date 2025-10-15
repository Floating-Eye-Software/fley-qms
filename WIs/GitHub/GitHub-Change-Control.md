# 🧭 **Work Instruction (WI): GitHub Pull Request and Branch Management**

**Document Number:** WI-005
**Revision:** r2
**Related SOPs:** Change Control, Document Control, Identification and Traceability
**Controlled Source:** [GitHub Repository URL]

---

## **1. Purpose**

To define the standardized method for proposing, reviewing, approving, and implementing changes to QMS-controlled documents and configurations using GitHub Issues, branches, and Pull Requests (PRs).
This Work Instruction implements the Change Control process in a Git-based environment.

---

## **2. Scope**

Applies to all repositories containing QMS-controlled documentation or configuration data managed in GitHub, including Standard Operating Procedures (SOPs), Work Instructions (WIs), Policies (POLs), and Records (RECs).

---

## **3. Responsibilities**

| Role                                 | Responsibilities                                                                           |
| ------------------------------------ | ------------------------------------------------------------------------------------------ |
| **Change Requestor (Author)**        | Initiates the change via a GitHub Issue and creates a branch implementing the update.      |
| **Reviewer / Approver**              | Reviews PRs for completeness, accuracy, and compliance before approval.                    |
| **Change Control Coordinator (CCC)** | Ensures each PR includes the correct Issue references, approvals, and tags before merging. |
| **Quality Manager**                  | Oversees adherence to change control and ensures retention of all electronic records.      |

---

## **4. Procedure**

### **4.1 Initiating a Change**

1. Open a **GitHub Issue** to serve as the Change Request (CR). Include:

   * Purpose and reason for change
   * Impact and risk assessment
   * Related SOPs, WIs, or CAPAs

2. Create a **branch** from the protected `main` branch:

   ```bash
   git checkout -b change/update-document-control
   ```

3. Implement the required changes in the branch.

4. Commit with a clear message referencing the CR:

   ```bash
   git commit -m "Fixes #42 – Updated document numbering section per new SOP"
   ```

Each commit and Issue reference provides traceability per ISO 9001 §7.5.3 and ISO 13485 §4.2.4.

---

### **4.2 Submitting for Review**

1. Open a **Pull Request (PR)** to merge the change branch into `main`.

2. PR title should clearly identify the document and revision, for example:

   ```
   SOP-004_r2 – Updated review and tagging procedure
   ```

3. The PR description must include:

   * Link to the related Issue (CR), e.g. `Fixes #42`
   * Summary of changes
   * Verification or validation notes (if applicable)

4. The PR acts as the **formal review and approval record**.

---

### **4.3 Review and Approval**

1. Reviewers use GitHub’s built-in review tools:

   * **“Approve”** = electronic approval
   * **“Request changes”** = return to author for correction

2. Required reviewers are defined in the repository’s `CODEOWNERS` file or approval matrix.

3. Approvals within GitHub constitute **electronic signatures** in accordance with 21 CFR Part 11 and ISO 13485 §4.2.4.

4. Once all required reviewers have approved, the PR is ready to merge.

---

### **4.4 Merging and Tagging Approved Changes**

1. After approval:

   * The **Change Control Coordinator** merges the PR into the `main` branch.
   * Create a Git tag matching the document identifier and revision:

     ```bash
     git tag SOP-004_r2
     git push origin SOP-004_r2
     ```

2. The tag marks the **approved and effective revision**.

3. The **HEAD of `main`** always represents the **current approved version** published to the QMS Wiki or controlled site.

4. Approval metadata (reviewers, timestamp, linked CR, and tag) are stored automatically in GitHub and Git history — no manual “Approved By” or “Effective Date” fields are required in the document header.

---

### **4.5 Branch and Access Control**

1. The `main` branch must be **protected** to ensure control integrity:

   * PR review required before merging
   * No direct commits
   * No force pushes or branch deletions
   * Require status checks to pass (optional)

2. Draft or in-progress changes must occur in branches named by convention:

   ```
   feature/update-sop-004
   fix/typo-wi-002
   change/update-qms-template
   ```

3. After the PR is merged, branches may be deleted to reduce clutter.
   The full history remains preserved in the repository and associated PR.

---

### **4.6 Handling Unintended or Noncompliant Changes**

1. If an unauthorized change is detected in `main`, immediately:

   * Open a **CAPA Issue** referencing the affected commit or PR.
   * Document the event, impact, and root cause.

2. Revert the change using a corrective PR, referencing the CAPA:

   ```bash
   git revert <commit-hash>
   ```

3. Tag the corrected version (e.g., `_r3`) and close the CAPA once verified.

---

### **4.7 Records and Retention**

| Record Type             | Description                                                | Location            | Retention |
| ----------------------- | ---------------------------------------------------------- | ------------------- | --------- |
| GitHub Issues           | Change Requests (CRs), CAPAs, and linked documentation     | GitHub              | Permanent |
| Pull Requests           | Review, approval, and merge record (electronic signatures) | GitHub              | Permanent |
| Commits                 | Change implementation history                              | GitHub Repository   | Permanent |
| Tags                    | Approved revision identifiers                              | GitHub              | Permanent |
| Branch protection rules | Configuration record of controls                           | Repository Settings | Permanent |

The GitHub system itself serves as the **record of change control**, approval, and traceability.

---

## **5. Integration with Related Procedures**

This WI implements and interfaces with:

* **SOP – Change Control:** Defines system-level requirements for evaluating, approving, and implementing changes.
* **SOP – Document Control:** Establishes that the HEAD of `main` is the controlled source.
* **WI – GitHub Version Control and Traceability:** Provides technical traceability and audit commands.

---

## **6. References**

* SOP – Change Control (r3)
* SOP – Document Control (r4)
* SOP – Identification and Traceability (r3)
* WI – GitHub Version Control and Traceability (r2)
* ISO 9001:2015 §§6.3, 7.5.2–7.5.3, 8.5.6
* ISO 13485:2016 §4.2.4–4.2.5
* 21 CFR Part 11 – Electronic Records and Signatures

---

## **7. Revision History**

| Revision | Date       | Description of Change                                                                                                         | Approved By |
| -------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------- |
| r1       | 2025-10-11 | Initial release integrating Git-based change and approval workflow                                                            | [Name]      |
| **r2**   | 2025-10-15 | Updated to align with new SOPs; clarified PR/tag approval model, main=approved version, and eliminated manual approval fields | [Name]      |
