# **Work Instruction – GitHub QMS Operations (FLEY)**

**WI Number:** WI-GIT-QMS-001  
**Related SOPs:** SOP-DOC-001 – Document Control, SOP-Quality-Planning  
**Effective Date:** ____  
**Owner:** Quality Manager  
**Review Cycle:** Annual  

---

## **1. Purpose**

This Work Instruction defines how Floating Eye Software (FLEY) uses **GitHub as the operational backbone of the QMS**, integrating:

* Document control (SOPs, WIs, Quality Plans, Templates)
* Quality planning (milestones, objectives, KPIs)
* Project management (project boards, issues, tasks)
* Change control (PR-based approval workflow)
* CAPA and risk management (linked Issues, records)
* Continuous improvement (ISO 9004 self-assessment, GDPR compliance)

It ensures compliance with:

* 21 CFR 820.20(d), 820.30, 820.40, 820.180  
* ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 5.4, 7.1, 7.3.10, 8.5  

---

## **2. Scope**

Applies to all FLEY controlled documentation and project execution activities, including organization-level and Red Witch project-level plans.

---

## **3. Responsibilities**

| Role                             | Responsibility |
| -------------------------------- | -------------- |
| **Document Owner**               | Draft, maintain, propose updates to controlled documents |
| **Quality Manager / QMS Owner**  | Review and approve controlled documents; verify process compliance |
| **Project Manager**              | Maintain project boards, link milestones/issues to documentation; ensure tasks follow WI |
| **Developers / Team Members**    | Reference controlled documents in Issues/PRs; complete tasks; provide execution evidence |
| **Privacy / Compliance Officer** | Ensure GDPR and regulatory content is current and referenced correctly |

---

## **4. GitHub Framework as a QMS Implementation Tool**

| QMS Requirement        | GitHub Implementation |
| ---------------------- | ------------------- |
| Document Control       | Wiki pages for SOPs, WIs, Plans, Templates; PR review workflow; revision history; Linkage to Execution |
| Quality Planning       | Plans in wiki, linked to milestones, project boards, and issues; measurable objectives tracked via GitHub metrics |
| Project Management     | Project Boards (Kanban), Milestones, and Issues to track tasks, responsibilities, timelines, and progress |
| Change Control         | PRs + linked Issues + Milestones act as a controlled process for proposing, reviewing, approving, and implementing changes |
| Risk Management        | Project-Docs (Risk Analysis, Hazard Logs) linked to Issues, traceable to design decisions |
| CAPA                   | Issues labeled CAPA, linked to Records wiki pages; closed with evidence and follow-up linked to SOP/WI |
| Continuous Improvement | ISO 9004 self-assessment plan and GDPR compliance linked to Milestones, Boards, Issues |
| Training & Competency  | Wiki pages with procedures; training records as Issues linked to participants and completion evidence |

---

## **5. Advantages of the GitHub QMS Framework**

1. **Single source of truth** – all controlled docs, plans, and project execution evidence live in wiki + repo evidence.  
2. **Full traceability** – SOP → plan → milestone → task → execution → evidence (CI/CD, test reports, audit logs).  
3. **Audit-ready by design** – automatic versioning, PR approval history, and issue tracking.  
4. **Process unification** – all QMS elements (change control, document control, planning, CAPA, risk) use the same workflow.  
5. **Continuous improvement** – measurable objectives and improvement actions tracked as Issues linked to SOPs, Plans, and CAPA.

---

## **6. Key Concepts**

1. **Controlled Documents** – SOPs, WIs, Plans, Templates, Project Docs, Records; stored in wiki folders with PR approval.  
2. **Execution Evidence** – GitHub Issues, Milestones, Project Boards, CI/CD logs, test reports.  
3. **Traceability** – Link every document → milestone → issue → execution → evidence.  
4. **Change Control** – Implemented via PR + Issue workflow; each revision tracked and approved.  
5. **Continuous Improvement** – ISO 9004 self-assessment, CAPA, and audit findings tracked as Issues linked to relevant docs.

---

## **7. Step-by-Step Instructions**

### **7.1 Creating / Drafting a Controlled Document**

1. Select the appropriate **template** from `/Templates/` (SOP, WI, Quality Plan).  
2. Create a new wiki page in the correct folder:

   * SOPs → `/SOPs/`  
   * WIs → `/WIs/`  
   * Quality Plans → `/Plans/`  
   * Project Docs → `/Project-Docs/`  
   * Records → `/Records/`  

3. Assign a **Document Owner** and add a **Revision History** table.  
4. Include an empty **Linkage to Execution** section to link evidence, milestones, and issues.

---

### **7.2 PR-Based Review and Approval**

1. Submit wiki changes as a **Pull Request (PR)**.  
2. Include in PR description:

   * Document purpose, scope, and type.  
   * Related milestones, project boards, and issues.  

3. Assign reviewers:

   * SOP/WI/Plan → Quality Manager  
   * Project Docs → Project Manager (+ QM if impacting QMS)  

