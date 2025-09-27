# **Red Witch – Project Quality Plan (PQP)**

## 1. Introduction

**Purpose:** Define quality objectives, processes, and metrics for the Red Witch software development project.
**Scope:** Applies to all Red Witch development activities.
**Applicable Standards & Regulations:** ISO 13485:2016 (Clauses 7.1, 7.3), ISO 9001:2015, 21 CFR 820.30, IEC 62304, GDPR.

---

## 2. Governance & Quality Planning

* **Objectives:**

  * Maintain bidirectional requirements traceability (requirements ↔ design ↔ code ↔ test).
  * ≥95% unit test pass rate before each release.
  * ≥80% code coverage.
  * All high-risk features undergo formal design review.
* **Planning:**

  * Milestone checkpoints per ODF framework.
  * Sprint retrospectives for continuous improvement.
* **KPIs:** Tracked in GitHub Insights and dashboards.

---

## 3. Document & Record Control

* Project documentation stored in **GitHub Wiki**.
* Controlled through **PR approvals and revision history**.
* Releases tagged in GitHub for baseline and traceability.
* Test reports archived in CI/CD pipelines.

---

## 4. Training & Competence

* Developer onboarding includes GDPR and security/privacy training.
* Training completion is tied to **repository access permissions**.
* Training logs maintained in Wiki.

---

## 5. Risk Management

* Risk register maintained in GitHub Wiki + Issues.
* Risks linked to specific requirements and mitigations.
* Reviewed at design reviews and project retrospectives.

---

## 6. Design & Development Control

* Requirements documented in GitHub Wiki.
* Traceability maintained through Issues ↔ PRs ↔ Tests.
* Formal design reviews at milestones (recorded in Wiki).
* ODF framework checkpoints used for planning.

---

## 7. Change & Configuration Management

* Controlled via **GitHub branch protections, PR workflow, and issue links**.
* PR approvals form the controlled change log.
* Baselines maintained via GitHub tags and releases.

---

## 8. Supplier & External Resource Management

* No third-party suppliers requiring qualification for core Red Witch development at present.
* Open-source components tracked via GitHub dependency management.

---

## 9. Production, Release & Deployment

* Release notes documented in Wiki and tagged in GitHub.
* Disaster recovery plan maintained as part of release process.
* Issue backlog reviewed before release.

---

## 10. Verification, Validation & Testing

* CI/CD executes **unit, integration, and regression tests**.
* Test evidence archived in pipelines.
* Verification evidence linked to requirements.
* User/stakeholder validation performed on major features.

---

## 11. Nonconformance & CAPA

* Defects and deviations logged as Issues using CAPA template.
* Root cause analysis conducted for recurring/high-risk issues.
* CAPA issues tracked to closure in GitHub.

---

## 12. Audit & Continuous Improvement

* Internal audit conducted every 6 months.
* Sprint retrospectives identify process improvements.
* SOPs/WIs updated based on audit findings and CAPA.
* ISO 9004 self-assessment and GDPR compliance milestones used for improvement planning.

---

## 13. Customer & Stakeholder Feedback

* Stakeholder feedback collected through usability testing and design reviews.
* Complaints/issues logged as GitHub Issues, linked to CAPA if applicable.
* Feedback integrated into backlog refinement and future sprints.

---

## 14. Infrastructure, Security & Work Environment

* Project infrastructure: GitHub repositories, CI/CD pipelines, Wiki.
* GDPR privacy considerations reviewed during design.
* Repo permissions aligned with training/roles.
* Security and access control managed through GitHub and organizational IT policies.

---

## PQP Matrix – Red Witch Project

| #  | Quality Element                  | SOP Category         | Work Instruction(s)           | Evidence / Toolchain Notes                               |
| -- | -------------------------------- | -------------------- | ----------------------------- | -------------------------------------------------------- |
| 1  | Governance & Quality Planning    | Governance           | WI-ODF-01, WI-GH-02           | Milestones, retrospectives, dashboards                   |
| 2  | Document & Record Control        | Document Control     | WI-GH-01                      | Wiki pages, PR approvals, revision history               |
| 3  | Training & Competence            | Resource Mgmt        | WI-GH-14                      | Training logs, repo access control                       |
| 4  | Risk Management                  | Risk Mgmt            | WI-GH-05                      | Risk register, Issues linked to requirements             |
| 5  | Design & Development Control     | Design Control       | WI-ODF-01, WI-GH-03, WI-GH-04 | Requirements, traceability, reviews in Wiki & Issues     |
| 6  | Change & Configuration Mgmt      | Change/Config Mgmt   | WI-GH-06, WI-GH-07            | PR workflow, branch protections, tags, baselines         |
| 7  | Supplier & External Resources    | Supplier Mgmt        | WI-GH-15                      | Open-source dependency tracking                          |
| 8  | Production, Release & Deployment | Release Control      | WI-GH-09                      | Release notes, GitHub tags, DR plan                      |
| 9  | Verification, Validation, Test   | Verification/Testing | WI-GH-08                      | CI/CD test reports, verification evidence linked to reqs |
| 10 | Nonconformance & CAPA            | CAPA                 | WI-GH-10                      | Issues logged as CAPA, tracked to closure                |
| 11 | Audit & Continuous Improvement   | Audit Program        | WI-GH-16                      | Audit reports, retrospectives, CAPA updates              |
| 12 | Customer & Stakeholder Feedback  | Feedback Mgmt        | WI-GH-17                      | Usability testing, Issues, stakeholder workshop notes    |
| 13 | Infrastructure & Security        | Infrastructure Mgmt  | WI-GH-14, WI-SEC-01           | Repo permissions, GDPR compliance review, IT policies    |

---

## Approval

| Role / Name      | Signature | Date |
| ---------------- | --------- | ---- |
| Project Manager  |           |      |
| Quality Manager  |           |      |
| Privacy Officer  |           |      |
| Sponsor / Client |           |      |

---
