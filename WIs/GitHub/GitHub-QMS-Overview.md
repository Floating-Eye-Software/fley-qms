# **REF - Red Witch QMS Base System Vision**

**Slug:** GitHub-QMS-Overview  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-QMS-Overview  

---

## 1  Purpose

*Draft for Milestone 1 (QMS Foundations)*

The Red Witch Quality Management System (QMS) establishes a lightweight, fully traceable, and continuously improving framework for managing software quality and compliance using **GitHub as the system of record**.

This “Base System” defines the minimum viable configuration required to:

* Control documentation through Git version history
* Standardize authoring with shared templates
* Drive process consistency via SOPs and Work Instructions (WIs)
* Track effectiveness and improvements through integrated GitHub workflows

---

## 2  System Design Principles

| Principle                           | Description                                                                                                                                                    |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Git = Source of Truth**           | All documents, templates, and records reside in version-controlled repositories. Traceability is intrinsic in commits and pull requests, not separate headers. |
| **Templates Drive Standardization** | Every SOP, WI, and Plan uses a shared Markdown template with common metadata fields (purpose, scope, roles, etc.).                                             |
| **Automation over Administration**  | GitHub automation (issue templates, PR workflows, labels) replaces manual tracking where possible.                                                             |
| **Evidence by Doing**               | Compliance evidence arises naturally from GitHub activity — issues, PRs, and comments — rather than from standalone logs.                                      |
| **Continuous Improvement**          | The QMS evolves through its own process: updates are proposed via PRs, reviewed, and merged under Change Control.                                              |

---

## 3  Repository Structure

| Folder          | Purpose                                                                        |
| --------------- | ------------------------------------------------------------------------------ |
| `QMS/`          | Core governance docs – Quality Manual, Policy, Process Map, Context, Org Chart |
| `SOPs/`         | Standard Operating Procedures defining *what* to do                            |
| `WIs/`          | Work Instructions defining *how* to do it (tool-specific)                      |
| `Templates/`    | Markdown templates for SOPs, WIs, Plans, Design Docs                           |
| `Plans/`        | Quality plans and continuous-improvement artifacts                             |
| `Compliance/`   | Standards and regulatory mappings                                              |
| `Project-Docs/` | Red Witch project-specific materials (requirements, risks, PMS, etc.)          |

---

## 4  Process Control Model

| Function                   | Mechanism                                      | Reference                                     |
| -------------------------- | ---------------------------------------------- | --------------------------------------------- |
| **Document Control**       | Git history + PR review under Change Control   | `WIs/GitHub/GitHub-Document-Control.md`                  |
| **Version Control**        | Git branching model                            | `WIs/GitHub/GitHub-Version-Control.md`        |
| **Change Requests**        | GitHub Issues + Pull Requests                  | `WIs/GitHub/GitHub-Change-Control.md`         |
| **Continuous Improvement** | CONTRIBUTING.md workflow + To-do tracking      | `WIs/GitHub/GitHub-Continuous-Improvement.md` |
| **Effectiveness Checks**   | Periodic review in Continuous Improvement Plan | `Plans/Continuous-Improvement-Plan.md`        |

---

## 5  Traceability and Evidence

* **No manual metadata headers** — control derives from:

  * Commit history (author, timestamp, hash)
  * Branch + PR workflow (review/approval)
  * Issue references (linking to QMS or compliance items)

* **Cross-links** maintain functional traceability:
  SOP → WI → Template → Compliance mapping.

---

## 6  Effectiveness & Improvement Loop

| Step                  | Mechanism                              | Evidence                   |
| --------------------- | -------------------------------------- | -------------------------- |
| Identify improvement  | GitHub Issue or To-Do item             | Issue log                  |
| Implement change      | PR referencing issue                   | Commit + PR                |
| Review / Approve      | Change Control SOP                     | Review comments            |
| Measure effectiveness | Metrics in Continuous Improvement Plan | Plan updates               |
| Record & Close        | Close issue and reference commit       | Closed issue + commit hash |

---

## 7  Definition of a “Working Base System”

The QMS is **functionally working** when:

1. All SOPs and WIs use the standard templates
2. Issue templates exist for Change Requests, Improvements, and SOP/WI updates
3. The Continuous Improvement Plan and CONTRIBUTING.md document the full feedback loop
4. Wiki navigation supports easy discovery (sidebar optional)
5. Evidence of change control and improvement is visible in Git history

Once these conditions are met, the system is **self-sustaining** — new SOPs or compliance modules can be added incrementally.

---

## 8  Milestone Alignment – Next Steps

| Priority | Task                                                                      | Source      |
| -------- | ------------------------------------------------------------------------- | ----------- |
| 🔧       | Create GitHub issue templates                                             | Milestone 1 |
| 🧩       | Update SOPs/WIs to use templates                                          | Milestone 1 |
| 📘       | Finalize CONTRIBUTING.md & Continuous Improvement WI                      | Milestone 1 |
| 💬       | Document “special files” rationale (Home.md)                              | Milestone 1 |
| ⚙️       | Evaluate removal of redundant metadata headers                            | Milestone 1 |
| 🧠       | After stabilization → expand compliance coverage (IEC 81001, 62366, etc.) | Later       |
