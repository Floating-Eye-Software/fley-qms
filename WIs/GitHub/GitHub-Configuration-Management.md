## 🧩 **Example 1 — Design/Development Change**

### 🎯 Scenario

You’re implementing a new feature: “Add audit logging to user authentication.”

### ⚙️ Step-by-Step Git Flow

#### **1. Start from the controlled main branch**

```bash
git checkout main
git pull origin main
```

*(This ensures you’re working on the latest approved baseline.)*

#### **2. Create a feature branch**

Use a naming convention that reflects the work unit or issue:

```bash
git checkout -b feature/audit-logging ISSUE-142
```

#### **3. Make your changes**

You edit the relevant code, documentation, or tests.

Example commits:

```bash
git add auth_service.py
git commit -m "Add audit logging for user login events (#142)"

git add tests/test_auth_audit.py
git commit -m "Add unit tests for audit logging feature"
```

Each commit represents traceable, atomic work — good for audit evidence.

#### **4. Push the branch to GitHub**

```bash
git push origin feature/audit-logging
```

#### **5. Open a Pull Request**

In GitHub:

* **Base branch:** `main`
* **Compare branch:** `feature/audit-logging`
* **Title:** “Feature: Add audit logging (#142)”
* **Description:** Include summary, related issue, and test evidence.
* Link to your Work Unit Design Output Record if you have one.

#### **6. Review and Approval**

* Reviewer checks the PR, runs CI, and adds comments if needed.
* Once satisfied, they click **“Approve”** in GitHub.

#### **7. Merge**

After approval:

* Click **Merge Pull Request** → **Squash and merge** (recommended for clarity)
* This creates one clean commit in `main`:

  ```
  Merge pull request #219 from feature/audit-logging
  ```
* GitHub automatically closes issue `#142`.

#### **8. Clean up**

```bash
git branch -d feature/audit-logging
git push origin --delete feature/audit-logging
```

#### ✅ Result

* The PR discussion + commits = your *design change record* (ISO 8.3.6 / 8.5.6).
* The merge commit is traceable evidence of review and approval.

---

## 🧾 **Example 2 — QMS Document Change (SOP Update)**

### 🎯 Scenario

You’re updating **SOP-07 Configuration Management** to add a GitHub branch protection rule.

### ⚙️ Step-by-Step Git Flow

#### **1. Start from main**

```bash
git checkout main
git pull origin main
```

#### **2. Create a branch for the document update**

```bash
git checkout -b doc/update-SOP07-branch-protection
```

#### **3. Edit the controlled QMS file**

You edit:

```
/qms/procedures/SOP-07_Configuration_Management.md
```

Add a new section:

> “Branch protection rules must require at least one approval before merging into main.”

#### **4. Commit your change**

```bash
git add qms/procedures/SOP-07_Configuration_Management.md
git commit -m "SOP-07: Add branch protection rule requirement (#CAR-24)"
```

#### **5. Push and open a Pull Request**

```bash
git push origin doc/update-SOP07-branch-protection
```

Then open a PR:

* **Base branch:** `main`
* **Compare branch:** `doc/update-SOP07-branch-protection`
* **Title:** “SOP-07 Update – Branch Protection Rules”
* **Description:**
  “Added section on GitHub branch protection per CAR-24. Reviewed by DevOps and Quality.”

#### **6. Review and Approve**

* The **Quality Manager** and **Process Owner** review it.
* They approve the PR using GitHub’s review workflow.

#### **7. Merge**

* Once approved, click **Merge Pull Request**.
* The change becomes the *controlled, approved version* of the SOP.
* The previous version remains visible in GitHub’s history.

---

## 🧠 Why This Works for ISO 9001

| ISO Clause                             | Evidence in GitHub                       |
| -------------------------------------- | ---------------------------------------- |
| **7.5.2 – Approval before issue**      | Reviewer approval in PR                  |
| **7.5.3 – Control of documents**       | Protected `main` branch + PR merge only  |
| **8.3.6 / 8.5.6 – Control of changes** | PR discussion, commits, and merge record |
| **9.1 – Performance evaluation**       | PR metrics (lead time, defects, etc.)    |

---

## ⚙️ Optional Extras for Strong Control

* Use **branch naming conventions** like `feature/`, `fix/`, `doc/`, `qms/` for traceability.
* Add a **GitHub CODEOWNERS** file to enforce correct reviewers automatically.
* Enable **branch protection rules** to *require* approvals before merging.
* Use **GitHub Actions** to generate PDF “change records” or update a revision table automatically when a PR is merged.

---

# 🧭 Overall Concept

You’ll have two key repositories:

| Repo                | Purpose                                                      | Controlled by |
| ------------------- | ------------------------------------------------------------ | ------------- |
| **`redwitch`**      | Source code, technical documentation, product design records | Dev Team & QA |
| **`redwitch.wiki`** | QMS: SOPs, policies, procedures, templates, and records      | Quality Team  |

Each repository will use **pull requests (PRs)** as the *sole* method for approving and merging controlled changes.

---

## 🧩 1. Branching Model Overview

### **Redwitch (Product / Code Repository)**

```
main                ← Production-ready, controlled baseline
├── develop          ← Integration branch (optional, for teams with multiple features)
│   ├── feature/*    ← Feature branches (e.g., feature/audit-logging)
│   ├── fix/*        ← Bugfix branches (e.g., fix/login-timeout)
│   ├── doc/*        ← Product documentation changes
│   └── hotfix/*     ← Urgent fixes applied directly to main
└── qms-design/*     ← Design control records (e.g., qms-design/new-component)
```

**Rules:**

* `main` is **protected** (requires at least one review approval).
* `develop` merges into `main` only via PR after review and testing.
* All work starts from the latest branch, never directly commits to `main`.

---

### **Redwitch.wiki (QMS Repository)**

```
main                        ← Approved and released QMS documents
├── draft/*                 ← Work-in-progress updates (e.g., draft/update-SOP07)
└── archive/*               ← Deprecated or superseded procedures
```

**Rules:**

* Only the **Quality Manager or Process Owners** can approve merges into `main`.
* Each SOP, WI, or Policy is a Markdown page (e.g., `SOP-07_Configuration_Management.md`).
* Every change goes through a **PR approval** — this is your *document control system.*

---

## 🧱 2. Example Repository Structures

### **`redwitch/`**

```
/src/
    auth/
        auth_service.py
    ui/
        dashboard.js
/tests/
    test_auth_audit.py
/docs/
    architecture.md
    user_manual.md
/qms/
    design-outputs/
        ISSUE-142_AuditLogging.md
.github/
    CODEOWNERS
    workflows/
        ci.yml
        qms_metrics.yml
```

**CODEOWNERS example:**

```
/src/ @dev-lead
/tests/ @qa-lead
/qms/design-outputs/ @quality-manager
```

---

### **`redwitch.wiki/`**

```
/SOPs/
    SOP-01_Document_Control.md
    SOP-07_Configuration_Management.md
/Policies/
    Quality_Policy.md
/Work_Instructions/
    WI-03_Work_Unit_Design_Output.md
/Templates/
    Design_Output_Template.md
/Records/
    Management_Review_Minutes_2025-10.md
```

**CODEOWNERS example:**

```
/SOPs/ @quality-manager
/Policies/ @exec-director
/Work_Instructions/ @process-owners
/Templates/ @quality-manager
```

---

## 🖼️ 3. Branching & Approval Diagram

Below is a simple conceptual diagram of how it all flows:

```
                  ┌────────────────────────┐
                  │    redwitch.wiki repo  │
                  │  (QMS Documentation)   │
                  └────────────┬───────────┘
                               │
                  Draft QMS Change Branch
                               │
        +------------------> [Pull Request]
        |                      │
        |                      ▼
        |                Review & Approval
        |                      │
        |                      ▼
        |              Merge to main branch
        |                      │
        |        QMS Doc = Approved Record (ISO 7.5)
        |______________________│


        ┌────────────────────────┐
        │     redwitch repo      │
        │ (Design & Development) │
        └────────────┬───────────┘
                     │
         Feature Branch (e.g., feature/audit-logging)
                     │
            [Pull Request → Review → Merge]
                     │
                     ▼
              main = Approved Design Output
```

---

## 🔐 4. Branch Protection Rules (Recommended)

**For `redwitch`:**

* Protect `main` and `develop` branches.
* Require:

  * 1–2 approvals before merge.
  * Passing status checks (CI).
  * Linear history (optional).

**For `redwitch.wiki`:**

* Protect `main` branch.
* Require:

  * 1 approval (Quality Manager).
  * Signed commits (optional).
  * Restrict who can push directly to `main`.

---

## 📊 5. Example Workflow Summary

| Activity                    | Repo          | Branch Type    | Reviewed By     | Merge Target | ISO Reference |
| --------------------------- | ------------- | -------------- | --------------- | ------------ | ------------- |
| Add new feature             | redwitch      | `feature/*`    | Dev Lead        | `develop`    | 8.3.6         |
| Hotfix                      | redwitch      | `hotfix/*`     | QA Lead         | `main`       | 8.5.6         |
| Update SOP                  | redwitch.wiki | `draft/*`      | Quality Manager | `main`       | 7.5.2 / 7.5.3 |
| Update QMS Template         | redwitch.wiki | `draft/*`      | Process Owner   | `main`       | 7.5.3         |
| Create Design Output Record | redwitch      | `qms-design/*` | QA or Dev Lead  | `main`       | 8.3.5         |

---

## 🧠 Summary Benefits

✅ **ISO-compliant evidence:** Every merge shows who changed what, when, and why.
✅ **Separation of concerns:** Product vs. QMS documentation are managed distinctly.
✅ **Audit-ready:** GitHub’s PRs, commits, and history serve as formal records.
✅ **No extra tooling:** Uses GitHub’s native mechanisms — lightweight but robust.

---
