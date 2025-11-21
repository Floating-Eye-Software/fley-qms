# 🧱 **FLEY QMS - Complete GitHub Governance Model**

Below is a **clean, harmonized specification** you can drop directly into **WI – GitHub-QMS-Setup** (or into a new subsection) so that:

1. **Branch protection is fully and unambiguously defined** in the setup process.
2. It aligns with **WI – GitHub-Change-Control** (the authoritative rule source).
3. It incorporates the **actual validated workflow** demonstrated in **GitHub-Pull-Test**.
4. It resolves the mismatch between the Setup WI and the Change-Control WI.

This gives you a *single, correct, authoritative statement of branch protection rules* that all WIs/SOPs must follow.

Below is the full set of GitHub settings required for a compliant QMS repository.
These should be documented in **WI – GitHub-QMS-Setup** and cross-referenced in **WI – GitHub-Change-Control**.

---

🎯 Summary - You must configure:  
* Branch protection → prevents uncontrolled changes to main
* Tag protection → prevents revision tampering
* Merge strategy restrictions → ensures audit trail integrity
* Team-based access control → enforces separation of duties
* CODEOWNERS → enforces approver review
* Action restrictions → prevent automation bypass
* Repo visibility / fork restrictions → protects draft content
* Disable wiki → prevents unreviewed content
* Enable audit logs → regulatory compliance

This is the complete set of required controls for an ISO/FDA-aligned GitHub-based QMS.

---
---

## **1. Controlled Branch: `main`**

The `main` branch represents the **controlled QMS baseline**.
No user may directly push to `main`.
All changes must pass through the **Pull Request–based change control workflow** defined in **WI–GitHub–Change–Control**.

---

## **2. Required Branch Protection Rules (Mandatory for Setup WI)**

Apply the following configuration in:

**Repository → Settings → Branches → Add Protection Rule → `main`**

### **2.1 Pull Request & Approval Requirements**

| Setting                                                 | Required                                      | Rationale                                                            |
| ------------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------------------- |
| **Require a pull request before merging**               | ✅                                             | Enforces controlled approval workflow                                |
| **Require approvals**                                   | ⚠️ *Enabled if organization has ≥2 approvers* | GitHub limitation when single-person org                             |
| **Required number of approvals**                        | **1**                                         | Minimum viable QMS approval                                          |
| **Require review from CODEOWNERS**                      | **✅ Required**                                | Ensures approval by QMS approvers (Quality Manager / Top Management) |
| **Dismiss stale approvals when new commits are pushed** | **Recommended**                               | Ensures final commit is reviewed                                     |
| **Require conversation resolution before merging**      | **Recommended**                               | Required in Change-Control WI                                        |

---

### **2.2 Push Restrictions**

| Rule                                           | Required                  | Notes                                         |
| ---------------------------------------------- | ------------------------- | --------------------------------------------- |
| **Restrict who can push to matching branches** | **Enabled**               | Enforcement mechanism for no-direct-commits   |
| **Allowed pushers**                            | `qms-approvers` team only | Prevents bypass except through PR merges      |
| **Allow force pushes**                         | ❌ Disabled                | Prevents rewriting of controlled history      |
| **Allow branch deletion**                      | ❌ Disabled                | Controlled branch must not be deletable       |
| **Allow bypassing branch protection**          | ❌ Disabled                | No exceptions allowed (per Change-Control WI) |

---

### **2.3 Matching What Actually Worked in GitHub-Pull-Test**

The GitHub-Pull-Test run demonstrated that:

* If only **one person** belongs to `qms-approvers`, the GitHub “Approve” button is unavailable.
* **PR comments** serve as the documented approval.
* **CODEOWNERS enforcement still works**, requiring the approver to be the PR author.

Therefore include:

> **NOTE (operative rule):**
> When GitHub does not allow formal approvals due to a single user in `qms-approvers`, PR approval is documented via **PR review comments**. This serves as the QMS approval record until multiple approvers are present.

This must be documented in QA records **and** in the Change-Control WI.

---

## **3. Branch Protection Rule Set (Copy/Paste Policy Block)**

Here is the distilled configuration block to include in your WI:

---

### **Branch Protection – Controlled QMS Baseline (`main`)**

The following protection rules **shall be applied** to the `main` branch:

1. **Require pull request before merging – ENABLED**
2. **Require review from CODEOWNERS – ENABLED**
3. **Require at least 1 approval – ENABLED when multi-reviewer org exists**
   *When only one approver exists, approvals are documented through PR comments.*
4. **Require conversation resolution before merging – ENABLED**
5. **Dismiss stale approvals – ENABLED (Recommended)**
6. **Restrict who can push – ENABLED**

   * Allowed: `qms-approvers` team **only**
   * Prevents direct commits by authors or contributors
7. **Do not allow bypassing branch protections – ENABLED**
8. **Force pushes – DISABLED**
9. **Branch deletion – DISABLED**

These combined controls ensure that **all edits to controlled QMS content require CODEOWNER (QMS Approver) review** and enter the baseline only through an approved Pull Request, preserving full traceability.

