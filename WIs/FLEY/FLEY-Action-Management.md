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

To define the **workflow for managing actions** in the Floating Eye Software (FLEY) QMS using GitHub, including initiation, planning, execution tracking, Verification of Effectiveness (VoE) at the plan level, MR-cycle management, and closure.

This WI ensures:

* Consistent and auditable workflows across all action types.
* Traceability from actions to Plans, PQPs, or DCPs.
* Proper use of MR milestones, dependencies, and triggers to drive continuous improvement.
* Verification of both action completion and plan-level effectiveness before milestone closure.

---

## **2. Scope**

**Applicability**

* Defines the **workflow layer** for all FLEY QMS actions, including:

  * QMS operational actions (audits, CAPAs, improvements)
  * Quality Plans, Projects, and Design-Control activities
  * MR-cycle workflows and related dependencies

**Exclusions**

* Day-to-day operational execution steps (covered in GitHub-QMS-Operations WI)
* GitHub setup, labeling, and repository configuration (covered in GitHub-QMS-Setup WI)

---

## **3. References**

* SOP – Project-Management
* SOP – Quality-Planning
* SOP – Change-Control
* WI – GitHub-QMS-Setup
* WI – GitHub-Document-Control
* Template – Quality Plan
* Template – Project Quality Plan (PQP)
* Template – Design Control Plan (DCP)
* ISO 9001:2015 – Clause 8.1 & 9.1 (Operational Planning and Monitoring)

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
| **Quality Manager / QMS Admin** | Oversees workflow adherence, traceability, milestone management, and VoE verification at the Plan level. | Approve Plans, PQPs, and MR-related actions. |
| **Project Manager / Owner**     | Ensures all project work is linked to a Plan or PQP; participates in VoE for project-level plans. | Approve project-level workflow assignments. |
| **Process Owner**               | Monitors action execution and closure within their process; participates in VoE for operational plans. | Approve closure of assigned actions.        |
| **Contributors / Team Members** | Create, execute, and link Issues; attach evidence.           | Close low-risk Issues per workflow rules.   |

---

## **6. Action Management Workflow**

### **6.1 Governance Tiers**

| Tier  | Governance Level | Artifact                        | Typical Trigger                             | Record Location         |
| ----- | ---------------- | ------------------------------- | ------------------------------------------ | ---------------------- |
| **1** | Issue Only       | GitHub Issue                     | Minor QMS task                             | FLEY QMS Board         |
| **2** | Plan             | Quality Plan / Planning Issue    | New initiative or quality improvement      | `/Plans/`              |
| **3** | Project          | Project Quality Plan (PQP)       | Formal project requiring defined governance| `/Plans/<Project>/`    |
| **4** | Design Control   | Design Control Plan (DCP)        | Regulated design/development activities    | `/Plans/<Project>/DCP/` |

### **6.2 Workflow Events and Issue Handling**

1. **New Action Initiation**
   * Record all actions as GitHub Issues.
   * Reference the governing Plan, PQP, or SOP.
   * Apply appropriate labels and link to MR milestone if relevant.

2. **Plan/PQP/DCP Association**
   * Tier 2-4 actions are linked to a Milestone corresponding to the governing Plan, PQP, or DCP.
   * Dependencies are explicitly defined via GitHub **Blocks / Blocked-by** relationships.

3. **Execution Tracking**
   * Issue status is monitored on the FLEY QMS Board or relevant project view.
   * Evidence is attached directly to the Issue or linked from other artifacts.
   * For MR-linked actions, progress is tracked under the corresponding MR milestone.

4. **Closure and Verification**
   * Actions close only after execution is complete.
   * For Tier 2-4 plans, **plan-level VoE** must be performed to verify that all objectives and intended outcomes are achieved.
   * If VoE confirms objectives are met, close the Plan/PQP/DCP and update status.
   * If VoE identifies gaps, generate follow-up Issues and reassign to the next MR cycle if needed.

### **6.2 When to Use an Issue Only**

**Criteria for Issue-Only Work**

* Low risk and limited scope.
* No new deliverables or measurable objectives.
* Falls within an existing approved Plan or PQP.

### **6.3 When a Plan Is Required**

1. If the action introduces new deliverables, measurable outcomes, or cross-functional collaboration, create a **Quality Plan** (`/Plans/`).

A formal Quality Plan document may exist when required by scope or regulatory need, but is not mandatory for all Plans. Each Quality Plan document shall have a corresponding Planning Issue in GitHub.

When a Quality Plan document exists, it shall be referenced in the Planning Issue. When no formal document is required, the Planning Issue itself serves as the planning artifact.

### **6.4 When a PQP Is Required**

1. If the activity constitutes a formal **Project**, create a **Project Quality Plan (PQP)**.
2. All design-controlled projects must also reference a DCP.

### **6.5 When a DCP Is Required**

1. Prepare a **Design Control Plan (DCP)** whenever design or development work affects regulated product performance, safety, or compliance.
2. Link the DCP to its governing PQP.

### **6.6 Managing Unplanned Work**

