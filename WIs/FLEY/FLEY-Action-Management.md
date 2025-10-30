# **WI – FLEY Action Management**

**Slug:** FLEY-Action-Management  
**Revision:** r2 **DRAFT**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Project-Management-SOP, Quality-Planning-SOP, Change-Control-SOP, Design-Control-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/FLEY/FLEY-Action-Management.md  

---

## **1. Purpose**

To define how actions are initiated, planned, tracked, and closed in the Floating Eye Software (FLEY) Quality Management System (QMS) using GitHub.

This WI ensures that:

* All work is traceable to a governing intent (Plan, Project, or SOP).
* The level of planning and governance is appropriate to the scope and risk.
* Execution, evidence, and closure are consistent and auditable in GitHub.

---

## **2. Scope**

**Applicability**

* Applies to all FLEY QMS actions, including:

  * QMS operational activities (audits, reviews, CAPAs, improvements)
  * Quality planning and project execution
  * Design-controlled work (when applicable)

**Exclusions**

* Routine operational work already governed by another active Plan or PQP (e.g., daily development tasks) does not require a separate Action record.

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

## **4. Responsibilities and Authorities**

| Role                            | Responsibilities                                                                  | Authority / Decision Rights                  |
| ------------------------------- | --------------------------------------------------------------------------------- | -------------------------------------------- |
| **Quality Manager / QMS Admin** | Oversees use of this WI and verifies traceability and closure quality.            | Approve QMS-level Plans and changes.         |
| **Project Manager / Owner**     | Defines project scope and ensures all related work has an associated Plan or PQP. | Approve project-level actions and schedules. |
| **Process Owner**               | Ensures actions within their process area follow this WI.                         | Approve closure of assigned actions.         |
| **Contributors / Team Members** | Create and execute Issues, attach evidence, and link to Plans.                    | Close low-risk Issues with peer review.      |

---

## **5. Step-by-Step Procedure**

### **5.1 Decide Governance Level**

All actions fall under one of four tiers of control:

| Tier  | Governance Level | Required Artifact          | Typical Triggers                             | Record Location         |
| ----- | ---------------- | -------------------------- | -------------------------------------------- | ----------------------- |
| **1** | Issue Only       | GitHub Issue               | Minor or routine QMS task                    | FLEY QMS Board          |
| **2** | Plan             | Quality Plan               | New initiative or quality improvement effort | `/Plans/`               |
| **3** | Project          | Project Quality Plan (PQP) | Formal project requiring defined governance  | `/Plans/<Project>/`     |
| **4** | Design Control   | Design Control Plan (DCP)  | Regulated design/development activities      | `/Plans/<Project>/DCP/` |

---

### **5.2 When to Use an Issue Only**

1. Create a **GitHub Issue** using the relevant template.
2. Apply the correct **label** (`Audit`, `CAPA`, `Improvement`, `Change Request`, etc.).
3. Reference the **governing Plan, PQP, or SOP** in the Issue description.
4. Execute the work and attach evidence (screenshots, links, or comments).
5. On completion, update the Issue with closure notes and supporting evidence.
6. Move the Issue to **Closed** on the FLEY QMS Board.

**Criteria for Issue-Only Work**

* Low risk and limited scope.
* No new deliverables or measurable objectives.
* Falls within an existing approved Plan or PQP.

---

### **5.3 When a Plan Is Required**

1. If the action introduces new deliverables, measurable outcomes, or cross-functional collaboration, create a **Quality Plan** (`/Plans/`).
2. Use the *Quality Plan Template* to define:

   * Purpose, Scope, Objectives
   * Applicable SOPs and Standards
   * Roles, Metrics, and Record Locations
3. Submit the Plan for **Quality Manager approval**.
4. Create linked Issues for each deliverable and group them into **Milestones**.
5. Track progress on the **FLEY QMS Board** or dedicated project view.

---

### **5.4 When a PQP Is Required**

1. If the activity constitutes a formal **Project**, create a **Project Quality Plan (PQP)**.
2. Define in the PQP:

   * Which SOPs and WIs apply
   * Quality objectives, risk, and review cadence
   * Documentation and retention requirements
3. Obtain approvals from **Project Manager** and **Quality Manager**.
4. Create and manage project Issues and Milestones under this PQP.

