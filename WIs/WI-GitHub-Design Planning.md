# **Work Instruction (WI) – Using GitHub for QMS Project Management**

**WI Number:** WI-PRJ-001
**Related SOP:** SOP-Quality-Planning
**Effective Date:** ____
**Owner:** Quality Manager
**Review Cycle:** Annual

---

## **1. Purpose**

This Work Instruction defines how GitHub tools (Issues, Milestones, Projects, Wiki, and Pull Requests) are used to meet project management requirements of **21 CFR 820.20(d), 820.30(b), and ISO 13485:2016 Clauses 5.4, 7.1, and 7.3**.

---

## **2. Scope**

Applies to all Floating Eye Software (FLEY) projects, including the Red Witch pilot project, and to organization-level QMS planning and continuous improvement activities.

---

## **3. Responsibilities**

* **Quality Manager:** Ensures this WI is followed, reviews records for completeness.
* **Project Manager:** Creates milestones, boards, and ensures issues are linked to quality plans.
* **Developers/Contributors:** Log work as issues, update boards, and reference wiki documentation.

---

## **4. Instructions**

### 4.1 Create and Manage **Wiki Pages**

1. For each new **SOP, Plan, or Template**, create a page in the repository Wiki under the correct folder (`/SOPs`, `/Plans`, `/Templates`).
2. At the end of each Wiki page, include a **“Linkage to Execution”** section with links to relevant Milestones, Project Boards, and Issues.

   ```markdown
   ## Linkage to Execution
   - [QMS Foundations Milestone](https://github.com/<org>/<repo>/milestone/1)
   - [Red Witch Project Board](https://github.com/<org>/<repo>/projects/1)
   - [Open Issues](https://github.com/<org>/<repo>/issues?q=is%3Aopen+label%3AQMS)
   ```

---

### 4.2 Use **Milestones** for Planning

1. Each **Quality Plan** (org-level or project-level) must have at least one corresponding GitHub Milestone.
2. Milestone naming convention:

   * `QMS Foundations` (organization-level setup)
   * `Audit-Ready QMS` (compliance readiness)
   * `Red Witch Phase 1 Design Review` (project-specific)
3. Link milestones in both:

   * The **Wiki plan page** (see 4.1).
   * The **Milestone description**, referencing the governing Wiki plan.

---

### 4.3 Use **Project Boards (Kanban)** for Tracking

1. Create a **Project Board** for each active Quality Plan or major project.
2. Standard columns:

   * **To Do** – open issues/tasks.
   * **In Progress** – tasks being actively worked.
   * **Review** – tasks pending verification, review, or approval.
   * **Done** – completed tasks (linked to evidence).
3. Add link to the governing Wiki plan in the **Project Board description**.
4. Add relevant Issues to the board when created (see 4.4).

---

### 4.4 Use **Issues** for Tasks and Evidence

1. Every QMS task (SOP drafting, audit, review, release testing) must be tracked as a GitHub Issue.
2. Issue body should reference:

   * Governing Wiki Plan (e.g., `[Red Witch Quality Plan]`)
   * Related SOP or WI
   * Acceptance criteria (what evidence is required)
3. Label Issues consistently:

   * `SOP` – drafting or updating SOPs
   * `Audit` – audits, assessments, reviews
   * `CAPA` – corrective or preventive actions
   * `Project` – project-specific design/development tasks
4. Close Issues only when evidence is attached (link to PR, CI/CD report, audit log, etc.).

---

### 4.5 Use **Pull Requests (PRs)** for Review and Approval

1. Any change to controlled documentation (SOPs, Plans, WIs) in the Wiki or repo must go through a PR.
2. At least one reviewer (Quality Manager or delegate) must approve before merging.
3. PR comments serve as the official **review record**.

---

### 4.6 Maintain **Traceability**

1. Link **Requirements → Design → Code → Test Evidence** using GitHub issue linking (`blocks`, `is blocked by`, or manual references).
2. Each closed issue must reference its upstream requirement and downstream verification evidence.
3. Wiki pages must show which Milestones/Issues provide evidence of execution.

---

## **5. Records**

* **Wiki Pages** – governing documents (SOPs, Plans, Templates).
* **Milestones** – planning checkpoints.
* **Project Boards** – visual tracking of progress.
* **Issues** – task records and evidence of execution.
* **Pull Requests** – review and approval records.
* **Releases/Tags** – baselined versions of deliverables.

Retention: All GitHub records are permanent unless archived under the Document Control SOP.

---

## **6. References**

* 21 CFR 820.20(d) – Quality Planning
* 21 CFR 820.30(b) – Design and Development Planning
* ISO 13485:2016 – Clauses 5.4, 7.1, 7.3, 8.5
* ISO 9004 – Continuous Improvement
* SOP-Quality-Planning
