# 📘 **Plan: Update SOPs and WIs for New Governance & Planning Workflow**

## **1. Purpose**

To update all QMS procedures to reflect the new governance model in which:

* **Management Reviews govern but do not own issues**
* **Plans (type:Plan Issues)** become the structured container for QMS initiatives
* **Milestones** represent execution cycles (like sprints)
* **Issues** may remain unscheduled until intentionally placed in a Plan milestone
* **VoE** (Verification of Effectiveness) occurs at the Plan level
* **Traceability links replace parent-child dependencies** between MR and issues

---

# ✔️ **2. Summary of Required Updates**

Below is a per-document breakdown with specific edit goals.

---

# **A. SOP – Management Review** (MR)

### **Objectives**

* Remove any implication that MR “owns” or “parents” actions.
* Replace with: *MR creates actions* (issues), and these actions remain in the backlog until scheduled into a Plan.
* Clarify that an “MR Plan” replaces the MR Issue Type.

### **Required Revisions**

1. **Replace MR Action Items → Child Issues**
   With:

   * “MR-generated actions are logged as Issues and linked to the MR for traceability only.”

2. **Add new concept: MR Plan Issue**

   * MR is documented in a `type:Plan` Issue labeled `Management Review`.
   * Inputs, decisions, outputs, and VoE are recorded within the Plan.

3. **Clarify Review of Prior Actions**
   Replace “review status of previous MR actions” with:

   * “Review the status of actions linked to previous MR Plans, regardless of whether they have been scheduled into a Plan.”

4. **Add Backlog Behavior**

   * “Unscheduled issues remain in the Backlog and do not delay MR cycles.”
   * “MR cycles may occur while issues remain open.”

5. **Add Scheduling Behavior**

   * “Issues are scheduled into Plans and milestones by intentional decision, not automatically by virtue of their MR linkage.”

6. **Add VoE Alignment**

   * MR Plan contains VoE for MR outputs.
   * Not all MR actions require VoE; only the MR Plan does.

---

# **B. SOP – Quality-Planning**

### **Objectives**

* Introduce the **Plan Issue Type** as the central object of QMS planning.
* Embed the Backlog → Plan → Milestone → VoE workflow.
* Remove implication that risks/opportunities must be immediately scheduled.

### **Required Revisions**

1. **Add Plan Issue Definition**

   * Define Plan as “a structured, time-bound QMS activity with milestones and VoE.”

2. **Add Issue Scheduling Rules**

   * Issues may be:

     * Unscheded in backlog (default)
     * Scheduled into a Plan milestone (implementation ready)

3. **Add Risk & Opportunity Handling**

   * Risks/Opportunities create Issues that go to Backlog unless immediately scheduled.

4. **Clarify that Milestones Represent Implementation**

   * Milestones define “execution cycles” (like sprints).
   * Quality objectives may map to Plan milestones.

5. **Add VoE Requirements for Plans**

   * VoE is executed once the Plan’s milestones are complete.

---

# **C. SOP – Change-Control**

### **Objectives**

* Align change actions with Plan scheduling model.
* Ensure change requests can remain unscheduled until capacity exists.

### **Required Revisions**

1. Add: “Change actions (issues) remain in Backlog until assigned to a Plan milestone.”
2. Add: “The Change Request Record may be the parent, but the Plan milestone is the scheduling unit.”
3. Clarify VoE responsibilities (the Plan performs VoE, not the CR itself).

---

# **D. SOP – Corrective and Preventive Action (CAPA)**

### **Objectives**

* Align NC/CAPA issues with the backlog model.
* Ensure CAPA implementation is scheduled like all other work.

### **Required Revisions**

1. Add: “Nonconformities and CAPA actions default to Backlog.”
2. Add: “Corrective actions are scheduled into Plan milestones when ready.”
3. Update: “Effectiveness verification for a CAPA occurs within the CAPA Issue, but implementation may occur within any Plan.”

---

# **E. SOP – Risk and Opportunity Management**

### **Objectives**

* Reflect that not all risks/opportunities map to immediate Plans.
* Keep Risk Register separate from scheduling.

### **Required Revisions**

1. Add: “Risk actions may remain in Backlog until scheduled.”
2. Add: “Management Review may identify risks; these remain unscheduled unless converted into a Plan action.”
3. Link Risk actions to Plans later for implementation.

---

# **F. WI – FLEY-Action-Management**

### **Objectives**

* Define the full lifecycle of Issue → Backlog → Plan → Milestone → VoE.
* Provide rules for links vs parent-child behavior.

### **Required Revisions**

1. Define **link types**:

   * `relates-to` for MR traceability
   * `blocked-by`/`blocks` for dependencies
   * Parent-child only within Plan’s internal decomposition

2. Add Backlog Behavior Section:

   * “Unscheduled issues reside in Backlog and have no milestone.”

3. Add Scheduling Rules:

   * Only Plans and Milestones may contain scheduled issues.
   * MR does *not* control the issue lifecycle.

4. Add Execution Rules:

   * Milestones act like sprints; unscheduled issues never block MR cycles.

---

# **G. WI – GitHub-QMS-Setup**

### **Objectives**

* Implement new labels, templates, boards, and roadmap configuration.

### **Required Revisions**

1. Add labels:

   * `type:Plan`
   * `category:MR`
   * `category:QMS-Improvement`
   * `Plan-Milestone`
   * etc.

2. Define Projects:

   * “QMS Roadmap” shows all Plans with timeboxes.

3. Document Templates:

   * Update `TPL-GH-Plan`
   * Update `Quality-Plan-Template`

4. Define Backlog Board:

   * All new actions default here.

5. Define Milestone/Plan Workflow:

   * Only Plan-owners assign issues to milestones.

---

# **3. Implementation Steps (Chronological)**

### **Phase 1 — Foundations**

1. Create `type:Plan` Issue Template
2. Create milestone structure for Plans
3. Update Roadmap configuration
4. Add required labels and fields

### **Phase 2 — Update Procedures**

5. Update:

   * SOP – Management Review
   * SOP – Quality Planning
   * WI – QMS Setup
   * WI – Action Management

### **Phase 3 — Integrate Risk, Change, CAPA**

6. Update Risk & Opportunity SOP
7. Update CAPA SOP
8. Update Change-Control SOP

### **Phase 4 — Validate in Real Use**

9. Execute one real Plan (with VoE)
10. Conduct an MR using Plan Issue Type
11. Perform internal audit to confirm:

    * traceability
    * scheduling model
    * VoE logic
    * backlog behavior

---

# **4. Deliverables**

| Deliverable                     | Description                                          |
| ------------------------------- | ---------------------------------------------------- |
| Updated SOP – MR                | MR becomes Plan-driven; issues are traceability only |
| Updated SOP – Quality Planning  | Backlog → Plan → Milestone model                     |
| Updated WI – Action Management  | Issue lifecycle and link rules                       |
| Updated WI – GitHub Setup       | Labels, templates, project rules                     |
| Updated CAPA, Risk, Change SOPs | Align with Plan scheduling                           |
| Demonstrated Plan Cycle         | Used to prove effectiveness                          |
| MR conducted using Plan         | First MR in new system                               |
| Internal Audit Evidence         | Confirms compliance                                  |

---
