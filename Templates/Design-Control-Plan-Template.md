# **TPL – Design Control Plan (DCP) Template**

**Slug:** Design-Control-Plan-Template  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Design-Control-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Design-Control-Plan-Template  

---

## **1. Purpose**

To define the design and development control framework for this project, ensuring that all stages — from requirements through release — are planned, documented, reviewed, verified, and validated in accordance with the Floating Eye Software (FLEY) Quality Management System (QMS).

---

## **2. Scope**

This plan applies to all design and development activities for the project identified above, including:

* Requirements definition and traceability
* Design and implementation
* Verification and validation
* Risk management and design review
* Configuration and change control

If this project does **not** include design or development (e.g., purely operational or maintenance work), reference this DCP section in the Project Quality Plan (PQP) and mark “Not Applicable”.

---

## **3. References**

| Document                            | Description                                              |
| ----------------------------------- | -------------------------------------------------------- |
| Design Control SOP                  | Defines FLEY’s standard design control process           |
| Project Management SOP              | Defines project planning, monitoring, and closure        |
| Risk and Opportunity Management SOP | Defines risk identification and control                  |
| Change Control SOP                  | Defines change evaluation and approval                   |
| [Project Quality Plan]              | Project-specific quality management plan                 |
| [Risk Register]                     | Risk log and mitigation actions                          |
| [Design Trace Matrix]               | Requirement → Design → Verification → Validation mapping |

---

## **4. Roles and Responsibilities**

| Role                                     | Responsibility                                                              |
| ---------------------------------------- | --------------------------------------------------------------------------- |
| **Project Manager**                      | Maintains this plan; ensures all design stages are executed and documented. |
| **Design Lead / Engineer**               | Develops design outputs, participates in reviews, ensures traceability.     |
| **Quality Manager**                      | Verifies compliance with QMS requirements; supports audits.                 |
| **Verification & Validation (V&V) Lead** | Plans and documents verification and validation activities.                 |
| **Regulatory / Privacy Officer**         | Reviews regulatory, data protection, and compliance aspects.                |
| **Configuration Manager**                | Manages baselines, version control, and change history.                     |

---

## **5. Design and Development Framework**

| Phase                             | Objectives                                                            | Key Deliverables                                                           | Review Points / Approval       |
| --------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------ |
| **5.1 Design Planning**           | Define scope, milestones, resources, and deliverables.                | Design Control Plan (this document), design schedule, risk updates.        | Design Control Kickoff Review  |
| **5.2 Requirements Definition**   | Capture and approve functional/non-functional requirements.           | Approved requirements list or backlog, acceptance criteria, risk analysis. | Requirements Review            |
| **5.3 Design & Implementation**   | Translate requirements into architecture, design, and implementation. | Design specifications, models, code, test plans.                           | Design Review(s), Code Reviews |
| **5.4 Verification**              | Confirm design outputs meet input requirements.                       | Test reports, inspection checklists, peer review records.                  | Verification Review            |
| **5.5 Validation**                | Demonstrate the final product meets intended use and user needs.      | Validation protocol and report, stakeholder approval.                      | Validation Review              |
| **5.6 Design Transfer / Release** | Ensure deliverables are ready for release or deployment.              | Release notes, deployment checklist, training materials.                   | Release Readiness Review       |

---

## **6. Design Reviews**

| Review Type             | Trigger / Timing                     | Participants                      | Expected Outputs                     |
| ----------------------- | ------------------------------------ | --------------------------------- | ------------------------------------ |
| **Kickoff Review**      | At project start                     | PM, Design Lead, Quality          | Approved DCP, roles confirmed        |
| **Requirements Review** | Upon completion of requirements      | PM, Design Lead, Stakeholders     | Requirements approved, risks updated |
| **Design Review(s)**    | At completion of major design stages | Design team, QA, optional experts | Review minutes, action items         |
| **Verification Review** | After testing                        | QA, Dev, V&V Lead                 | Verification summary approved        |
| **Validation Review**   | After validation                     | QA, Stakeholders                  | Validation summary approved          |
| **Release Review**      | Prior to deployment                  | PM, QA, Ops                       | Release authorization                |

---

## **7. Risk and Opportunity Management**

