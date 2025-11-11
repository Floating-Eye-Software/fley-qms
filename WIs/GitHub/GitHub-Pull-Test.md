---
slug: GitHub-Pull-Test
revision: r1
type: REF
status: draft
effective: null
related:
  - redwitch#7
  - redwitch#29
  - fley-qms#16
  - fley-qms#19
---

## **Walkthrough Plan – Pull Request Process (Supports Implementation of redwitch#7)**

### **Execution Context: redwitch#29 (Implements fley-qms#16, fley-qms#19)**

### **Purpose**

This walkthrough demonstrates the **Pull Request–based change control process** that will inform and finalize the implementation of **redwitch#7 – Establish Pull Request Procedure**.

It executes **redwitch#29 – Establish GitHub Project Views for QMS Workflows**, integrating the related improvements:

* **fley-qms#16** – Establish recurring Management Review schedule and Action Tracker
* **fley-qms#19** – Adopt YAML Headers for all controlled documents

The outcome of this walkthrough will confirm that the Work Instructions, templates, and configuration files can be fully managed through the standardized PR workflow under the FLEY QMS.

This document serves as a *reflexive process validation run* demonstrating and refining the PR-based change control workflow. The steps defined here both execute and inform the evolving process definition under *redwitch#7*. Finalized procedures will integrate validated elements from this run.

---

### **1. Prepare Working Branch**

```bash
git checkout main
git pull
git checkout -b change/establish-qms-workflows
git checkout feature/qms-foundation -- .github .gitignore Templates/Header-Template.md WIs/GitHub/GitHub-Document-Control.md WIs/GitHub/GitHub-QMS-Operations.md WIs/GitHub/GitHub-QMS-Setup.md
```

> **Purpose:** Bring finalized WIs and configuration files from your foundation branch into a controlled change branch for Pull Request review.

---

### **2. Commit with Issue Traceability**

```bash
git add .
git commit -m "Implements redwitch#29 (child of redwitch#7); integrates fley-qms#16, fley-qms#19 – Walkthrough of standardized QMS workflows"
git push origin change/establish-qms-workflows
```

> This commit establishes the traceable relationship between the demonstration branch, the child issue (#29), and its parent (#7).

---

### **3. Open Pull Request**

Open a PR using the template (`TPL-GH-Pull-Request`) and complete these fields:

| Section  | Entry |
| -------- | ----- |
| **Linked Change Request Issue**  | `Fixes redwitch#29 (child of redwitch#7)` |
| **Summary of Proposed Changes** | Updates all GitHub Work Instructions and templates for standardized QMS workflows; integrates Management Review linkages and YAML header adoption. |
| **Verification / Validation Notes** | YAML headers validate via linter; PR process verified against WI–GitHub–Change–Control; all CODEOWNERS rules enforced in branch protection. |

---

### **4. Review and Approve**

**Review Scope:**

* Confirm YAML headers follow the new template (`slug`, `revision`, `type`, `status`, `effective`, `controlled_source`).
* Verify cross-references between:

  * *WI–GitHub–Document–Control*
  * *WI–GitHub–Change–Control*
  * *WI–GitHub–QMS–Setup*
  * *WI–GitHub–QMS–Operations*
* Ensure `effective` fields are `null` (draft) prior to approval.
* Confirm `.github` configuration and templates match approved workflow definitions.

**Approvers:** Quality Manager + DCC per `CODEOWNERS`.

> This step validates the Pull Request review process itself — the approvals and metadata edits performed here demonstrate how controlled document changes will be managed going forward under redwitch#7.

---

### **5. Finalize Metadata Before Merge**

After approval, update document headers to mark as approved and effective:

```bash
sed -i 's/status: draft/status: approved/' WIs/GitHub/*.md
```

Then manually update YAML headers to include:

```yaml
effective: 2025-11-11
```

Commit and push:

```bash
git add .
git commit -m "Finalize approval and effective dates for WI and template updates (redwitch#29 walkthrough)"
git push
```

---

### **6. Merge to Main**

* Merge via Pull Request (do **not** squash — preserve commit signatures).
* Verify all required CODEOWNERS approvals and automated checks pass.
* The merged PR serves as the electronic approval record for this walkthrough.

---

### **7. Tag All Document Revisions (Per WI–GitHub–Change–Control §5.4)**

After the merge, tag all approved controlled files as individual revision identifiers:

```bash
git checkout main
git pull

# Core configuration and templates
git tag CFG-GH-CODEOWNERS_r1
git tag TPL-GH-Change-Request_r1
git tag CFG-GH-Issue-Templates_r1
git tag TPL-GH-Management-Review_r1
git tag TPL-GH-Pull-Request_r1
git tag CFG-gitignore_r1
git tag Header-Template_r2

# Work Instructions
git tag GitHub-Document-Control_r2
git tag GitHub-QMS-Operations_r2
git tag GitHub-QMS-Setup_r2

git push origin --tags
```

> Each tag represents an **approved, immutable revision record** for its respective controlled file.

---

### **8. Outcome**

This walkthrough:

* Confirms that all QMS-controlled files (including `.github` configuration and templates) can be managed under the standardized PR approval process.
* Demonstrates compliance with **WI–GitHub–Change–Control** and **WI–GitHub–Document–Control**.
* Provides the working reference implementation that will be used to finalize **redwitch#7 – Establish Pull Request Procedure**.
