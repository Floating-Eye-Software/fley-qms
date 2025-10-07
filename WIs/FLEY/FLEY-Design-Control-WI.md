# **Work Instruction: WI-QMS-09-04 — FLEY Design Control Framework**

**Document Number:** WI-QMS-09-04
**Revision:** 1.0
**Effective Date:** [Insert Date]
**Related SOP:** QMS-SOP-09 — Design and Development Control

---

## **1. Purpose**

To define the **Floating Eye Software (FLEY) standard design and development framework**, ensuring that all project stages—from requirements through release—are controlled, traceable, verified, validated, and compliant with applicable regulatory and quality standards.

This WI ensures that all deliverables outlined in the **FLEY Design Control Plan (DCP)** are created, reviewed, and approved in accordance with **QMS-SOP-09**.

---

## **2. Scope**

Applies to all projects that adopt the **FLEY SDLC methodology**, including software, health software, or system development projects. This WI covers:

* Requirements capture and traceability
* Design, implementation, and testing
* Verification and validation
* Risk and opportunity management
* Configuration and change control
* Design transfer and release

Projects not involving design or development (e.g., operational maintenance) should reference this WI in the **Project Quality Plan (PQP)** and mark relevant sections as “Not Applicable.”

---

## **3. References**

| Reference                | Document No.                   | Title / Purpose                                         |
| ------------------------ | ------------------------------ | ------------------------------------------------------- |
| QMS-SOP-09               | Design and Development Control | Defines high-level design control requirements          |
| QMS-SOP-07               | Project Management             | Defines project planning, monitoring, and closure       |
| QMS-SOP-08               | Risk & Opportunity Management  | Defines risk identification and control                 |
| QMS-SOP-02               | Change Control                 | Defines change evaluation and approval process          |
| FLEY Design Control Plan | [Link]                         | Defines project-specific deliverables, reviews, and V&V |
| Risk Register            | [Link]                         | Risk tracking and mitigation                            |
| Design Trace Matrix      | [Link]                         | Traceability from requirements → outputs → V&V          |

---

## **4. Roles and Responsibilities**

| Role                                     | Responsibilities                                                        |
| ---------------------------------------- | ----------------------------------------------------------------------- |
| **Project Manager (PM)**                 | Maintains DCP, ensures design stages are executed and reviewed per WI.  |
| **Design Lead / Engineer**               | Develops design outputs, ensures traceability, participates in reviews. |
| **Quality Manager / QA Lead**            | Verifies compliance, reviews deliverables, maintains audit readiness.   |
| **Verification & Validation (V&V) Lead** | Plans, executes, and documents V&V activities, maintains evidence.      |
| **Regulatory / Privacy Officer**         | Reviews regulatory and data protection compliance.                      |
| **Configuration Manager**                | Maintains baselines, version control, and change records.               |
| **Project Team / Developers**            | Produce design and implementation deliverables, participate in reviews. |

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

## **10. Deliverables Checklist by Phase**

| Phase                   | Deliverable                                                        | Description                                | Responsible              | SOP / Standard           | Status | Reference / Link |
| ----------------------- | ------------------------------------------------------------------ | ------------------------------------------ | ------------------------ | ------------------------ | ------ | ---------------- |
| Planning                | DCP / Project Schedule / Risk Register                             | Project planning artifacts                 | PM / QA                  | QMS-SOP-09               | ☐ / ☑  |                  |
| Requirements            | SRS / Acceptance Criteria / Risk Analysis                          | Capture user, functional, regulatory needs | Design Lead              | ISO 9001:2015, IEC 62304 | ☐ / ☑  |                  |
| Design & Implementation | Architecture / Detailed Design / Code / Test Plan                  | Design and implementation outputs          | Design Lead / Developers | QMS-SOP-09               | ☐ / ☑  |                  |
| Verification            | Test Reports / Inspection / Peer Review                            | Confirm outputs meet inputs                | QA / V&V Lead            | ISO 9001, IEC 62304      | ☐ / ☑  |                  |
| Validation              | Validation Plan / Report / Stakeholder Approval                    | Confirm intended use and user satisfaction | PM / QA / Stakeholders   | ISO 9001, IEC 62304      | ☐ / ☑  |                  |
| Release                 | Release Package / Deployment / Training / Post-Release Risk Review | Final release and documentation            | PM / QA / Ops            | ISO 9001, IEC 62304      | ☐ / ☑  |                  |

---

## **11. Records & Retention**

| Record                            | Storage Location              | Retention Period |
| --------------------------------- | ----------------------------- | ---------------- |
| Design Control Plan (DCP)         | Project repository            | 10 years         |
| Design Review Minutes             | Linked to issues / Confluence | 10 years         |
| Risk Register                     | Central QMS repository        | 10 years         |
| Verification & Validation Records | Repository / Test system      | 10 years         |
| Release Records                   | QMS / Product repository      | Permanent        |

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

## **13. Review & Approval**

| Role / Name                                  | Signature | Date |
| -------------------------------------------- | --------- | ---- |
| Project Manager                              |           |      |
| Design Lead                                  |           |      |
| Quality Manager                              |           |      |
| Regulatory / Privacy Officer (if applicable) |           |      |

---

### 💡 *Implementation Notes*

* Maintain **phase artifacts in GitHub / Jira / Confluence** and link directly to DCP deliverables.
* Use **labels / tags**: Design Input, Design Output, Verification, Validation, Release.
* Conduct reviews at **predefined SDLC gates**.
* Continuously update **traceability and risk records**.
