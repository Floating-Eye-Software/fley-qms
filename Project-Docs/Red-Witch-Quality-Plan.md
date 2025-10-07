# **Red Witch – Project Quality Plan (PQP) (FLEY Updated)**

## 1. Introduction

**Purpose:** Define quality objectives, processes, and metrics for the Red Witch software development project under the FLEY QMS framework.

**Scope:** Applies to all Red Witch development activities, including requirements, design, development, verification, validation, release, and post-release monitoring.

**Applicable Standards & Regulations:** ISO 13485:2016 (Clauses 7.1, 7.3, 8.5), ISO 9001:2015, IEC 62304, IEC 62366, 21 CFR 820.30, GDPR, HIPAA, EU MDR.

---

## 2. Governance & Quality Planning

**Objectives:**

* Maintain complete bidirectional traceability: Requirements ↔ Design ↔ Implementation ↔ Verification ↔ Validation.
* ≥95% unit test pass rate before each release.
* ≥80% code coverage.
* High-risk features undergo formal design and risk review.

**Planning:**

* Milestone checkpoints per **ODF/FLEY framework**.
* Sprint retrospectives for continuous improvement.
* KPIs tracked in GitHub Insights, dashboards, and traceability matrices.

**Evidence/Tools:** Milestone documentation, retrospectives, dashboards, traceability matrix (Design Trace Matrix).

---

## 3. Document & Record Control

* All project documentation maintained in **GitHub Wiki**, PRs, and CI/CD pipelines.
* Controlled via **PR approvals, branch protection rules, and revision history**.
* Releases tagged in GitHub for baseline control and traceability.
* Verification/Validation reports archived in pipelines and linked to DCP/WI checkpoints.

---

## 4. Training & Competence

* Developer onboarding includes GDPR, security/privacy, and QMS training.
* Access to repositories tied to training completion.
* Training logs maintained in Wiki.

---

## 5. Risk Management

* Risk Register maintained in GitHub Wiki + Issues, linked to specific requirements.
* Risks reviewed during design reviews, retrospectives, and at milestone approvals.
* Risk mitigation tracked and verified as part of **DCP deliverables**.

---

## 6. Design & Development Control

* Requirements documented in GitHub Wiki; traceability maintained through Issues → PRs → Tests → Validation.
* Formal design reviews at each milestone, recorded in Wiki.
* DCP/WI-QMS-09-04 deliverables produced per phase:

  * Design Planning → DCP, Risk Register
  * Requirements Definition → Approved backlog & SRS
  * Design & Implementation → Architecture, detailed design, code
  * Verification → Test plans, results
  * Validation → Validation reports, stakeholder approval
  * Release → Release notes, deployment checklist, post-release review

---

## 7. Change & Configuration Management

* Controlled via **GitHub branch protection, PR workflow, linked issues**.
* PR approvals constitute controlled change logs.
* Baselines maintained via GitHub tags/releases.
* Changes impact-assessed against traceability matrix and DCP deliverables.

---

## 8. Supplier & External Resource Management

* No third-party suppliers currently require qualification.
* Open-source components tracked via GitHub dependency management and license compliance.

---

## 9. Production, Release & Deployment

* Releases documented with notes, GitHub tags, and DCP compliance evidence.
* Disaster recovery plan maintained and verified before release.
* Issue backlog reviewed and prioritized prior to deployment.

---

## 10. Verification, Validation & Testing

* Automated CI/CD executes unit, integration, and regression tests.
* Test evidence archived in pipelines and linked to requirements.
* Validation performed with stakeholders for major features; results documented in validation reports.
* Traceability verified against DCP/WI deliverables.

---

## 11. Nonconformance & CAPA

* Defects and deviations logged as GitHub Issues with CAPA label.
* Root cause analysis conducted for recurring/high-risk issues.
* CAPA tracked to closure; outcomes linked to SOP/WI updates.

---

## 12. Audit & Continuous Improvement

