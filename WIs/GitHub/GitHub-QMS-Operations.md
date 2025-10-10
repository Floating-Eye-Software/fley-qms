# ⚙️ **Work Instruction: Operate the QMS in GitHub**

**Document No.:** WI-QMS-09-01
**Title:** Operating the QMS in GitHub – Single FLEY Board
**Revision:** 2.0
**Effective Date:** [Insert Date]
**Approved By:** [Top Management]

---

## **1. Purpose**

To define how the organization **operates and maintains** its QMS using GitHub’s tools, ensuring full compliance with ISO 9001:2015 Clauses 4–10.

---

## **2. Scope**

Applies to all QMS operation activities, including:

* Leadership and Management Review
* Quality objectives planning and tracking
* Risk and opportunity management
* CAPA and continual improvement
* Change control and document updates
* Records management and traceability

---

## **3. GitHub Project Tabs and Their QMS Roles**

| GitHub Tab                       | QMS Function                                                                       |
| -------------------------------- | ---------------------------------------------------------------------------------- |
| **Repository (`redwitch.wiki`)** | Home for all controlled QMS documentation (manual, SOPs, WIs, templates, records). |
| **Wiki**                         | User-facing view for SOPs, WIs, and policies.                                      |
| **Issues**                       | Used for all QMS records (risks, CAPAs, improvements, objectives, reviews).        |
| **Pull Requests**                | Formal change approvals under Document Control SOP.                                |
| **Projects**                     | The single “FLEY QMS” board for all QMS authoring and operations.                  |
| **Discussions**                  | Optional collaboration, brainstorming, or feedback.                                |
| **Actions (CI/CD)**              | Future automation: notifications, exports, and backups.                            |
| **Security**                     | Controls contributor access and permissions.                                       |
| **Insights**                     | Repository metrics and participation history.                                      |
| **Settings**                     | Repository configuration, branch rules, and visibility.                            |

---

## **4. QMS Operation Using the FLEY Board**

### 4.1 Issue Workflow

All QMS activity is tracked through the FLEY QMS board:

```
Backlog → Drafting → Review / Approval → Active → Validated / Closed
```

* **Authoring Issues**: SOPs, WIs, templates, policies
* **Operational Issues**: Risk, Opportunity, CAPA, Improvement, Objective, Management Review

Each Issue must:

* Use the appropriate label and Issue template
* Link related Issues and PRs
* Include responsible owner and due dates

---

### 4.2 Leadership and Governance

1. Quality Policy and Objectives are stored in `/QMS/Quality-Manual.md`.
2. Management Review is initiated quarterly using the `Management Review` Issue template.
3. Review input includes:

   * Internal/external issues
   * Interested parties
   * Risks, opportunities, objectives
   * CAPA, audit, and feedback results
4. Minutes and actions are attached to the Issue and archived in `/records/management-reviews/`.

---

### 4.3 Risk and Opportunity Management

1. Create an Issue labeled `Risk` or `Opportunity`.
2. Include likelihood, impact, mitigation/enhancement, and owner.
3. Review open risks quarterly in Management Review.
4. Mitigation actions tracked as linked Issues (`Action` or `CAPA`).
5. Closed Issues serve as permanent risk records.

---

### 4.4 Corrective Action and Continual Improvement

1. Create Issues labeled `CAPA` or `Improvement`.
2. Root cause and corrective actions are documented within the Issue.
3. Approval and closure recorded via comments or linked PRs.
4. Review open actions in the next Management Review.

---

### 4.5 Quality Objectives

1. Each Quality Objective = one Issue labeled `Objective`.
2. Define metric, target, owner, due date, and link to relevant process/SOP.
3. Move through the FLEY board as progress occurs.
4. Review quarterly and update results in comments.

---

### 4.6 Change Control and Documented Information

* Use Pull Requests for any QMS document or SOP/WI modification.
* Reference the associated `Change Request` Issue.
* Merge only after review and approval (digital signature).
* Obsolete versions are automatically preserved in Git history.

---

### 4.7 Records and Traceability

* All Issues, PRs, and comments are QMS records.
* Closed Issues and PRs remain accessible for audit.
* Periodic exports (manual backup) per WI-QMS-10-02 Section 9.
* Documented Information Control SOP applies to all repositories.

---

## **5. Continual Improvement Cycle**

Every quarter (or during each Management Review):

1. Reassess internal/external issues.
2. Update interested parties and requirements.
3. Review objectives, risks, and opportunities.
4. Verify effectiveness of actions taken.
5. Identify new improvements.
6. Document all updates in the relevant Issues and files.

---

## **6. References**

* ISO 9001:2015 – Clauses 4–10
* ISO 9004:2018 – Clauses 4–9
* QMS-SOP-03 – Documented Information Control
* QMS-SOP-04 – Change Control
* QMS-SOP-05 – Leadership
* QMS-SOP-06 – Planning
* QMS-SOP-08 – Risk & Opportunity Management
* WI-QMS-10-02 – QMS Setup in GitHub

---

## **7. Revision History**

| Rev | Date   | Description                                                                   | Approved By |
| --- | ------ | ----------------------------------------------------------------------------- | ----------- |
| 2.0 | [Date] | Integrated Establish and Operation content; aligned to single-board QMS model | [Name]      |

---

## 💡 **Implementation Notes**

* The **FLEY QMS board** in `redwitch.wiki` is the *only* board used for QMS activity — covering authoring, risks, CAPA, objectives, and management review.
* Product repos (e.g., `redwitch`, `snowplow`) maintain their own project boards for development and link relevant QMS Issues.
* Periodic exports and manual backups ensure ISO 9001 record control until automation (via Actions) is implemented.
* The Management Review ensures all ISO-required “determine / monitor / review / establish / update” actions are documented and traceable.
