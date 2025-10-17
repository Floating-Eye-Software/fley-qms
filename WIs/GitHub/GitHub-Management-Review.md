# **WI – Conduct Management Review in GitHub**

**Slug:** GitHub-Management-Review
**Revision:** r1
**Effective Date:** [YYYY-MM-DD]
**Related SOP:** Management-Review-SOP
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/GitHub-Management-Review

---

## **1. Purpose**

To define how to plan, conduct, and record Management Reviews (MRs) of the Quality Management System (QMS) using GitHub as the controlled environment.
This instruction ensures that Management Reviews are performed consistently, that all ISO 9001:2015 Clause 9.3 requirements are met, and that digital records are complete and auditable.

---

## **2. Scope**

* **Applicability:** Applies to all QMS Management Review activities conducted in the `redwitch.wiki` repository using GitHub Issues, Projects, and Actions.
* **Exclusions:** This instruction does not cover informal leadership or departmental meetings that are not designated as official Management Reviews.

---

## **3. References**

* **Related SOP:** `SOP_Management-Review`
* **Related SOPs:**

  * `SOP_Leadership`
  * `SOP_Quality-Planning`
  * `SOP_Risk-and-Opportunity-Management`
* **Related WIs:**

  * `WI_GitHub-QMS-Operations`
  * `WI_GitHub-QMS-Setup`
* **Standards:** ISO 9001:2015 — Clause 9.3: Management Review

---

## **4. Responsibilities and Authorities**

| Role                             | Responsibilities                                                                                                         | Authority / Decision Rights                                |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------- |
| **Quality Manager**              | Initiates, schedules, and documents the Management Review issue; compiles required inputs; ensures proper recordkeeping. | Can open and close MR issues; approve minutes for release. |
| **Top Management**               | Chairs the Management Review; ensures participation of relevant process owners; approves decisions and actions.          | Can approve MR outcomes and assign resources.              |
| **Process Owners**               | Provide data for MR inputs (KPIs, audit results, objectives, risks, CAPAs).                                              | Approve process-level actions assigned during MR.          |
| **Document Control / QMS Admin** | Maintains MR record structure under `/records/management-reviews/`.                                                      | Can merge related PRs and tag records.                     |

---

## **5. Step-by-Step Procedure**

### **5.1 Create and Schedule a Management Review Issue**

1. Navigate to the **Issues** tab in the `redwitch.wiki` repository.
2. Click **New Issue** → Select the `management-review.yml` template.
3. Title the issue:

   ```
   Management Review – [Quarter/Year] (e.g., Q1 2025)
   ```
4. Assign the issue to **Quality Manager** and label it `Management Review`.
5. Schedule recurrence:

   * Quarterly by default (manual duplication or via GitHub Action `management-review-recurring.yml`).
   * Adjust frequency if triggered by significant change, nonconformity, or leadership request.

---

### **5.2 Prepare Inputs**

1. Quality Manager compiles current data and attaches or links to each input source within the issue body:

   * Previous MR actions and status (linked issues or Action Tracker)
   * Context and interested parties summary
   * Process performance metrics and QMS effectiveness indicators
   * Customer satisfaction and feedback
   * Internal and external audit results
   * Nonconformities and CAPA status
   * Risk and opportunity register updates
   * Resource adequacy (staffing, tools, training)
   * Quality objectives progress
   * Improvement recommendations

2. Tag or link related GitHub issues using syntax:

   ```
   Related Issues: #45 #98 #112
   ```

3. Confirm that all attachments are placed under `/records/management-reviews/YYYY-Q#/inputs/` for traceability.

---

### **5.3 Conduct the Management Review Meeting**

1. The **Top Management** representative chairs the meeting.

2. Attendees: Quality Manager, Process Owners, and any invited participants.

3. The **agenda** follows the required ISO 9001 input sequence (from SOP_Management-Review §6.2).

4. Discussion items and key decisions are captured as **issue comments**, using this syntax for structure:

   ```
   ## Agenda Item: [Topic]
   - Discussion Summary:
   - Decision:
   - Responsible:
   - Due Date:
   ```

5. Major improvement opportunities or actions may be created as separate GitHub issues and linked back to the MR issue.

---

### **5.4 Define and Record Outputs**

1. Record all outputs (decisions, actions, policy updates, resource changes) in the issue under the section:

   ```
   ## Outputs
   - [ ] Action 1 – Assigned to @user, due YYYY-MM-DD
   - [ ] Action 2 – Assigned to @user, due YYYY-MM-DD
   ```
2. Each action item should have a corresponding linked issue with the appropriate label (`Improvement`, `CAPA`, `Risk`, or `Objective`).
3. Tag action owners in comments to trigger notifications.

---

### **5.5 Review, Approve, and Close**

1. Quality Manager reviews the issue for completeness and accuracy.
2. Top Management confirms all decisions and approves closure by commenting:

   ```
   ✅ Approved by [Name, Role, Date]
   ```
3. Attach final minutes as a Markdown or PDF file under:

   ```
   /records/management-reviews/YYYY-Q#/minutes/
   ```
4. Close the MR issue with the comment:

   ```
   MR complete and records archived.
   ```
5. Optionally tag the closing commit:

   ```
   git tag MR_Q1_2025
   git push origin MR_Q1_2025
   ```

---

### **5.6 Follow-Up Actions**

1. Track all open actions from MR in the **FLEY QMS Board** under the appropriate workflow column.
2. Verify completion during subsequent MRs or monthly leadership reviews.
3. Document verification results directly as comments in the linked issues.

---

## **6. Records**

| Record / Artifact                                  | Responsible Owner | Storage Location                      | Retention                          | Control Method                     |
| -------------------------------------------------- | ----------------- | ------------------------------------- | ---------------------------------- | ---------------------------------- |
| MR Issue (`Management Review` label)               | Quality Manager   | GitHub Issues (`redwitch.wiki`)       | Permanent                          | Git issue tracking                 |
| MR Agenda / Minutes                                | Quality Manager   | `/records/management-reviews/`        | Permanent                          | Version-controlled Markdown or PDF |
| MR Action Tracker                                  | Quality Manager   | `/records/management-reviews/`        | Until all actions closed + 3 years | Linked issue tracking              |
| Supporting Data (KPIs, Audit Results, Risks, etc.) | Process Owners    | Linked issues or `/inputs/` subfolder | As per related process             | Git version control                |
