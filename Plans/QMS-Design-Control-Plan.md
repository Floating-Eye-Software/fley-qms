# **Design Control Plan (DCP) – FLEY Quality Management System (QMS)**

**Slug:** QMS-Design-Control-Plan  
**Revision:** r1  
**Effective Date:** 2025-10-28  
**Related SOP:** Design-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/Plans/QMS-Design-Control-Plan.md  

---

## **1. Purpose**

To define the design and development control framework for the **FLEY Quality Management System (QMS)**, ensuring that all stages — from requirements through release — are planned, documented, reviewed, verified, and validated in accordance with ISO 9001:2015 + Amendment 1:2024, internal ethical/privacy principles, and FLEY QMS standards.

This plan applies **design control principles to the QMS itself** as a “product” to ensure its intended use is met.

---

## **2. Scope**

* Covers creation, operation, and continual improvement of the QMS supporting **Red Witch–related activities**.
* Excludes unrelated FLEY activities (e.g., blogs, NetHack servers).
* Applies to all QMS artifacts, SOPs, Work Instructions, Risk Register, CAPA processes, and related workflows.
* Includes QMS deployment, training (sole proprietor), and maintenance.

---

## **3. References**

| Document                          | Description                                          |
| --------------------------------- | ---------------------------------------------------- |
| Design Control SOP                | FLEY’s standard design control process               |
| Project Management SOP            | Project planning, monitoring, and closure            |
| Risk & Opportunity Management SOP | Risk identification, assessment, and mitigation      |
| Change Control SOP                | Change evaluation and approval                       |
| Quality Manual                    | Top-level QMS commitments and framework              |
| Context Analysis                  | Internal and external context influencing QMS design |
| Process Map                       | QMS process interactions                             |
| Organizational Chart              | Roles, responsibilities, and authorities             |
| GitHub QMS Operations WI          | Operational procedures for QMS maintenance           |

---

## **4. Roles and Responsibilities**

| Role                                | Responsibility                                                                                        |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **QMS Owner / Sole Proprietor**     | Maintains DCP; approves QMS design, reviews, and validation; ensures alignment with ISO 9001 & ethics |
| **Quality Manager**                 | Verifies compliance; reviews design outputs, risk integration, and documentation integrity            |
| **Project Manager / Process Owner** | Coordinates QMS workflow implementation; ensures traceability and PDCA cycle                          |
| **Design / Documentation Lead**     | Develops SOPs, WIs, process diagrams, and record templates                                            |
| **Risk Owner / QA**                 | Ensures risk identification, mitigation, and traceability                                             |
| **Stakeholders / Advisors**         | Provide guidance on privacy, ethics, and regulatory requirements                                      |

---

## **5. Design and Development Framework**

| Phase                              | Objectives                                                                         | Key Deliverables / Outputs                                           | Review Points / Approval      |
| ---------------------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ----------------------------- |
| **5.1 Design Planning**            | Define QMS scope, structure, milestones, and responsibilities                      | DCP, Quality Manual draft, SOP/WI list, Process Map draft            | Design Control Kickoff Review |
| **5.2 Requirements Definition**    | Capture QMS requirements from ISO 9001, Amendment 1:2024, and organizational needs | Requirements list, risk assessment, intended use statement           | Requirements Review           |
| **5.3 Design & Implementation**    | Develop SOPs, Work Instructions, repositories, process boards, traceability matrix | Completed SOPs, WIs, GitHub boards, traceability matrix              | Design Review(s)              |
| **5.4 Verification**               | Confirm QMS outputs meet requirements and traceability                             | Verification checklists, internal audit logs                         | Verification Review           |
| **5.5 Validation**                 | Confirm QMS achieves intended use for planning, monitoring, and improvement        | Validation report, PDCA demonstration, mock audit results            | Validation Review             |
| **5.6 Design Transfer / Release**  | Deploy operational QMS and finalize documentation                                  | GitHub QMS repository, version-controlled SOPs/WIs, archived records | Release Readiness Review      |
| **5.7 Post-Release / Maintenance** | Maintain, monitor, and improve QMS via PDCA cycle                                  | Updated SOPs/WIs, CAPA logs, risk register updates, audit actions    | Management Review             |

---

## **6. Design Reviews**

