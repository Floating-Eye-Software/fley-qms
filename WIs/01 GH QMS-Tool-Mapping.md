That’s actually a great setup — GitHub gives you a lightweight, auditable framework that maps nicely to regulatory expectations if you structure it carefully. Let me show you how you can align your **GitHub workflow (issues, milestones, projects, wiki)** with **21 CFR 820** and **ISO 13485** for **quality planning** and **design planning**.

---

## 🔗 Mapping GitHub Tools to QMS Expectations

### **1. Quality Planning (Org-Level)**

**Regulatory anchors:**

* 21 CFR 820.20(d) – Quality Planning
* ISO 13485:2016, Clause 5.4.2 – QMS Planning

**GitHub implementation:**

* **Milestones** = high-level quality plans (e.g., “QMS Foundations,” “Audit-Ready QMS”).
* **Issues** = specific quality activities (e.g., draft SOP, run ISO 9004 self-assessment).
* **Project Board (Kanban)** = tracking of quality initiatives from *To Do → In Progress → Done*.
* **Wiki** = houses the approved Quality Planning SOP and Quality Plan templates.

---

### **2. Design & Development Planning (Project-Level)**

**Regulatory anchors:**

* 21 CFR 820.30(b) – Design and Development Planning
* ISO 13485:2016, Clause 7.3.2 – Design and Development Planning

**GitHub implementation:**

* **Project Board (Kanban)** = your “design plan in action.” Each column represents lifecycle stages (Planning → Design → Verification → Validation → Transfer).
* **Issues** = individual design tasks, linked to requirements, verification, or risk controls.
* **Milestones** = design control phases (e.g., “Phase 1 Design Review,” “Validation Complete”).
* **Linked Issues** = traceability (requirements ↔ design tasks ↔ test cases).
* **Wiki** =

  * SOPs (Design Control SOP, Test SOP).
  * Work Instructions (how to run reviews, how to execute regression suite).
  * Templates (Design Input Form, Verification Record).

---

### **3. Records & Evidence**

**Regulatory anchors:**

* 21 CFR 820.30(j) – Design History File
* ISO 13485:2016, Clause 7.3.10 – Design and Development File

**GitHub implementation:**

* **Closed issues** = objective evidence of completed tasks.
* **Pull Requests (PRs)** = design outputs & review evidence.
* **CI/CD logs** = automated test evidence (verification).
* **Wiki pages** = central document control (SOPs, approved plans, design review minutes).
* **Tags/Releases** = record of baselined versions.

Together, your GitHub repo + wiki essentially functions as the **Design History File (DHF)** and **Quality Records repository**.

---

### **4. Continuous Improvement**

**Regulatory anchors:**

* 21 CFR 820.100 – Corrective and Preventive Action (CAPA)
* ISO 13485:2016, Clause 8.5 – Improvement

**GitHub implementation:**

* **Issues labeled “CAPA”** = track nonconformities, audit findings, complaints.
* **Milestones** = group CAPA actions into improvement cycles.
* **Wiki** = CAPA SOP and logs.
* **Project Board** = improvement pipeline, so nothing falls through the cracks.

---

## ✅ Benefits of This Mapping

* **Traceability**: GitHub issue linking gives a requirements–design–test chain.
* **Audit Readiness**: GitHub history (commits, PRs, issue closure) provides timestamps, accountability, and approvals.
* **Simplicity**: Developers don’t have to learn a parallel QMS tool — the QMS *lives where the work is already happening*.
* **Scalability**: Same workflow can support both *organization-level* planning and *project-level* design control.

---

👉 Next step could be: I draft a **“GitHub as QMS Infrastructure” appendix** for your **Quality Planning SOP**, showing auditors how your GitHub setup meets regulatory expectations. Would you like me to prepare that as a reusable SOP section?

Perfect — a **Document Location Matrix (DLM)** is a simple table auditors love because it clearly shows **where each type of document lives, how it’s controlled, and where the evidence of execution is**. Here’s a draft you can use in your Document Control SOP or Wiki README:

---

# **Document Location Matrix – Red Witch / FLEY QMS**

