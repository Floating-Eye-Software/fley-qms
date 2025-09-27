
## **Floating Eye Software (FLEY) Quality Management System (QMS) Architecture**

The Red Witch Project Quality Management System (QMS) is designed to ensure compliance with ISO 9001, ISO 13485, 21 CFR 820, Ontario Digital Service Standard (DSS), and organizational quality objectives, while remaining flexible across multiple project methodologies and toolchains.

---

### **1. Hierarchical Structure**

The QMS uses a **layered, modular architecture**:

1. **SOPs (Standard Operating Procedures)** – Define *what* processes are required. SOPs are **tool-agnostic** and describe mandatory processes including design & development control, project management, change control, risk management, configuration management, document control, CAPA, and governance.

2. **Work Instructions (WIs)** – Define *how* each SOP is implemented within specific project environments or toolchains. WIs translate the intent of SOPs into actionable, project-specific steps. Examples:

   * GitHub: pull requests, issues, and wiki pages implement change control and version management.
   * Jira/SVN: epics, Confluence pages, and SVN branches implement equivalent workflows.
   * Lightweight text-file projects: file-naming conventions, spreadsheet-based traceability, and manual approvals.
     WIs are **modular and reusable** across projects.

3. **Project Quality Plan (PQP)** – Maps all 14 quality elements (e.g., Document Control, Risk Management, Design & Development, etc.) to relevant tool-specific WIs for the project. The PQP ensures all quality processes are implemented and provides **traceable links to project artifacts**.
   *(Visual placeholder: “Diagram showing SOP → WI → PQP → Project Artifacts / Records”)*

4. **Project Artifacts and Records** – All deliverables, records, and evidence generated during project execution. Artifacts reside in project toolchains (e.g., GitHub, Confluence, OneNote, file shares) and are traceable back to SOPs and WIs via the PQP.

---

### **2. Tool-Agnostic Design**

The QMS architecture is deliberately **tool-agnostic at the SOP level**, allowing adoption of different frameworks, methodologies, and tools without changing core quality requirements.

**Example Implementation:**

| SOP              | WI Implementation Options                                                                               |
| ---------------- | ------------------------------------------------------------------------------------------------------- |
| Design Control   | GitHub: Issues & PRs; Jira/SVN: Epics & Confluence; Lightweight: Spreadsheet & manual approvals         |
| Change Control   | GitHub: Pull request workflow; Jira/SVN: Change request ticket; Lightweight: Manual form & approval log |
| Document Control | Confluence / Wiki pages; File shares with naming conventions; GitHub README/versioned docs              |

---

### **3. Traceability and Compliance**

Traceability is central to the QMS:

**Regulatory / Standard → SOP → WI → PQP → Project Artifacts / Records**

Traceability is maintained via:

* **Project Quality Plans (PQP):** Explicitly map all quality elements to tool-specific WIs.
* **Work Instruction Repositories:** Step-by-step execution guidance.
* **Artifact Storage:** All deliverables, approvals, and test results are auditable and traceable.

---

### **4. Flexibility and Continuous Improvement**

* Supports multiple lifecycles (Agile, Waterfall, ODF).
* Tools may be substituted without modifying SOPs.
* Continuous improvement embedded via CAPA, internal audits, and governance reviews, ensuring lessons learned are incorporated into SOPs, WIs, and PQPs.

---

### **5. Organization-Level Quality Activities**

These enterprise-wide activities are SOP-driven and **stable across projects**:

| Element                                      | Scope / Notes                                                 | ISO / 21 CFR 820 Reference                      |
| -------------------------------------------- | ------------------------------------------------------------- | ----------------------------------------------- |
| Document Control                             | Policies for creation, approval, distribution, retention      | ISO 9001:7.5; 21 CFR 820.40                     |
| Training & Competence                        | Staff qualification, ongoing training, competency records     | ISO 9001:7.2; 21 CFR 820.25                     |
| Quality Planning                             | QMS objectives, KPIs, and planning of processes               | ISO 9001:6.2; 21 CFR 820.20                     |
| Risk Management                              | Enterprise-level risk assessment and mitigation               | ISO 9001:6.1; ISO 13485:7.1; 21 CFR 820.30      |
| Design & Development Control                 | Policies for planning, inputs/outputs, reviews                | ISO 13485:7.3; 21 CFR 820.30                    |
| Configuration Management                     | Versioning of controlled documents, baselines, master records | ISO 9001:7.5; 21 CFR 820.40                     |
| Change Control                               | Change approval, impact assessment, traceability              | ISO 9001:6.3; 21 CFR 820.30, 820.70             |
| CAPA                                         | Nonconformity analysis, root cause, corrective actions        | ISO 9001:10.2; 21 CFR 820.100                   |
| Audit Program / Continuous Improvement       | Internal audits, management review, improvement initiatives   | ISO 9001:9.2, 9.3, 10.3; 21 CFR 820.22, 820.100 |
| Supplier / External Resource Management      | Qualification, monitoring, evaluation of vendors              | ISO 9001:8.4; 21 CFR 820.50                     |
| Release & Deployment                         | Guidance for product release and post-release monitoring      | ISO 13485:7.5.1; 21 CFR 820.40                  |
| Management Review                            | Periodic review of QMS effectiveness                          | ISO 9001:9.3; 21 CFR 820.20                     |
| Customer / Stakeholder Feedback              | Complaints, satisfaction, performance monitoring              | ISO 9001:9.1.2; 21 CFR 820.198                  |
| Regulatory / Legal Compliance Monitoring     | Ensure ongoing compliance                                     | ISO 13485:4.2.3; 21 CFR 820.1, 820.100          |
| Infrastructure & Work Environment Management | Facilities, IT systems, and controlled environments           | ISO 9001:7.1; 21 CFR 820.70                     |

