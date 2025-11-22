
### **2.3 Matching What Actually Worked in GitHub-Pull-Test**

The GitHub-Pull-Test run demonstrated that:

* If only **one person** belongs to `qms-approvers`, the GitHub “Approve” button is unavailable.
* **PR comments** serve as the documented approval.
* **CODEOWNERS enforcement still works**, requiring the approver to be the PR author.

Therefore include:

> **NOTE (operative rule):**
> When GitHub does not allow formal approvals due to a single user in `qms-approvers`, PR approval is documented via **PR review comments**. This serves as the QMS approval record until multiple approvers are present.

This must be documented in QA records **and** in the Change-Control WI.