| Review Type                     | Timing / Trigger                          | Participants                 | Expected Outputs                          |
| ------------------------------- | ----------------------------------------- | ---------------------------- | ----------------------------------------- |
| Kickoff Review                  | Project start                             | QMS Owner, Quality Manager   | Approved DCP, roles confirmed             |
| Requirements Review             | Completion of QMS requirement capture     | QMS Owner, Quality Manager   | Requirements approved, risks logged       |
| Preliminary Design Review (PDR) | Completion of initial SOP/WI drafts       | QMS Owner, Design Lead       | Draft QMS artifacts reviewed              |
| Critical Design Review (CDR)    | Finalization of SOPs/WIs & workflows      | QMS Owner, QA / Stakeholders | QMS design approved for verification      |
| Verification Review             | After internal audits of QMS artifacts    | QA / QMS Owner               | Verification evidence documented          |
| Validation Review               | Confirm intended use via pilot PDCA cycle | QMS Owner / Quality Manager  | Validation report & approvals             |
| Release Review                  | Before operational deployment             | QMS Owner, QA / Stakeholders | QMS released for use, repository baseline |

---

## **7. QMS Requirements**

* Compliance with ISO 9001:2015 + Amendment 1:2024 (Climate Action)
* Defined workflows for **QMS Creation, QMS Operation, Product Development**
* Traceable SOPs and WIs for each process
* Risk-based thinking integrated in all phases
* Capability for continual improvement and management review
* Privacy-first, ethical, and inclusive design principles
* Repository structure supporting document control, traceability, and versioning

---

## **8. Verification and Validation**

| Activity                | Description                                              | Method / Evidence                         | Responsible    |
| ----------------------- | -------------------------------------------------------- | ----------------------------------------- | -------------- |
| SOP/WI Completeness     | Ensure all required SOPs/WIs exist and are controlled    | Checklist, repository review              | QA / QMS Owner |
| Traceability            | Requirements → SOP/WI → Risk → Verification → Validation | Traceability matrix                       | QMS Owner      |
| Functional Verification | QMS workflows operate as intended                        | Mock workflow execution, audit simulation | QA / PM        |
| Validation              | Confirm QMS supports intended use                        | PDCA demonstration, internal audit review | QMS Owner / QA |

---

## **9. Risk and Opportunity Management**

* Identify risks associated with QMS design, operation, and deployment (e.g., missing SOP, ineffective traceability, non-compliance with ISO 9001).
* Log risks in **Risk Register** with mitigation actions.
* Review risks during design reviews, verification, validation, and management review.
* Include opportunities for automation, improved traceability, and continuous improvement.

---

## **10. Configuration and Change Control**

* All QMS artifacts (SOPs, WIs, records, repositories) are **version-controlled**.
* Changes follow **Change Control SOP** with impact assessment on requirements, risk, verification, and validation.
* Maintain traceability of all changes with approvals documented in the QMS repository.

---

## **11. Records and Retention**

| Record                             | Storage Location    | Retention Period |
| ---------------------------------- | ------------------- | ---------------- |
| QMS Design Control Plan (DCP)      | QMS Repository      | Permanent        |
| Design Review Minutes / Approvals  | QMS Repository      | 10 years         |
| Verification & Validation Evidence | QMS Repository      | 10 years         |
| Risk Register                      | QMS Repository      | 10 years         |
| CAPA / Improvement Logs            | QMS Repository      | 10 years         |
| Version-Controlled SOPs & WIs      | GitHub / Repository | Permanent        |
| Management Review Records          | QMS Repository      | 10 years         |

---

## **12. Traceability Matrix (Summary Example)**

| Requirement / ISO Clause | QMS Output (SOP/WI/Artifact) | Verification Evidence  | Validation Evidence            | Status   |
| ------------------------ | ---------------------------- | ---------------------- | ------------------------------ | -------- |
| ISO 9001:2015 §4.1       | Context Analysis             | Review checklist       | Demonstration of annual review | Complete |
| ISO 9001:2015 §5.3       | Organizational Chart         | Audit record           | Management review              | Complete |
| ISO 9001:2015 §7.2       | Roles & Responsibilities SOP | Audit checklist        | PDCA demonstration             | Complete |
| ISO 9001:2015 §8.3       | Design-Control-SOP & DCP     | Verification checklist | QMS supports intended use      | Complete |

> Full traceability matrix maintained in **QMS Repository / GitHub**.
