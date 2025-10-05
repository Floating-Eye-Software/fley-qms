# **Work Instruction: Project & Quality Planning using GitHub**

**Document No.:** QMS-WI-06-02
**Title:** Project & Quality Planning using GitHub
**Revision:** 1.1
**Effective Date:** [Insert Date]
**Approved By:** [Quality Manager]

---

## **1. Purpose**

To define the process for creating, maintaining, and monitoring project and quality plans using GitHub tools in support of QMS planning requirements.
This WI ensures effective management of:

* Project and quality plans
* Risks and opportunities
* Quality objectives
* Milestones and deliverables
* Change control and evidence management

---

## **2. Scope**

Applies to all QMS users involved in project or quality planning, including preparation of plans, tracking progress, and maintaining evidence in GitHub repositories.

---

## **3. Responsibilities**

| Role                               | Responsibilities                                                                                                                               |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Quality Manager**                | Maintains GitHub repositories and structure; reviews plans, milestones, and project boards monthly; ensures records are retained and approved. |
| **Process Owners / Project Leads** | Create and maintain project and quality plans; update linked issues, risks, and objectives; report status in project boards.                   |
| **Top Management**                 | Reviews key milestones, objectives, and planning outcomes during Management Review.                                                            |

---

## **4. Definitions**

* **GitHub Issue:** Record used to capture a deliverable, task, risk, opportunity, or objective.
* **Wiki Page:** Markdown document stored in the GitHub Wiki repository used for formal plans and reports.
* **Milestone:** GitHub grouping of related issues with defined scope, objectives, and acceptance criteria.
* **Project Board:** Kanban-style dashboard used to monitor progress of QMS and project activities.
* **Label:** Tag assigned to issues for categorization (e.g., `Risk`, `Opportunity`, `Objective`, `Change`).

---

## **5. Procedure**

### **5.1 Creating a Project Plan**

1. Create a new wiki page under `/Project-Docs/` named:
   `Project-Name-Quality-Plan.md`
2. Include the following sections:

   * Scope & deliverables
   * Resources & responsibilities
   * Schedule & phases
   * Risk management approach
   * Linked quality objectives and compliance requirements
   * References to applicable SOPs and WIs
3. Link the plan in the project’s **README** or summary page.

---

### **5.2 Linking Risks and Opportunities**

1. For each project plan, identify risks and opportunities relevant to project success or product/service quality.
2. Create or link GitHub Issues labeled `Risk` or `Opportunity`.
3. Record issue numbers and mitigation summaries in the **Risk Management** section of the plan.
4. Update linked issues as actions are implemented; reflect results in milestone or plan updates.

---

### **5.3 Quality Plans**

#### 5.3.1 Organization-Level Plans

1. Store in `/Plans/` (e.g., `Continuous-Improvement-Plan.md`).
2. Include:

   * Applicable standards & regulations
   * Organization-wide quality objectives (linked issue numbers)
   * Metrics & assurance activities
   * Key milestones or initiatives

#### 5.3.2 Project-Level Plans

1. Store in `/Project-Docs/`.
2. Include design/development planning details, linked objectives, and relevant milestones.
3. Reference evidence sources (issues, pull requests, test logs, CI/CD artifacts).

---

### **5.4 Issues**

1. For each deliverable, create a **GitHub Issue** using the template:

   * **Title:** Descriptive name (e.g., “Draft Design Control SOP”).
   * **Description:** Summary, objectives, acceptance criteria.
   * **Checklist:** Sub-tasks.
   * **Labels:** `SOP`, `WI`, `CAPA`, etc.
   * **Assignee:** Responsible owner.
2. Link issues to relevant **milestones** and **plans** via URLs.
3. Update issue status as progress occurs; close when acceptance criteria are met.

---

### **5.5 Milestones**

1. Navigate to **Issues → Milestones → New Milestone**.
2. Define:

   * Title (e.g., “QMS Foundations”)
   * Purpose and scope (list issues/deliverables)
   * Goals and acceptance criteria
   * Links to quality plans or objectives
   * Due date (if applicable)
3. Link milestone pages within related quality plans.
4. **Closure:**

   * Confirm all associated issues are closed.
   * Verify acceptance criteria met (Quality Manager approval).
   * Document closure summary in the linked plan.

---

### **5.6 Project Boards**

1. Create a **Project Board** under **Projects → New Project (Kanban template)**.
2. Name example: “Red Witch QMS Board”.
3. Columns: *Backlog*, *In Progress*, *Review*, *Done*.
4. Add issues via **Projects → Add to Project**.
5. **Ownership & Review:**

   * Process Owners update issue status weekly.
   * Quality Manager reviews board status monthly.
   * Key summaries included in management review inputs.

---

### **5.7 Approval & Change Control**

1. All plans, updates, and controlled documents must be approved via **Pull Request (PR)**.
2. At least one reviewer must be the **Quality Manager** or designated compliance owner.
3. PR history serves as formal evidence of approval and change control.
4. Significant QMS changes (new process, policy revision, resource change) must be documented as GitHub Issues labeled `Change`, linked to the PR, and reviewed for effectiveness.

---

### **5.8 Monitoring & Review**

* Review all open milestones, issues, and plans **at least annually** and during **Management Review**.
* Update plans and boards based on outcomes, audits, and improvement activities.
* Document results in plan update history and management review records.

---

## **6. Documentation & Records**

| Record Type                 | Storage Location             | Control / Retention                                     |
| --------------------------- | ---------------------------- | ------------------------------------------------------- |
| Org-Level Quality Plans     | `/Plans/` (Wiki)             | Retained indefinitely; PR approval required for changes |
| Project-Specific Plans      | `/Project-Docs/`             | Retained indefinitely; PR approval required for changes |
| Risk & Opportunity Issues   | `QMS-Risks` repo             | Controlled via issue history                            |
| Quality Objectives          | `QMS-Objectives` repo        | Controlled via issue history                            |
| Change Records              | `QMS-Changes` repo           | Controlled via issue and PR linkage                     |
| Project Boards & Milestones | GitHub Projects / Milestones | Archived electronically; referenced in plans            |
| Pull Requests & Logs        | GitHub Repository History    | Permanent digital record of review and approval         |

Only authorized contributors may modify QMS records.
Access permissions and repository settings are maintained by the Quality Manager.

---

## **7. References**

* **QMS-SOP-05 Leadership**
* **QMS-SOP-06 Quality Planning**
* **ISO 9001:2015**, Clauses 5 & 6

---
