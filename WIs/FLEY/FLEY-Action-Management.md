---
slug: FLEY-Action-Management
revision: r4
type: WI
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/FLEY/FLEY-Action-Management.md
---

# **WI – FLEY Action Management**

## **1. Purpose**

This Work Instruction defines the **end-to-end workflow for managing actions in the FLEY QMS using GitHub**, including:

* Initiation and classification of actions
* Assignment to governance levels (Issue, Plan, PQP, DCP)
* Planning and execution tracking
* Management Review (MR) cycle management
* Verification of Effectiveness (VoE)
* Closure and records management

This ensures consistent, traceable, and auditable workflows across all action types and guarantees that **both action completion and plan-level effectiveness** are verified prior to closing milestones or MR cycles.

---

## **2. Scope**

**Applicability**

This WI governs the workflow layer for all FLEY QMS actions, including:

* QMS operational actions (audits, CAPAs, improvements)
* Quality Plans and project governance
* Design Control activities
* Management Review (MR) cycle creation, execution, dependencies, and triggers

**Exclusions**

* Day-to-day operational execution steps (covered in GitHub-QMS-Operations WI)
* GitHub setup, labeling, and repository configuration (covered in GitHub-QMS-Setup WI)

---

## **3. References**

* SOP – Quality-Planning
* SOP – Management-Review
* WI – GitHub-QMS-Setup
* WI – GitHub-QMS-Operations
* WI – GitHub-Change-Control
* WI – GitHub-Document-Control
* Templates: Quality-Plan, Project-Quality-Plan (PQP), Design-Control-Plan (DCP), TPL-GH-Plan, TPL-GH-Management-Review
* ISO 9001:2015 – Clause 8.1 & 9.1

---

## **4. Definitions**

| **Term**                         | **Definition**                                                                                                                  |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Milestone**                    | GitHub object grouping related Issues or Pull Requests representing a phase, cycle, or objective.                                |
| **Planning Issue**               | Issue defining objectives, actions, and verification criteria linked to Plans or PQPs.                                          |
| **Management Review (MR) Issue** | Planning Issue representing a formal MR cycle, including decisions and actions.                                                |
| **MR Milestone**                 | Milestone representing the active MR cycle, linking all related Issues.                                                         |
| **Dependency**                   | Relationship between Issues, Plans, or Milestones indicating blocking or triggering conditions.                                  |
| **Cycle Trigger**                | Event that initiates a new MR cycle (e.g., Plan completion, project closure, CAPA resolution).                                  |
| **Verification of Effectiveness (VoE)** | Assessment of whether the objectives and intended outcomes of a Plan, PQP, or DCP have been achieved.                  |

---

## **5. Responsibilities and Authorities**

| Role                            | Responsibilities                                             | Authority / Decision Rights                  |
| ------------------------------- | ------------------------------------------------------------ | ------------------------------------------- |
| **Top Management**              | Leads MR cycles and approves strategic actions.             | Approve MR outputs and workflow adjustments. |
| **Quality Manager / QMS Admin** | Manage workflow adherence, traceability, milestones, MR cycles, and VoE. | Approve Plans, PQPs, and MR actions.               |
| **Project Manager / Owner**     | Ensures all project work is linked to a Plan or PQP; support VoE.  | Approve project-level workflow assignments. |
| **Process Owner**               | Monitors action execution and closure within their process; support VoE for process-level plans. | Approve closure of assigned actions.        |
| **Contributors / Team Members** | Create, execute, and link Issues; attach evidence.           | Close low-risk Issues per workflow rules.   |

---

## **6. Action Management Workflow**

The workflow is organized into governance tiers, followed by the procedural steps for initiation, planning, execution, VoE, MR-cycle management, and closure.

### **6.1 Governance Tiers**

