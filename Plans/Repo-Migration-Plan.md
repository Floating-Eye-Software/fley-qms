# **PLAN – QMS Repository Architecture and Go-Live Transition**

**Slug:** Repo-Migration-Plan  
**Revision:** r2  
**Effective Date:** 2025-10-31  
**Related SOP:** Quality-Planning-SOP, Change-Control-SOP, Document-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/Plans/Repo-Migration-Plan.md  

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
* Achieve **baseline sign-off** (`FLEY-QMS_r1`) by Top Management.
* Ensure **change control readiness**: no direct commits to `main`; all future edits via PR workflow.
* Separate **product website** (`redwitch`) from **QMS governance system** (`fley-qms`).

---

## **3. Quality Processes**

* **Design & Development Controls:**
  Plan and execute migration activities as controlled design changes under the *Change-Control-SOP*.
* **Configuration Management:**
  Establish protected `main` branch and enforce CODEOWNERS approvals.
* **Verification of Effectiveness:**
  Verify that Pull Request workflow and branch protection operate as intended.
* **Risk & Opportunity Management:**
  Address the limitation identified during pilot (“GitHub wikis cannot support Pull Requests”) by implementing a compliant architecture.

---

## **4. Metrics & Measurement**

| Metric                                 | Target                   | Measurement Method          |
| -------------------------------------- | ------------------------ | --------------------------- |
| Controlled repository created          | 1 (`fley-qms`)           | GitHub UI verification      |
| Branch protection enabled              | 100% (`main`)            | Review repository settings  |
| Successful migration PR merged         | ≥ 1 baseline PR          | Pull Request logs           |
| Baseline tag created                   | `FLEY-QMS_r1`            | `git tag -l` output         |
| Per-document approval tags created     | ≥ 1 per updated document | `git tag -l` output         |

---

## **5. Quality Assurance Activities**

* Internal review of the `qms-setup` branch before migration PR.
* Pull Request approval by Quality Manager and Top Management.
* Post-merge verification of protection rules and `CODEOWNERS`.
* Tag creation and validation of repository integrity.
* Verification of migration effectiveness using checklist in Appendix A.

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
| Tag `FLEY-QMS_r1`                | Git repository       | Permanent |
| Verification evidence            | GitHub Issues        | Permanent |
| Archived `redwitch.wiki` content | Git repository       | Permanent |

---

## **8. Linkage to Execution**

