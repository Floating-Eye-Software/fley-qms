# **TPL - Design Control Plan (Ontario DSS Framework)**

**Slug:** DCP-Template-Ontario-DSS  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Design-Control-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/DCP-Template-Ontario-DSS  

---

## **1. Purpose**

This Design Control Plan (DCP) defines the process for managing **design and development activities** under the **Ontario Digital Service Standard (DSS)**. The plan ensures:

* Traceability of all design inputs and outputs.
* Verification and validation of deliverables at each phase.
* Compliance with applicable standards and regulations.
* Controlled records for audit readiness.

---

## **2. Scope**

Applies to any project adopting the **Ontario DSS framework**, including digital services, software, health software, or other service development initiatives. It covers:

* DSS Phases: Discovery → Alpha → Beta → Live.
* User research, prototyping, MVP development, and post-launch service improvements.
* Accessibility, security, privacy, and compliance activities.
* Continuous improvement and change control.

---

## **3. References**

* SOP-DC-001 — Design and Development Control
* WI-DC-002 — Ontario DSS Implementation
* Ontario Digital Service Standard (DSS)
* Service Design Playbook
* ISO 9001:2015, ISO 90003, ISO 13485 (if applicable)
* IEC 62304, IEC 62366, ISO 14971
* ISO/IEC 27001, ISO/IEC 27701
* FDA 21 CFR Part 11 (if applicable)
* Open Data Guidebook

---

## **4. Roles and Responsibilities**

| Role                                       | Responsibilities                                                                                                                           |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Design Owner / Product Manager**         | Leads DSS implementation, approves deliverables, ensures SOP compliance, oversees user research, prototypes, MVP, and live service.        |
| **QA / Compliance Lead**                   | Reviews DSS outputs for compliance with SOP and regulatory requirements, ensures traceability, maintains verification/validation evidence. |
| **Management**                             | Reviews and approves phase outputs, ensures resources and governance oversight.                                                            |
| **Project Team / Multi-disciplinary Team** | Execute DSS activities including research, prototyping, testing, and documentation.                                                        |

---

## **5. DSS-Aligned Design Control Phases**

### **5.1 Discovery Phase**

**Objectives:** Understand user needs, identify barriers, assess feasibility.
**Activities:**

* Conduct user research, interviews, and stakeholder analysis.
* Identify primary user groups, personas, and needs.
* Evaluate existing services and barriers.
* Document findings, regulatory constraints, and feasibility.
* Assign product manager and establish agile workflow.

**Deliverables / Records:** User research report, personas, needs analysis, feasibility study, project initiation documentation.
**Verification / Validation:** Confirm outputs accurately reflect user needs and initial requirements.
**Risk Management:** Capture early risks related to feasibility, accessibility, and compliance.

---

### **5.2 Alpha Phase**

**Objectives:** Co-create solutions and validate technical and financial feasibility.
**Activities:**

* Conduct stakeholder co-creation sessions.
* Build and test prototypes.
* Plan and execute user testing, journey mapping, and usability assessments.
* Conduct technical and financial feasibility assessment.
* Document required process changes.

**Deliverables / Records:** Prototypes, usability reports, journey maps, initial project plan.
**Verification / Validation:** Ensure prototypes meet user needs and SOP requirements.
**Risk Management:** Log risks in Risk Register; define mitigation strategies.

---

### **5.3 Beta Phase**

**Objectives:** Build MVP, validate accessibility, security, and performance.
**Activities:**

* Develop minimum viable product (MVP).
* Conduct continuous user testing and automated testing.
* Perform device and accessibility validation (WCAG, inclusive design).
* Monitor KPIs and service performance.
* Maintain privacy and security compliance.

**Deliverables / Records:** MVP, testing logs, accessibility reports, KPIs, privacy/security reports, maintenance plan.
**Verification / Validation:** Confirm MVP meets requirements; review against DSS principles.
**Risk Management:** Implement risk controls and update mitigation actions.

