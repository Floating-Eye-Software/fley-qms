# **PLAN – QMS Repository Architecture and Go-Live Transition**

**Slug:** Repo-Migration-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP, Change-Control-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan  

---

## **1. Introduction**

* **Purpose:**
Define and control the transition from the Red Witch wiki-based QMS prototype to a dedicated, controlled GitHub repository (`fley-qms`) that supports branch protection, Pull Request approvals, and formal document change control.

* **Scope:**
  Organization-wide. Applies to all QMS-controlled documentation, including the Quality Manual, SOPs, Work Instructions, Templates, and Records migrated from `redwitch.wiki`.

* **Applicable Standards & Regulations:**

  * ISO 9001:2015 § 6.3 – Planning of Change
  * ISO 13485:2016 § 4.2 – Document Control
  * 21 CFR 820.40 – Document Controls

---

## **2. Quality Objectives**

* Establish a **controlled repository** (`fley-qms`) with protected `main` branch and enforced review rules.
* Preserve the **complete commit history** from the Red Witch wiki.
* Achieve **baseline sign-off** (`QMS_Baseline_r1`) by Top Management.
* Ensure **change control readiness**: no direct commits to `main`; all future edits via PR workflow.
* Separate **product website** (`redwitch`) from **QMS governance system** (`fley-qms`).

---

## **3. Quality Processes**

* **Design & Development Controls:**
  Plan and execute migration activities as controlled design changes under the *Change-Control-SOP*.
* **Configuration Management:**
  Establish protected `main` branch and enforce CODEOWNERS approvals.
* **Verification of Effectiveness:**
  Verify that Pull Request workflow, branch protection, and publication synchronization operate as intended.
* **Risk & Opportunity Management:**
  Address the limitation identified during pilot (“GitHub wikis cannot support Pull Requests”) by implementing a compliant architecture.

---

## **4. Metrics & Measurement**

| Metric                         | Target            | Measurement Method          |
| ------------------------------ | ----------------- | --------------------------- |
| Controlled repository created  | 1 (`fley-qms`)    | GitHub UI verification      |
| Branch protection enabled      | 100% (`main`)     | Review repository settings  |
| Successful migration PR merged | ≥ 1 baseline PR   | Pull Request logs           |
| Baseline tag created           | `QMS_Baseline_r1` | `git tag -l` output         |
| Verification record approved   | 1 completed issue | Go-Live Verification Record |

---

## **5. Quality Assurance Activities**

* Internal review of the `qms-setup` branch before migration PR.
* Pull Request approval by Quality Manager and Top Management.
* Post-merge verification of protection rules and `CODEOWNERS`.
* Tag creation and validation of repository integrity.
* Independent verification of migration effectiveness using checklist in Appendix A.

---

## **6. Roles & Responsibilities**

| Role                              | Responsibilities                                            | Authority                               |
| --------------------------------- | ----------------------------------------------------------- | --------------------------------------- |
| **Quality Manager**               | Approves plan, reviews configuration, and verifies baseline | Approve Go-Live PR and baseline tag     |
| **Project Owner / Administrator** | Executes migration, applies branch protection, manages tags | Manage repo settings and configurations |
| **Top Management**                | Approves baseline go-live                                   | Authorize QMS activation                |
| **Contributors**                  | Follow controlled change workflow post-go-live              | Submit PRs under Change-Control-SOP     |

---

## **7. Records & Documentation**

| Record                           | Location             | Retention |
| -------------------------------- | -------------------- | --------- |
| Controlled QMS repository        | `fley-qms`           | Permanent |
| Migration / Go-Live PR           | GitHub Pull Requests | Permanent |
| Branch protection configuration  | GitHub settings      | Permanent |
| Tag `QMS_Baseline_r1`            | Git repository       | Permanent |
| Go-Live Verification Record      | GitHub Issues        | Permanent |
| Archived `redwitch.wiki` content | Git repository       | Permanent |

---

## **8. Linkage to Execution**

