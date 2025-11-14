---
slug: GitHub-QMS-Setup
revision: r2
type: WI
status: approved
effective: 2025-11-14
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/WIs/GitHub/GitHub-QMS-Setup.md
---

# **WI – Set Up the QMS in GitHub**

## **1. Purpose**

To define the method for **establishing and configuring the FLEY Quality Management System (QMS)** in GitHub using a single controlled Project titled **“FLEY QMS”** within the `fley-qms` repository.

This setup event represents the formal creation of the organization’s **controlled digital quality environment**, forming the foundation upon which all QMS evidence, workflows, and continual improvement activities are built.

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
* Setup of automation and export routines

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
## **5. Establishing the QMS in GitHub**

The following steps define how the FLEY QMS is formally initialized and configured in GitHub. Completing this setup establishes the baseline for controlled documentation and operational traceability.

### **5.1 Repository Structure**

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

### **5.2 Project: FLEY QMS**

#### **1. Columns & Status Colors**

```
Backlog (GREY) → In Progress (GREEN) → In Test (YELLOW) → Closed (BLUE)
```

#### **2. Project Views**

| View                          | Type / Filter                       | Purpose                                  |
| ----------------------------- | ----------------------------------- | ---------------------------------------- |
| Development (Board)           | type:Development                    | Track QMS framework creation or updates. |
| QMS Actions (Table)           | label:"Management Review",Objective | Plan and track leadership actions.       |
| Changes (Table)               | label:"Change Request",Change       | Full lifecycle of changes.               |
| Improvements (Table)          | label:Improvement                   | Continual improvement actions.           |
| Risks & Opportunities (Table) | label:Risk,Opportunity              | Risk-based thinking dashboard.           |
| Audits (Table)                | label:Audit                         | Internal and external audits.            |
| CAPAs (Table)                 | label:CAPA                          | Corrective/Preventive Actions.           |
| Nonconformances (Table)       | label:Nonconformance                | Track deviations.                        |
| Missing Label (Table)         | no:label -type:Development          | Classification completeness check.       |
| All Issues (Table)            | *(no filter)*                       | Complete record view.                    |

---

### **5.3 Issue Types & Colors**

| Type            | Color  | Definition                                                          | Typical Use                                       |
| --------------- | ------ | ------------------------------------------------------------------- | ------------------------------------------------- |
| **Development** | BLUE   | Activities that create or improve products, processes, or systems.  | QMS framework setup, automation, template design. |
| **Operations**  | PURPLE | Activities that manage, maintain, or monitor processes and systems. | CAPA, Audit, Objective, Risk, Management Review.  |

---

### **5.4 Label Scheme & Colors**

| Label             | Color   | Definition                                           |
| ----------------- | ------- | ---------------------------------------------------- |
| Audit             | #0E8A16 | Internal/external audit records                      |
| CAPA              | #B60205 | Corrective and preventive actions                    |
| Change            | #F9D71C | Implementation of a Change Request                   |
| Change Request    | #E4B400 | Proposed QMS-level change needing review or approval |
| Improvement       | #2EA44F | General improvement actions not requiring CAPA       |
| Management Review | #7057FF | MR records and outputs                               |
| Nonconformance    | #D73A49 | Record of non-fulfilment of a requirement            |
| Objective         | #0366D6 | Quality objectives and performance tracking          |
| Opportunity       | #34D058 | Positive improvement opportunities                   |
| Risk              | #E36209 | Risk identification, evaluation, and mitigation      |

Templates for each record type are stored in `.github/ISSUE_TEMPLATE/`.

---

### **5.5 Automation and Workflows**

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
   [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)

---

### **5.6 Establish the QMS Framework**

| Document             | Purpose                                        |
| -------------------- | ---------------------------------------------- |
| Quality Manual       | Defines scope and structure of QMS.            |
| Context Analysis     | Captures internal/external issues and parties. |
| Organizational Chart | Defines roles and responsibilities.            |
| Process Map          | Shows process relationships.                   |
| Quality Policy       | Declares company quality commitments.          |

Tracked as **Development Issues**, closed upon PR approval.

The formal approval and release of the **Quality Manual** marks the **official activation of the QMS**, signifying management’s commitment and the readiness of the system to enter operation under ISO 9001 principles.

---

### **5.7 Integration with Other Repositories**

* `fley-qms` remains the QMS master record.
* Each product repository (e.g., redwitch, snowplow) maintains its own development board.
* Product repositories maintain consistent Issue Type and Label use.
* Use Linked Issues for traceability between QMS and development work.

---

### **5.8 Backup and Export**

Regular exports safeguard QMS continuity and provide offline verification of controlled records in the event of repository loss or service disruption.

Until automation is deployed:

1. Perform **manual quarterly exports**:
   * Use `gh issue list` or GitHub’s export feature for issues and comments.
   * Download Wiki and repo as ZIP.
   * Save under `/records/github-exports/YYYY-MM/`.
2. Clone repository locally for offline backup and verification.

---

## **6. Records**

| Record                     | Location                           | Retention |
| -------------------------- | ---------------------------------- | --------- |
| QMS Framework Docs         | `/QMS/`                            | Permanent |
| Repository Exports         | `/records/github-exports/YYYY-MM/` | 5 years   |
| Setup Issues (Development) | GitHub Project                     | Permanent |
