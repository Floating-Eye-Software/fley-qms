## **Work Instruction (WI): GitHub Pull Request and Branch Management**

**Document Number:** [To be assigned]
**Effective Date:** [To be assigned]
**Revision:** [To be assigned]
**Related SOP:** Change Control

---

### **1. Purpose**

To define the process for proposing, reviewing, approving, and implementing changes to controlled information using GitHub branches and Pull Requests (PRs), ensuring changes are authorized, traceable, and properly recorded.

---

### **2. Scope**

Applies to all repositories containing QMS documents, processes, or controlled outputs subject to change control requirements.

---

### **3. Responsibilities**

| Role                                 | Responsibilities                                                                           |
| ------------------------------------ | ------------------------------------------------------------------------------------------ |
| **Change Requestor**                 | Initiates a change by creating a branch and PR with a clear description and justification. |
| **Reviewer/Approver**                | Reviews the change for accuracy, completeness, and impact.                                 |
| **Change Control Coordinator (CCC)** | Ensures changes follow approval workflows and that records are properly maintained.        |

---

### **4. Procedure**

#### **4.1 Initiating a Change**

1. Create a **GitHub Issue** describing the proposed change. Include:

   * Reason for change
   * Impact assessment (if applicable)
   * Linked related SOPs or records
2. Create a **branch** from `main` to implement the change.

   * Branch naming convention: `change/<short-description>`
   * Example: `change/update-traceability-wi`
3. Commit updates with clear, descriptive commit messages referencing the Issue (e.g., `Fixes #27 – Updated review workflow section`).

---

#### **4.2 Review and Approval**

1. Submit a **Pull Request (PR)** to merge the change into `main`.
2. Assign required reviewers according to repository CODEOWNERS or approval matrix.
3. Reviewers assess:

   * Impact on related processes or documents
   * Compliance with QMS and SOPs
   * Clarity and adequacy of documentation
4. Approval is provided through GitHub’s PR approval feature, which serves as an authenticated digital signature.
5. Once approved, the PR is merged into `main` by an authorized user (typically the CCC or Process Owner).

---

#### **4.3 Implementation and Tagging**

1. After merging, create a new **Git tag** representing the approved revision (e.g., `SOP-002_r3`).
2. The tag must be referenced in the document header and recorded in the revision history.
3. If the change is significant, update the GitHub Wiki and/or notify affected users.

---

#### **4.4 Control of Unintended Changes**

1. Unintended or unauthorized commits to `main` are prevented through branch protection.
2. If an unintended change occurs, it must be reviewed via a corrective Pull Request referencing a CAPA Issue.
3. The correction must include root cause and preventive actions documented in the linked Issue.

---

#### **4.5 Records**

| Record Type               | Location      | Retention |
| ------------------------- | ------------- | --------- |
| Issues (change requests)  | GitHub Issues | Permanent |
| Pull Requests (approvals) | GitHub        | Permanent |
| Commit history            | Repository    | Permanent |
| Tags/releases             | GitHub        | Permanent |

---

### **5. References**

* Change Control SOP
* Documented Information Control SOP
* Identification and Traceability SOP
* GitHub Documentation ([docs.github.com](https://docs.github.com))

---

### **6. Revision History**

| Revision | Date   | Description of Change | Approved By |
| -------- | ------ | --------------------- | ----------- |
| 0        | [Date] | Initial Release       | [Name]      |
