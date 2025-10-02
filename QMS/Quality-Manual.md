# **Quality Manual – Floating Eye Software (FLEY)**

---

## **Overview**

The Floating Eye Software Quality Management System (QMS) provides a structured pathway from **intended use** to **regulatory compliance**. Each project begins by identifying the **applicable standards and regulations** based on its feature set, labeling, and intended use (e.g., ISO 13485, IEC 62304, GDPR).

For each standard, this wiki maintains a **compliance mapping page** linking regulatory clauses to required **quality activities**. These activities are implemented through:

* **Standard Operating Procedures (SOPs):** Define what must be done.
* **Work Instructions (WIs):** Detail how tasks are executed in our tools.
* **Records and Evidence:** Stored in controlled repositories, demonstrating compliance during audits and reviews.

This creates a clear, auditable chain:

**Regulations → SOPs → WIs → Execution → Evidence**

---

## **1. Purpose and Scope**

The purpose of this Quality Manual is to define the FLEY QMS, its alignment to international standards, and its applicability to software projects.

The QMS applies to all FLEY activities impacting **product quality, safety, security, and regulatory compliance**.

---

## **2. Applicable Standards and Regulations**

The QMS integrates requirements from:

* ISO 9001:2015 – Quality Management Systems
* ISO 9004:2018 – Guidance for Sustained Success
* ISO 13485:2016 – Medical Devices QMS
* IEC 62304:2006+A1:2015 – Medical Device Software Lifecycle
* ISO 14971:2019 – Risk Management for Medical Devices
* 21 CFR 820 – FDA Quality System Regulation
* GDPR – Data Protection
* Ontario Digital Service Standard (ODF-DSS)

Compliance pages in `/Compliance/` map clauses from these standards to **SOPs, WIs, and records**.

---

## **3. QMS Structure**

The QMS is organized into interconnected elements:

1. **Compliance** – External regulations and standards.
2. **QMS Governance** – Internal system management.
3. **SOPs** – Define required activities.
4. **Work Instructions (WIs)** – Step-by-step guidance.
5. **Plans** – Project-specific tailoring of QMS practices.
6. **Records** – Evidence of execution and compliance.
7. **Templates** – Standardized document scaffolding.

---

## **4. Governance and Responsibilities**

| Role                | Responsibilities                                                   |
| ------------------- | ------------------------------------------------------------------ |
| **Quality Manager** | Oversees QMS operation, ensures compliance, approves SOPs/WIs      |
| **Project Manager** | Integrates QMS into projects, ensures team adherence               |
| **Developers**      | Follow SOPs/WIs, maintain traceability and risk mitigation records |
| **Privacy Officer** | Ensures GDPR compliance, monitors data protection activities       |
| **Auditors**        | Conduct internal reviews and assessments, verify compliance        |

---

## **5. Process Approach and PDCA Cycle**

FLEY applies the **Process Approach** and **Plan–Do–Check–Act (PDCA)** cycle to ensure systematic, consistent, and continually improving quality management across all projects.

### **5.1 Plan**

* Define objectives, requirements, and resources.
* Align SOPs, WIs, tools, infrastructure, and staffing with project needs.
* Identify, assess, and mitigate risks per ISO 14971.
* Include verification and validation strategies.

**Evidence:** Project Quality Plans, risk registers, SOP assignments, documented quality objectives.

### **5.2 Do**

* Execute software design, development, and verification per SOPs/WIs.
* Follow controlled workflows (e.g., GitHub PRs, CI/CD pipelines).
* Implement risk mitigations.
* Maintain records in controlled repositories.

**Evidence:** Work logs, version-controlled code, CI/CD test reports, design reviews, risk treatment records.

### **5.3 Check**

* Monitor process outputs and software performance metrics.
* Conduct internal audits and SOP/WI compliance reviews.
* Collect feedback, bug reports, and stakeholder validation.
* Analyze deviations, nonconformances, and CAPA effectiveness.

**Evidence:** Audit reports, KPI dashboards, test results, feedback logs, CAPA records.

### **5.4 Act**

* Implement corrective and preventive actions.
* Update SOPs, WIs, and project plans based on lessons learned.
* Incorporate process improvements into subsequent cycles.

**Evidence:** Updated SOPs/WIs, CAPA records, improvement project documentation.

### **5.5 Integration of the Process Approach**

FLEY links all QMS elements:

1. **Planning** → Guides execution and compliance alignment.
2. **Execution** → Produces records and measurable outputs.
3. **Evaluation** → Identifies gaps or deviations.
4. **Improvement** → Feeds back into planning, closing the loop.

---

## **6. Core QMS Processes**

* **Document and Record Control:** Versioning, approval, retention via GitHub.
* **Design and Development Control:** Requirements management, traceability, design reviews.
* **Risk Management:** Continuous risk identification, mitigation, and review.
* **Change Control:** GitHub PR workflows as controlled change logs.
* **Verification and Validation:** CI/CD pipelines, stakeholder validation.
* **Training and Competence:** Role-based onboarding, GDPR/security training.
* **Audit and Improvement:** Internal audits, CAPA, self-assessments.

---

## **7. Planning SOP Integration**

The **Project & Quality Planning SOP** guides the “Plan” phase of PDCA. It defines **project plans, quality plans, milestones, risk management, and traceability**.

### **7.1 Where the Planning SOP Fits in the PDCA Cycle**

| PDCA Phase | SOP / Process                  | Key Activities                                                                                                                                                     | Evidence / Records                                                                    |
| ---------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| **Plan**   | Project & Quality Planning SOP | - Define project scope, resources, milestones, quality objectives<br>- Identify risks and mitigation<br>- Assign responsibilities<br>- Map regulatory requirements | Project Plans, Quality Plans, Risk Registers, SOP references, Milestone documentation |
| **Do**     | Execution per WIs              | - Follow planned project steps<br>- Perform development, testing, and design reviews<br>- Implement risk mitigations                                               | Work items, CI/CD logs, test reports, traceability matrices                           |
| **Check**  | Audits & Reviews               | - Review milestones, QA activities, and process adherence<br>- Track metrics and KPIs                                                                              | Audit reports, KPI dashboards, milestone completion records                           |
| **Act**    | Continuous Improvement         | - Update SOPs/WIs based on lessons learned<br>- Implement CAPA<br>- Adjust project/quality plans for next cycle                                                    | CAPA records, updated plans, updated SOPs/WIs                                         |

---

## **8. Compliance Mapping and Traceability**

Each compliance page (e.g., `ISO-13485.md`, `IEC-62304.md`) links to:

* Relevant **SOPs** (required activities)
* **WIs** (execution steps)
* **Records** (evidence storage)

Project-level matrices maintain full traceability.

---

## **9. Continuous Improvement**

The QMS is a **living system**. Improvement comes from:

* Sprint retrospectives (incremental process feedback)
* Internal audits (systematic review)
* CAPA (Corrective and Preventive Actions)
* ISO 9004 self-assessments and GDPR compliance checks

Findings lead to updates in SOPs, WIs, and plans to mature the QMS over time.

---

## **10. References**

* `/Compliance/` – External standard mappings
* `/SOPs/` – System-level operating procedures
* `/WIs/` – Implementation guidance
* `/Plans/` – Project-specific tailoring
* `/Records/` – Evidence of compliance

Versioning policy, access control, and archival rules are defined in the respective SOPs.
