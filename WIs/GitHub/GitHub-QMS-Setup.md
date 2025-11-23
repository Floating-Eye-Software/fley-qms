---
slug: GitHub-QMS-Setup
revision: r3
type: WI
status: approved
effective: 2025-11-23
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
* Creation of QMS framework documents (Manual, Context, Policy, Process Map, Org Chart)
* Assignment of users to QMS GitHub teams (`qms-authors`, `qms-approvers`)
* GitHub organization settings
* Automation and export routines

---

## **3. References**

* SOP – Document Control
* SOP – Change Control
* WI – GitHub–Document–Control
* WI – GitHub–Change–Control
* WI – GitHub–Version–Control
* WI - GitHub-QMS-Operations
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

## **5. Procedure**

The following steps define how the FLEY QMS is initialized and configured in GitHub. Completion establishes the baseline for controlled documentation and operational traceability.

### **5.1 Repository Structure**

```
.github/
    CODEOWNERS
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

The `fley-qms` repository serves as the published, user-facing interface for controlled QMS content.

### **5.2 Repository Configuration**

#### **5.2.1 General Settings**

**Repository → Settings → General → Default branch**

| Setting        | Value  | Notes                           |
| -------------- | ------ | ------------------------------- |
| Default branch | `main` | Location of approved documents  |

**Repository → Settings → General → Releases**

| Setting                     | Value   | Notes                                         |
| --------------------------- | ------- | --------------------------------------------- |
| Enable release immutability | Enabled | Prevents modification of released assets/tags |

**Repository → Settings → General → Pull Requests**

| Setting             | Value    | Notes                                    |
| ------------------- | -------- | ---------------------------------------- |
| Allow merge commits | Enabled  | Preserves full audit trail               |
| Squash merging      | Disabled | Squash hides intermediate history        |
| Rebase merging      | Disabled | Rewriting commits violates recordkeeping |

#### **5.2.2 Branch Protection Rules**

Apply the following configuration:

**Repository → Settings → Branches → Add Protection Rule → `main`**

| Setting                                    | Value           | Notes                                                   |
| ------------------------------------------ | --------------- | ------------------------------------------------------- |
| Require a pull request before merging      | Enabled         | Enforces controlled approval workflow                   |
| Require approvals                          | Enabled (*)     | GitHub limitation if organization has only one approver |
| Required number of approvals               | 1 (*)           | Minimum viable QMS approval                             |
| Require review from CODEOWNERS             | Enabled (*)     | Ensures approval by QMS approvers                       |
| Allow specified actors to bypass PRs       | Disabled        | No users, teams, or apps may bypass controls            |
| Require linear history                     | Disabled        | Merge commits permitted for auditability                |
| Do not allow bypassing protections         | Enabled         | Applies to admins and bypass-enabled roles              |
| Restrict who can push to matching branches | Enabled         | Prevents direct commits                                 |
| Push access                                | `qms-approvers` | Only qms-approvers make changes in `main`               |
| Allow force pushes                         | Disabled        | Prevents history modification                           |
| Allow branch deletions                     | Disabled        | Controlled branch must not be deletable                 |

(\*) *Enabled only if the organization has ≥2 approvers*

#### **5.2.3 Tag Rulesets**

**Repository → Settings → Rules → Rulesets → New ruleset → New tag ruleset**

Create the following tag rulesets:

* **Restrict tag creation**  
 * Bypass list: QMS-Approvers  
 * Target tags: \*r_\*  
 * Rules: Restrict creations, Block force pushes  


* **Restrict tag modification**  
 * Bypass list: None  
 * Target tags: \*r_\*  
 * Rules: Restrict updates, Restrict deletions, Block force pushes  

#### **5.2.4 CODEOWNERS Configuration**

Create `.github/CODEOWNERS` in the `main` branch with the following content:

```plaintext
# Require approval from Approvers for any change to controlled content
* @Floating-Eye-Software/qms-approvers
````

### **5.3 Project Configuration**

#### **5.3.1 Project Columns**

**Project → Settings → Status → Options**

```
Backlog → In Progress → In Test → Closed
```

| Option      | Color  | Definition                          |
| ------------| ------ | ----------------------------------- |
| Backlog     | GREY   | This item hasn't been started       |
| In Progress | GREEN  | This is actively being worked on    |
| In Test     | YELLOW | This is being verified or validated |
| Closed      | BLUE   | This has been completed             |

#### **5.3.2 Project Views**