* Internal audits every 6 months; audit findings documented in Wiki/GitHub Issues.
* Sprint retrospectives identify process improvements.
* CAPA outcomes and audit findings feed updates to SOPs, WIs, and DCP processes.
* ISO 9004 self-assessment and GDPR compliance milestones inform continuous improvement planning.

---

## 13. Customer & Stakeholder Feedback

* Feedback collected via usability testing, design reviews, and stakeholder workshops.
* Issues logged, prioritized, and linked to CAPA if necessary.
* Feedback integrated into backlog refinement, sprint planning, and future release planning.

---

## 14. Infrastructure, Security & Work Environment

* Project infrastructure: GitHub repositories, CI/CD pipelines, Wiki.
* GDPR, HIPAA, and security/privacy considerations reviewed during design.
* Access permissions tied to role and training.
* Security and access control maintained per organizational IT policies.

---

## 15. Regulatory Compliance

* ISO 13485:2016 – Medical device QMS
* IEC 62304 – Medical device software lifecycle
* IEC 62366 – Usability engineering
* ISO 9001:2015 – Quality management systems
* GDPR / HIPAA / EU MDR

---

## 16. International Standards

* IEC 82304-1:2016 – Health Software Product Safety
* ISO/TS 82304-2:2021 – Health & Wellness Apps, Quality & Reliability
* ISO/IEC 27001:2013 – Information Security
* ISO/IEC 27701:2019 – Privacy Information Management

---

## 17. PQP Matrix – Red Witch Project

| #  | Quality Element                  | SOP Category         | Work Instruction(s)           | Evidence / Toolchain Notes                                                   |
| -- | -------------------------------- | -------------------- | ----------------------------- | ---------------------------------------------------------------------------- |
| 1  | Governance & Quality Planning    | Governance           | WI-ODF-01, WI-GH-02           | Milestones, retrospectives, dashboards, DCP checkpoints                      |
| 2  | Document & Record Control        | Document Control     | WI-GH-01                      | Wiki pages, PR approvals, revision history                                   |
| 3  | Training & Competence            | Resource Mgmt        | WI-GH-14                      | Training logs, repo access control                                           |
| 4  | Risk Management                  | Risk Mgmt            | WI-GH-05, WI-QMS-09-04        | Risk register, linked issues, traceability to design                         |
| 5  | Design & Development Control     | Design Control       | WI-ODF-01, WI-GH-03, WI-GH-04 | Requirements, traceability, DCP deliverables, reviews                        |
| 6  | Change & Configuration Mgmt      | Change/Config Mgmt   | WI-GH-06, WI-GH-07            | PR workflow, branch protections, tags, baselines                             |
| 7  | Supplier & External Resources    | Supplier Mgmt        | WI-GH-15                      | Open-source dependency tracking                                              |
| 8  | Production, Release & Deployment | Release Control      | WI-GH-09, WI-QMS-09-04        | Release notes, GitHub tags, DR plan, DCP evidence                            |
| 9  | Verification, Validation, Test   | Verification/Testing | WI-GH-08                      | CI/CD test reports, verification evidence linked to reqs                     |
| 10 | Nonconformance & CAPA            | CAPA                 | WI-GH-10                      | Issues logged as CAPA, tracked to closure                                    |
| 11 | Audit & Continuous Improvement   | Audit Program        | WI-GH-16, WI-QMS-09-04        | Audit reports, retrospectives, CAPA updates, continuous improvement tracking |
| 12 | Customer & Stakeholder Feedback  | Feedback Mgmt        | WI-GH-17                      | Usability testing, Issues, stakeholder workshop notes                        |
| 13 | Infrastructure & Security        | Infrastructure Mgmt  | WI-GH-14, WI-SEC-01           | Repo permissions, GDPR/HIPAA review, IT policies                             |

---

## 18. Approval

| Role / Name      | Signature | Date |
| ---------------- | --------- | ---- |
| Project Manager  |           |      |
| Quality Manager  |           |      |
| Privacy Officer  |           |      |
| Sponsor / Client |           |      |
