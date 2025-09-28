# **Floating Eye Software (FLEY) Quality Management System (QMS) Manual**

**Version 2.0 – Draft**

---

## **Introduction**

The Floating Eye Software (FLEY) Red Witch Project Quality Management System (QMS) is designed to ensure compliance with **ISO 9001, ISO 13485, 21 CFR Part 820, Ontario Digital Service Standard (DSS)**, and organizational quality objectives.

This Quality Manual describes the **structure, processes, and traceability mechanisms** that enable FLEY to:

* Demonstrate **compliance with regulatory and standard requirements**.
* Maintain **toolchain flexibility** across projects.
* Ensure **continuous improvement** and quality assurance.
* Provide **audit-ready traceability** from regulation → evidence.

---

## **1. QMS Hierarchical Structure**

The QMS uses a **layered, modular architecture**:

1. **Standard Operating Procedures (SOPs)** – Define *what* processes are required. SOPs are **tool-agnostic** and describe mandatory processes such as design & development control, project management, change control, risk management, configuration management, document control, CAPA, governance, and **regulatory traceability**.

2. **Work Instructions (WIs)** – Define *how* each SOP is implemented within a specific toolchain or project. WIs are modular and reusable across projects. Examples:

   * GitHub – pull requests, issues, and wiki pages.
   * Jira/SVN – epics, Confluence pages, and SVN branches.
   * Lightweight projects – file-naming conventions, spreadsheets, manual approvals.

3. **Project Quality Plan (PQP)** – Maps **all quality elements** to relevant SOPs/WIs for a specific project and provides traceable links to project artifacts.

4. **Project Artifacts & Records** – Deliverables and evidence generated during execution (e.g., GitHub PRs, Confluence pages, test reports). Artifacts are **traceable back to SOPs and WIs via the PQP**.

---

## **2. Tool-Agnostic Design**

The QMS is **tool-agnostic at the SOP level**, enabling projects to adopt new frameworks and tools without modifying core quality processes.

**Example SOP-to-WI mappings:**

| SOP                     | WI Implementation Options                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------- |
| Design Control          | GitHub: Issues & PRs; Jira/SVN: Epics & Confluence; Lightweight: Spreadsheets & approvals |
| Change Control          | GitHub: PR workflow; Jira/SVN: Change request tickets; Lightweight: Approval forms        |
| Document Control        | Confluence/Wiki; File shares with naming rules; GitHub versioned docs                     |
| Regulatory Traceability | Master Traceability Matrix; PQP clause mapping; Artifact tagging with standard IDs        |

---

## **3. Traceability and Compliance**

**Traceability Framework:**

**Regulatory / Standard → SOP → WI → PQP → Project Artifact / Record**

Compliance is demonstrated through:

* **Master Traceability Matrix (TM):** Controlled document mapping every standard/regulation clause → QMS element → SOP/WI → PQP → sample artifact.
* **Project Quality Plans (PQPs):** Map project-specific activities to SOPs/WIs and reference actual artifacts.
* **Work Instructions:** Provide consistent execution steps, including how to tag and store artifacts.
* **Artifact Storage:** Controlled repositories (e.g., GitHub, Confluence, file shares).

Traceability is **bidirectional**: each clause traces to evidence, and each artifact can trace back to the clause.

---

## **4. Flexibility and Continuous Improvement**

* Supports multiple lifecycles (Agile, Waterfall, Open Development Framework).
* Tools and methods may be substituted without rewriting SOPs.
* Continuous improvement is embedded through:

  * **CAPA (Corrective and Preventive Actions).**
  * **Internal audits and reviews.**
  * **Governance checkpoints.**
  * **Annual updates of the Traceability Matrix.**

---

## **5. Organization-Level Quality Activities**