---

### **6. Project-Level Quality Activities**

Project-specific execution is defined per PQP:

| Element                                | Scope / Notes                                                    | ISO / 21 CFR 820 Reference                 |
| -------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------ |
| Configuration & Version Control        | Track project artifacts, code, design docs                       | ISO 9001:7.5; 21 CFR 820.70                |
| Change Control Workflow                | Project-specific requests and approvals                          | ISO 9001:6.3; 21 CFR 820.30, 820.70        |
| Requirements & Design Traceability     | Ensure traceability: requirements → design → testing             | ISO 13485:7.3.3; 21 CFR 820.30             |
| Risk Management                        | Identify, mitigate, monitor project risks                        | ISO 13485:7.1; 21 CFR 820.30               |
| Testing / Verification & Validation    | Ensure product meets functional requirements                     | ISO 13485:7.3.6; 21 CFR 820.75             |
| Security & Access Control              | Manage project-level data, IP, and patient info                  | ISO 13485:4.1; 21 CFR 820.70               |
| Project Management                     | Task tracking, sprints, milestones                               | ISO 9001:8; 21 CFR 820.30                  |
| Planning                               | Feasibility, schedules, resources, milestones                    | ISO 9001:6; 21 CFR 820.30                  |
| Governance & Sign-off                  | Phase gates, design reviews, ARB/DFA checkpoints                 | ISO 13485:7.3.2; 21 CFR 820.30             |
| Release & Maintenance                  | Deployment, updates, hotfixes, post-release monitoring           | ISO 13485:7.5.1; 21 CFR 820.70             |
| Open Data & Transparency               | Data anonymization, publication, monitoring                      | ISO 9001:7.5; 21 CFR 820.180               |
| Measurement & KPIs                     | Track performance metrics, defect rates                          | ISO 9001:9.1; 21 CFR 820.100               |
| Agile Workflow                         | Scrum/Kanban, backlog management, sprint planning                | ISO 9001:8; 21 CFR 820.30                  |
| Prototyping & Testing                  | Early-stage verification, user feedback integration              | ISO 13485:7.3.5; 21 CFR 820.30             |
| Accessibility & Compliance             | Privacy, security, accessibility testing, regulatory checks      | ISO 13485:7.3, 4.1; 21 CFR 820.70, 820.100 |
| Requirements & KPI Tracking            | Align project metrics to business/technical requirements         | ISO 9001:9; 21 CFR 820.100                 |
| Supplier / Vendor QA at Project Level  | Incoming inspection, supplier performance monitoring             | ISO 9001:8.4; 21 CFR 820.50, 820.80        |
| Nonconformance Reporting               | Document defects, failures, deviations at project level          | ISO 9001:10.2; 21 CFR 820.100, 820.198     |
| Design / Development Reviews           | Formal inspection/review of design outputs                       | ISO 13485:7.3.2; 21 CFR 820.30             |
| Change Impact Analysis                 | Evaluate effect of changes on requirements, risk, cost, timeline | ISO 9001:6.3; 21 CFR 820.30                |
| Release Acceptance Criteria / Sign-off | Validate product readiness before release                        | ISO 13485:7.5.1; 21 CFR 820.70             |

**Note:** Organization-level policies guide project-level execution, clarifying scope boundaries and reducing duplication of effort.

---

### **7. Summary**

The Red Witch QMS provides a **structured, modular, auditable framework** for managing quality across diverse projects.

* **SOPs** define *what* must be done.
* **WIs** define *how* each SOP is implemented per project/toolchain.
* **PQP** ensures **all quality elements are mapped and traceable** to project artifacts.

This architecture ensures:

* Regulatory compliance (ISO 9001, ISO 13485, 21 CFR 820, DSS).
* Toolchain flexibility.
* Continuous improvement through CAPA, audits, and lessons learned.

---
