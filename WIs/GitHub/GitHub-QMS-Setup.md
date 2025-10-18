# **WI - Set Up the QMS in GitHub**

**Slug:** GitHub-QMS-Setup  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Document-Control-SOP, Change-Control-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-QMS-Setup  

---

## **1. Purpose**

To define the method for **establishing the FLEY Quality Management System (QMS)** in GitHub using a **single Kanban board** named **“FLEY QMS”** within the `redwitch.wiki` repository.

This work instruction ensures that:

* The QMS framework (manual, context, process map) is created in a controlled, auditable environment.
* All QMS setup and operational activities are managed through one traceable board.
* Digital evidence of implementation is captured and retained as QMS records.

---

## **2. Scope**

This WI applies to all setup and configuration activities required to establish the QMS in GitHub, including:

* Repository and Wiki structure
* Issue templates and label scheme
* Creation of the Quality Manual, Context, and Process Map
* Setup of the **FLEY QMS** Kanban board and views
* Management Review scheduling
* Integration with product repositories
* Record retention and export

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* WI – GitHub–Document–Control
* WI – GitHub–Change–Control
* WI – GitHub–Version–Control
* [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)

---

## **4. Responsibilities and Authorities**

| Role                            | Responsibilities                                                                                                   | Authority / Decision Rights                |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| **Quality Manager / QMS Admin** | Create repository structure, configure board, define issue templates, and initialize management review recurrence. | Approve initial setup and request changes. |
| **Top Management**              | Approve the Quality Manual, Policy, and Review Schedule.                                                           | Final approval of QMS readiness.           |
| **Process Owners**              | Provide process inputs and validate SOP/WI links.                                                                  | Approve their process definitions.         |
| **Contributors / SMEs**         | Assist in drafting and populating base documents.                                                                  | Suggest edits; no direct approval rights.  |

---

## **5. Repository and Wiki Structure**

Create or verify the following structure in `redwitch.wiki`:

```
QMS/
   Quality-Manual.md
   Context-Analysis.md
   Organizational-Chart.md
   Process-Map.md
   Quality-Policy.md
SOPs/
WIs/
Plans/
Templates/
Records/
```

The **Wiki** mirrors key documents (manual, SOPs, WIs) for user-friendly navigation.

---

## **6. Kanban Board: FLEY QMS**

**Purpose:** To manage all QMS setup and operational activities using one board.

**Columns:**

```
Backlog → In Progress → In Test → Closed
```

**Views:**

* **Board View** – visual workflow management.
* **Planning List View** – simplified issue list for intake and prioritization.

---

### **6.1 Label Scheme**

The following labels are used to organize and track QMS setup and operations:

| Category                | Labels                                                                                                    | Description                                                                                                                                     |
| ----------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Setup Phase**         | `Setup`                                                                                                   | Used for all activities related to establishing or configuring the QMS (e.g., creating documents, setting up repositories, defining workflows). |
| **QMS Operations**      | `Audit`, `CAPA`, `Change Request`, `Improvement`, `Management Review`, `Objective`, `Opportunity`, `Risk` | Used for active QMS management once the system is operational. These correspond to key ISO 9001 records and processes.                          |
| **Planning (Optional)** | `Plan`                                                                                                    | *(Optional)* – used only if specific planning documents or initiatives are tracked separately.                                                  |

> **Note:** During initial implementation, all issues related to setup activities are labeled only `Setup`. Operational labels are applied once the QMS transitions into steady-state use.

Each issue type has a **GitHub Issue Template** in `.github/ISSUE_TEMPLATE/` for consistent metadata.

---

## **7. Automation and Workflows**

1. **Enable Auto-Add to Project**

   * In project settings, enable *Auto-add new issues* for the repository.
   * Ensures all new issues are automatically added to the FLEY QMS board.

2. **Set Default Column for New Items**

   * Add a workflow rule:

     ```
     When: Item added to project  
     Then: Set status to "Backlog"
     ```
   * Ensures every new issue starts in the Backlog column.

3. **Reference:**
   See GitHub’s official documentation for setup details and advanced options:
   🔗 [**GitHub Projects Documentation**](https://docs.github.com/en/issues/planning-and-tracking-with-projects)

---

## **8. Establish the QMS Framework**

### 8.1 Quality Manual (`/QMS/Quality-Manual.md`)

* Defines the scope of the QMS and its interaction with related processes.
* References the Quality Policy, Context Analysis, and Process Map.
* Approved by Top Management via Pull Request.
* Tracked using an issue labeled `Setup` during authoring; closed when approved.

### 8.2 Context Analysis (`/QMS/Context-Analysis.md`)

* Identifies internal and external issues affecting the QMS.
* Updated as part of each Management Review cycle.
* Each revision approved through a Pull Request and recorded in comments.

### 8.3 Organizational Chart (`/QMS/Organizational-Chart.md`)

* Defines reporting lines, roles, and responsibilities.
* Updated when structure changes; linked to related procedures.

### 8.4 Process Map (`/QMS/Process-Map.md`)

* Lists all core and support processes, their inputs, outputs, and interactions.
* Includes references to related SOPs/WIs.
* Optionally includes a `Process-Map.png` diagram.

### 8.5 Quality Policy (`/QMS/Quality-Policy.md`)

* States the organization’s quality commitments and objectives.
* Approved by Top Management; displayed in the Wiki.

---

## **9. Configure Management Review Recurrence**

1. Create an issue labeled `Management Review` using the `management-review.yml` template.
2. Schedule quarterly recurrence (manual duplication or via GitHub Action).
3. Agenda includes:

   * Review of QMS performance and effectiveness
   * Evaluation of context and interested parties
   * Review of risks, opportunities, objectives, and actions
   * Assessment of audits, CAPAs, and improvements
   * Identification of new improvement opportunities
4. Record minutes as issue comments or attach under `/records/management-reviews/`.

---

## **10. Integration with Product Repositories**

* Each product repository (e.g., `redwitch`, `snowplow`) maintains its own development board.
* QMS-related issues (e.g., validation, CAPA, risk) are **linked** back to the FLEY QMS board for traceability.
* Links are recorded in issue comments or using GitHub’s “Linked Issues” feature.
* Implementation evidence (e.g., a product feature verifying a QMS requirement) is referenced in the associated QMS issue.

---

## **11. Backup and Export**

Until automation is deployed:

1. Perform **manual quarterly exports**:

   * Use `gh issue list` or GitHub’s export feature for issues and comments.
   * Download Wiki and repo as ZIP.
   * Save under `/records/github-exports/YYYY-MM/`.
2. Clone repository locally for offline backup and verification.

---

## **12. Records**

| Record                    | Location                           | Retention                     |
| ------------------------- | ---------------------------------- | ----------------------------- |
| Quality Manual            | `/QMS/Quality-Manual.md`           | Permanent                     |
| Context Analysis          | `/QMS/Context-Analysis.md`         | Reviewed annually             |
| Organizational Chart      | `/QMS/Organizational-Chart.md`     | Updated as needed             |
| Process Map               | `/QMS/Process-Map.md`              | Updated when processes change |
| Quality Policy            | `/QMS/Quality-Policy.md`           | Permanent                     |
| Management Review Minutes | `/records/management-reviews/`     | Permanent                     |
| Repository Exports        | `/records/github-exports/YYYY-MM/` | 5 years                       |
