# 🧩 **QMS-SOP-09 — Design and Development Control**

**Document No.:** QMS-SOP-09
**Title:** Design and Development Control
**Revision:** 2.0
**Effective Date:** [Insert Date]
**Approved By:** [Top Management]

---

## **1. Purpose**

To define the process for controlling the design and development of products, software, or systems to ensure that outputs meet input requirements and applicable regulatory, safety, and quality standards.

This SOP satisfies the design control requirements of **ISO 9001:2015 Clause 8.3**, and provides a foundation for compliance with **ISO 13485:2016 Clause 7.3** and **IEC 62304** where applicable.

---

## **2. Scope**

This procedure applies to all design and development projects undertaken by the organization, including:

* New product, system, or software development.
* Major enhancements or redesigns of existing products.
* Design verification and validation activities.
* Design transfer to production or release.

Projects may follow a specific framework implemented through a **Design Control Work Instruction (WI)** — e.g.:

* **WI-QMS-09-01** – Standard Software Development Lifecycle (SDLC).
* **WI-QMS-09-02** – Ontario Design Framework.
* **WI-QMS-09-03** – Agile / Incremental Design Model.

---

## **3. References**

* ISO 9001:2015, Clauses 4–10
* ISO 13485:2016, Clause 7.3
* IEC 62304:2006/Amd1:2015
* QMS-SOP-06 — Quality Planning
* QMS-SOP-07 — Project Management
* QMS-SOP-08 — Risk and Opportunity Management
* **Template:** *Design Control Plan (DCP)*
* **Template:** *Project Quality Plan (PQP)*

---

## **4. Responsibilities**

| Role                              | Responsibilities                                                                                                                        |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Project Manager / Design Lead** | Develop and maintain the **Design Control Plan**; coordinate design reviews; ensure deliverables meet plan and regulatory requirements. |
| **Design & Development Team**     | Execute design tasks; maintain records and traceability of inputs, outputs, verification, and validation.                               |
| **Quality Manager**               | Verify compliance with this SOP; ensure risk-based thinking and traceability; review and approve deliverables.                          |
| **Top Management**                | Approve design plans, major reviews, and final design transfer.                                                                         |
| **Process Owners / SMEs**         | Provide technical input and participate in reviews.                                                                                     |

---

## **5. Procedure**

### **5.1 Design and Development Planning**

1. Each project shall have a **Design Control Plan (DCP)** defining:

   * Applicable development framework (referenced WI).
   * Design stages, activities, and review points.
   * Deliverables checklist (design outputs).
   * Risk and opportunity integration.
   * Verification, validation, and transfer criteria.
2. The DCP may be integrated into the **Project Plan** or **Project Quality Plan (PQP)**.
3. The DCP shall be reviewed and approved prior to initiating design activities.

---

### **5.2 Design and Development Inputs**

Design inputs shall be:

* Documented, reviewed, and approved prior to use.
* Complete, unambiguous, and testable.
* Derived from:

  * Customer or user requirements
  * Regulatory and safety requirements
  * Risk analysis and prior product experience
  * Standards and performance criteria

Inputs are recorded within the **Design Input Specification** or equivalent artifact (e.g., user stories, PRD, requirements database).

---

### **5.3 Design and Development Outputs**

Design outputs shall:

* Meet input requirements.
* Provide adequate information for verification and validation.
* Identify acceptance criteria.
* Define critical characteristics essential for safety and performance.

Outputs may include:

* Architecture or design documents
* Source code / configuration
* Test cases and protocols
* User documentation
* Risk controls
* Release notes and deployment guides

Outputs are reviewed and approved before release to the next phase.

---

### **5.4 Design and Development Review**

* Conduct reviews at defined **milestones or stage gates** in the Design Control Plan.
* Participants must include representatives of **design, quality, and management**.
* Reviews evaluate:

  * Conformance to requirements and plan
  * Risk status
  * Adequacy of verification and validation
  * Readiness for next stage
* Record outcomes and actions in the **Design Review Record**.

---

### **5.5 Design and Development Verification**

* Verify that design outputs meet design inputs.
* Verification may include:

  * Inspections, walkthroughs, peer reviews
  * Unit, integration, and system testing
  * Static analysis or simulation results
* Verification evidence must be documented in **Verification Reports** and linked to corresponding requirements and risk controls.

---

### **5.6 Design and Development Validation**

* Confirm that the resulting product or system meets user and intended-use needs.
* Validation methods include:

  * User acceptance testing (UAT)
  * Clinical evaluation (if applicable)
  * Pilot deployment or beta testing
* Validation records include test plans, reports, and acceptance evidence.

---

### **5.7 Design Risk Management**

* All design risks must be identified and managed in accordance with **QMS-SOP-08 Risk and Opportunity Management**.
* Each design risk shall have traceability to:

  * A design input (source of risk).
  * A control measure (design, process, or verification).
  * A verification or validation record confirming control effectiveness.
* Design risk reviews occur at each design review stage.

---

### **5.8 Design and Development Changes**

* Proposed changes to the design shall follow the **Change Control SOP (QMS-SOP-02)**.
* Assess the impact on requirements, verification, validation, and regulatory compliance.
* Document approvals and maintain version control in the design repository.

---

### **5.9 Design Transfer and Closure**

* Confirm all deliverables from the **Design Control Plan** are complete and accepted.
* Ensure training, documentation, and configuration baselines are ready for production or release.
* Archive all design documentation, including:

  * Design Inputs/Outputs
  * Review, Verification, and Validation Records
  * Risk Management File
  * Change History

---

## **6. Records**

| Record                            | Retention                  | Location             |
| --------------------------------- | -------------------------- | -------------------- |
| Design Control Plan (DCP)         | Life of product + 10 years | Project repository   |
| Design Inputs/Outputs             | Life of product            | Project repo / DHF   |
| Verification & Validation Records | Life of product            | Test evidence folder |
| Design Reviews                    | 10 years                   | QMS repository       |
| Risk Management File              | 10 years                   | Risk Register / DHF  |

---

## **7. References**

* QMS-SOP-07 — Project Management
* QMS-SOP-08 — Risk & Opportunity Management
* QMS-SOP-02 — Change Control
* Project Quality Plan (PQP) Template
* Design Control Plan (DCP) Template