---

### **5.4 Live Phase**

**Objectives:** Maintain, improve, and monitor service post-launch.
**Activities:**

* Service maintenance, updates, and feature releases.
* Ongoing usability testing and user feedback evaluation.
* Monitor web analytics and performance metrics.
* Open data publication and disaster recovery planning.
* Ensure continued compliance with DSS and SOP.

**Deliverables / Records:** Maintenance logs, performance metrics, open data, lessons learned, recovery plan.
**Verification / Validation:** Monitor service against intended outcomes and collect evidence for compliance.
**Risk Management:** Continuously review and mitigate operational risks.

---

## **6. Methodologies and Tools**

* Agile methodology for iterative development.
* User-centered design practices with continuous user feedback.
* Low- to high-fidelity prototyping and MVP development.
* Accessibility and inclusive design (WCAG / AODA).
* Traceability maintained via QMS-approved platforms (GitHub, Jira, Confluence, etc.).
* Security and privacy controls (ISO/IEC 27001 & 27701).
* DSS phase approvals aligned with SOP management reviews.

---

## **7. Risk Management**

* Maintain a **Risk Log** for all phases.
* Identify, assess, and mitigate design, operational, and regulatory risks.
* Apply ISO 14971, IEC 62304, and SOP-DC-001 principles.
* Review risks at each phase and at project closure.

---

## **8. Traceability & Verification/Validation**

* Link all deliverables to DSS phases, SOP clauses, and applicable standards.
* Maintain evidence of verification and validation (test reports, usability reports, pull requests, review minutes).
* Update the **traceability matrix** continuously.

---

## **9. Change Control**

* Document all changes in project tracking or controlled record repository.
* Review by Design Owner and QA for SOP/DSS compliance.
* Approve changes prior to implementation.
* Update related deliverables and traceability records.

---

## **10. Deliverables Checklist (Generic, DSS-Aligned)**