| Element                                      | Scope / Notes                                              | ISO / 21 CFR 820 Reference                      |
| -------------------------------------------- | ---------------------------------------------------------- | ----------------------------------------------- |
| Document Control                             | Creation, approval, retention of controlled documents      | ISO 9001:7.5; 21 CFR 820.40                     |
| Training & Competence                        | Staff qualification, training, competency records          | ISO 9001:7.2; 21 CFR 820.25                     |
| Quality Planning                             | Objectives, KPIs, QMS planning                             | ISO 9001:6.2; 21 CFR 820.20                     |
| Risk Management                              | Enterprise-level risk assessment and mitigation            | ISO 9001:6.1; ISO 13485:7.1; 21 CFR 820.30      |
| Design & Development Control                 | Policies for planning, inputs/outputs, reviews             | ISO 13485:7.3; 21 CFR 820.30                    |
| Configuration Management                     | Versioning, baselines, master records                      | ISO 9001:7.5; 21 CFR 820.40                     |
| Change Control                               | Change approval, impact analysis, traceability             | ISO 9001:6.3; 21 CFR 820.30, 820.70             |
| **Regulatory Traceability**                  | Master TM mapping all clauses to QMS elements and evidence | ISO 9001:4.4; ISO 13485:4.2; 21 CFR 820.20      |
| CAPA                                         | Nonconformity analysis, corrective actions                 | ISO 9001:10.2; 21 CFR 820.100                   |
| Audit & Continuous Improvement               | Internal audits, management reviews, CAPA-driven updates   | ISO 9001:9.2, 9.3, 10.3; 21 CFR 820.22, 820.100 |
| Supplier / Vendor Management                 | Qualification, monitoring, evaluation                      | ISO 9001:8.4; 21 CFR 820.50                     |
| Release & Deployment                         | Controlled release, post-release monitoring                | ISO 13485:7.5.1; 21 CFR 820.40                  |
| Management Review                            | Executive review of QMS effectiveness                      | ISO 9001:9.3; 21 CFR 820.20                     |
| Customer / Stakeholder Feedback              | Complaints, satisfaction, monitoring                       | ISO 9001:9.1.2; 21 CFR 820.198                  |
| Regulatory / Legal Compliance Monitoring     | Continuous monitoring of compliance obligations            | ISO 13485:4.2.3; 21 CFR 820.1, 820.100          |
| Infrastructure & Work Environment Management | Facilities, IT, secure environments                        | ISO 9001:7.1; 21 CFR 820.70                     |

---

## **6. Project-Level Quality Activities**

Project-specific execution is documented in the **PQP**.

| Element                            | Scope / Notes                                           | ISO / 21 CFR 820 Reference                 |
| ---------------------------------- | ------------------------------------------------------- | ------------------------------------------ |
| Configuration & Version Control    | Manage project artifacts, code, and documentation       | ISO 9001:7.5; 21 CFR 820.70                |
| Change Control Workflow            | Approvals and change tracking                           | ISO 9001:6.3; 21 CFR 820.30, 820.70        |
| Requirements & Design Traceability | Requirements → design → testing                         | ISO 13485:7.3.3; 21 CFR 820.30             |
| Risk Management                    | Identification, mitigation, monitoring of project risks | ISO 13485:7.1; 21 CFR 820.30               |
| Verification & Validation          | Testing and acceptance criteria                         | ISO 13485:7.3.6; 21 CFR 820.75             |
| Security & Access Control          | Project-level data/IP/patient info protection           | ISO 13485:4.1; 21 CFR 820.70               |
| Project Management                 | Task tracking, milestones, delivery oversight           | ISO 9001:8; 21 CFR 820.30                  |
| Governance & Design Reviews        | Phase gates, review checkpoints                         | ISO 13485:7.3.2; 21 CFR 820.30             |
| Release & Maintenance              | Deployment, updates, monitoring                         | ISO 13485:7.5.1; 21 CFR 820.70             |
| Nonconformance Reporting           | Document and resolve defects, failures                  | ISO 9001:10.2; 21 CFR 820.100, 820.198     |
| Supplier / Vendor QA               | Incoming inspection, project-level vendor oversight     | ISO 9001:8.4; 21 CFR 820.50, 820.80        |
| Measurement & KPIs                 | Track performance, defect rates                         | ISO 9001:9.1; 21 CFR 820.100               |
| Accessibility & Compliance         | Privacy, accessibility, security testing                | ISO 13485:7.3, 4.1; 21 CFR 820.70, 820.100 |

**Traceability Requirement:**
Each PQP must reference the **Traceability Matrix (TM)** and link artifacts to clauses and SOP/WIs.

---

## **7. SOP on Regulatory Traceability**

**SOP-QMS-TRC-001: Regulatory Traceability (Standard → Evidence)** defines:

* **Master Traceability Matrix** – listing every clause from ISO 9001, ISO 13485, 21 CFR 820, DSS.
* **Mappings** – Standard clause → QMS element → SOP/WI → PQP → artifact.
* **Responsibilities** – Quality Manager maintains TM; PMs ensure artifact linkage.
* **Evidence Requirements** – Artifacts must be uniquely identified, tagged with clause IDs, and retrievable within 24 hours.
* **Audit Protocol** – Verify bidirectional traceability.

This SOP is a **core element** of the QMS, ensuring compliance across all projects.

---

## **8. Records and Audit Readiness**

Key records maintained:

* **Master Traceability Matrix (controlled).**
* **Project Quality Plans (PQP).**
* **Controlled SOPs & WIs.**
* **Artifacts & approvals (audit-ready).**
* **Internal/External audit reports.**
* **CAPA records.**

---

## **9. Summary**

The FLEY Red Witch QMS provides a **structured, modular, auditable framework** that ensures:

* **Compliance** with ISO 9001, ISO 13485, 21 CFR 820, and DSS.
* **Traceability** from regulatory clauses → SOP/WI → PQP → artifacts.
* **Toolchain flexibility** without compromising compliance.
* **Continuous improvement** through CAPA, audits, and governance.

By embedding **regulatory traceability** as a formal QMS element, FLEY ensures every regulatory requirement is mapped, evidenced, and audit-ready.