| **Document Type**             | **Location**                  | **Control / Approval Method**                     | **Evidence / Execution Trace**                        | **Notes**                                   |
| ----------------------------- | ----------------------------- | ------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------- |
| SOPs (all types)              | `redwitch.wiki/SOPs/`         | PR review workflow; Quality Manager approval      | PR review comments, merged wiki history               | Controlled documents                        |
| Work Instructions (WIs)       | `redwitch.wiki/WIs/`          | PR review workflow; Quality Manager approval      | PR review comments, merged wiki history               | Task-level guidance                         |
| Quality Plans (org-level)     | `redwitch.wiki/Plans/`        | PR review workflow; Quality Manager approval      | Milestones, linked Issues, CAPA records               | Pilot SOP Plan, Continuous Improvement Plan |
| Quality Plans (project-level) | `redwitch.wiki/Plans/`        | PR review workflow; Project Manager + QM approval | Milestones, linked Issues, CI/CD test reports         | Red Witch project plan                      |
| Templates                     | `redwitch.wiki/Templates/`    | PR review workflow; Quality Manager approval      | PR review comments, merged wiki history               | SOP / WI / Plan templates                   |
| Project Requirements          | `redwitch.wiki/Project-Docs/` | PR review workflow; Project Manager approval      | Linked Issues, traceability matrix                    | Specific to Red Witch project               |
| Design / Architecture Docs    | `redwitch.wiki/Project-Docs/` | PR review workflow; Project Manager approval      | Linked Issues, design review PRs                      | Red Witch-specific                          |
| Risk Analysis / Hazard Logs   | `redwitch.wiki/Project-Docs/` | PR review workflow; Project Manager approval      | Linked Issues, mitigation evidence                    | Risk logs for Red Witch project             |
| Verification / Test Protocols | `redwitch.wiki/Project-Docs/` | PR review workflow; QA review                     | CI/CD test reports, linked PRs                        | May link to repo for automated outputs      |
| Traceability Matrices         | `redwitch.wiki/Project-Docs/` | PR review workflow; QA review                     | Linked Issues, PR references                          | Requirements → code → test mapping          |
| CAPA / Audit Registers        | `redwitch.wiki/Records/`      | PR review workflow; Quality Manager approval      | Linked Issues labeled CAPA / Audit                    | Organization-wide improvement               |
| Training Records              | `redwitch.wiki/Records/`      | PR review workflow; Quality Manager approval      | Attendance logs, completion evidence linked to issues | Employee training evidence                  |
| CI/CD Build Artifacts & Logs  | `redwitch/` repo              | Automated / versioned in pipeline                 | CI/CD system logs, GitHub Actions outputs             | Evidence only, not controlled doc           |
| Automated Test Reports        | `redwitch/` repo              | Automated / versioned in pipeline                 | CI/CD test reports, coverage reports                  | Evidence only, linked from wiki             |

---

### ✅ Notes / Guidelines

1. **All controlled documentation** (SOPs, WIs, Plans, Templates, Project Docs, Records) lives exclusively in the **wiki**.
2. **Repo contains only generated evidence** — build artifacts, automated test outputs, CI/CD logs.
3. Every wiki page should include a **Linkage to Execution** section pointing to relevant milestones, project boards, or issues.
4. PRs provide a full **approval and change history** for all wiki documents.
5. Links from wiki → repo evidence ensure traceability: auditors can follow SOP → plan → issue → CI/CD output.
6. Use consistent naming conventions for folders, files, milestones, and labels to make navigation and audits easier.

---

If you want, I can **also add a “Quick Reference” visual table that maps wiki folders → GitHub boards → milestones → evidence**, so your team can see at a glance exactly where to look and where to record everything. This often works really well as a 1-page cheat sheet for auditors and developers.

Do you want me to make that visual cheat sheet next?



Perfect — a **visual cheat sheet** gives developers and auditors a **one-glance map** of where documents live, how they’re controlled, and where the evidence is. You can include this in the **Wiki README** or as a PDF reference.

Here’s a draft **Visual Document-Evidence Map** for Red Witch / FLEY QMS:

---

# **Red Witch / FLEY QMS – Document & Evidence Cheat Sheet**

```
┌───────────────────────────────┬───────────────────────────────┬───────────────────────────────┐
│        Document Type           │        Wiki Folder             │       Evidence / Repo         │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ SOPs                           │ /SOPs/                        │ PR review comments, merged wiki history │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Work Instructions (WIs)        │ /WIs/                         │ PR review comments, merged wiki history │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Quality Plans (Org-level)      │ /Plans/                       │ Milestones, linked Issues, CAPA logs │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Quality Plans (Project-level)  │ /Plans/                       │ Milestones, linked Issues, CI/CD test reports │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Templates                      │ /Templates/                   │ PR review comments, merged wiki history │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Project Requirements           │ /Project-Docs/Requirements.md │ Linked Issues, traceability matrix │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Design / Architecture Docs     │ /Project-Docs/Design.md       │ Linked Issues, design review PRs │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Risk Analysis / Hazard Logs    │ /Project-Docs/Risk-Analysis.md│ Linked Issues, mitigation evidence │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Verification / Test Protocols  │ /Project-Docs/Verification.md │ CI/CD test reports, linked PRs │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Traceability Matrices          │ /Project-Docs/Traceability.md │ Linked Issues, PR references │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ CAPA / Audit Registers         │ /Records/                     │ Linked Issues labeled CAPA / Audit │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Training Records               │ /Records/                     │ Attendance logs, evidence linked to issues │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ CI/CD Build Artifacts & Logs   │ repo/build/, repo/logs/       │ GitHub Actions logs, pipeline outputs │
├───────────────────────────────┼───────────────────────────────┼───────────────────────────────┤
│ Automated Test Reports         │ repo/test-results/            │ CI/CD test outputs, coverage reports │
└───────────────────────────────┴───────────────────────────────┴───────────────────────────────┘
```

---

### **How to Use This Cheat Sheet**

1. **Developers:**

   * Know exactly where to find SOPs, work instructions, and project requirements in the wiki.
   * Know where to store or reference automated test results or build logs in the repo.

2. **Auditors:**

   * Trace a controlled document → execution milestone → evidence quickly.
   * Links in wiki pages take them directly to the corresponding milestone, board, or issue.

3. **Project Managers / QA:**

   * Ensure that every issue, PR, and milestone is linked back to a wiki document.
   * Use the table to verify **completeness** and **traceability** during internal audits.

---

If you want, I can also **make a “graphical version”** of this cheat sheet using **boxes and arrows** showing flow from **Wiki → Milestones → Project Board → Issues/PRs → CI/CD outputs**. This works really well for onboarding new team members and for auditors.

Do you want me to create that graphical flow diagram next?
