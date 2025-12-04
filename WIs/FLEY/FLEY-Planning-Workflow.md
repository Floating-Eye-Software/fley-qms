---
slug: FLEY-Planning-Workflow
revision: r4
type: WI
status: approved
effective: 2025-12-04
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/FLEY/FLEY-Planning-Workflow.md
---

# **WI – FLEY Planning Workflow**

## **1. Purpose**

This Work Instruction defines how Floating Eye Software (FLEY) plans, sequences, executes, verifies, and reviews all quality-related activities using GitHub. It integrates:

* **Issues** (Development and Operations)
* **Planning Issues** (Plan Issues, Phase Issues, Management Review Issues)
* **Milestones**
* **Dependencies**
* **Verification of Effectiveness (VoE)**
* **Management Review cycles**

This WI ensures a **single, coherent planning and execution workflow** providing traceability, sequencing, and auditability aligned with ISO 9001:2015.

---

## **2. Scope**

### **Applicability**

This WI applies to:

* All quality-related planning activities
* Quality Plans, Project Quality Plans, and Design Control Plans
* Sequencing of phases and plan-level activities
* Management Review planning and execution
* All Issues linked to a Plan Issue, Phase Issue, or Management Review Issue

### **Exclusions**

* Operational GitHub actions (labels, repos, board usage) - covered in **GitHub-QMS-Operations**
* Repository configuration and setup - covered in **GitHub-QMS-Setup**

---

## **3. References**

* SOP – Quality-Planning-SOP
* SOP – Management-Review-SOP
* WI – GitHub-QMS-Setup
* WI – GitHub-QMS-Operations
* WI – GitHub-Change-Control
* WI – GitHub-Document-Control
* Template – Quality Plan
* Template – Project Quality Plan (PQP)
* Template – Design Control Plan (DCP)
* Template – TPL-GH-Plan
* Template – TPL-GH-Management-Review
* ISO 9001:2015 — Clause 8.1, 8.3, 9.1, 9.3

---

## **4. Definitions**

| Term | Definition |
|------|------------|
| **Issue** | A standard GitHub Issue used to plan, execute, document, and verify work. Issues are typed as **Development** or **Operations**, with QMS labels (CAPA, Audit, Objective, Risk, etc.) applied as appropriate. |
| **Planning Issue** | The core planning artifact. Used for Plans, Phases, and Management Review cycles. Contains objectives, milestones, dependencies, linked Issues, traceability, and VoE results. |
| **Plan Issue** | A Planning Issue representing a planning entity such as a Quality Plan, PQP, DCP plan, or improvement initiative. |
| **Phase Issue** | A Planning Issue representing a Milestone, enabling sequencing through GitHub dependencies. |
| **Quality Plan (Document)** | A controlled planning document created when required for regulated or high-impact work. Referenced by a Plan Issue. |
| **Milestone** | GitHub Milestone grouping Issues. Cannot use dependency relationships. |
| **Dependency** | GitHub Issue → Issue “Blocks / Blocked-by” relationship used for sequencing. |
| **Management Review Issue** | A Planning Issue representing the MR cycle, used to track MR readiness, required inputs, linked Plans and Phases, and MR follow-up Issues. |
| **Verification of Effectiveness (VoE)** | Confirmation that objectives were achieved, evidence is complete, and results are verified. |

---

## **5. Responsibilities and Authorities**

| Role | Responsibilities | Authority |
|------|------------------|-----------|
| **Top Management** | Lead MR cycles; approve strategic decisions | Approve MR outputs and planning adjustments |
| **Quality Manager / QMS Admin** | Maintain workflow adherence; manage MR cycles; verify VoE at Plan/Phase/MR levels | Approve Plans, PQPs, DCPs, MR plans |
| **Project Manager / Owner** | Manage project Plans, sequencing, Phases, and related Issues | Approve project-level Plans and related Issues |
| **Process Owner** | Own planning and execution of Issues within their processes | Approve Issue closure |
| **Contributors** | Execute work; attach evidence; update Issues | May close low-risk Issues |

---

## **6. Governance Structure**

FLEY uses a unified planning model:

**Issues → Phase Issues → Milestones → Plan Issues → Management Review Issues**

### **6.1 Governance Tiers**

| Tier | Artifact | Use Case |
|------|----------|----------|
| **1. Issue Only** | GitHub Issue | Low-risk, small-scope work |
| **2. Plan** | Plan Issue | Initiatives, planning, operational improvements |
| **3. Project (PQP)** | Plan Issue referencing a PQP | Formal project planning |
| **4. Design Control (DCP)** | Plan Issue referencing a DCP | Regulated or product-development planning |
| **MR Cycle** | Management Review Issue | MR planning, readiness, and execution |

---

## **7. Planning Process (Planning Issues)**

