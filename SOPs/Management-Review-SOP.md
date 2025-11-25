---
slug: Management-Review-SOP
revision: r3
type: SOP
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/SOPs/Management-Review-SOP.md
---

# **SOP – Management Review**

## **1. Purpose**

To define how the organization conducts **Management Reviews** that evaluate the continuing suitability, adequacy, and effectiveness of the QMS.
This revision introduces an **event-driven, dependency-based review-cycle system** that replaces fixed-interval scheduling with flexible triggers tied to meaningful organizational events.

---

## **2. Scope**

Applies to all QMS activities that require top-management oversight, including review of performance data, risks and opportunities, audit results, policy changes, and improvement initiatives.

---

## **3. References**

* ISO 9001:2015 § 9.3
* SOP – Leadership
* SOP – Quality-Planning
* WI – FLEY-Action-Management
* SOP – Change-Control
* SOP – Corrective and Preventive Action
* SOP – Risk and Opportunity Management


---

## **4. Definitions**

| Term                        | Definition                                                                                                         |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Management Review (MR)** | A formal evaluation by top management of QMS performance and strategic alignment. |
| **Review Cycle**           | The interval between Management Reviews, determined by completion of defined triggers rather than time periods. |
| **Trigger**                | A condition or event that initiates a new review cycle. |
| **Action Tracker:**        | A controlled record used to monitor progress of MR action items. |

---

## **5. Responsibilities and Authorities**

| **Role**            | **Responsibilities**                                                                                                                                                              | **Authorities**                                                                 |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Top Management**  |  Lead each Management Review; Ensure inputs are complete and factual; Approve review outputs and assign follow-up actions; Verify QMS adequacy and effectiveness. |  Convene Management Reviews; Approve policies, objectives, and resources. |
| **Quality Manager** |  Coordinate preparation of review inputs; Maintain records of reviews and outcomes; Ensure follow-up actions are tracked to completion.                                |  Ensure completeness of inputs and records.                                  |
| **Process Owners**  |  Supply data and evidence from their process areas; Report on progress, risks, and opportunities.                                                                           |  Implement review outputs relevant to their processes.                         |
| **All Personnel**   |  Participate in improvement actions as assigned; Provide feedback and data when requested.                                                                                  |  Raise issues or suggestions for leadership consideration.                     |

---

## **6. Process Description**

### **6.1 Initiating a Review Cycle**

A new **Management Review Cycle** begins when one or more triggers occur, such as:

1. Completion of a **major plan, project, or change initiative**.
2. Achievement of a **defined readiness or maturity milestone** (e.g., *Audit-Ready QMS*).
3. Occurrence of a **significant risk, nonconformance, or compliance event**.

The **Quality Manager** proposes initiation of the cycle; **Top Management** confirms commencement and designates participants.
If no triggering event occurs within a twelve (12) month period, a Management Review shall be convened proactively to ensure the QMS is reviewed at least annually, maintaining conformance with ISO 9001:2015 §9.3.1.

### **6.2 Review Inputs**

Each review shall consider, as applicable:

1. Status of actions from previous review cycles.
 * **Critical MR outputs** (child issues that must be completed for MR closure)
 * **Long-term follow-ups** (tracked in milestone; reviewed in later MR cycle when actions completed)
2. Changes in external or internal context relevant to the QMS.
3. Performance data and metrics (objectives, KPIs, trend analysis).
4. Results of audits and evaluations of compliance.
5. Effectiveness of risk and opportunity actions.
6. Adequacy of resources, competence, and infrastructure.
7. Customer and stakeholder feedback.
8. Process and product performance, including incidents or nonconformities.
9. Emerging opportunities for improvement or innovation.

The Quality Manager shall verify that all required inputs listed in ISO 9001:2015 §9.3.2 are complete, current, and supported by evidence before the review begins.

### **6.3 Conducting the Review**

1. **Preparation** – The Quality Manager consolidates inputs and circulates a draft agenda.
2. **Discussion and Evaluation** – Top Management reviews each input, assesses overall QMS health, and identifies needed changes.
3. **Decision Recording** – Outcomes are captured in a *Management Review Record* noting:
   * Decisions made
   * Actions assigned
   * Responsible owners and dependencies
   * Target conditions for closure (not deadlines)
4. **Communication** – Key decisions are communicated to all relevant personnel.

### **6.4 Outputs of the Management Review**

Management Review shall identify needs and opportunities for improvement, including actions related to process performance, customer satisfaction, resource adequacy, risk and opportunity status, and the effectiveness of previously implemented changes. These outputs form part of the organization’s continual improvement process.

Management Review outputs are categorized into:

1. **Critical MR Outputs (Child Issues)**
   * Actions directly tied to MR decisions and strategic alignment.
   * **Must be completed before the MR issue can be closed.**
   * Recorded as **child issues** in GitHub for traceability and verification.

2. **Long-Term Follow-Up Actions (Milestone)**
   * Actions that are important but may extend beyond the MR cycle.
   * **Do not block MR closure**.
   * Tracked using a dedicated milestone or label and reviewed during the next MR cycle.

Outputs shall include:

* Decisions and actions related to:
  * Improvement of the QMS and its processes
  * Updates to the Quality Policy or objectives
  * Resource and competence needs
  * Risk mitigation or opportunity exploitation
* Confirmation of QMS adequacy and continued alignment with organizational direction
* Identification of follow-up items for the next review cycle, including critical outputs and long-term follow-ups

Each output is entered into the project tracking system for tracking and verification.

### **6.5 Follow-Up and Effectiveness Verification**

1. **Critical MR Outputs**
   * Each child issue must be tracked until verified effective.
   * Verification confirms that the intended result has been achieved and sustained.
   * MR issue **cannot be closed** until all critical outputs are completed or dispositioned.
2. **Long-Term Follow-Up Actions**
   * Verified during the **next MR cycle**.
   * Completion is not required for closure of the current MR issue.
   * Evidence of completion (plans, reports, metrics) is linked to the governing issue.
3. Any incomplete or partially effective actions, critical or long-term, are carried forward and referenced in the next MR cycle.
4. Verification and traceability records are maintained in the QMS repository and linked to the MR record for audit purposes.

---

## **7. Records**

| Record / Artifact              | Responsible Owner | Storage Location                            | Retention                          | Control Method                          |
| ------------------------------ | ----------------- | ------------------------------------------- | ---------------------------------- | --------------------------------------- |
| Management Review Record       | Quality Manager   | Controlled QMS Repository | Permanent                          | Version-controlled Markdown or PDF file |
| MR Action Tracker              | Quality Manager   | QMS Repository / Issue Tracker              | Until all actions closed + 3 years | Controlled by Change Control SOP        |
| Updated Policies or Objectives | Quality Manager   | QMS Documents                               | Per document control policy        | Controlled versioning                   |
