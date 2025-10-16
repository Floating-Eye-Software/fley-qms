# **WI - FLEY Design Control Framework**

**Slug:** FLEY-Design-Control-WI  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Design-Control-SOP   
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/FLEY-Design-Control-WI  

---

## **1 Purpose**

To define the **Floating Eye Software (FLEY)** design, development, maintenance, and retirement framework ensuring traceable, verified, and validated lifecycle control compliant with QMS-SOP-09 v 3.0.

---

## **2 Scope**

Applies to all projects using the **FLEY SDLC**: requirements → design → implementation → V&V → release → maintenance → retirement.
Non-design projects mark sections “N/A” in the PQP.

---

## **3 References**

QMS-SOP-09 Design & Development Control
QMS-SOP-07 Project Management
QMS-SOP-08 Risk & Opportunity Management
QMS-SOP-02 Change Control
QMS-SOP-05 Document & Record Control
FLEY Design Control Plan (DCP) | Risk Register | Design Trace Matrix

---

## **4 Roles & Responsibilities**

| Role                         | Responsibilities                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------- |
| Project Manager (PM)         | Owns DCP, ensures execution of all phases including post-release maintenance.         |
| Design Lead / Engineer       | Produces design outputs, maintains traceability.                                      |
| QA / Quality Manager         | Verifies compliance, reviews deliverables, approves releases and maintenance updates. |
| V&V Lead                     | Plans and executes V&V activities through maintenance releases.                       |
| Regulatory / Privacy Officer | Reviews compliance and data protection impacts.                                       |
| Configuration Manager        | Maintains baselines and version control.                                              |
| Maintenance Lead / Ops Team  | Implements bug fixes, patches, and retirement plans under change control.             |

---

## **5. Procedure**

### **5.1 Design Planning**

* Define project scope, milestones, resources, and deliverables.
* Complete and approve the **FLEY DCP**.
* Review and update the **Risk Register** for potential design and regulatory risks.
* Conduct **Design Control Kickoff Review** (PM, Design Lead, QA).

**Deliverables:** DCP, Project Schedule, Risk Register updates.
**Review:** Design Control Kickoff Review.

---

### **5.2 Requirements Definition**

* Capture functional and non-functional requirements, user needs, and intended use.
* Identify regulatory and compliance requirements.
* Conduct preliminary risk assessment.
* Approve requirements and acceptance criteria.

**Deliverables:** Requirements Specification (SRS), Acceptance Criteria, Risk Analysis.
**Review:** Requirements Review.
**Traceability:** Map requirements to design outputs, verification, and validation evidence.

---

### **5.3 Design & Implementation**

* Translate requirements into architecture, component designs, and implementation plans.
* Develop source code, models, and design documentation.
* Conduct internal **peer and code reviews**.
* Update the **traceability matrix** continuously.

**Deliverables:** System Architecture, Detailed Design Docs, Source Code, Test Plans.
**Review:** Preliminary Design Review (PDR) and Critical Design Review (CDR).
**Risk:** Ensure design mitigations are incorporated.

---

### **5.4 Verification**

* Confirm design outputs meet specified requirements.
* Methods include unit testing, integration testing, inspections, and static analysis.
* Document evidence in **Verification Reports** and link to corresponding requirements.

**Deliverables:** Test Reports, Inspection Checklists, Peer Review Records.
**Review:** Verification Review.

---

### **5.5 Validation**

* Demonstrate the final product meets intended use and user needs.
* Methods include user acceptance testing (UAT), pilot testing, or simulated use.
* Document results in **Validation Reports** and obtain stakeholder approval.

**Deliverables:** Validation Plan, Validation Report, Stakeholder Approval.
**Review:** Validation Review.

---

### **5.6 Design Transfer / Release**

* Ensure deliverables are ready for production or deployment.
* Include release notes, deployment checklists, user documentation, and training materials.
* Conduct final risk review to confirm mitigations are effective.

**Deliverables:** Release Package, Deployment Checklist, Training Materials, Post-Release Risk Review.
**Review:** Release Readiness Review.

---

### **5.7 Post-Release Maintenance and Retirement**

* Post-release activities are managed as controlled design changes.
* Inputs → CAPA items, user feedback, vulnerability or regulatory updates.
* Process:

  1. Triage & impact assessment.
  2. Plan maintenance (define scope, verification, validation).
  3. Implement and test under configuration control.
  4. Record results in Maintenance Log and DHF.
  5. Review and approve release by PM and QA.
* **Deliverables:** Maintenance Plan, Maintenance Log, Updated Risk Register, Updated Trace Matrix.
* **Retirement:**
  – Plan decommissioning, obtain approval.
  – Ensure customer notification and data archival.
  – Retain records per QMS-SOP-05.