**Project → New View**

| View                          | Type / Filter                       | Purpose                                 |
| ----------------------------- | ----------------------------------- | --------------------------------------- |
| Active (Table)                | status:"In Progress","In Test"      | Currently active issues                 |
| QMS Actions (Table)           | label:"Management Review",Objective | Plan and track leadership actions       |
| Changes (Table)               | label:"Change Request",Change       | Full lifecycle of changes               |
| Development (Board)           | type:Development                    | Track QMS framework creation or updates |
| Risks & Opportunities (Table) | label:Risk,Opportunity              | Risk-based thinking dashboard           |
| Improvements (Table)          | label:Improvement                   | Continual improvement actions           |
| Nonconformances (Table)       | label:Nonconformance                | Track deviations                        |
| Audits (Table)                | label:Audit                         | Internal and external audits            |
| CAPAs (Table)                 | label:CAPA                          | Corrective/Preventive Actions           |
| All Issues (Table)            | *(no filter)*                       | Complete record view                    |

#### **5.3.3 Project Workflows**

Enable the following workflows:

**Project → Workflows → Default Workflows**

* Auto-add sub-issues to project
* Auto-add to project
* Auto-close issue
* Item added to project → Set status: Backlog
* Item closed

### **5.4 Organization Settings**

In the Floating Eye Software organization:

#### **5.4.1 Labels**

**Organization → Settings → Repository → General → Repository Labels**

| Label             | Color   | Definition                                      |
| ----------------- | ------- | ----------------------------------------------- |
| Audit             | #0E8A16 | Internal/external audit records                 |
| CAPA              | #B60205 | Corrective and preventive actions               |
| Change            | #F9D71C | Implementation of a Change Request              |
| Change Request    | #E4B400 | Proposed change for review and approval         |
| Improvement       | #2EA44F | General improvement actions                     |
| Management Review | #7057FF | MR records and outputs                          |
| Nonconformance    | #D73A49 | Record of non-fulfilment of a requirement       |
| Objective         | #0366D6 | Quality objectives and performance tracking     |
| Opportunity       | #34D058 | Positive improvement opportunities              |
| Risk              | #E36209 | Risk identification, evaluation, and mitigation |

Templates for each record type are stored in `.github/ISSUE_TEMPLATE/`.

#### **5.4.2 Issue Types**

**Organization → Settings → Planning → Issue Types**

| Type            | Color  | Definition                                                          | Typical Use                                       |
| --------------- | ------ | ------------------------------------------------------------------- | ------------------------------------------------- |
| **Development** | BLUE   | Activities that create or improve products, processes, or systems.  | QMS framework setup, automation, template design. |
| **Operations**  | PURPLE | Activities that manage, maintain, or monitor processes and systems. | CAPA, Audit, Objective, Risk, Management Review.  |

#### **5.4.3 Teams**

**Organization → Teams → New Team**

* QMS-Authors: Creates or updates controlled docs
* QMS-Approvers: Reviews, approves, and merges

**Organization → Settings → Organization roles → Role assignments → New role assignment**

* QMS-Authors: All-repository write
* QMS-Approvers: All-repository maintain

#### **5.4.4 Actions & Logs**

**Organization → Settings → Actions → General**

* Artifact and log retention: 400 days (maximum limit)
* Allow GitHub Actions to create and approve pull requests: Disabled

**Organization → Settings → Logs → Audit Log**

* Ensure the Audit Log is enabled.

---

### **5.5 Define the QMS Framework**

| Document             | Purpose                                        |
| -------------------- | ---------------------------------------------- |
| Quality Manual       | Defines scope and structure of QMS.            |
| Context Analysis     | Captures internal/external issues and parties. |
| Organizational Chart | Defines roles and responsibilities.            |
| Process Map          | Shows process relationships.                   |
| Quality Policy       | Declares company quality commitments.          |

These are tracked as **Development Issues** and closed upon approval of the associated Pull Request.

The formal approval and release of the **Quality Manual** marks the **official activation of the QMS**, signifying management’s commitment and the readiness of the system to enter operation under ISO 9001 principles.

---

### **5.6 Integration with Other Repositories**

* `fley-qms` remains the QMS master record.
* Each product repository (e.g., redwitch, snowplow) maintains its own development board.
* Product repositories maintain consistent Issue Type and Label use.
* Use Linked Issues for traceability between QMS and development work.

---

### **5.7 Backup and Export**

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