| DSS Phase     | Deliverable                         | SOP Clause | DSS Principle / Objective            | Applicable Standards / Regulations         | Completed (✓) | Reference / Record |
| ------------- | ----------------------------------- | ---------- | ------------------------------------ | ------------------------------------------ | ------------- | ------------------ |
| **Discovery** | User research report                | 6.2        | Data-informed, prioritize user needs | ISO 9001:2015, ISO 90003, ISO/IEC 27001    |               |                    |
|               | Personas & primary user groups      | 6.2, 6.3   | Equitable access, user-centered      | ISO 9001:2015, IEC 62366                   |               |                    |
|               | Needs & requirements analysis       | 6.2        | Data-informed                        | ISO 9001:2015, ISO 90003                   |               |                    |
|               | Market/regulatory/feasibility study | 6.2, 6.3   | Transparency, feasibility            | Ontario DSS, ISO 9001:2015                 |               |                    |
|               | Product manager assignment          | 5          | Governance, accountability           | ISO 9001:2015                              |               |                    |
|               | Agile workflow setup                | 6.1, 6.3   | Iterative development                | Ontario DSS, ISO 90003                     |               |                    |
| **Alpha**     | Co-creation session notes           | 6.3, 6.4   | User-centered, transparent           | IEC 62366, ISO 9001:2015                   |               |                    |
|               | Prototypes / mockups                | 6.3        | Iterative design                     | ISO 90003, IEC 62304                       |               |                    |
|               | User testing plan                   | 6.3, 6.4   | User-centered design                 | IEC 62366, ISO 9001:2015                   |               |                    |
|               | Usability testing reports           | 6.4        | Accessibility, inclusive             | IEC 62366, AODA/WCAG                       |               |                    |
|               | Journey map                         | 6.3        | Data-informed                        | ISO 9001:2015, Ontario DSS                 |               |                    |
|               | Technical feasibility assessment    | 6.2, 6.3   | Data-informed, risk-aware            | ISO 90003, IEC 62304                       |               |                    |
|               | Financial feasibility assessment    | 6.3        | Data-informed                        | ISO 9001:2015                              |               |                    |
|               | Initial project plan                | 6.1, 6.3   | Governance, transparency             | ISO 9001:2015                              |               |                    |
| **Beta**      | Minimum Viable Product (MVP)        | 6.3, 6.4   | Iterative, user-centered             | ISO 90003, IEC 62304, IEC 62366, ISO 13485 |               |                    |
|               | Continuous user testing results     | 6.4        | User-centered                        | IEC 62366, AODA/WCAG                       |               |                    |
|               | Device validation                   | 6.4        | Accessibility                        | IEC 62366, WCAG                            |               |                    |
|               | Accessibility testing               | 6.4        | Inclusive access                     | IEC 62366, AODA/WCAG                       |               |                    |
|               | KPIs and performance metrics        | 6.4        | Data-informed                        | ISO 9001:2015                              |               |                    |
|               | Privacy & security report           | 6.3, 6.4   | Data protection                      | ISO/IEC 27001, ISO/IEC 27701               |               |                    |
|               | Automated testing results           | 6.4        | Continuous improvement               | ISO 90003, IEC 62304                       |               |                    |
|               | Branding compliance                 | 6.3        | Transparency, consistent design      | Ontario Design System                      |               |                    |
|               | Maintenance & update plan           | 6.5        | Continuous improvement               | ISO 9001:2015, IEC 62304                   |               |                    |
| **Live**      | Service maintenance logs            | 6.5, 6.6   | Continuous improvement               | ISO 9001:2015, IEC 62304                   |               |                    |
|               | Ongoing usability testing           | 6.4, 6.6   | User-centered                        | IEC 62366, WCAG                            |               |                    |
|               | Feature backlog updates             | 6.3, 6.5   | Iterative design                     | ISO 90003                                  |               |                    |
|               | Web analytics reports               | 6.4        | Data-informed                        | ISO 9001:2015 | | |
| | Performance metrics | 6.4, 6.6 | Data-informed | ISO 9001:2015 | | |
| | Open data publication | 6.6 | Transparency, access | Open Data Guidebook, ISO/IEC 27001 | | |
| | Disaster recovery / recovery plan | 6.3, 6.5 | Risk mitigation | ISO/IEC 27001, ISO 9001:2015 | | |
| | Lessons learned / continuous improvement | 6.6, 6.1 | Continuous improvement | ISO 9001:2015 | | |

---

## **11. Records & Archiving**

| Record Type                        | Location / Reference      | Retention Period |
| ---------------------------------- | ------------------------- | ---------------- |
| DSS Phase Deliverables & Evidence  | Project repository / Wiki | 10 years         |
| Risk Log                           | Central QMS repository    | 10 years         |
| Verification & Validation Evidence | Test system / Repo        | 10 years         |
| Phase Approvals / Review Minutes   | QMS repository / Jira     | 10 years         |
| Release Record                     | QMS / Product repository  | Permanent        |

---

## **12. Compliance & Standards Matrix (Generic)**

| DSS Phase | Deliverables / Activities                                                           | Applicable Standards / Regulations                                       |
| --------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Discovery | Research reports, personas, feasibility study                                       | ISO 9001, ISO 90003, IEC 62366, ISO/IEC 27001, ISO 14971                 |
| Alpha     | Prototypes, journey maps, feasibility assessment                                    | ISO 90003, IEC 62304, IEC 62366, ISO 13485                               |
| Beta      | MVP, user testing, device & accessibility validation, KPIs, privacy/security report | ISO 90003, IEC 62304, IEC 62366, ISO 13485, ISO/IEC 27001, ISO/IEC 27701 |
| Live      | Service maintenance, updates, web analytics, open data, disaster recovery           | ISO 9001, ISO 90003, IEC 62304, IEC 62366, ISO/IEC 27001                 |