4. Merge PR after approval → merged wiki page becomes **controlled**.

---

### **7.3 Planning & Milestones**

1. Each Quality Plan must reference **GitHub Milestones**.  
2. Milestone naming examples:

   * `QMS Foundations` – organization-level setup  
   * `Audit-Ready QMS Documentation` – readiness for audits  
   * `Red Witch Phase 1 Design Review` – project-specific  

3. Update the “Linkage to Execution” section to include milestone references:

```markdown
## Linkage to Execution
- Milestones: [QMS Foundations](https://github.com/<org>/<repo>/milestone/1)
- Project Board: [Red Witch Kanban](https://github.com/<org>/<repo>/projects/1)
- Issues: [#42 Draft Design Control SOP](https://github.com/<org>/<repo>/issues/42)
````

---

### **7.4 Project Management (Issues & Boards)**

1. Create **Issues** for all tasks related to planning, design, verification, CAPA, audits, and training.
2. Assign labels consistently: `SOP`, `WI`, `Plan`, `CAPA`, `Audit`, `Project`.
3. Use **Project Boards** (Kanban) to visualize task progress:

   * Columns: To Do → In Progress → Review → Done
   * Link issues to the board and governing wiki page.

---

### **7.5 Change Control**

1. Propose a change via a **new PR** or linked Issue.
2. Include all affected documents and tasks.
3. PR review constitutes **formal approval**.
4. Merge PR to implement changes; revision history updates automatically.

---

### **7.6 CAPA & Risk Management**

1. Log CAPA or risk tasks as **Issues**.
2. Link to governing SOP/WI/Plan.
3. Track progress via Project Board.
4. Close Issues only after attaching evidence (PRs, CI/CD reports, test results).

---

### **7.7 Verification / Evidence Linking**

1. Link CI/CD artifacts, test reports, or audit logs from the **repo** to the relevant wiki document or Issue.
2. Ensure each wiki page’s **Linkage to Execution** section reflects all evidence.
3. Maintain full **traceability**: Document → Milestone → Issue → Execution → Evidence.

---

### **7.8 Document Revision / Retirement**

1. Update revision table on every change.
2. Mark obsolete pages with `Obsolete` in the title.
3. Retired documents remain in **GitHub wiki history** for traceability.
4. Update dependent links to point to current active documents.

---

## **8. Document Location Matrix**

| Document Type                  | Location             | Control / Approval Method | Evidence / Execution Trace           | Notes                             |
| ------------------------------ | -------------------- | ------------------------- | ------------------------------------ | --------------------------------- |
| SOPs / WIs / Plans / Templates | `wiki/<folder>`      | PR review; QM approval    | PR comments, merged wiki history     | Controlled documents              |
| Project Docs                   | `wiki/Project-Docs/` | PR review; PM approval    | Linked Issues, design review PRs     | Project-specific                  |
| Risk Analysis / Hazard Logs    | `wiki/Project-Docs/` | PR review; PM approval    | Linked Issues, mitigation evidence   | Project-specific                  |
| Verification / Test Protocols  | `wiki/Project-Docs/` | PR review; QA review      | CI/CD test reports, linked PRs       | Evidence linked from repo         |
| Traceability Matrices          | `wiki/Project-Docs/` | PR review; QA review      | Linked Issues, PR references         | Req → code → test mapping         |
| CAPA / Audit Registers         | `wiki/Records/`      | PR review; QM approval    | Linked Issues labeled CAPA/Audit     | Organization-wide improvement     |
| Training Records               | `wiki/Records/`      | PR review; QM approval    | Attendance logs linked to issues     | Employee training evidence        |
| CI/CD Build Artifacts & Logs   | repo                 | Automated / versioned     | CI/CD system logs                    | Evidence only, not controlled doc |
| Automated Test Reports         | repo                 | Automated / versioned     | CI/CD test reports, coverage reports | Evidence only, linked from wiki   |

---

## **9. Records**

* Controlled wiki pages
* PR review history
* GitHub Issues & Milestones
* Project Boards
* CI/CD artifacts & test reports
* CAPA / audit records linked in wiki

---

## **10. References**

* SOP-DOC-001 – Document Control
* SOP-Quality-Planning
* WI-Project Management
* 21 CFR 820.20(d), 820.30, 820.40, 820.180
* ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 5.4, 7.1, 7.3.10, 8.5
* ISO 9004 – Continuous Improvement

---

## **11. Appendix A – Example Linkage to Execution Table**

| Document                 | Milestone                       | Project Board                | Issue / Evidence                      |
| ------------------------ | ------------------------------- | ---------------------------- | ------------------------------------- |
| Red Witch Quality Plan   | Red Witch Phase 1 Design Review | Red Witch Kanban             | #42 Draft Design Control SOP          |
| ISO 9004 Self-Assessment | QMS Foundations                 | Continuous Improvement Board | #56 Complete ISO 9004 Self-Assessment |
