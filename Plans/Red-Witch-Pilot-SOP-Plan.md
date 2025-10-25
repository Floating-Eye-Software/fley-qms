# **PLAN – Quality Plan – Pilot SOP Implementation (Red Witch)**

**Slug:** Red-Witch-Pilot-SOP-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Quality-Planning-SOP, Design-Control-SOP  
**Controlled Source:** https://github.com/mlehotay/fley-qms/blob/main/Plans/Red-Witch-Pilot-SOP-Plan.md  

---

## **1. Introduction**

* **Purpose:**
  Pilot the Red Witch project workflows to draft, test, validate, and refine FLEY QMS Standard Operating Procedures (SOPs) **as a controlled design project**, ensuring alignment with ISO 9001, ISO 13485, IEC 62304, GDPR, and internal Design Control requirements.

* **Scope:**
  Organization-wide; applies to SOP development, WI drafting, template standardization, and QMS deployment activities **within the Red Witch pilot**, including the application of **Design Control principles** for intended-use validation of the QMS.

* **Applicable Standards & Regulations:**

  * ISO 13485:2016 Clauses 5.4, 7.1
  * ISO 9001:2015 + Amendment 1:2024
  * IEC 62304
  * 21 CFR 820.20(d), 820.30(b)
  * GDPR
  * ISO 9004
  * Internal Design Control SOP (FLEY)

---

## **2. Quality Objectives**

* Draft ≥5 SOPs based on Red Witch project experience (Design Control, CAPA, Code Review, Testing, Privacy).
* Apply **Design Control principles**: define QMS intended use, establish inputs/outputs, perform verification and validation of SOP implementation.
* Conduct **stage-gate reviews** per DCP for each SOP and QMS artifact.
* Capture evidence to demonstrate that the QMS achieves its intended use.
* Establish a functioning QMS baseline ready for internal audit and external certification preparation.

---

## **3. Design Control Integration**

* **Design Inputs:**

  * Intended use of QMS (supporting development, quality assurance, compliance).
  * Applicable ISO, IEC, and regulatory requirements.
  * Stakeholder needs (project team, management).
  * Risk analysis of SOP implementation and pilot workflows.

* **Design Outputs:**

  * Draft SOPs and WIs in Markdown.
  * Controlled QMS repository structure (`fley-qms`).
  * Traceability matrix linking SOPs → WIs → DCP deliverables → verification/validation evidence.

* **Design Reviews:**

  * Kickoff Review – confirm DCP alignment.
  * Requirements Review – approve intended use statement and QMS inputs.
  * Preliminary Design Review (PDR) – review SOP/WI drafts and repository structure.
  * Critical Design Review (CDR) – approve finalized SOPs/WIs for pilot implementation.
  * Verification Review – ensure SOP/WI use aligns with requirements.
  * Validation Review – confirm pilot workflows demonstrate intended QMS use.

* **Verification & Validation:**

  * Verification: SOP completeness, traceability, and repository controls.
  * Validation: Pilot workflow performance demonstrating intended QMS use.
  * Evidence stored in GitHub Issues, Pull Requests, CI/CD logs, and traceability matrix.

---

## **4. Quality Processes**

* Identify Red Witch workflows suitable for SOP standardization.
* Draft SOPs in Markdown and submit via GitHub Pull Requests for review.
* Pilot SOPs in real project workflows; document operational evidence.
* Conduct **Design Reviews** at defined DCP milestones.
* Incorporate design improvements into SOPs and repository architecture.
* Maintain all records under controlled versioning with full traceability.

---

## **5. Metrics & Measurement**

| Metric                                        | Target              | Method                                |
| --------------------------------------------- | ------------------- | ------------------------------------- |
| Number of SOPs drafted                        | ≥ 5                 | Document count                        |
| SOPs validated through project evidence       | ≥ 80%               | Evidence review, traceability checks  |
| SOPs updated based on pilot feedback          | ≥ 50%               | Change history and pull request logs  |
| Traceability from SOP → WI → DCP deliverable  | 100%                | Cross-reference audit                 |
| QMS baseline established under design control | 1 (QMS_Baseline_r2) | Repository configuration verification |

---

## **6. Quality Assurance & Design Control Activities**

* QA review of SOP/WI drafts prior to approval.
* Internal audits to verify SOP effectiveness in pilot workflows.
* Verification of traceability matrix completeness.
* Validation of intended-use achievement via pilot execution.
* Documentation of lessons learned and improvement decisions in GitHub Issues.
* Post-pilot **Management Review** to approve baseline QMS and define next milestone (Audit-Ready QMS Documentation).

---

## **7. Roles & Responsibilities**

| Role                            | Responsibilities                                                                                                |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **QMS Owner / Quality Manager** | Oversees DCP adherence, verifies design inputs/outputs, approves SOP/WI drafts, confirms repository compliance. |
| **Project Manager (Red Witch)** | Ensures SOPs/WIs are applied in pilot workflows, coordinates design reviews, captures pilot evidence.           |
| **Developers & Team Members**   | Follow SOPs, participate in design reviews, provide feedback and operational evidence.                          |
| **Top Management**              | Reviews pilot results, approves QMS baseline, authorizes next milestone per DCP stage-gates.                    |
| **Design / Documentation Lead** | Develops traceable SOPs/WIs, links artifacts to DCP, supports verification & validation.                        |

---

## **8. Records & Documentation**

* SOP/WI drafts, approvals, and revisions stored in controlled repository (`fley-qms`).
* Pilot evidence captured in GitHub Issues, Pull Requests, and CI/CD logs.
* Lessons learned and design refinement decisions documented in GitHub Issues (e.g., [#7 Change Control SOP](https://github.com/mlehotay/redwitch/issues/7)).
* Traceability matrices link SOPs/WIs to DCP inputs/outputs and verification/validation evidence.
* Repository migration actions governed by: [PLAN – QMS Repository Architecture and Go-Live Transition](https://github.com/mlehotay/fley-qms/blob/main/<dir>/Repo-Migration-Plan).

---

## **9. Linkage to Execution**

* **Milestones / Stage Gates (per DCP):**

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

## **10. Continuous Improvement & Design Changes**

* Design improvement feedback captured as design changes in GitHub Issues.
* Implement corrective design changes per [Repo Migration Plan](https://github.com/mlehotay/fley-qms/blob/main/<dir>/Repo-Migration-Plan).
* Integrate validated SOPs/WIs into controlled repository under formal change control.
* Conduct post-pilot **Management Review**: assess pilot results, approve baseline, define Milestone 2 objectives.
* Align ongoing improvements with **Continuous Improvement Plan** and CAPA SOP once established.