| Tier  | Governance Level | Artifact                        | Typical Trigger                             | Record Location         |
| ----- | ---------------- | ------------------------------- | ------------------------------------------ | ---------------------- |
| **1** | Issue Only       | GitHub Issue                     | Minor QMS task                             | FLEY QMS Board         |
| **2** | Plan             | Quality Plan / Planning Issue    | New initiative or quality improvement      | `/Plans/`              |
| **3** | Project          | Project Quality Plan (PQP)       | Formal project requiring defined governance| `/Plans/<Project>/`    |
| **4** | Design Control   | Design Control Plan (DCP)        | Regulated design/development activities    | `/Plans/<Project>/DCP/` |

1. **Record every action as a GitHub Issue.**
2. Reference the governing **Plan, PQP, DCP, or SOP**.
3. Apply relevant labels and assign to the **MR milestone** if MR-related.
4. For Tiers 2–4, link the Issue to the governing Milestone.
5. Define **dependencies** using Blocks / Blocked-by.

### **6.2 Criteria for "Issue-Only" Work**

Use an Issue without a Plan only if:

* Low risk and limited scope.
* No new deliverables or measurable objectives.
* Work is fully covered by an existing SOP, Plan, or governing PQP.

### **6.3 When a Plan Is Required**

1. If the action introduces new deliverables, measurable outcomes, or cross-functional collaboration, create a **Quality Plan** (`/Plans/`).

2. A formal Quality Plan document may exist when required by scope or regulatory need but is not mandatory for all Planning Issues. If a Quality Plan document exists, reference it in the Planning Issue.

3. When no formal Quality Plan document is required, the Planning Issue itself serves as the planning artifact.

### **6.4 When a PQP Is Required**

A **Project Quality Plan (PQP)** is required when:

1. If the activity constitutes a formal project needing defined governance, create a **Project Quality Plan (PQP)**.
2. All design-controlled projects must also reference a DCP.

### **6.5 When a DCP Is Required**

1. Prepare a **Design Control Plan (DCP)** whenever design or development work affects regulated product performance, safety, or compliance.
2. Link the DCP to its governing PQP.

### **6.6 Managing Unplanned Work**

If work arises outside an approved Plan or PQP:

1. Record unexpected work as a **new Issue**.
2. Reference the most relevant governing SOP or Plan.
3. If no Plan exists, the responsible person **creates one** before proceeding.
4. The Quality Manager reviews patterns of unplanned work during Management Review.

### **6.7 Execution and Closure Requirements**

All work (Issues, Plans, PQPs, DCPs) must be executed and closed according to its governance level.

If an MR output requires a Plan or PQP, the associated deliverables must be linked to the MR milestone.

**VoE is mandatory** for all Plans, PQPs, and DCPs before closing the related milestone or MR cycle.

#### **6.7.1 Issues**

1. Issues appear on the **FLEY QMS Board** workflow (Backlog → In Progress → In Test → Closed).
2. Attach or link all evidence within the Issue.
3. MR-related Issues must be assigned to the MR milestone and reference the MR Issue.
4. Issues close only after full execution and verification.

#### **6.7.2 Plans**

   1. Group related Issues under a **Milestone** or **linked board view** corresponding to the Plan deliverables and stages.
   2. Monitor progress toward objectives and update the Plan status as milestones are achieved.
   3. **Perform Verification of Effectiveness (VoE):**

      * Verify deliverables and evidence against the objectives, success criteria, and acceptance metrics defined in the governing Plan.
      * Record a summary of verification results and effectiveness assessment in the Plan.
      * Create a **new revision** of the Plan per *Change-Control-SOP* when verification results are added.
      * Capture residual risks, lessons learned, or follow-up actions as new Issues if applicable.