* Risks shall be identified and tracked per **Risk-and-Opportunity-Management-SOP**.
* Use the project’s **Risk Register** or linked Issues in GitHub/Confluence.
* Key risks should include:

  * Design complexity and feasibility
  * Regulatory / compliance risk
  * Data protection or security risk
  * Schedule or dependency risk
* All design risks must have associated mitigation actions before release.

**Link to Risk Register:** [Insert link or ID]

---

## **8. Design Traceability**

All design outputs must be traceable to their corresponding inputs, verification, and validation evidence.

| Requirement ID | Design Output(s)         | Verification Evidence  | Validation Evidence              | Status      |
| -------------- | ------------------------ | ---------------------- | -------------------------------- | ----------- |
| REQ-001        | [Design Spec / Code Ref] | [Unit Test # / Report] | [User Test / Validation Summary] | Complete    |
| REQ-002        | ...                      | ...                    | ...                              | In Progress |

(Attach or link to a complete traceability matrix where appropriate.)

---

## **9. Configuration and Change Control**

All design artifacts (requirements, designs, code, tests, etc.) must be controlled through the configuration management tool defined in the **PQP**.

* **Tool:** [GitHub / Jira / Confluence / Other]
* **Change Workflow:**

  1. Submit change request or pull request.
  2. Review by design lead and quality rep.
  3. Assess impact on risks and requirements.
  4. Approve and merge / implement.

All changes must be traceable to their originating request, issue, or CAPA.

---

## **10. Verification and Validation Plan Summary**

| Activity            | Description                                    | Method                        | Responsible   | Evidence           |
| ------------------- | ---------------------------------------------- | ----------------------------- | ------------- | ------------------ |
| Unit Testing        | Verify each module meets design requirements   | Automated tests               | Developer     | Unit Test Report   |
| Integration Testing | Verify subsystems work together                | Test suites                   | QA / V&V Lead | Integration Report |
| System Testing      | Verify complete system behavior                | Full system tests             | QA            | Test Report        |
| Validation          | Demonstrate intended use and user satisfaction | User acceptance or simulation | Stakeholders  | Validation Report  |

Full V&V evidence shall be attached to this plan or referenced by link.

---

## **11. Design Outputs and Deliverables Checklist**


### **11.1. Design Planning**

| Deliverable                   | Description                                            | Responsible     | Status | Reference / Link |
| ----------------------------- | ------------------------------------------------------ | --------------- | ------ | ---------------- |
| Design Control Plan (DCP)     | Defines framework, stages, and reviews for the project | Project Manager |        |                  |
| Project Quality Plan (PQP)    | Defines quality and compliance requirements            | Quality Manager |        |                  |
| Project Plan / Schedule       | Defines tasks, milestones, and dependencies            | Project Manager |        |                  |
| Risk & Opportunity Register   | Project-level risks, updated throughout design         | Risk Owner / QA |        |                  |
| Configuration Management Plan | Defines versioning and change control tools            | Design Lead     |        |                  |

---

### **11.2. Design Inputs**

| Deliverable                             | Description                                                 | Responsible          | Status | Reference / Link |
| --------------------------------------- | ----------------------------------------------------------- | -------------------- | ------ | ---------------- |
| User Needs / Intended Use               | Problem statement, user stories, or stakeholder needs       | Project Manager      |        |                  |
| System Requirements Specification (SRS) | Functional and non-functional requirements                  | Design Lead          |        |                  |
| Regulatory / Compliance Requirements    | Applicable standards, laws, or regulatory clauses           | Quality / Regulatory |        |                  |
| Risk Analysis (Initial)                 | Design risk assessment — hazard identification and controls | QA / Risk Lead       |        |                  |

---

### **11.11.3. Design Outputs**

| Deliverable                                | Description                                        | Responsible            | Status | Reference / Link |
| ------------------------------------------ | -------------------------------------------------- | ---------------------- | ------ | ---------------- |
| System Architecture / Design Specification | High-level design and interfaces                   | Design Lead            |        |                  |
| Detailed Design Documents                  | Component or module-level design                   | Developers / Engineers |        |                  |
| Source Code / Implementation Artifacts     | Executable design outputs                          | Developers             |        |                  |
| Test Specifications / Procedures           | Verification protocols                             | QA / V&V               |        |                  |
| Traceability Matrix                        | Links Inputs → Outputs → Verification → Validation | Design Lead            |        |                  |

---

### **11.4. Design Reviews**

| Deliverable                     | Description                                               | Responsible           | Status | Reference / Link |
| ------------------------------- | --------------------------------------------------------- | --------------------- | ------ | ---------------- |
| Kickoff / Planning Review       | Confirms plan, roles, and deliverables                    | PM / QA               |        |                  |
| Requirements Review             | Confirms completeness and testability of inputs           | PM / QA               |        |                  |
| Preliminary Design Review (PDR) | Verifies initial architecture/design                      | Design Lead / QA      |        |                  |
| Critical Design Review (CDR)    | Confirms detailed design and readiness for implementation | Design Lead / QA      |        |                  |
| Verification Review             | Confirms all verification evidence is complete            | QA / V&V              |        |                  |
| Validation Review               | Confirms intended use is achieved                         | PM / QA / Stakeholder |        |                  |
| Release Review                  | Final approval before release                             | PM / QA / Regulatory  |        |                  |

---

### **11.5. Verification and Validation**

| Deliverable         | Description                                                    | Responsible | Status | Reference / Link |
| ------------------- | -------------------------------------------------------------- | ----------- | ------ | ---------------- |
| Verification Plan   | Defines test methods, responsibilities, and pass/fail criteria | QA / V&V    |        |                  |
| Verification Report | Results demonstrating design meets requirements                | QA / V&V    |        |                  |
| Validation Plan     | Defines validation environment and acceptance criteria         | PM / QA     |        |                  |
| Validation Report   | Confirms final product meets intended use                      | QA / PM     |        |                  |

---

### **11.6. Design Transfer and Release**

| Deliverable                   | Description                                   | Responsible      | Status | Reference / Link |
| ----------------------------- | --------------------------------------------- | ---------------- | ------ | ---------------- |
| Release Record / Package      | Configuration baseline for release            | PM / QA          |        |                  |
| Deployment Checklist          | Validation of deployment steps                | PM / Ops         |        |                  |
| User Documentation / Training | Manuals, help guides, training materials      | PM / Tech Writer |        |                  |
| Post-Release Risk Review      | Final check of residual risks and mitigations | QA / Risk Lead   |        |                  |

---

### **11.7 Post-Release Maintenance and Retirement**

| Deliverable                      | Purpose                                                                                            | Responsible           | Status | Reference / Link |
| -------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------- | ------ | ---------------- |
| **Maintenance Plan**             | Defines maintenance classification (routine patch vs corrective change) and verification strategy. | Maintenance Lead / QA |        |                  |
| **Maintenance Log**              | Tracks maintenance releases, CAPAs, verification & validation, and DHF updates.                    | Maintenance Lead      |        |                  |
| **Post-Market Feedback Summary** | Records user feedback, complaints, or CAPA drivers used for design improvement.                    | QA / Regulatory       |        |                  |
| **Retirement Plan**              | Defines archival, decommissioning, and record retention actions.                                   | PM / QA               |        |                  |

---

## **12. Records and Retention**

| Record                              | Storage Location         | Retention Period             |
| ----------------------------------- | ------------------------ | ---------------------------- |
| Design Control Plan                 | Project Repository       | 10 years                     |
| Design Review Minutes               | Linked / Confluence      | 10 years                     |
| Risk Register                       | Central QMS Repository   | 10 years                     |
| Verification & Validation Records   | Test System              | 10 years                     |
| Release Records                     | QMS / Product Repository | Permanent                    |
| **Maintenance Logs (NEW)**          | DHF / Maintenance Folder | 10 years after final release |
| **Retirement Plan & Records (NEW)** | QMS Repository           | Permanent                    |

---

### 💡 *Implementation Notes*

* If using GitHub:

  * Each **design deliverable** can be tracked as an **Issue** or **Milestone**.
  * **Project board** represents design phase progress.
  * Use labels: “Design Input,” “Design Output,” “Verification,” “Validation,” etc.
* If using Confluence or similar:

  * Maintain a page hierarchy reflecting the above phases.
  * Link artifacts directly to their review records.