The Planning Issue is used for **every planning activity**, including:

* Quality Plans
* PQPs
* DCP-linked plans
* Phase sequencing
* Management Review cycles

Each Plan Issue includes:

* Objectives  
* Milestones  
* Linked Issues  
* Dependencies (Plan ↔ Plan, Plan ↔ Phase, Phase ↔ Phase)  
* Traceability to controlled documents  
* VoE and results  
* Lessons learned, residual risks, MR inputs  

### **7.1 Plan Creation**

1. Create a controlled Quality Plan **when required** (regulatory or high-impact).  
2. Create a corresponding **Plan Issue** using TPL-GH-Plan.  
3. Define:  
   * Objectives  
   * Milestones (GitHub Milestones)  
   * Phase sequencing (Phase Issues)  
   * Dependencies  
4. Link relevant SOPs, standards, or controlled documents.

### **7.2 Milestones and Phase Issues**

#### Milestones  
Used to group work and visualize progress.  
Cannot directly participate in dependencies.

#### Phase Issues  
Phase Issues represent Milestones **with sequencing capability**.

Phase Issues enable:

* Phase sequencing  
* Blocking/unblocking Plans or MR cycles  
* Rolling up Issue progress  
* MR readiness triggers  

---

## **8. Issue Execution**

### **8.1 Creating Issues**

Every activity is recorded as a **GitHub Issue**:

* Link to the governing Planning Issue  
* Assign to a Milestone (or Phase Issue when sequencing is required)  
* Add dependencies where applicable  
* Attach or link required evidence  

### **8.2 Execution Tracking**

* Issues appear on the QMS Board (Backlog → In Progress → In Test → Closed)  
* Phase Issues roll up the status of their linked Issues  
* Milestones show aggregate progress  

### **8.3 Issue Closure Criteria**

An Issue may be closed when:

* Work is completed  
* Evidence is attached or referenced  
* Blocking dependencies are resolved  
* Verification appropriate to the governing Plan is complete  

---

## **9. Dependencies and Sequencing**

GitHub supports only **Issue → Issue** dependencies.

Valid sequencing paths:

* **Plan Issue → Plan Issue**  
* **Plan Issue → Phase Issue**  
* **Phase Issue → Phase Issue**  
* **Issue → Issue or Phase Issue**  

This enables:

* Program-level sequencing  
* Project sequencing  
* MR cycle triggering  
* Conditional readiness (e.g., “Audit-Ready QMS”)  

---

## **10. Verification of Effectiveness (VoE)**

VoE is performed at completion of:

* A Plan Issue  
* A Phase Issue  
* A Management Review Issue  

VoE includes:

* Confirmation that objectives were met  
* Verification that all linked Issues are complete or dispositioned  
* Review of evidence and traceability  
* Documentation of:  
  * Residual risks  
  * Lessons learned  
  * Follow-up Issues  

VoE results feed into the next Management Review cycle.

---

## **11. Management Review Cycle**

### **11.1 MR Cycle as a Planning Issue**

Each MR cycle is represented by a **Management Review Issue**, containing:

* Required ISO 9001 §9.3 inputs  
* Dependencies (e.g., Plans that must be complete before MR)  
* Linked Issues and MR actions  
* VoE summaries from completed Plans and Phases  
* Decisions, risks, and follow-up Issues  

### **11.2 MR Cycle Triggers**

An MR Issue may be blocked until prerequisite Plans or Phases close.

Typical triggers:

* Completion of major Plans or PQPs  
* Closure of readiness Phases (e.g., “Audit-Ready QMS”)  
* Significant nonconformance or change  
* Strategic initiative completion  

### **11.3 MR Cycle Execution**

1. Open MR Issue + MR Milestone  
2. Link all relevant Plans, Phases, and Issues  
3. Track progress using dependencies and Milestones  
4. Perform VoE on completed Plans feeding into MR  
5. Document MR decisions, risks, opportunities, and required follow-up  
6. Close the MR Issue and Milestone  
7. Open next MR Issue (if triggered)  

---

## **12. Records**

| Record / Artifact | Owner | Location | Retention | Method |
|-------------------|--------|----------|-----------|--------|
| Issues | Process Owner | GitHub QMS Board | 5 years | System record |
| Plan Issues | Quality Manager | GitHub | 5 years | System record |
| Quality Plans (Documents) | Quality Manager | `/Plans/` | 5 years | Revision control |
| PQPs | Project Manager | `/Plans/<Project>/` | 10 years | Revision control |
| DCPs | Design Lead | `/Plans/<Project>/DCP/` | 10 years or life | Revision control |
| MR Cycles (Issues + Milestones) | Quality Manager | GitHub | 5 years | System record |
| Evidence Attachments | Issue Owner | GitHub/Repo | Match governing record | Linked record |
