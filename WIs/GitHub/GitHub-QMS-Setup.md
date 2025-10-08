# **Work Instruction: GitHub QMS Setup**

**Document No.:** WI-QMS-10-02
**Title:** GitHub QMS Setup – Single FLEY QMS Board
**Revision:** 2.0
**Effective Date:** [Insert Date]
**Approved By:** [Top Management]

---

## **1. Purpose**

To define the GitHub configuration for implementing the FLEY Quality Management System (QMS) pilot, including QMS authoring and operations, using a **single Kanban board** named **“FLEY QMS”**.

This setup ensures:

* QMS authoring (SOPs, WIs) is traceable and auditable.
* QMS operations (risks, CAPA, management review, objectives) are tracked consistently.
* Evidence of QMS implementation is captured digitally and linked to relevant Issues.

---

## **2. Scope**

This work instruction applies to all QMS activities performed in GitHub for the FLEY pilot project, including:

* SOP/WI authoring and review
* Risk & opportunity management
* CAPA and continual improvement
* Management review
* Quality objectives tracking

It covers the **single FLEY QMS Kanban board** in the `redwitch.wiki` repository.

---

## **3. Responsibilities**

| Role                                    | Responsibility                                                                             |
| --------------------------------------- | ------------------------------------------------------------------------------------------ |
| **Top Management**                      | Approves GitHub QMS setup and ensures resources are available.                             |
| **Quality Manager / QMS Administrator** | Maintains the board, labels, repository structure, and ensures issues are properly linked. |
| **Process Owners / Contributors**       | Create, manage, and link Issues for SOPs/WIs, QMS operations, and CAPA.                    |
| **All Contributors**                    | Follow labeling, linking, and workflow procedures on the board.                            |

---

## **4. Repository and Board Setup**

### **4.1 Repository Structure**

All QMS documentation lives in the **`redwitch.wiki`** repository. Recommended structure:

```
QMS/            → Quality Manual, process map, org chart, context, risk register
SOPs/           → Standard Operating Procedures
Plans/          → Continuous Improvement Plan, QMS pilot plans
Project-Docs/   → Red Witch product-specific documentation (requirements, roadmap, architecture)
WIs/            → Work instructions (tool-specific or framework-specific)
Templates/      → SOP/WI/plan templates
```

### **4.2 Kanban Board: FLEY QMS**

**Purpose:** Track **all QMS authoring and operational activities** during the pilot phase.

**Columns:**

```
Backlog → Drafting → Review / Approval → Active → Validated / Closed
```

**Types of Issues to Track:**

| Category           | Example Labels                                                                          |
| ------------------ | --------------------------------------------------------------------------------------- |
| QMS Authoring      | `SOP`, `WI`, `Authoring`                                                                |
| QMS Operations     | `Risk`, `Opportunity`, `CAPA`, `Improvement`, `Management Review`, `Objective`, `Audit` |
| Validation / Pilot | `Validation`, `Pilot`                                                                   |

**Notes:**

* SOP/WI authoring issues remain on this board until validated.
* QMS operational issues (risks, CAPA, objectives) are added as new Issues on the same board.
* Use labels to filter and organize the board by type or workflow stage.

---

## **5. Issue Lifecycle and Workflow**

### **5.1 QMS Authoring**

1. Create Issue for SOP/WI → label as `SOP` or `WI`.
2. Draft document in Wiki or `/SOPs` folder.
3. Move Issue to `Review / Approval` → PR or Wiki review; record approval in comments.
4. Apply SOP/WI in pilot (Red Witch or future projects).
5. Link validation results in Issue comments.
6. Move Issue to `Validated / Closed` when evidence is complete.

### **5.2 QMS Operations**

1. Create Issue for risk, opportunity, CAPA, or objective.
2. Assign responsible owner, due date, and relevant labels.
3. Track progress through the same columns (`Backlog → Drafting → Review / Approval → Active → Validated / Closed`).
4. Link related authoring Issues if actions depend on a SOP/WI.
5. Close Issues when actions are complete and evidence documented.

---

## **6. Linking with Product Repos**

* **Red Witch** product repo remains separate for future development.
* Validation and pilot evidence in Red Witch should be referenced in FLEY QMS Issues via Issue links.
* Cross-repo links maintain traceability of SOP/WI implementation and CAPA actions.

---

## **7. Record Retention**

* All closed Issues, PR comments, and board history serve as QMS records.
* Periodically export Issues, PRs, and Wiki content to `/records/YYYY-MM/`.
* Maintain version history of SOP/WI documents in the Wiki or repository folders.

---

## **8. References**

* ISO 9001:2015 – Clauses 4–10
* QMS-SOP-03 – Documented Information Control
* QMS-SOP-04 – Change Control
* QMS-SOP-05 – Leadership
* QMS-SOP-06 – Planning
* QMS-SOP-08 – Risk & Opportunity Management

---

## **9. Revision History**

| Revision | Date   | Description                                                          | Approved By |
| -------- | ------ | -------------------------------------------------------------------- | ----------- |
| 2.0      | [Date] | Updated to single FLEY QMS Kanban board for authoring and operations | [Name]      |

---

## 💡 **Implementation Notes**

* One Kanban board in `redwitch.wiki` now tracks **both QMS authoring and operations**.
* Future Red Witch coding will use a **separate dev board** in the `redwitch` repo.
* Central QMS (`fley-qms`) may be created later for multi-project use; for now, keep the pilot QMS in `redwitch.wiki`.
* Use labels, cross-links, and consistent columns to maintain audit-ready traceability.
