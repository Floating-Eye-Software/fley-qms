# **Work Instruction: WI-DC-002 — Ontario Design System Implementation**

**Document Number:** WI-DC-002
**Revision:** 1.0
**Effective Date:** [Insert Date]
**Related SOP:** SOP-DC-001 — Design and Development Control

---

## **1. Purpose**

To define how the Ontario Service Design Framework (Digital Service Standard, Service Design Playbook) is implemented to satisfy the organization’s Design Control SOP (SOP-DC-001). This WI ensures traceability, verification, validation, and controlled records for projects following the Ontario design and release methodology.

---

## **2. Scope**

Applies to all projects adopting the Ontario Service Design Framework, including digital services, software development, and health software projects. This WI maps the **DSS phases** (Discovery, Alpha, Beta, Live) to **design control requirements** in SOP-DC-001.

---

## **3. References**

* SOP-DC-001 — Design and Development Control
* Ontario Digital Service Standard (DSS)
* Ontario Service Design Playbook
* Red Witch Design Control Plan
* ISO 9001:2015 Clause 8.3
* ISO 90003 — Software engineering guidelines
* IEC 62304, IEC 62366, ISO 14971, ISO 13485
* ISO/IEC 27001, ISO/IEC 27701
* FDA 21 CFR Part 11

---

## **4. Responsibilities**

| Role                                       | Responsibilities                                                                                                                                                         |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Design Owner / Product Manager**         | Leads the Ontario DSS implementation, ensures compliance with SOP-DC-001, approves deliverables, oversees user research, prototypes, MVP, and live service improvements. |
| **QA / Compliance Lead**                   | Ensures DSS activities meet design control, ISO 9001, and regulatory standards. Reviews evidence and traceability.                                                       |
| **Management**                             | Reviews and approves outputs at key DSS phase checkpoints. Ensures resources and governance oversight.                                                                   |
| **Team Members / Multi-disciplinary Team** | Execute discovery, alpha, beta, and live activities. Conduct usability testing, prototype development, and documentation.                                                |

---

## **5. Procedure: DSS Phases Mapped to Design Control**

| DSS Phase     | Design Control Activities                                                                                                                                       | Deliverables / Records                                                                                         | SOP-DC-001 Mapping                                          |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Discovery** | Conduct user research, identify user groups, assess existing services, document barriers, designate Product Manager, establish Agile workflow                   | User research reports, personas, needs analysis, feasibility study, project initiation documents               | Design Inputs, Planning, Roles & Responsibilities           |
| **Alpha**     | Co-create solutions with users/stakeholders, build/test prototypes, assess technical/financial feasibility, journey mapping, initial project plan               | Prototypes, usability reports, journey maps, initial project plan                                              | Design Execution, Verification, Initial Output              |
| **Beta**      | Build MVP, perform continuous user testing, device/accessibility validation, measure KPIs, resolve technical/process challenges, privacy/security documentation | MVP, automated testing results, device validation logs, accessibility reports, privacy/security reports, KPIs  | Design Execution, Verification, Validation, Output Approval |
| **Live**      | Service maintenance, ongoing usability testing, continuous improvement, performance measurement, open data publication, disaster recovery                       | Maintenance logs, usability reports, web analytics, performance metrics, recovery plans, open data publication | Design Execution, Validation, Change Control, Records       |

---

## **6. Methodologies and Tools**

* **Agile Development**: Iterative delivery aligned with DSS phase outputs.
* **User-Centered Design**: Continuous user research, testing, and feedback.
* **Prototyping**: Low-fidelity to MVP in Alpha and Beta phases.
* **Accessibility & Inclusive Design**: WCAG compliance, inclusive design cards, testing with accessibility-challenged users.
* **Governance & Compliance**: Phase approvals mapped to management review points; DSS checkpoints used for verification and validation.
* **Traceability**: All deliverables linked to project management artifacts (e.g., GitHub Issues, PRs, Wiki, or other QMS-approved tools).
* **Security & Privacy**: ISO/IEC 27001, ISO/IEC 27701, privacy impact assessments, security logs.
* **Open Data Compliance**: Open data published per Open Data Guidebook, 100% traceable and archived.

---

## **7. Design Change Management**

1. Document all changes during any DSS phase (Discovery → Live) in the project tracking tool or controlled record repository.
2. Review changes by Design Owner and QA for compliance with SOP-DC-001 and DSS principles.
3. Approve changes prior to implementation.
4. Update related deliverables, prototypes, MVP, or live service components.

---

## **8. Verification & Validation**

* **Verification**: Confirm DSS outputs (deliverables, prototypes, reports, MVP) meet design inputs and SOP requirements.
* **Validation**: Confirm the service meets user needs and intended purpose using usability testing, KPIs, and performance metrics.
* Maintain verification/validation records as controlled evidence (project plan, Jira/GitHub Issues, PRs, Wiki, reports).

---

## **9. Records**

Acceptable records for compliance with SOP-DC-001 include:

* Discovery reports, personas, feasibility studies
* Alpha prototypes, usability testing reports, journey maps
* Beta MVP, automated testing logs, device validation reports, KPIs, privacy/security reports
* Live service maintenance logs, usability tests, web analytics, performance metrics, open data publication
* Phase approval records, change requests, and related review notes

All records must be **retained per QMS record retention policy** and linked to DSS phase checkpoints for traceability.

---

## **10. Regulatory & Standards Compliance**

* ISO 9001:2015 — Design & development requirements
* ISO 90003 — Software engineering guidance
* IEC 62304 — Medical device software lifecycle (if applicable)
* IEC 62366 — Usability engineering
* ISO 13485 — Medical device QMS
* ISO 14971 — Risk management
* ISO/IEC 27001 & 27701 — Information security & privacy
* FDA 21 CFR Part 11 — Electronic records & signatures (if applicable)
* Optional / Conditional: ISO 14155, IEC 60601-1, HIPAA, 21 CFR 820

Traceability between DSS phases, Red Witch deliverables, and applicable standards must be maintained for audit purposes.

---

## **11. Review & Approval**

| Role                           | Name | Signature | Date |
| ------------------------------ | ---- | --------- | ---- |
| Design Owner / Product Manager |      |           |      |
| QA / Compliance Lead           |      |           |      |
| Management                     |      |           |      |

---

### **12. Notes**

* WI-DC-002 is **modular** and can be used as a drop-in work instruction instead of WI-DC-001 for projects adopting the Ontario DSS.
* All DSS deliverables satisfy SOP-DC-001 requirements for design control: inputs, outputs, verification, validation, change control, and records.
* Traceability of design decisions and approvals is mandatory.
* Risk management, usability, accessibility, security, privacy, and governance activities are integral to every DSS phase.