* **Milestones:**
  * [FLEY-QMS Launch (Go-Live)](https://github.com/Floating-Eye-Software/fley-qms/milestone/1)
  * [QMS Foundations](https://github.com/Floating-Eye-Software/redwitch/milestone/1)

* **Project Board:**
  * [FLEY QMS Kanban](https://github.com/orgs/Floating-Eye-Software/projects/1)

* **Pull Requests:**
  * [#1 - FLEY-QMS_r1 - Initial Controlled QMS Baseline](https://github.com/Floating-Eye-Software/fley-qms/pull/1)
  * [#3 - Create FLEY Organization and Teams](https://github.com/Floating-Eye-Software/fley-qms/pull/3)

* **Issues:**
  * [#28 - Create Controlled QMS Repository](https://github.com/Floating-Eye-Software/redwitch/issues/28)
  * [#7 - SOP: Pull Request Procedure (Change Control)](https://github.com/Floating-Eye-Software/redwitch/issues/7)
  * [#2 - Create Organization and Update CODEOWNERS](https://github.com/Floating-Eye-Software/fley-qms/issues/2)

* **Linked Work Instructions:**
  * [WI - GitHub-Change-Control](../WIs/GitHub/GitHub-Change-Control.md)
  * [WI - GitHub-QMS-Setup](../WIs/GitHub/GitHub-QMS-Setup.md)

* **Appendices:**
  * [Appendix A - Repository Migration Execution](#appendix-a--repository-migration-execution)
  * [Appendix B - Organization Configuration](#appendix-b---organization-configuration)

---

## **9. Verification of Effectiveness**

**Verification Date:** 2025-10-31  

**Summary:**  
Verification confirmed completion of the organizational transition defined in Appendix B, following the initial migration executed under Appendix A.
All deliverables were implemented and validated through Pull Requests [fley-qms #1](https://github.com/Floating-Eye-Software/fley-qms/pull/1) and [fley-qms #3](https://github.com/Floating-Eye-Software/fley-qms/pull/3).
The QMS repository now operates under controlled, role-based governance within the Floating Eye Software organization.
The Verification of Effectiveness (VoE) process was introduced in this revision to formally close the migration plan and establish a recurring effectiveness review framework.


**Evidence:**  
  * PR fley-qms #1 (FLEY-QMS_r1 baseline)
  * PR fley-qms #3 (Org and Teams configuration, VoE integration)
  * Issues [redwitch #28](https://github.com/Floating-Eye-Software/redwitch/issues/28) and [fley-qms #2](https://github.com/Floating-Eye-Software/fley-qms/issues/2)
  * Screenshots of organization, team, and branch-protection settings
  * Controlled document revisions showing updated VoE sections

**Residual Risk:**  
During verification it was confirmed that GitHub’s built-in “Approve / Request Changes” feature cannot be used in a single-person organization.
Current approvals are documented via PR comments instead of the formal approval UI.
While configuration control remains effective, this limitation reduces visual traceability of approvals.
A new Risk & Opportunity Register entry will be opened to track and evaluate this constraint.

**Follow-Up Actions:**
* Create risk record *Single-Person Approval Constraint* to document and monitor the limitation.
* Continue recording approval evidence through PR discussion threads until a multi-reviewer configuration is established.
* Review effectiveness of the organizational setup at the next Management Review.

**Assessment:** ✅ **Effective**  
All objectives of the Repo-Migration-Plan were met. The identified residual risk is documented for further review but does not affect compliance or operational control.

---

# **Appendix A – Repository Migration Execution**

## **Purpose:**

Define the controlled, auditable process for migrating the Red Witch QMS wiki to `fley-qms`, preserving full commit history, establishing a controlled baseline (`main`), and segregating work-in-progress (WIP) materials for continued development.  

---

## **A1. Pre-Execution Checklist**

1. Migration plan approved by Quality Manager and Top Management.
2. Confirm access to both repositories:

   * **Source:** `redwitch.wiki`
   * **Target:** `fley-qms`
3. Verify Git and GitHub credentials for `@mlehotay`.
4. Ensure Red Witch wiki content is finalized.
5. Communicate go-live readiness to approvers.

---

## **A2. Migration Preparation – Preserve Full History**

### **Step 1: Clone the Source Wiki**

```bash
git clone https://github.com/mlehotay/redwitch.wiki.git
cd redwitch.wiki
```

### **Step 2: Rename the Wiki Branch**

```bash
git branch -m master qms-setup
```

### **Step 3: Add Target Repository as Remote**

```bash
git remote add fley git@github.com:mlehotay/fley-qms.git
```

### **Step 4: Push the History-Preserved Branch**

```bash
git push -u fley qms-setup
```

✅ This creates the initial `qms-setup` branch in `fley-qms` containing full commit history.

---

## **A3. Initialize the Controlled `main` Branch**

1. Create a new orphan branch for the controlled baseline:

   ```bash
   git checkout --orphan main
   git reset --hard
   ```

2. Create a `.github/CODEOWNERS` file to define repository control:

   ```bash
   mkdir -p .github
   echo "/* @mlehotay" > .github/CODEOWNERS
   git add .github/CODEOWNERS
   git commit -m "Initialize controlled main branch with CODEOWNERS"
   git push origin main
   ```

✅ `main` is now initialized with governance controls and no content files.

---

## **A4. Configure Repository Settings in GitHub**

### **Set Default Branch**

1. Go to **Settings → Branches → Default branch**.
2. Set to **main** and confirm.

### **Enable Branch Protection**

In **Settings → Branches → Add rule**, configure:

| Setting                               | Value  |
| ------------------------------------- | ------ |
| Branch name pattern                   | `main` |
| Require a pull request before merging | ✅      |
| Require approvals                     | ✅      |
| Required number of approvals          | 1      |
| Require review from CODEOWNERS        | ✅      |
| Do not allow bypassing protections    | ✅      |
| Allow force pushes                    | ❌      |
| Allow deletions                       | ❌      |

Save rule.

---

## **A5. Branch Segregation – Controlled vs. Development Work**

The imported branch (`qms-setup`) contains mixed materials. Separate it into two new branches to isolate controlled baseline content from ongoing development.

### **Step 1: Create Segregation Branches**

```bash
cd ~/projects/fley-qms
git checkout qms-setup
git pull

# Core controlled content for baseline
git checkout -b feature/qms-setup

# WIP and project development content
git checkout qms-setup
git checkout -b feature/qms-foundation
```

Resulting structure:

```
qms-setup
├── feature/qms-setup         (core baseline content)
└── feature/qms-foundation    (WIP and project docs)
```

---

### **Step 2: Isolate Content per Branch**

#### **`feature/qms-setup` – Controlled Baseline Content**

```bash
git checkout feature/qms-setup
git rm -r --cached .
git add "Quality Manual.md" "SOPs/" "Templates/" "Repo-Migration-Plan.md" "WIs/WI-GitHub-QMS-Setup.md"
git commit -m "Isolate core controlled QMS documents for baseline"
```

#### **`feature/qms-foundation` – Ongoing Work**

```bash
git checkout feature/qms-foundation
git rm -r --cached .
git add "WIs/" "Projects/" "Checklists/" "Planning/" "Docs/"
git commit -m "Preserve WIP and project documentation for QMS Foundations milestone"
```

Push both branches:

```bash
git push origin feature/qms-setup
git push origin feature/qms-foundation
```

✅ Both branches are now visible in GitHub under **Branches**.

---

## **A6. Create the Go-Live Pull Request**

1. Go to **Pull Requests → New pull request** in `fley-qms`.

   * **Base:** `main`
   * **Compare:** `feature/qms-setup`

2. Title:

   ```
   FLEY QMS Go-Live – Initial Controlled Baseline
   ```

3. Description:
   Reference this Appendix A and describe that it migrates all approved QMS documents from `redwitch.wiki` under change control.
   Link to related issue (`redwitch#28`).

4. Submit PR for approval by **Quality Manager** and **Top Management**.

5. Merge using **Merge Commit** (not squash or rebase).

---

## **A7. Tag the Controlled Baseline**

After PR merge:

```bash
git fetch origin
git checkout main
git tag FLEY-QMS_r1
git push origin FLEY-QMS_r1
```

✅ This tag represents the first controlled QMS baseline.

---

## **A8. Post-Merge Verification and Configuration**

1. Confirm `main` is protected and approvals are enforced.
2. Lock or archive `qms-setup` branch (read-only).
3. Verify that `feature/qms-foundation` remains available for active development.
4. Update GitHub issues and comments with screenshots and other evidence.

---

## **A9. Verification Checklist**

| Verification Item              | Evidence Source                 |
| ------------------------------ | ------------------------------- |
| Controlled repo created        | GitHub UI                       |
| Branch protection active       | Settings screenshot             |
| Migration PR merged            | PR log                          |
| Tag `FLEY-QMS_r1` created      | `git tag -l` output             |
| Feature branches created       | `git branch -a` output          |
| Verification evidence recorded | GitHub Issues                   |
| WIP and project docs preserved | `feature/qms-foundation` branch |

---

## **A10. Post-Go-Live Branch Model**

| Branch                   | Purpose                                              |
| ------------------------ | ---------------------------------------------------- |
| `main`                   | Controlled QMS baseline (protected)                  |
| `feature/qms-setup`      | Temporary branch for Go-Live PR (delete after merge) |
| `feature/qms-foundation` | Ongoing milestone development (WIP)                  |
| `change/*`               | Approved document change requests                    |
| `feature/*`              | New documents or processes                           |
| `fix/*`                  | Minor corrections                                    |

✅ All changes to `main` occur **only via approved Pull Requests** under *Change-Control-SOP*.

---

## **A11. Records and Retention**

| Record                                               | Location             | Retention |
| ---------------------------------------------------- | -------------------- | --------- |
| Go-Live PR and approvals                             | GitHub Pull Requests | Permanent |
| Tag `FLEY-QMS_r1`                                    | Git tags             | Permanent |
| Branch protection configuration                      | GitHub settings      | Permanent |
| Verification evidence                                | GitHub Issues        | Permanent |
| Archived wiki import (`qms-setup`)                   | Git repository       | Permanent |
| Active development branch (`feature/qms-foundation`) | Git repository       | Ongoing   |

---

# **Appendix B - Organization Configuration**

## **Purpose**
To establish a minimal, auditable permission structure within the **Floating Eye Software (FLEY)** GitHub Organization that enforces QMS change-control requirements using role-based access and mandatory peer review.

---

## **B.1 Teams**

| Team | Access Level | Purpose | Typical Members |
|------|---------------|----------|----------------|
| **@Floating-Eye-Software/qms-authors** | **Write** | Create branches, draft and submit Pull Requests for controlled documentation. | Process Owners, Project Managers, Document Authors |
| **@Floating-Eye-Software/qms-approvers** | **Maintain** | Review, approve, and merge Pull Requests after required approvals. | Quality Manager, Top Management, Compliance Approvers |

> Only these two teams are required to support full QMS change control.  
> Administrators (org owners) retain configuration rights but do not participate in routine change approvals.

---

## **B.2 Repository Transfer and Team Setup Steps**

1. **Transfer Repository**
   - Move `fley-qms` into the **Floating Eye Software** organization.

2. **Create Teams**
   - Under *Organization → Teams*, create:
     - `qms-authors`
     - `qms-approvers`

3. **Assign Permissions**
   - In the `fley-qms` repository:
     - Grant **Write** access to `qms-authors`.
     - Grant **Maintain** access to `qms-approvers`.

4. **Add Members**
   - Add contributors to `qms-authors`.
   - Add reviewers and QA leadership to `qms-approvers`.

---

## **B.3 CODEOWNERS Configuration**

Create `.github/CODEOWNERS` with the following content:

```plaintext
# Require approval from Approvers for any change to controlled content
* @Floating-Eye-Software/qms-approvers
````

This configuration enforces that only members of the **qms-approvers** team may merge changes to controlled content.

---

## **B.4 Branch Protection Rules**

Apply the following protection to the `main` (controlled) branch:

| Rule                                   | Setting                |
| -------------------------------------- | ---------------------- |
| Require pull request before merging    | ✅ Enabled              |
| Restrict who can push                  | ✅ Only `qms-approvers` |
| Dismiss stale approvals on new commits | ✅ Recommended          |
| Do not allow bypassing settings        | ✅ Recommended          |

---

## **B.5 Controlled Change Flow**

```
Author (qms-authors)
   ↓  opens Pull Request
Approver (qms-approvers)
   ↓  reviews & approves
Branch Protection enforces approval
   ↓
Approver merges → controlled baseline or release tag
```

This two-team model satisfies QMS requirements for separation of duties, traceable review, and controlled baseline creation with minimal administrative overhead.

---
