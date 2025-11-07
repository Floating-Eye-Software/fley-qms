# **WI – Set Up the QMS in GitHub**

**Slug:** GitHub-QMS-Setup  
**Revision:** r2 **Draft**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Document-Control-SOP, Change-Control-SOP, Identification-and-Traceability-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Setup.md  

---

## **1. Purpose**

To define the method for **establishing and configuring the FLEY Quality Management System (QMS)** in GitHub using a single, controlled Kanban board titled **“FLEY QMS”** within the `redwitch` repository.

This ensures that:

* The QMS framework (manual, process map, policies) is built in an auditable, traceable environment.
* All setup and operational records share a single workflow.
* The system is ready for digital quality management, continual improvement, and ISO 9001 evidence capture.

---

## **2. Scope**

Applies to all activities required to **create and configure the QMS infrastructure** in GitHub, including:

* Repository and Wiki structure
* Issue type and label configuration
* QMS framework documents (Manual, Context, Policy, Process Map)
* Setup of the **FLEY QMS Project Board**
* Definition of automation, recurrence, and export routines

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

| Role                            | Responsibilities                                                                        | Authority / Decision Rights                                 |
| ------------------------------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Quality Manager / QMS Admin** | Configure repository, define templates, establish board, maintain recurrence schedules. | Approve setup configuration and request structural changes. |
| **Top Management**              | Approve Quality Manual, Policy, and QMS readiness.                                      | Final approval of setup completion.                         |
| **Process Owners**              | Validate SOP/WI links, define process inputs.                                           | Approve process documentation for their areas.              |
| **Contributors / SMEs**         | Provide inputs and support drafting.                                                    | Suggest edits only.                                         |

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

The **Wiki** provides user-friendly navigation for published QMS content.

---

## **6. Project Board: FLEY QMS**

### **Purpose**

To manage both **QMS setup (Development)** and **QMS operation (Operation)** activities on one board.

### **Columns**

```
Backlog → In Progress → In Test → Closed
```

### **Views**

* **Board View** – visual workflow.
* **List View** – planning and prioritization.

---

## **7. Issue Types**

To unify management across all repositories (QMS, software, and operations), only two Issue types are used:

| Type            | Usage                                                              | Examples                                                           |
| --------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Development** | Setup, configuration, product development, or infrastructure work. | Creating QMS framework, implementing features, defining templates. |
| **Operation**   | QMS record management and process execution.                       | CAPA, Risk, Objective, Audit, Management Review, Change Request.   |

Each issue type has a matching GitHub Issue Template in `.github/ISSUE_TEMPLATE/` for consistency.

---

## **8. Label Scheme**

Labels categorize operational and contextual aspects:

| Category          | Labels                                                                                                    | Description                                                 |
| ----------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Issue Type**    | `Development`, `Operation`                                                                                | Distinguishes QMS setup or execution activity.              |
| **Record Labels** | `Audit`, `CAPA`, `Change Request`, `Improvement`, `Management Review`, `Objective`, `Opportunity`, `Risk` | Identifies the QMS record type when Issue type = Operation. |
| **Status / Meta** | `Pending Approval`, `Obsolete`, `Linked`                                                                  | Used to signal workflow or traceability metadata.           |

---

## **9. Automation and Workflow Rules**

1. **Auto-add to Project:**
   Enable in Project settings so all new issues are added automatically to “FLEY QMS.”

2. **Default Column Rule:**

   ```
   When: Item added to project  
   Then: Set status to "Backlog"
   ```

3. **Reference:**
   [GitHub Project Automation Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project)

---

## **10. Establish the QMS Framework**

| Document                 | Purpose                                                   | Control Method                      |
| ------------------------ | --------------------------------------------------------- | ----------------------------------- |
| **Quality Manual**       | Defines QMS scope, processes, and structure.              | Approved via Pull Request.          |
| **Context Analysis**     | Captures internal/external issues and interested parties. | Reviewed during Management Reviews. |
| **Organizational Chart** | Defines roles and responsibilities.                       | Updated when roles change.          |
| **Process Map**          | Identifies core/support processes and relationships.      | Reviewed during Management Review.  |
| **Quality Policy**       | States FLEY’s quality commitments and direction.          | Approved by Top Management.         |

Each document’s creation is tracked as a **Development Issue** and closed upon PR approval.

---

## **11. Configure Management Review Recurrence**

1. Create an **Operation Issue** labeled `Management Review` using its template.
2. Schedule quarterly recurrence manually or with GitHub Actions.
3. Store review minutes in `/records/management-reviews/`.

---

## **12. Integration with Other Repositories**

* QMS board remains the master control record.
* Product repos (e.g., `redwitch`) maintain their own boards but can link relevant issues (e.g., Change Requests, CAPAs).
* Use GitHub “Linked Issues” or comments for traceability.

---

## **13. Backup and Export**

Until automation is implemented:

1. Perform **quarterly manual exports** of issues, Wiki, and repository ZIPs.
2. Store in `/records/github-exports/YYYY-MM/`.

---

## **14. Records**

| Record                     | Location                           | Retention |
| -------------------------- | ---------------------------------- | --------- |
| QMS Framework Docs         | `/QMS/`                            | Permanent |
| Management Review Minutes  | `/records/management-reviews/`     | Permanent |
| Repository Exports         | `/records/github-exports/YYYY-MM/` | 5 years   |
| Setup Issues (Development) | GitHub Project                     | Permanent |