1. If work arises outside an approved Plan or PQP:

   * Record it as a **new Issue**.
   * Reference the most relevant governing SOP or Plan.
2. If no suitable Plan exists, the responsible person shall **create one** before proceeding.
3. The Quality Manager reviews during Management Review to ensure no recurring gaps.

### **6.7 Execution and Closure**

- All actions and records in GitHub shall be executed and closed according to their governance level. The following subsections define execution and closure requirements for Issues, Plans, and Projects.
- If an MR output requires a Plan or PQP, assign the Plan’s deliverables to the MR milestone.
- Verification of Effectiveness shall confirm completion of all linked outputs before the milestone is closed.

#### **6.7.1 Issues**

   1. All Issues are automatically added to the **FLEY QMS Board** (Backlog → In Progress → In Test → Closed).
   2. Attach or link all evidence within the Issue.
   3. MR-related Issues are assigned to the MR milestone.
   4. Each MR-related issue must reference the originating MR issue for traceability.
   5. Close the issue only when the action is complete and verified.

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

### **6.9 Management Review (MR) Workflow**

The MR process in GitHub ensures leadership oversight, performance review, and a traceable record of decisions and actions. Each MR cycle is represented by a **GitHub milestone** linking related Issues.

#### **6.9.1 MR Cycle and Milestones**

Top Management leads each MR cycle with support from the Quality Manager, ensuring all required inputs per ISO 9001:2015 §9.3 are reviewed.

1. **Triggering an MR Cycle**
   * MR cycles start when a Cycle Trigger occurs:
     - Completion of a Plan, PQP, or significant change
     - Audit or nonconformance outcomes
     - Strategic initiative or policy change
2. **MR Issue and Milestone Creation**
    * Create an MR Issue documenting decisions, outputs, and related actions.
    * Create a corresponding MR milestone and link all relevant Issues.
3. **Related Work & Linking** – Assign all relevant Issues, Plans, and Projects arising from that MR to the MR milestone. Use **Blocks / Blocked-by** relationships to represent dependencies between actions.
4. **Progress Tracking** – Use milestone progress bars and Project boards to monitor completion.
5. **Cycle Closure**
   * Verify all linked Issues are completed and effective.
   * Perform VoE for all associated Plans, PQPs, and DCPs before closing MR milestone.
   * Record summary outcomes in the MR Issue.
   * Initiate the next MR cycle as needed.

#### **6.9.2 Dependencies and Triggers for MR Cycles**

MR cycles are **event-driven** and may begin when any of the following occurs:

1. Completion of a major Plan, Project, or Change initiative.
2. Achievement of a defined readiness or maturity milestone (e.g., *Audit-Ready QMS*).
3. Occurrence of a significant nonconformance, risk, or policy change.

Each trigger is documented as an Issue that either:

* **Blocks** the next MR milestone until resolved, or
* **Unblocks** the next MR milestone once complete.

The Quality Manager tracks these dependencies across repositories to ensure that MR cycles start under appropriate conditions.

#### **6.9.3 Managing MR Milestones**

1. **Initiation** – When a trigger is met, create a new MR Issue and corresponding milestone; assign ownership to Top Management or the Quality Manager.
2. **During the Cycle** – Link all relevant Issues (Objectives, Risks, Improvements, CAPAs) to the MR milestone; update status and evidence regularly; monitor progress via milestone bar or dashboards.
3. **Closing the Cycle** – When all linked Issues are verified effective, close the milestone; record summary of outcomes in the MR Issue; initiate the next cycle if needed.

#### **6.9.4 Traceability and Evidence**

* Each MR milestone links to its MR Issue.
* Linked Issues must reference the MR (e.g., “Linked to MR-2”).
* Cross-repository Issues use GitHub cross-reference syntax or dependency links.
* All MR-related records remain visible in GitHub history for full traceability.

#### **6.9.5 Verification of Effectiveness**

* Before closing an MR milestone, verify that all linked Issues are completed and effective.
* Record verification summaries in the MR Issue per *Action-Management WI*.
* If any action is Partially Effective or Ineffective, reassign it to the next MR milestone for continued tracking.

---

## **7. Records**

| Record / Artifact            | Responsible Owner | Storage Location          | Retention                   | Control Method   |
| ---------------------------- | ----------------- | ------------------------- | --------------------------- | ---------------- |
| Issues              | Process Owner     | GitHub QMS Board          | 5 years                     | System record    |
| Milestones      | Process Owner       | GitHub Milestones     | 5 years                     | System record    |
| Quality Plans                | Quality Manager   | `/Plans/`                 | 5 years                     | Version control  |
| Project Quality Plans (PQP)  | Project Manager   | `/Plans/<Project>/`     | 10 years                    | Version control |
| Design Control Plans (DCP)   | Design Lead       | `/Plans/<Project>/DCP/` | 10 years or life of product | Version control |
| Management Review records    | Quality Manager   | GitHub Issues & Milestones      | 5 years                     | System record   |
| Evidence attachments / links | Action Owner      | GitHub / Wiki             | Match governing record      | Linked records   |