---

## **4. Workflow Alignment Summary (for your document narrative)**

To resolve inconsistencies across documents:

### **WI–GitHub-QMS-Setup must state:**

* How to configure the branch protection settings.
* That protection must match **WI–GitHub-Change-Control**.
* That `main` is initialized empty and protected *before* any controlled documents are merged.

### **WI–GitHub-Change-Control remains the authoritative policy:**

* Defines the PR approval workflow.
* Defines metadata, tags, and review requirements.
* Defines the rule that **all controlled changes must use a PR**.

### **GitHub-Pull-Test provides the validated implementation evidence:**

* Demonstrates the exact workflow that works with GitHub’s constraints.
* Shows how approvals are documented when GitHub refuses to display the “Approve” button.
* Confirms the Change-Control WI is technically enforceable.

---

# ✅ Recommended Final Integration into WI – GitHub-QMS-Setup

Add a new section:

---

## **5.x Branch Protection Configuration (Mandatory QMS Control)**

*(Insert the “Branch Protection – Controlled QMS Baseline (`main`)" block.)*

---

## **5.x Dependencies and Alignment**

*These settings enforce the workflow defined in **WI–GitHub–Change–Control** and validated in **GitHub-Pull-Test**.
All future changes to controlled QMS documents must enter `main` via Pull Request review with enforced CODEOWNERS approvals. Direct pushes to `main` are prohibited.*

---
---

# 1. **Merge Strategy Restrictions**

**Settings → General → Pull Requests**

Set:

| Setting                   | Required     | Reason                                              |
| ------------------------- | ------------ | --------------------------------------------------- |
| ✔ **Allow merge commits** | **Required** | Preserves full audit trail                          |
| ❌ Squash merging          | **Disable**  | Merges hide intermediate history                    |
| ❌ Rebase merging          | **Disable**  | Rewrites commits; violates controlled recordkeeping |

This matches the workflow validated in **GitHub-Pull-Test**.

---

# 2. **Repository Visibility & Access Control**

You should set:

| Setting                            | Required                       | Reason                                       |
| ---------------------------------- | ------------------------------ | -------------------------------------------- |
| **Repository visibility: Private** | Required                       | Ensures QMS confidentiality & draft control  |
| **Manage access using teams**      | `qms-authors`, `qms-approvers` | Required for separation of duties            |
| **Admin bypass: disable**          | Required                       | Prevents accidental override of QMS controls |
| **Restrict forking**               | Recommended                    | Avoids uncontrolled clones of draft content  |

---

# 3. **Branch Protection (already aligned earlier)**

You already have:

✔ Require PRs
✔ Require CODEOWNERS
✔ No direct pushes
✔ No bypass
✔ No force pushes
✔ Require conversation resolution

Two more recommended settings:

| Setting                                 | Reason                                                 |
| --------------------------------------- | ------------------------------------------------------ |
| ✔ **Require linear history = Disabled** | Allows merge commits, required for auditability        |
| ✔ **Require status checks = Optional**  | If you add linters or markdown schema validation later |

---

# 4. **Repository Content Controls**

### **4.1 CODEOWNERS Enforcement**

Your current:

```
* @Floating-Eye-Software/qms-approvers
```

is correct.

To make it complete, add:

```
.github/ @Floating-Eye-Software/qms-approvers
*.md @Floating-Eye-Software/qms-approvers
```

This ensures:

* All templates
* All documents
* All config
* All workflows

are protected.

---

### **4.2 Protected default branch**

Mandatory:

| Setting                    | Required    |
| -------------------------- | ----------- |
| Default branch = `main`    | Required    |
| Lock other legacy branches | Recommended |

---

### **4.3 Disable wiki & projects unless controlled**

In **Settings → Features**:

| Feature      | Required                              |
| ------------ | ------------------------------------- |
| **Wiki**     | OFF                                   |
| **Projects** | Optional (you use org-level projects) |
| **Issues**   | ON (required for QMS workflows)       |

Wiki must be off because **wiki edits are not PR-controlled**.

---

# 5. **Actions / Workflows Security**

Even if you don’t use actions yet, set:

| Setting                                                           | Required |
| ----------------------------------------------------------------- | -------- |
| Disable “Allow GitHub Actions to create or approve pull requests” | Required |
| Disable “Allow GitHub Actions to bypass rules”                    | Required |

This prevents automation from bypassing QMS approvals.

---

# 6. **Audit Log Availability (Org-level)**

Not a repo setting, but required for compliance:

✔ Ensure GitHub **Organization Audit Log** is enabled
✔ Retain logs for minimum retention period (5 years typical for ISO; 2 for FDA)

This is automatic for paid orgs.

---

# 7. **Required Guidance in the WI**

Your Work Instructions must add a subsection:

### **Tag Protection Rules – Required Configuration**

Add the two tag protection rules above, and include:

> **All controlled document revisions are identified using Git tags.
> Tag protection rules shall prevent modification or deletion of these tags, ensuring permanent and immutable revision records per Document-Control-SOP.**

This links GitHub configuration to QMS document control requirements.

---