#### **6.7.3 Projects**

   1. Manage all project-related Issues and deliverables under the approved **Project Quality Plan (PQP)** or **Design Control Plan (DCP)**.
   2. Track progress using GitHub **Milestones**, **Boards**, or **linked repositories**, ensuring each major phase or gate review corresponds to defined PQP milestones.
   3. Perform Verification and Validation (V&V) per the PQP or DCP; use testing evidence, review minutes, and release records as proof of effectiveness.
   4. When all milestones are complete, perform a **Verification of Effectiveness** review at the project level:
      * Confirm that all PQP or DCP objectives were achieved and that outputs meet acceptance criteria.
      * Record the summary and effectiveness outcome in the **final PQP revision** or closing GitHub record.
      * Log any lessons learned or improvement actions as new Issues under the Continuous Improvement board.
   5. The **Project Manager** and **Quality Manager** jointly approve project closure and effectiveness verification.

### **6.8 Review and Approval**

| Level | Reviewer(s)                       | Approval Authority                              |
| ----- | --------------------------------- | ----------------------------------------------- |
| Issue | Process Owner / Project Lead      | Process Owner                                   |
| Plan  | Quality Manager / Process Owner   | Quality Manager                                 |
| PQP   | Project Manager + Quality Manager | Both                                            |
| DCP   | Design Lead + Quality Manager     | Quality Manager / Top Management (if regulated) |

---

## **7. Management Review (MR) Workflow**

MR cycles ensure leadership oversight, evaluation of QMS performance, and traceable decisions.

### **7.1 MR Cycle Structure**

1. **Triggering Events (Cycle Triggers)**

   * Completion of a Plan or PQP
   * Audit or nonconformance
   * Policy or strategic change
   * Major readiness/maturity milestone

2. **Creating the MR Issue and Milestone**

   * Create an MR Issue documenting required inputs (ISO 9001:2015 §9.3).
   * Create the corresponding MR milestone.
   * Link all relevant Issues via milestone assignment and dependencies.

3. **Tracking During the Cycle**

   * Use milestone progress bars and boards.
   * Update evidence and statuses.
   * Use Blocks / Blocked-by relationships to express dependencies.

4. **Cycle Closure**

   * All linked Issues must be completed and **verified effective**.
   * Perform VoE for associated Plans, PQPs, and DCPs.
   * Record summary outcomes in the MR Issue.
   * Start the next MR cycle as needed.

### **7.2 Dependencies and Event Triggers**

* Completion or occurrence of significant outputs may **block** or **unblock** the next MR milestone.
* Each dependency must be expressed using GitHub dependency links.
* The Quality Manager monitors cross-repository dependencies to ensure cycles start appropriately.

### **7.3 Traceability and Evidence**

* Every MR milestone links to its MR Issue.
* Each linked Issue references the MR (e.g., “Linked to MR-2”).
* Cross-repo linking uses GitHub’s native cross-reference syntax.
* All MR records remain visible in GitHub for full traceability.

### **7.4 MR Verification of Effectiveness**

Before closing an MR milestone:

* Verify that all linked Issues are complete and effective.
* Document VoE summaries in the MR Issue.
* Ineffective or Partially Effective actions are reassigned to the next MR cycle.

---

## **8. Records**

| Record / Artifact            | Responsible Owner | Storage Location          | Retention                   | Control Method   |
| ---------------------------- | ----------------- | ------------------------- | --------------------------- | ---------------- |
| Issues              | Process Owner     | GitHub QMS Board          | 5 years                     | System record    |
| Milestones      | Process Owner       | GitHub Milestones     | 5 years                     | System record    |
| Quality Plans                | Quality Manager   | `/Plans/`                 | 5 years                     | Version control  |
| Project Quality Plans (PQP)  | Project Manager   | `/Plans/<Project>/`     | 10 years                    | Version control |
| Design Control Plans (DCP)   | Design Lead       | `/Plans/<Project>/DCP/` | 10 years or life of product | Version control |
| Management Review records    | Quality Manager   | GitHub Issues & Milestones      | 5 years                     | System record   |
| Evidence attachments / links | Action Owner      | GitHub / Wiki             | Match governing record      | Linked records   |