> All design-controlled projects must also reference a DCP.

---

### **5.5 When a DCP Is Required**

1. Prepare a **Design Control Plan (DCP)** whenever design or development work affects regulated product performance, safety, or compliance.
2. Link the DCP to its governing PQP.
3. Maintain traceability from requirements → design outputs → verification → validation.
4. Follow the design reviews defined in the DCP until release or closure.

---

### **5.6 Managing Unplanned Work**

1. If work arises outside an approved Plan or PQP:

   * Record it as a **new Issue**.
   * Reference the most relevant governing SOP or Plan.
2. If no suitable Plan exists, the responsible person shall **create one** before proceeding.
3. The Quality Manager reviews during Management Review to ensure no recurring gaps.

---

### **5.7 Execution and Closure**

All actions and records in GitHub shall be executed and closed according to their governance level. The following subsections define execution and closure requirements for Issues, Plans, and Projects.

#### **1. Issues**

   1. All Issues are automatically added to the **FLEY QMS Board** (Backlog → In Progress → In Test → Closed).
   2. Attach or link all evidence within the Issue.
   3. Upon completion, confirm:

     * Objectives met
     * Records updated or archived
     * Linked Issues closed
   4. Comment “**Action complete – evidence attached**” and close the Issue.

#### **2. Plans**

   1. Group related Issues under a **Milestone** or **linked board view** corresponding to the Plan deliverables and stages.
   2. Monitor progress toward objectives and update the Plan status as milestones are achieved.
   3. **Perform Verification of Effectiveness (VoE):**

      * Verify deliverables and evidence against the objectives, success criteria, and acceptance metrics defined in the governing Plan.
      * Record a summary of verification results and effectiveness assessment (“Effective / Partially Effective / Ineffective”) in **Plan §9**.
      * Create a **new revision** of the Plan per *Change-Control-SOP* when verification results are added.
      * Capture residual risks, lessons learned, or follow-up actions as new Issues if applicable.
   4. Comment “**Verification complete – Plan closed**” on the Plan Issue or board item when completed.

#### **3. Projects**

   1. Manage all project-related Issues and deliverables under the approved **Project Quality Plan (PQP)** or **Design Control Plan (DCP)**.
   2. Track progress using GitHub **Milestones**, **Boards**, or **linked repositories**, ensuring each major phase or gate review corresponds to defined PQP milestones.
   3. Perform Verification and Validation (V&V) per the PQP or DCP; use testing evidence, review minutes, and release records as proof of effectiveness.
   4. When all milestones are complete, perform a **Verification of Effectiveness** review at the project level:
      * Confirm that all PQP or DCP objectives were achieved and that outputs meet acceptance criteria.
      * Record the summary and effectiveness outcome in the **final PQP revision** or closing GitHub record.
      * Log any lessons learned or improvement actions as new Issues under the Continuous Improvement board.
   5. The **Project Manager** and **Quality Manager** jointly approve project closure and effectiveness verification.

---

### **5.8 Review and Approval**

| Level | Reviewer(s)                       | Approval Authority                              |
| ----- | --------------------------------- | ----------------------------------------------- |
| Issue | Process Owner / Project Lead      | Process Owner                                   |
| Plan  | Quality Manager / Process Owner   | Quality Manager                                 |
| PQP   | Project Manager + Quality Manager | Both                                            |
| DCP   | Design Lead + Quality Manager     | Quality Manager / Top Management (if regulated) |

---

## **6. Records**

| Record / Artifact            | Responsible Owner | Storage Location          | Retention                   | Control Method   |
| ---------------------------- | ----------------- | ------------------------- | --------------------------- | ---------------- |
| Issues (completed)           | Process Owner     | GitHub QMS Board          | 5 years                     | System record    |
| Quality Plans                | Quality Manager   | `/Plans/`                 | 5 years                     | Version control  |
| Project Quality Plans (PQP)  | Project Manager   | `/Plans/<Project>/`     | 10 years                    | Revision control |
| Design Control Plans (DCP)   | Design Lead       | `/Plans/<Project>/DCP/` | 10 years or life of product | Revision control |
| Evidence attachments / links | Action Owner      | GitHub / Wiki             | Match governing record      | Linked records   |
