# **PLAN – Quality Plan – Pilot SOP Implementation (Red Witch)**

**Slug:** Red-Witch-Pilot-SOP-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Red-Witch-Pilot-SOP-Plan  

---

## **1. Introduction**

* **Purpose:**
  Pilot the Red Witch project workflows to draft, test, validate, and refine FLEY QMS Standard Operating Procedures (SOPs), ensuring alignment with ISO 9001, ISO 13485, IEC 62304, and GDPR.

* **Scope:**
  Organization-wide; applies to SOP development, Work Instruction (WI) drafting, and template standardization activities within the Red Witch pilot.

* **Applicable Standards & Regulations:**
  * ISO 13485:2016 Clauses 5.4, 7.1
  * ISO 9001:2015
  * IEC 62304
  * 21 CFR 820.20(d), 820.30(b)
  * GDPR
  * ISO 9004

---

## **2. Quality Objectives**

* Draft ≥5 SOPs based on Red Witch project experience (Design Control, CAPA, Code Review, Testing, Privacy).
* Validate each SOP with real project evidence and alignment to Design Control Plan (DCP) deliverables.
* Conduct post-pilot “lessons learned” reviews after each release.
* Establish a functioning QMS baseline ready for audit preparation.

---

## **3. Quality Processes**

* Identify Red Witch workflows suitable for SOP standardization.
* Draft SOPs in Markdown format and review via GitHub Pull Requests.
* Pilot SOPs within the Red Witch project; collect operational evidence (issues, PRs, CI/CD logs).
* Incorporate improvement findings (e.g., wiki limitations) into new QMS architecture and processes.
* Ensure that all QMS records are linked to controlled repositories and traceable through Git history.

---

## **4. Metrics & Measurement**

| Metric                                        | Target              | Method                          |
| --------------------------------------------- | ------------------- | ------------------------------- |
| Number of SOPs drafted                        | ≥ 5                 | Document count                  |
| SOPs validated through project evidence       | ≥ 80%               | Evidence review                 |
| SOPs updated based on pilot feedback          | ≥ 50%               | Change history                  |
| Traceability from SOP → WI → DCP deliverable  | 100%                | Cross-reference audit           |
| QMS baseline established under change control | 1 (QMS_Baseline_r1) | Repo configuration verification |

---

## **5. Quality Assurance Activities**

* QA review of each draft SOP prior to approval.
* Internal audits to verify SOP effectiveness in pilot workflows.
* Cross-functional review sessions between development and QA teams.
* Verification that QMS baseline migration and branch protection meet quality system requirements.

---

## **6. Roles & Responsibilities**

| Role                            | Responsibilities                                                                                                        |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Quality Manager**             | Oversees drafting, review, and approval of SOPs. Confirms compliance of repository configuration with QMS requirements. |
| **Project Manager (Red Witch)** | Ensures pilot SOPs are applied in development workflows and that improvement feedback is captured.                      |
| **Developers & Team Members**   | Follow SOPs, participate in reviews, and provide pilot feedback and evidence.                                           |
| **Top Management**              | Reviews pilot results, approves QMS baseline transition, and authorizes next milestone (Audit-Ready QMS Documentation). |

---

## **7. Records & Documentation**

* SOP drafts, approvals, and revisions stored in controlled repository (`fley-qms`).
* Pilot evidence captured in GitHub Issues, Pull Requests, and CI/CD logs.
* Lessons learned and design refinement decisions documented in GitHub Issues (e.g., [#7 Change Control SOP](https://github.com/mlehotay/redwitch/issues/7)).
* Migration actions governed by:
  → [**PLAN – QMS Repository Architecture and Go-Live Transition**](https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan)

---

## **8. Linkage to Execution**

* **Milestones:**

  * [QMS Foundations](https://github.com/mlehotay/redwitch/milestone/1)
  * [Audit-Ready QMS Documentation](https://github.com/mlehotay/redwitch/milestone/2)
  * [Compliance Backbone](https://github.com/mlehotay/redwitch/milestone/3)

* **Project Boards:**

  * [FLEY QMS Kanban](https://github.com/users/mlehotay/projects/3)
  * [Red Witch Kanban](https://github.com/users/mlehotay/projects/4)

* **Key Issues:**

  * [#5 Draft Software Development Lifecycle SOP](https://github.com/mlehotay/redwitch/issues/5)
  * [#7 SOP – Pull Request Procedure (Change Control)](https://github.com/mlehotay/redwitch/issues/7)

---

## **9. Continuous Improvement**

* Capture findings from the pilot (e.g., GitHub wiki limitations) as design improvements rather than CAPAs.
* Implement corrective design changes per the [Repo Migration Plan](https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan).
* Integrate validated processes into the controlled `fley-qms` repository under formal change control.
* Conduct post-pilot Management Review to assess pilot results, approve baseline, and define objectives for Milestone 2 (Audit-Ready QMS).
* Maintain ongoing alignment with the Continuous Improvement Plan and CAPA SOP once established.