* **Milestones:**
  * [QMS Foundations](https://github.com/mlehotay/redwitch/milestone/1)

* **Project Board:**
  * [FLEY QMS Kanban](https://github.com/users/mlehotay/projects/3)

* **Issues:**

  * [#28 Create Controlled QMS Repository](https://github.com/mlehotay/redwitch/issues/28)
  * [#7 - SOP: Pull Request Procedure (Change Control)](https://github.com/mlehotay/redwitch/issues/7)

* **Linked Work Instructions:**

  * [WI – GitHub-Change-Control](https://github.com/mlehotay/redwitch/wiki/GitHub-Change-Control)
  * [WI – GitHub-QMS-Setup](https://github.com/mlehotay/redwitch/wiki/GitHub-QMS-Setup)

* **Appendix:**

  * [Appendix A – Repository Migration Execution](#appendix-a--repository-migration-execution) – Defines the controlled step-by-step execution process referenced by this plan.

---

## **9. Continuous Improvement**

* The migration serves as the **first continuous improvement cycle** validating QMS configuration management.
* Capture lessons learned and review during the next Management Review.
* Update *Document-Control-SOP*  to reference `fley-qms` as the controlled document source.
* Conduct annual verification of branch protection, tagging, and access control effectiveness.

---

# **Appendix A - Repository Migration Execution**

**Linked Plan:** Repo-Migration-Plan
**Purpose:** Define controlled steps for migrating `redwitch.wiki` to `fley-qms` while preserving full commit history, setting up an empty controlled `main` branch, and enforcing branch protection and approvals via GitHub web interface.

---

## **A1. Pre-Execution Checklist**

1. Plan approved by Quality Manager and Top Management.
2. Confirm access to `redwitch.wiki` and `fley-qms` repositories.
3. Prepare `CODEOWNERS` file for `main` branch, specifying `@mlehotay` as reviewer.

---

## **A2. Migration Preparation (Preserve History and Rename Branch)**

### **Step 1: Clone the source wiki repository**

```bash
git clone https://github.com/mlehotay/redwitch.wiki.git
cd redwitch.wiki
```

---

### **Step 2: Rename `master` branch to `qms-setup`**

```bash
git branch -m master qms-setup
```

* This branch will serve as the historical import branch in the new repository.

---

### **Step 3: Add target repository as remote**

```bash
git remote add fley git@github.com:mlehotay/fley-qms.git
```

---

### **Step 4: Push `qms-setup` to target repository**

```bash
git push -u fley qms-setup
```

* Commit history is preserved.
* `qms-setup` will be read-only after go-live.

---

## **A3. Initialize Empty Controlled `main` Branch**

```bash
git checkout --orphan main
git reset --hard
git push origin main
```

* `main` is empty and ready for controlled Pull Requests only.

---

## **A4. Configure Branch Protection and CODEOWNERS via GitHub Web UI**

### **Step 1: Add `CODEOWNERS` file**

1. In the GitHub repository, navigate to `fley-qms`.
2. Go to the folder `.github` (create it if it doesn’t exist).
3. Create a file named `CODEOWNERS` with the following content:

```
/* @mlehotay
```

4. Commit directly to the `main` branch.

---

### **Step 2: Enable branch protection**

1. In the repository, go to **Settings → Branches → Branch protection rules**.
2. Click **Add rule** and enter `main` as the branch name pattern.
3. Enable the following options:

   * **Require pull request reviews before merging**

     * Set **Required approving reviewers** to **1**
     * Require review from **CODEOWNERS**
   * **Require status checks to pass before merging** (optional if you have CI)
   * **Include administrators** (enforce rules even for admins)
   * **Restrict who can push to matching branches** → add **mlehotay** only
   * **Disallow force pushes**
   * **Disallow deletions**
4. Click **Create** to save the rule.

---

## **A5. Go-Live Pull Request**

1. Create a Pull Request:

   * **Base:** `main`
   * **Compare:** `qms-setup`
   * **Title:** “FLEY QMS Go-Live – Initial Controlled Baseline”
   * **Description:** “Migration of Red Witch wiki content with full history. Controlled under QMS change control plan.”
2. Review & merge PR:

   * Approver: `mlehotay`
   * Merge via **Merge Commit** to retain full commit history.

---

## **A6. Tag Baseline**

```bash
git tag QMS_Baseline_r1
git push origin QMS_Baseline_r1
```

* Establishes official QMS baseline.

---

## **A7. Post-Merge Configuration**

* Verify branch protection is active in the GitHub web UI.
* Archive or lock the `qms-setup` branch to prevent direct edits.
* Create a **Go-Live Verification Record** issue including:

  * PR number
  * Tag name (`QMS_Baseline_r1`)
  * Approval date
  * Verification checklist results

---

## **A8. Verification Checklist**

| Verification Item             | Evidence            |
| ----------------------------- | ------------------- |
| Controlled repo created       | GitHub UI           |
| Branch protection active      | Settings screenshot |
| Migration PR merged           | PR log              |
| Tag `QMS_Baseline_r1` created | `git tag -l`        |
| Verification record approved  | GitHub Issue        |

---

## **A9. Post-Go-Live Branch Model**

| Branch      | Purpose                            |
| ----------- | ---------------------------------- |
| `main`      | Controlled, empty QMS baseline     |
| `qms-setup` | Historical wiki import (read-only) |
| `change/*`  | Active change requests             |
| `feature/*` | New processes or documents         |
| `fix/*`     | Minor corrections                  |

*All changes to `main` require approved Pull Requests.*

---

## **A10. Records and Retention**

| Record                   | Location             | Retention |
| ------------------------ | -------------------- | --------- |
| Go-Live PR and approvals | GitHub Pull Requests | Permanent |
| Tag `QMS_Baseline_r1`    | Repository tags      | Permanent |
| Branch protection config | Repo settings        | Permanent |
| Verification Record      | GitHub Issues        | Permanent |
| Archived `redwitch.wiki` | `qms-setup` branch   | Permanent |

---

### ✅ **Outcome**

* `fley-qms` repository created with **full history preserved**.
* Empty `main` branch is protected and controlled.
* `qms-setup` branch retains historical commits.
* Only `mlehotay` can approve Pull Requests.
* Baseline `QMS_Baseline_r1` approved by Top Management.
* QMS operational under formal change control.