---

## **6. Risk & Opportunity Management**

* Identify risks at each SDLC phase in the **Risk Register**.
* Assign mitigation actions and track closure.
* Review key risks during design, verification, validation, and release phases.
* Apply ISO 14971, IEC 62304, and QMS-SOP-08 principles.

---

## **7. Design Traceability**

* Maintain a **Traceability Matrix** linking:

  1. Requirements → Design Outputs
  2. Outputs → Verification Evidence
  3. Outputs → Validation Evidence
  4. Associated Risk Controls

* Update continuously and attach or link to the DCP.

---

## **8. Configuration & Change Control**

* All design artifacts must be version-controlled in the approved **CM tool** (GitHub, Jira, Confluence, etc.).

* **Change workflow:**

  1. Submit request / pull request
  2. Review by Design Lead and QA
  3. Assess impact on requirements, risks, and deliverables
  4. Approve and implement changes

* Record all changes in the traceability matrix.

---

## **9. Verification & Validation (V&V) Plan**

| Activity            | Method / Criteria                       | Responsible            | Evidence           |
| ------------------- | --------------------------------------- | ---------------------- | ------------------ |
| Unit Testing        | Automated / manual per module           | Developer              | Unit Test Report   |
| Integration Testing | Test suites for component interaction   | QA / V&V Lead          | Integration Report |
| System Testing      | Complete system verification            | QA                     | System Test Report |
| Validation          | UAT or simulation, stakeholder approval | PM / QA / Stakeholders | Validation Report  |

---

## **10 Deliverables Checklist by Phase**

| Phase                              | Deliverable                                           | Description                          | Responsible            | Status |
| ---------------------------------- | ----------------------------------------------------- | ------------------------------------ | ---------------------- | ------ |
| Planning                           | DCP / Schedule / Risk Register                        | Project planning artifacts           | PM / QA                | ☐ / ☑  |
| Requirements                       | SRS / Acceptance Criteria / Risk Analysis             | Define user and regulatory needs     | Design Lead            | ☐ / ☑  |
| Design & Implementation            | Architecture / Design Docs / Code / Test Plan         | Design outputs                       | Design Lead / Dev      | ☐ / ☑  |
| Verification                       | Test Reports / Peer Reviews                           | Confirm outputs meet inputs          | QA / V&V               | ☐ / ☑  |
| Validation                         | Validation Plan / Report                              | Confirm intended use                 | PM / QA / Stakeholders | ☐ / ☑  |
| Release                            | Release Package / Training / Post-Release Risk Review | Ready for deployment                 | PM / QA                | ☐ / ☑  |
| Maintenance & Retirement           | Maintenance Plan / Maintenance Log / Retirement Plan  | Post-release control and EOL records | Maintenance Lead / QA  | ☐ / ☑  |

---

## **11 Records & Retention**

| Record                 | Storage             | Retention                  |
| ---------------------- | ------------------- | -------------------------- |
| Design Control Plan    | Project repo        | 10 yrs                     |
| Design Review Minutes  | Confluence / Issues | 10 yrs                     |
| Risk Register          | Central QMS repo    | 10 yrs                     |
| V&V Records            | Test system         | 10 yrs                     |
| Release Records        | QMS repo            | Permanent                  |
| **Maintenance Logs**   | Maintenance folder  | 10 yrs after final release |
| **Retirement Records** | QMS repo            | Permanent                  |

---

## **12. Compliance & Standards Matrix**

| Phase                   | Deliverables / Activities                   | Applicable Standards / Regulations      |
| ----------------------- | ------------------------------------------- | --------------------------------------- |
| Requirements            | SRS, Acceptance Criteria                    | ISO 9001:2015 8.3, IEC 62304, IEC 62366 |
| Design & Implementation | Architecture, Design Docs, Code, Test Plans | ISO 9001:2015 8.3, IEC 62304            |
| Verification            | Unit / Integration / System Testing         | ISO 9001:2015 8.3, IEC 62304            |
| Validation              | UAT, Pilot Testing                          | ISO 9001:2015 8.3, IEC 62304            |
| Release                 | Deployment, Training, Documentation         | ISO 9001:2015 8.3, IEC 62304            |

---

### 💡 *Implementation Notes*

* Maintain **phase artifacts in GitHub / Jira / Confluence** and link directly to DCP deliverables.
* Use **labels / tags**: Design Input, Design Output, Verification, Validation, Release.
* Conduct reviews at **predefined SDLC gates**.
* Continuously update **traceability and risk records**.
