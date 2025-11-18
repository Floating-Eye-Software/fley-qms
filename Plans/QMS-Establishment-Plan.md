# **PLAN – Establish the FLEY Quality Management System (QMS)**

**Slug:** QMS-Establishment-Plan
**Revision:** r1
**Effective Date:** 2025-10-28
**Related SOPs:** Quality-Planning-SOP, Design-Control-SOP
**Controlled Source:** `/Plans/QMS-Establishment-Plan.md`

---

## **1. Introduction**

**Purpose:**
To establish the Floating Eye Software Quality Management System (FLEY-QMS) through a structured, design-controlled development process. This plan defines how the QMS will be designed, implemented, verified, validated, and released under configuration control.

**Scope:**
This plan governs all QMS establishment activities, including:

* Core documentation (Quality Manual, policies, and foundational SOPs)
* Repository architecture and governance
* Evidence management, traceability, and record retention
* Continuous Improvement and CAPA mechanisms
* Integration of pilot study results (from the Red Witch plan) into the controlled QMS

**The Red Witch Pilot Plan is a separate, subordinate plan** providing evidence and validation data for QMS design inputs.
Its outputs inform—not replace—the QMS design controlled in this plan.

**Applicable Standards & Regulations:**
ISO 9001:2015+A1:2024, ISO 13485:2016, IEC 62304, 21 CFR 820, GDPR, ISO 9004.

---

## **2. Quality Objectives**

* Establish a functioning, controlled QMS repository (`fley-qms`).
* Define and approve the initial QMS architecture, governance model, and change control workflows.
* Draft and validate core QMS documents (minimum viable QMS backbone).
* Integrate validated pilot workflows (from Red Witch) into QMS design.
* Create a reusable governance model: **Plans → Milestones → Issues → Evidence**.
* Achieve a validated **QMS Baseline (QMS_Baseline_r1)**.

---

## **3. Design Control Integration**

### **Design Inputs**

* Regulatory, ISO, and customer requirements
* Intended use of the QMS (support compliant development, governance, traceability)
* Pilot workflow results from Red Witch
* Repository governance requirements (branch protection, CODEOWNERS, controlled CI/CD)
* Internal resource and tooling constraints

### **Design Outputs**

* Core QMS documentation set
* QMS repository structure + governance
* Plan–Milestone–Issue model
* Evidence management system
* Continuous Improvement workflow
* Initial QMS baseline tag (`QMS_Baseline_r1`)

### **Design Reviews**

* **Requirements Review**: confirm QMS intended use and constraints
* **Architecture Review**: approve repository structure + governance model
* **Preliminary QMS Review (PDR)**: approve draft SOPs, workflows
* **Final QMS Review (FDR/CDR)**: approve QMS baseline release

### **Verification & Validation**

* *Verification:* Check completeness, correctness, and governance compliance
* *Validation:* Confirm that QMS works in real pilot workflows (using Red Witch)

---

## **4. Quality Processes**

* Draft and review foundational SOPs and policies
* Configure controlled repository governance
* Apply change control to all QMS artifacts
* Import pilot feedback from Red Witch as design change issues
* Validate effectiveness and readiness for audit

---

## **5. Metrics & Measurement**

| Metric                      | Target                | Method                     |
| --------------------------- | --------------------- | -------------------------- |
| Core QMS documents approved | ≥5                    | Document approvals         |
| Foundational SOPs validated | ≥3                    | Evidence review            |
| Governance compliance       | 100%                  | Repo configuration audit   |
| Traceability completeness   | 100%                  | Traceability matrix review |
| QMS baseline released       | 1 (`QMS_Baseline_r1`) | Tag + approval record      |

---

## **6. Quality Assurance & Design Control Activities**

* QA review of all controlled documents
* Verification of repository protections, CODEOWNERS enforcement
* Validation of workflows using Red Witch execution evidence
* Internal pre-audit once baseline is established

---

## **7. Roles & Responsibilities**

(Identical to your earlier roles, but now **QMS Owner** is primary and Red Witch PM becomes *pilot owner* under separate plan.)

---

## **8. Records & Documentation**

* All QMS development issues and evidence stored in `fley-qms`
* All pilot issues/evidence stored in Red Witch repository
* Traceability between Plans ↔ Milestones ↔ Issues maintained
* Controlled documents retained per Record Retention SOP

---

## **9. Linkage to Execution (Governance Model)**

### **Plan → Milestones → Issues**

This plan governs the following milestones:

1. **QMS Foundations**
2. Audit-Ready QMS
3. Compliance Backbone
4. SOP & WI Expansion
5. Certification Preparation

Each milestone contains:

* Issues (documentation, evidence, nonconformances, SOP drafts)
* Pull requests
* Verification/validation artifacts

### **Subordinate Plan (Input):**

* **PLAN – Red Witch Pilot SOP Implementation**
  (Design validation input feeding this plan)

---

## **10. Continuous Improvement & Design Changes**

* All QMS design observations tracked as Continuous Improvement issues
* Pilot findings entered as design changes
* CAPA integration planned for Milestone 3 (Compliance Backbone)
* Management Review after each major milestone

---
