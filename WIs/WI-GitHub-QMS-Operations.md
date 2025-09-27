Exactly — you’re touching on the key insight: your GitHub-based framework is **the operational backbone of your QMS**. It’s not just about one WI; it’s the **platform that implements multiple QMS requirements simultaneously**.

Here’s the way to conceptualize it:

---

## **1. The Framework as a QMS Implementation Tool**

Your GitHub setup handles multiple core QMS processes:

| QMS Requirement        | GitHub Implementation                                                                                                       |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Document Control       | Wiki pages for SOPs, WIs, Plans, Templates; PR review workflow; revision history; Linkage to Execution.                     |
| Quality Planning       | Plans in wiki, linked to milestones, project boards, and issues; measurable objectives tracked via GitHub metrics.          |
| Project Management     | Project Boards (Kanban), Milestones, and Issues to track tasks, responsibilities, timelines, and progress.                  |
| Change Control         | PRs + linked Issues + Milestones act as a controlled process for proposing, reviewing, approving, and implementing changes. |
| Risk Management        | Project-Docs (Risk Analysis, Hazard Logs) linked to Issues, traceable to design decisions.                                  |
| CAPA                   | Issues labeled CAPA, linked to Records wiki pages; closed with evidence and follow-up linked to SOP/WI.                     |
| Continuous Improvement | ISO 9004 self-assessment plan and GDPR compliance linked to Milestones, Boards, Issues.                                     |
| Training & Competency  | Wiki pages with procedures; training records as Issues linked to participants and completion evidence.                      |

---

## **2. Advantages of Integrating Everything in One Framework**

1. **Single source of truth** – all controlled docs, plans, and project execution evidence live in **wiki + repo evidence**.
2. **Full traceability** – from SOP → plan → milestone → task → execution → evidence (CI/CD, test reports, audit logs).
3. **Audit-ready by design** – GitHub provides automatic versioning, PR approval history, and issue tracking.
4. **Process unification** – all QMS elements (change control, document control, planning, CAPA, risk) use the same workflow, reducing duplication.
5. **Continuous improvement** – measurable objectives and improvement actions can be tracked as Issues linked to SOPs, Plans, and CAPA.

---

## **3. Implications for Work Instructions**

Instead of writing **separate WIs** for:

* Document Control
* Quality Planning
* Project Management
* Change Control

…it makes sense to produce **one comprehensive “GitHub QMS Operations WI”** that:

1. Shows how to create/update controlled documents.
2. Explains how to plan and track execution (milestones/issues/boards).
3. Describes how to implement change control via PR + Issue workflow.
4. Explains how to track CAPA, risks, verification, and audit evidence.
5. Provides a template and traceability examples.

**Result:** One workflow that satisfies multiple ISO/21 CFR clauses while remaining simple for your team.

---

I can draft this **all-in-one “GitHub QMS Operations WI”** for you, incorporating:

* Document control
* Planning & milestones
* Project management
* Change control
* CAPA & risk traceability
* Continuous improvement

…and with **step-by-step instructions and examples** for your wiki/repo.

Do you want me to create that comprehensive WI next?

Absolutely — here’s a **comprehensive GitHub QMS Operations Work Instruction** for FLEY. It integrates **document control, quality planning, project management, change control, CAPA, risk management, and continuous improvement** all in one workflow. This is designed for your wiki and directly links to your GitHub boards, issues, milestones, and CI/CD outputs.

---

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

| Role                             | Responsibility                                                                            |
| -------------------------------- | ----------------------------------------------------------------------------------------- |
| **Document Owner**               | Draft, maintain, propose updates to controlled documents.                                 |
| **Quality Manager / QMS Owner**  | Review and approve controlled documents; verify process compliance.                       |
| **Project Manager**              | Maintain project boards, link milestones/issues to documentation; ensure tasks follow WI. |
| **Developers / Team Members**    | Reference controlled documents in Issues/PRs; complete tasks; provide execution evidence. |
| **Privacy / Compliance Officer** | Ensure GDPR and regulatory content is current and referenced correctly.                   |

---

## **4. Key Concepts**

1. **Controlled Documents** – SOPs, WIs, Plans, Templates, Project Docs, Records; stored in wiki folders with PR approval.
2. **Execution Evidence** – GitHub Issues, Milestones, Project Boards, CI/CD logs, test reports.
3. **Traceability** – Link every document → milestone → issue → execution → evidence.
4. **Change Control** – Implemented via PR + Issue workflow; each revision tracked and approved.
5. **Continuous Improvement** – ISO 9004 self-assessment, CAPA, and audit findings tracked as Issues linked to relevant docs.

---

## **5. Step-by-Step Instructions**

