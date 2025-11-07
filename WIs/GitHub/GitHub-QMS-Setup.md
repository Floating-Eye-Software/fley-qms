# **WI – Set Up the QMS in GitHub**

**Slug:** GitHub-QMS-Setup  
**Revision:** r2 **Draft**  
**Effective Date:** [YYYY-MM-DD]  
**Related SOPs:** Document-Control-SOP, Change-Control-SOP, Identification-and-Traceability-SOP  
**Controlled Source:** https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Setup.md  

---

## **1. Purpose**

To define the method for **establishing and configuring the FLEY Quality Management System (QMS)** in GitHub using a single controlled Project titled **“FLEY QMS”** within the `fley-qms` repository.

This ensures that:

* The QMS framework is built in a fully traceable, auditable environment.
* All QMS setup and operational records share a common workflow and classification model.
* The digital QMS supports continual improvement, risk-based thinking, and ISO 9001 evidence capture.

---

## **2. Scope**

Applies to all activities required to create and configure the **QMS infrastructure** in GitHub, including:

* Repository directory structure
* Issue Type and Label configuration
* Project View configuration
* Creation of QMS framework documents (Manual, Context, Policy, Process Map)
* Setup of automation, recurrence, and export routines

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

| Role                            | Responsibilities                                                                       | Authority / Decision Rights                  |
| ------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------- |
| **Quality Manager / QMS Admin** | Configure repository, define templates, establish project views, maintain automations. | Approve configuration and structure changes. |
| **Top Management**              | Approve Quality Manual, Policy, and initial QMS readiness.                             | Final approval of setup completion.          |
| **Process Owners**              | Validate SOP/WI links and process inputs.                                              | Approve documentation for their areas.       |
| **Contributors / SMEs**         | Provide technical or procedural input.                                                 | Suggest edits only.                          |

---

## **5. Repository Structure**

Verify the following structure in the `fley-qms` repository:

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

The `fley-qms` repository serves as the published, user-friendly interface for controlled QMS content.

---

## **6. Project: FLEY QMS**

### **Purpose**

To manage both **Development** (creation and improvement) and **Operations** (execution and maintenance) within one integrated project.

### **Columns**

```
Backlog → In Progress → In Test → Closed
```

### **Views**

| View                              | Type  | Filter                                 | Purpose                                                            |
| --------------------------------- | ----- | -------------------------------------- | ------------------------------------------------------------------ |
| **Development (Board)**           | Board | `type:Development`                     | Tracks creation or improvement of products, processes, or systems. |
| **QMS Actions (Board)**           | Board | `label:"Management Review", Objective` | Management reviews and objectives tracking.                        |
| **Change Log (Table)**            | Table | `label:"Change Request", Change`       | Records lifecycle of proposed and implemented changes.             |
| **Risks & Opportunities (Table)** | Table | `label:Risk, Opportunity`              | Risk and opportunity management overview.                          |
| **CAPAs (Table)**                 | Table | `label:CAPA`                           | Corrective and preventive action tracking.                         |
| **Audits (Table)**                | Table | `label:Audit`                          | Internal/external audit registry.                                  |
| **Nonconformances (Table)**       | Table | `label:Nonconformance`                 | Nonconformance tracking.                                           |
| **Improvements (Table)**          | Table | `label:Improvement`                    | Continual improvement opportunities.                               |
| **Missing Label (Table)**         | Table | `no:label -type:Development`           | Detects issues missing proper QMS classification.                  |

---

## **7. Issue Types**

| Type            | Definition                                                                     | Typical Use                                       |
| --------------- | ------------------------------------------------------------------------------ | ------------------------------------------------- |
| **Development** | Activities that create, enhance, or implement products, processes, or systems. | QMS framework setup, automation, template design. |
| **Operations**  | Activities that manage, maintain, or monitor processes and systems.            | CAPA, Audit, Objective, Risk, Management Review.  |

Templates for each Issue Type are stored in `.github/ISSUE_TEMPLATE/`.

---

## **8. Label Scheme**

| Label                 | Definition                                                                     | Use Case                                     |
| --------------------- | ------------------------------------------------------------------------------ | -------------------------------------------- |
| **Audit**             | Record of an internal or external audit, including findings and actions.       | Create an issue for each audit event.        |
| **CAPA**              | Corrective or Preventive Action to address a nonconformity or potential issue. | Link to related risks or audits.             |
| **Change**            | Implementation of an approved Change Request.                                  | Execution step post-approval.                |
| **Change Request**    | Proposal for a controlled QMS change requiring review/approval.                | Initiate here; link related “Change” issues. |
| **Improvement**       | Continual improvement action not requiring CAPA.                               | General enhancements or optimization.        |
| **Management Review** | Record of management review meeting and outputs.                               | Quarterly or ad hoc MR issues.               |
| **Nonconformance**    | Record of failure to meet a requirement or standard.                           | Document deviations, link to CAPA.           |
| **Objective**         | Quality objective or KPI for performance tracking.                             | Link to MR or Risk issues.                   |
| **Opportunity**       | Positive factor or idea for improvement.                                       | Link to MR or Objective.                     |
| **Risk**              | Source of uncertainty affecting objectives; includes mitigation actions.       | Link to Objective or CAPA.                   |

---

## **9. Automation Rules**

1. **Auto-Add to Project:** Enabled so all new issues are captured.
2. **Default Column:**

   ```
   When: Item added to project  
   Then: Set status to "Backlog"
   ```
3. **Reference:** [GitHub Project Automation Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project)

---

## **10. Establish the QMS Framework**

| Document             | Purpose                                        | Control                      |
| -------------------- | ---------------------------------------------- | ---------------------------- |
| Quality Manual       | Defines scope and structure of QMS.            | Controlled via Pull Request. |
| Context Analysis     | Captures internal/external issues and parties. | Reviewed during MR.          |
| Organizational Chart | Defines roles and responsibilities.            | Updated as needed.           |
| Process Map          | Shows process relationships.                   | Reviewed during MR.          |
| Quality Policy       | Declares company quality commitments.          | Approved by Top Management.  |

Each tracked as a **Development Issue**, closed upon PR approval.

---

## **11. Configure Management Review Recurrence**

1. Create an **Operations Issue** labeled `Management Review`.
2. Schedule recurrence quarterly (manual or automated).
3. Store records in `/records/management-reviews/`.

---

## **12. Integration with Other Repositories**

* `fley-qms` remains the QMS master record.
* Product repositories maintain consistent Issue Type and Label use.
* Use Linked Issues for traceability between QMS and development work.

---

## **13. Backup and Export**

Quarterly (until automated):

1. Export issues, Wiki, and repo ZIPs.
2. Store under `/records/github-exports/YYYY-MM/`.

---

## **14. Records**

| Record                     | Location                           | Retention |
| -------------------------- | ---------------------------------- | --------- |
| QMS Framework Docs         | `/QMS/`                            | Permanent |
| Management Review Minutes  | `/records/management-reviews/`     | Permanent |
| Repository Exports         | `/records/github-exports/YYYY-MM/` | 5 years   |
| Setup Issues (Development) | GitHub Project                     | Permanent |
