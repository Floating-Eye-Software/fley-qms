# **Quality Manual – Floating Eye Software (FLEY)**

---

## **Overview**

The Floating Eye Software Quality Management System (QMS) provides a structured path from **intended use** to **regulatory compliance**. Each project begins by identifying the **applicable standards and regulations** based on its feature set, labeling, and intended use (e.g., ISO 13485, IEC 62304, GDPR). For each standard, this wiki maintains a **compliance mapping page** that links regulatory clauses to the required **quality activities**. Those activities are implemented through **Standard Operating Procedures (SOPs)**, which define what must be done, and **Work Instructions (WIs)**, which describe how to do it in our tools. Execution of these activities produces **records and evidence**, stored in controlled repositories, which demonstrate compliance during audits and reviews.

This ensures a clear, auditable chain: **Regulations → SOPs → WIs → Execution → Evidence**.

---

## **1. Purpose and Scope**

The purpose of this Quality Manual is to define the FLEY Quality Management System (QMS), its alignment to international standards and regulations, and its applicability to software projects such as the **Red Witch Pilot Project**.

The QMS applies to all Floating Eye Software activities that impact product quality, safety, security, and compliance.

---

## **2. Applicable Standards and Regulations**

The QMS framework references and integrates requirements from:

* ISO 9001:2015 (Quality Management Systems – Requirements)
* ISO 9004:2018 (Quality of an Organization – Guidance for Sustained Success)
* ISO 13485:2016 (Medical Devices – Quality Management Systems)
* IEC 62304:2006+A1:2015 (Medical Device Software – Software Life Cycle Processes)
* ISO 14971:2019 (Application of Risk Management to Medical Devices)
* 21 CFR 820 (FDA Quality System Regulation)
* GDPR (General Data Protection Regulation)
* Ontario Digital Service Standard (ODF-DSS)

Each compliance page in `/Compliance/` maps clauses from these standards to specific quality activities and evidence.

---

## **3. QMS Structure**

The QMS is structured into distinct but connected elements:

* **Compliance** – External requirements and regulations.
* **QMS** – Internal system definition and governance.
* **SOPs** – Define what must be done.
* **Work Instructions (WIs)** – Step-by-step tool-specific guidance.
* **Plans** – Project-level tailoring of QMS practices.
* **Records** – Evidence of execution and compliance.
* **Templates** – Reusable document scaffolding for consistency.

This wiki acts as the central hub, ensuring traceability across all levels.

---

## **4. Governance and Responsibilities**

* **Quality Manager** – Oversees QMS operation and compliance.
* **Project Manager** – Ensures QMS integration into projects.
* **Developers** – Follow SOPs/WIs and maintain traceability.
* **Privacy Officer** – Ensures GDPR compliance.
* **Auditors** – Conduct periodic reviews and assessments.

---

## **5. Core QMS Processes**

* **Document and Record Control** – Versioning, approval, and retention via GitHub.
* **Design and Development Control** – Requirements management, traceability, design reviews.
* **Risk Management** – Ongoing risk identification, mitigation, and review.
* **Change Control** – GitHub PR workflows as the controlled change log.
* **Verification and Validation** – CI/CD test pipelines and stakeholder validation.
* **Training and Competence** – Role-based onboarding and GDPR/security training.
* **Audit and Improvement** – Regular internal audits, CAPA, and self-assessment.

---

## **6. Compliance Mapping and Traceability**

Each compliance page (e.g., `ISO-13485.md`, `IEC-62304.md`) links to:

* Relevant SOPs (what activities are required).
* WIs (how those activities are executed).
* Records (where evidence is stored).

Traceability is maintained in project-level matrices (e.g., Red Witch PQP) to ensure coverage and evidence can be demonstrated at any time.

---

## **7. Continuous Improvement**

The QMS is a **living system**. Improvement comes from:

* Sprint retrospectives (incremental process feedback).
* Internal audits (systematic review).
* CAPA (Corrective and Preventive Actions).
* ISO 9004 self-assessments and GDPR compliance checks.

Findings lead to updates in SOPs, WIs, and plans to mature the QMS over time.

---

## **8. References**

* `/Compliance/` folder for external standard mappings.
* `/SOPs/` folder for system-level operating procedures.
* `/WIs/` folder for implementation details.
* `/Plans/` folder for project-specific tailoring.
* `/Records/` folder for compliance evidence.
