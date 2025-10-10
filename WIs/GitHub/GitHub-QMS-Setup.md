# 🧭 **Work Instruction: Set Up the QMS in GitHub**

**Document No.:** WI-QMS-10-02
**Title:** QMS Setup – Single FLEY Board in GitHub
**Revision:** 3.0
**Effective Date:** [Insert Date]
**Approved By:** [Top Management]

---

## **1. Purpose**

To define the method for **establishing the FLEY Quality Management System (QMS)** in GitHub using a **single Kanban board** named **“FLEY QMS”** within the `redwitch.wiki` repository.

This work instruction ensures that:

* The QMS framework (manual, context, process map) is created in a controlled, auditable environment.
* All QMS authoring and operational activities are managed through one traceable board.
* Digital evidence of implementation is captured and retained as QMS records.

---

## **2. Scope**

This WI applies to all setup and configuration activities required to establish the QMS in GitHub, including:

* Repository and Wiki structure
* Issue templates and label scheme
* Creation of the Quality Manual, Context, and Process Map
* Setup of the FLEY QMS Kanban board
* Management Review scheduling
* Integration with product repositories
* Record retention and export

---

## **3. Responsibilities**

| Role                                    | Responsibility                                                                                         |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Top Management**                      | Approves the QMS setup, Quality Manual, and ensures adequate resources.                                |
| **Quality Manager / QMS Administrator** | Creates repository structure, configures the FLEY QMS board, maintains templates, and manages records. |
| **Process Owners**                      | Define their processes, interactions, and supply input for the process map.                            |
| **Contributors / SMEs**                 | Participate in authoring, review, and data collection for context, risks, and interested parties.      |

---

## **4. Repository and Wiki Structure**

Create or verify the following structure in `redwitch.wiki`:

```
QMS/
   Quality-Manual.md
   Context-Analysis.md
   Interested-Parties.md
   Process-Map.md
SOPs/
WIs/
Plans/
Templates/
records/
```

The **Wiki** mirrors key documents (manual, SOPs, WIs) for user-friendly navigation.

---

## **5. Kanban Board: FLEY QMS**

**Purpose:** To manage **all QMS authoring and operational activities** using one board.

**Columns:**

```
Backlog → Drafting → Review / Approval → Active → Validated / Closed
```

**Recommended Labels:**

| Category           | Labels                                                                                  |
| ------------------ | --------------------------------------------------------------------------------------- |
| Document Authoring | `SOP`, `WI`, `Template`, `Manual`                                                       |
| QMS Operations     | `Risk`, `Opportunity`, `CAPA`, `Improvement`, `Objective`, `Audit`, `Management Review` |
| Process Definition | `Process`, `Context`, `Interested Parties`, `Scope`                                     |
| Validation / Pilot | `Validation`, `Pilot`                                                                   |
| Change Control     | `Change Request`, `Update`                                                              |

Each Issue type has a **GitHub Issue Template** in `.github/ISSUE_TEMPLATE/` for consistent metadata.

---

## **6. Establish the QMS Framework**

### 6.1 Create the Quality Manual

1. In `/QMS/Quality-Manual.md`, include:

   * Purpose and scope of the QMS
   * QMS policy and objectives (from Leadership SOP)
   * Process map summary and context links
   * Management review and continual improvement structure
2. Submit via Pull Request for Top Management approval.
3. Label the related Issue as `Manual` and move to **Validated / Closed** after approval.

### 6.2 Determine Internal and External Issues

1. Create `/QMS/Context-Analysis.md` using the `context-template.yml`.
2. Document internal (resources, culture, technology) and external (market, regulatory, environmental) issues.
3. Review and update quarterly during Management Review.

### 6.3 Determine Interested Parties

1. Create `/QMS/Interested-Parties.md`.
2. List customers, employees, suppliers, regulators, etc.
3. Include their relevant needs, expectations, and how they’re monitored.

### 6.4 Create the Process Map

1. Create `/QMS/Process-Map.md` and, if possible, a diagram (`Process-Map.png`).
2. Include:

   * Process name
   * Inputs / Outputs
   * SOP/WI references
   * Interactions between processes
3. Link each process definition to an Issue labeled `Process`.

---

## **7. Configure Management Review Recurrence**

1. Create a **GitHub Issue** labeled `Management Review` using the template `management-review.yml`.
2. Schedule recurrence (quarterly) via manual duplication or GitHub Action.
3. Include agenda to ensure all ISO-required “determine / monitor / review / establish / update” actions occur:

   * Review QMS performance and effectiveness
   * Evaluate context and interested parties
   * Review risks, opportunities, objectives, and actions
   * Assess audit and CAPA results
   * Identify continual improvement needs
4. Attach minutes in Issue comments or `/records/management-reviews/`.

---

## **8. Integration with Product Repositories**

* **Product Boards**: Each project (e.g., `redwitch`, `snowplow`) has its own board for development.
* **Cross-Linking**:

  * Product Issues related to QMS (e.g., validation, risk, CAPA) are linked back to their parent QMS Issue in `redwitch.wiki`.
  * Use “Linked Issues” or URLs in comments for traceability.
* **Validation Evidence**: Product-side implementation results are attached or linked in QMS Issues (e.g., “Implemented SOP-05 in Snowplow”).

---

## **9. Backup and Export**

Until automated Actions are implemented:

1. Perform **manual quarterly exports**:

   * Use GitHub’s export or `gh issue list` CLI to export all Issues and comments.
   * Export Wiki and repository contents as ZIP.
   * Save under `/records/github-exports/YYYY-MM/`.
2. Periodically clone the repository locally for offline storage.

---

## **10. Records**

| Record                    | Location                           | Retention                     |
| ------------------------- | ---------------------------------- | ----------------------------- |
| Quality Manual            | `/QMS/Quality-Manual.md`           | Permanent                     |
| Context Analysis          | `/QMS/Context-Analysis.md`         | Reviewed annually             |
| Process Map               | `/QMS/Process-Map.md`              | Updated when processes change |
| Management Review Minutes | `/records/management-reviews/`     | Permanent                     |
| Exports                   | `/records/github-exports/YYYY-MM/` | 5 years                       |

---

## **11. References**

* ISO 9001:2015 – Clauses 4–6
* ISO 9004:2018 – Clauses 4–5
* QMS-SOP-03 – Documented Information Control
* QMS-SOP-04 – Change Control
* QMS-SOP-05 – Leadership
* QMS-SOP-06 – Planning
* QMS-SOP-08 – Risk & Opportunity Management
* WI-QMS-09-01 – QMS Operations in GitHub

---

## **12. Revision History**

| Rev | Date   | Description                                                                                         | Approved By |
| --- | ------ | --------------------------------------------------------------------------------------------------- | ----------- |
| 3.0 | [Date] | Consolidated Establish QMS content, single-board model, integrated context/manual setup and exports | [Name]      |
