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

# **Appendix A – Repository Transition Execution**

**Linked Plan:** Repo-Migration-Plan  
**Purpose:** Define the controlled technical execution steps for migrating and activating the `fley-qms` repository as the authoritative QMS configuration source.  

---

### **A1. Pre-Execution Checklist**

1. Plan approved by Quality Manager and Top Management.
2. Confirm access to source (`redwitch.wiki`) and target (`fley-qms`).
3. Verify draft branch protection and CODEOWNERS file exist.
4. Communicate go-live readiness to all approvers.

---

### **A2. Migration Preparation**

```bash
git clone https://github.com/mlehotay/redwitch.wiki.git
git clone https://github.com/mlehotay/fley-qms.git
cp -r redwitch.wiki/* fley-qms/
cd fley-qms
git checkout -b qms-setup
git add .
git commit -m "Import Red Witch QMS content"
git push origin qms-setup
```

Verify content completeness and integrity.

---

### **A3. Initialize Controlled Branch**

```bash
git checkout --orphan main
echo "# FLEY QMS" > README.md
git add README.md
git commit -m "Initialize controlled main branch"
git push origin main
```

**Configure GitHub repository settings:**

* Set `main` as the default branch
* Enable branch protection
* Require Pull Request reviews
* Disallow force pushes and direct commits
* Require `CODEOWNERS` review

---

### **A4. Go-Live Pull Request**

1. **Create PR**

   * Base: `main`
   * Compare: `qms-setup`
   * Title: “FLEY QMS Go-Live – Initial Controlled Baseline”
   * Description references this Plan and Appendix A.

2. **Review & Merge**

   * Follow *Change-Control-SOP* approval process.
   * Approvers: Quality Manager and Top Management.
   * Merge via **Merge Commit** (retain history).

3. **Tag Baseline**

   ```bash
   git tag QMS_Baseline_r1
   git push origin QMS_Baseline_r1
   ```

---

### **A5. Post-Merge Configuration**

* Verify that branch protection is enforced.
* Lock or archive the `qms-setup` branch.
* Create a **Go-Live Verification Record** issue including:

  * PR number
  * Tag name (`QMS_Baseline_r1`)
  * Approval date and approvers
  * Verification checklist results

---

### **A6. Verification Checklist**

| Verification Item             | Evidence            |
| ----------------------------- | ------------------- |
| Controlled repo created       | GitHub UI           |
| Branch protection active      | Settings screenshot |
| Migration PR merged           | PR log              |
| Tag `QMS_Baseline_r1` created | `git tag -l`        |
| Verification record approved  | GitHub Issue        |

---

### **A7. Post-Go-Live Branch Model**

| Branch      | Purpose                           |
| ----------- | --------------------------------- |
| `main`      | Controlled, approved QMS baseline |
| `qms-setup` | Archived import (read-only)       |
| `change/*`  | Active change requests            |
| `feature/*` | New processes or documents        |
| `fix/*`     | Minor corrections                 |

All changes to `main` require approved Pull Requests.

---

### **A8. Records and Retention**

| Record                   | Location             | Retention |
| ------------------------ | -------------------- | --------- |
| Go-Live PR and approvals | GitHub Pull Requests | Permanent |
| Tag `QMS_Baseline_r1`    | Repository tags      | Permanent |
| Branch protection config | Repo settings        | Permanent |
| Verification Record      | GitHub Issues        | Permanent |
| Archived `redwitch.wiki` | Git Repository       | Permanent |

---

### ✅ **Outcome**

* Controlled repository (`fley-qms`) created and active.
* Historical data from `redwitch.wiki` preserved.
* Protected `main` branch established.
* Baseline `QMS_Baseline_r1` approved by Top Management.
* QMS is now operational under formal change control.
