# **PLAN – Quality Plan – Continuous Improvement (FLEY)**

**Slug:** Continuous-Improvement-Plan  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Continuous-Improvement-Plan  

---

## **1. Introduction**

* **Purpose:**
  Establish a systematic framework for maintaining and improving the FLEY Quality Management System (QMS), ensuring continual maturity growth, regulatory compliance, and feedback integration consistent with ISO 9001, ISO 13485, ISO 9004, IEC 62304, and GDPR.

* **Scope:**
  Organization-wide; applies to all QMS processes, design control activities, and compliance programs across repositories (`fley-qms`, `redwitch`, and associated projects).

* **Applicable Standards & Regulations:**
  * ISO 9001:2015 (Clause 10 – Improvement)
  * ISO 9004:2018 (Maturity Assessment)
  * ISO 13485:2016 § 8.5 (Improvement)
  * IEC 62304:2006 § 5.1.1 (Process Improvement)
  * 21 CFR 820.100 (Corrective and Preventive Action)
  * GDPR Articles 5 & 32 (Accountability & Data Protection by Design)

---

## **2. Quality Objectives**

* Conduct **annual ISO 9004-based maturity assessments** of the FLEY QMS.
* Perform **annual GDPR and data protection compliance audits.**
* Close all audit and CAPA findings within **60 calendar days.**
* Maintain ≥95% traceability of **design inputs → outputs → V&V evidence** across all active design projects.
* Review QMS effectiveness and CI progress at each **Management Review** meeting.

---

## **3. Quality Processes**

* Maintain CI-related plans, checklists, and review records as controlled documents in `fley-qms/docs/continuous-improvement/`.
* Log all audit findings, CAPAs, and improvement initiatives as **GitHub issues** labeled `audit`, `capa`, or `improvement`.
* Manage process changes and SOP updates via **Pull Request–based change control** in `fley-qms`.
* Integrate lessons learned from design projects and pilot activities into new or revised SOPs.
* Use the **[Repo-Migration-Plan](https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan)** as the reference case study for system-level corrective design actions.
* Ensure that improvement data feeds directly into risk management and objective-setting processes.

---

## **4. Metrics & Measurement**

| Metric                            | Target                        | Method / Source            |
| --------------------------------- | ----------------------------- | -------------------------- |
| Audit findings per year           | ≤ 10                          | Internal audit log         |
| CAPA closure within 60 days       | ≥ 90%                         | Issue tracker metrics      |
| QMS maturity score (ISO 9004)     | ≥ 4.0 / 5.0                   | Annual self-assessment     |
| Traceability coverage (DCP → V&V) | ≥ 95%                         | DCP audits                 |
| QMS repository compliance         | 100% of docs under PR control | Review `fley-qms` settings |

---

## **5. Quality Assurance Activities**

* **Annual ISO 9004 Self-Assessment** performed by the Quality Manager using the FLEY QMS Maturity Checklist.
* **Annual GDPR and Data Privacy Audit** led by the Privacy Officer.
* **Quarterly CAPA Review Sessions** held by the Quality Manager and Project Leads.
* **Post-Milestone Lessons Learned** sessions after each major QMS release or design project.
* Verification of continuous improvement effectiveness via internal audit sampling and KPI tracking.

---

## **6. Roles & Responsibilities**

| Role                | Responsibilities                                                                    |
| ------------------- | ----------------------------------------------------------------------------------- |
| **Quality Manager** | Oversees audits, CI program execution, and CAPA verification; maintains CI metrics. |
| **Privacy Officer** | Leads GDPR audits and data protection reviews.                                      |
| **Project Leads**   | Implement CAPA actions within their projects; ensure process adherence.             |
| **Top Management**  | Reviews CI outcomes, approves improvement initiatives, and allocates resources.     |

---

## **7. Records & Documentation**

* Controlled CI documentation stored in `fley-qms/docs/continuous-improvement/`.
* Audit reports and CAPA records tracked as **GitHub issues** with relevant labels (`audit`, `capa`, `improvement`).
* Approved SOP updates recorded through **Pull Request history**.
* Management Review minutes and audit summaries archived under `fley-qms/records/management-reviews/`.
* Historical reference: *[PLAN – QMS Repository Architecture and Go-Live Transition](https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan)* documents the first systemic improvement to the QMS architecture.

---

## **8. Linkage to Execution**

* **Recurring Activities:**

  * [ISO 9004 Self-Assessment Checklist](https://github.com/mlehotay/redwitch/wiki/ISO-9004-Self-Assessment)
  * [GDPR Audit Checklist](https://github.com/mlehotay/redwitch/wiki/GDPR-Audit-Checklist)

* **Tracking:**

  * [CAPA Issues (label:capa)](https://github.com/mlehotay/redwitch/issues?q=label%3Acapa)
  * [Audit Findings (label:audit)](https://github.com/mlehotay/redwitch/issues?q=label%3Aaudit)
  * [Improvement Actions (label:improvement)](https://github.com/mlehotay/redwitch/issues?q=label%3Aimprovement)

* **Related Plans:**

  * [Repo-Migration-Plan](https://github.com/mlehotay/redwitch/wiki/Repo-Migration-Plan)
  * [Red-Witch-Pilot-SOP-Plan](https://github.com/mlehotay/redwitch/wiki/Red-Witch-Pilot-SOP-Plan)

---

## **9. Continuous Improvement**

* All improvement data (audits, CAPAs, lessons learned) feed directly into SOP revision and management review cycles.
* Process effectiveness reviewed annually using ISO 9004 criteria; maturity trend tracked over time.
* Improvements that modify QMS architecture or core workflows are managed as **controlled design changes** under Change-Control-SOP.
* The **Repo Migration Plan** serves as the baseline precedent for future system-level corrective design actions.
* Management Review ensures CI activities align with strategic objectives and regulatory obligations.
