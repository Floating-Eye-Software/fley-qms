# **Floating Eye Software Quality Manual (QM)**

## Purpose

The Floating Eye Software Quality Manual (QM) defines the organization-level compliance framework, regulatory requirements, and governance hierarchy for all projects. It ensures regulatory alignment, audit readiness, and consistent quality across all initiatives.

---

## 1. Governance Hierarchy

### 1.1 Organization Level (Floating Eye Software)

* Defines **regulatory-compliant SOPs** (ISO 13485, IEC 62304, IEC 27001, GDPR, HIPAA, EU MDR, etc.)
* SOP = “the way we must work” → mandatory artifacts, traceability, controls
* Responsibilities:

  * Define baseline SDLC: planning, development, release, maintenance
  * Specify mandatory regulatory artifacts:

    * Software Requirements Specification (SRS)
    * Risk Management File (ISO 14971)
    * Usability Engineering File (IEC 62366)
    * Traceability Matrix
  * Provide **work instruction templates** for projects:

    * GitHub issues, pull requests, project boards, commit policies

### 1.2 Frameworks (Execution Models)

* Examples: ODF (Ontario Digital Framework), Agile Scrum, SAFe
* Framework = “how we structure our work” → phases, rituals, ceremonies
* Projects use frameworks to organize tasks, milestones, and deliverables

### 1.3 Projects (Implementation Layer)

* Projects = “the tools + regulatory environment we’re in”
* Each project must map back to Floating Eye SOPs so auditors can see:

  1. Which SOP requirements are satisfied
  2. Where evidence/artifacts live
  3. Which regulatory environments apply

---

## 2. Standard Operating Procedures (SOPs)

* **Baseline SDLC**: planning, development, release, maintenance
* **Mandatory artifacts**:

  * SRS
  * Risk Management File
  * Usability Engineering File
  * Traceability Matrix
* **Work instructions**:

  * Templates for issues, pull requests, project boards
  * Guidance for traceability, commits, and CI/CD pipelines

---

## 3. Compliance Architecture

* **SOP Mapping Layer**: Projects must map SOP requirements to their execution model
* **Traceability**: Requirement → Task → Commit → Test → Result → Risk Control
* Auditors can review any project artifact to verify SOP compliance

---

## 4. Regulatory Compliance

* ISO 13485 (Medical devices – quality management systems)
* IEC 62304 (Medical device software lifecycle)
* IEC 27001 (Information security management)
* GDPR (EU General Data Protection Regulation)
* HIPAA (Health Insurance Portability and Accountability Act)
* EU MDR (Medical Device Regulation)

---

## 5. International Standards

* IEC 82304-1:2016 – Health Software, Product Safety
* ISO/TS 82304-2:2021 – Health and Wellness Apps, Quality & Reliability
* ISO/IEC 27001:2013 – Information Security Management Systems
* ISO/IEC 27701:2019 – Privacy Information Management

---

## 6. Auditability

* Projects must maintain a **traceable link from SOP → Project → Artifacts → Results**
* SOP Mapping Table is mandatory for every project kickoff
* Tools used for mapping may vary (project-level SOPs decide implementation)
