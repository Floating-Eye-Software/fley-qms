# **PLAN – QMS Repository Architecture and Go-Live Transition**

**Slug:** Repo-Migration-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan  

---

## **1. Introduction**

* **Purpose:**
  Define and control the transition from the Red Witch wiki-based QMS prototype to a dedicated, controlled GitHub repository (`fley-qms`) that supports branch protection, Pull Request approvals, and formal document change control.

* **Scope:**
  Organization-wide; applies to all QMS documentation, including the Quality Manual, SOPs, Work Instructions, Templates, and Records migrated from `redwitch.wiki`.

* **Applicable Standards & Regulations:**
  * ISO 9001:2015 § 6.3 (Change Management)
  * ISO 13485:2016 § 4.2 (Document Control)
  * IEC 62304 § 5.1 (Configuration Management)
  * 21 CFR 820.40 (Document Controls)

---

## **2. Quality Objectives**

* Establish a **controlled QMS repository** that enforces Pull Request review and branch protection.
* Preserve the **complete commit history** from the Red Witch wiki.
* Separate **governance documentation** (`fley-qms`) from **product/web hosting** (`redwitch`).
* Provide a **read-only publication layer** for approved documents via `fley-qms.wiki`.
* Achieve QMS baseline tag **`QMS_Baseline_r1`** sign-off by Top Management.

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

| Metric                          | Target                               | Measurement Method    |
| ------------------------------- | ------------------------------------ | --------------------- |
| Controlled repository created   | 1 (`fley-qms`)                       | Verified in GitHub UI |
| Branch protection enabled       | 100 % (`main`)                       | Review repo settings  |
| Successful migration PR merged  | ≥ 1 (“Initial QMS Go-Live Baseline”) | PR review log         |
| Wiki publication synchronized   | ≥ 1 approved push                    | Manual verification   |
| Tag created (`QMS_Baseline_r1`) | 1                                    | `git tag -l` output   |

---

## **5. Quality Assurance Activities**

* Internal review of migration branch (`qms-setup`) before merge.
* Pull Request approval by Quality Manager / Project Owner.
* Post-merge verification of branch protection and CODEOWNERS.
* Spot audit of migrated documents for completeness and integrity.
* Validation of public wiki publication accuracy.

---

## **6. Roles & Responsibilities**

| Role                              | Responsibilities                                                       | Authorities                                            |
| --------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------ |
| **Quality Manager**               | Approves migration plan; verifies configuration and baseline tagging.  | Approve QMS Baseline PR; enforce change control.       |
| **Project Owner / Administrator** | Executes technical migration steps and configures repository settings. | Create and manage repositories; set branch protection. |
| **Top Management**                | Reviews and approves go-live baseline.                                 | Authorize release of QMS Baseline r1.                  |
| **Developers / Contributors**     | Follow Pull Request and Change Control procedures post-migration.      | Propose changes via approved workflow.                 |

---

## **7. Records & Documentation**

* `fley-qms` repository – controlled documents (main branch).
* `fley-qms.wiki` – approved, read-only publication view.
* `redwitch.wiki` – archived historical QMS content.
* Pull Request review records and approval comments.
* Git tags (`QMS_Baseline_r1`) as configuration identifiers.
* Migration audit checklist and verification notes.

---

## **8. Linkage to Execution**

* **Milestones:**

* [QMS Foundations](https://github.com/mlehotay/redwitch/milestone/1) → identifies need for controlled repo.
* [Audit-Ready QMS Documentation](https://github.com/mlehotay/redwitch/milestone/2) → baseline validation.

* **Project Board / Tracking Tool:**
  [FLEY QMS Kanban](https://github.com/users/mlehotay/projects/3)

* **Issues / CAPA References:**

  * [#7 SOP – Pull Request Procedure (Change Control)](https://github.com/mlehotay/redwitch/issues/7)
  * Observation recorded under [Issue #7 comment](https://github.com/mlehotay/redwitch/issues/7#issuecomment-3393627464) (QMS pilot finding).

---

## **9. Continuous Improvement**

* Treat the migration as the first **continuous improvement cycle** validating the QMS architecture.
* Capture lessons learned (“wiki cannot support PRs”) for design review in next Management Review.
* Update the *Change-Control-SOP* to reference `fley-qms` as the controlled document source.
* Review repository configuration annually for effectiveness and scalability (auto-publish, tagging, CI/CD integration).