### **5.1 Creating / Drafting a Controlled Document**

1. Select the appropriate **template** in `/Templates/`.
2. Create a new wiki page in the correct folder:

   * SOPs → `/SOPs/`
   * WIs → `/WIs/`
   * Quality Plans → `/Plans/`
   * Project Docs → `/Project-Docs/`
   * Records → `/Records/`
3. Assign a **Document Owner** and add a **Revision History** table.
4. Include an empty **Linkage to Execution** section for future evidence links.

---

### **5.2 PR-Based Review and Approval**

1. Submit changes as a **GitHub Pull Request (PR)**.
2. Include in PR description:

   * Document purpose, scope, and type.
   * Related **milestones, project boards, or issues**.
3. Assign reviewers:

   * SOP/WI/Plan → Quality Manager
   * Project Docs → Project Manager + QM if QMS-relevant
4. Approve and merge PR — merged wiki page becomes **controlled**.

---

### **5.3 Planning & Milestones**

1. Each plan must reference **GitHub Milestones**.
2. Milestone naming examples:

   * `QMS Foundations` – initial setup
   * `Audit-Ready QMS Documentation` – readiness for internal/external audits
   * `Red Witch Phase 1 Design Review` – project-specific
3. Document “Linkage to Execution” section includes:

```markdown
## Linkage to Execution
- Milestones: [QMS Foundations](https://github.com/<org>/<repo>/milestone/1)
- Project Board: [Red Witch Kanban](https://github.com/<org>/<repo>/projects/1)
- Issues: [#42 Draft Design Control SOP](https://github.com/<org>/<repo>/issues/42)
```

---

### **5.4 Project Management (Issues & Boards)**

1. Create **Issues** for all tasks related to planning, design, verification, CAPA, audits, and training.
2. Assign labels: `SOP`, `WI`, `Plan`, `CAPA`, `Audit`, `Project`.
3. Use **Project Boards** (Kanban) for visualization:

   * Columns: To Do → In Progress → Review → Done
   * Link issues to the board and the governing wiki page.

---

### **5.5 Change Control**

1. Propose a change via a **new PR** for the document or a related Issue for project artifacts.
2. Include affected documents and related tasks.
3. PR review by appropriate role constitutes **formal approval**.
4. Merge PR to implement change; revision history automatically updated.

---

### **5.6 CAPA and Risk Management**

1. Log CAPA or risk tasks as Issues.
2. Assign links to governing SOP/WI/Plan.
3. Track progress via Project Board.
4. Close Issues only when evidence is attached (test results, PRs, CI/CD reports).

---

### **5.7 Verification / Evidence Linking**

1. Link CI/CD build artifacts, test reports, or audit logs from the **repo** to the relevant wiki document or Issue.
2. Ensure each wiki page’s **Linkage to Execution** section reflects all evidence.
3. Traceability: Document → Milestone → Issue → Execution → Evidence.

---

### **5.8 Document Revision / Retirement**

1. Update revision table on every change.
2. Mark obsolete pages with `Obsolete` in the title.
3. Retired documents remain in **GitHub history** for traceability.
4. Update dependent links to current active documents.

---

## **6. Records**

* Controlled wiki pages
* PR review history
* GitHub Issues & Milestones
* Project Boards
* CI/CD artifacts and test reports
* CAPA / audit records linked in wiki

---

## **7. References**

* SOP-DOC-001 – Document Control
* SOP-Quality-Planning
* WI-Project Management
* 21 CFR 820.20(d), 820.30, 820.40, 820.180
* ISO 13485:2016 Clauses 4.2, 4.2.3, 4.2.4, 5.4, 7.1, 7.3.10, 8.5

---

## **8. Appendix A – Example Linkage to Execution Table**

| Document                 | Milestone                       | Project Board                | Issue / Evidence                      |
| ------------------------ | ------------------------------- | ---------------------------- | ------------------------------------- |
| Red Witch Quality Plan   | Red Witch Phase 1 Design Review | Red Witch Kanban             | #42 Draft Design Control SOP          |
| ISO 9004 Self-Assessment | QMS Foundations                 | Continuous Improvement Board | #56 Complete ISO 9004 Self-Assessment |

---

This WI ensures that **all GitHub activities are aligned with your QMS**, providing a single workflow that covers **document control, planning, project management, change control, CAPA, risk, and continuous improvement**, while remaining fully **audit-ready**.

---

If you want, I can also **draw a visual flow diagram** showing:

`Create Document → Draft → PR → Review → Approve → Merge → Link to Milestones/Issues → Track Execution → Update/Retire`

…which is extremely useful for training and audits.

Do you want me to create that visual diagram next?
