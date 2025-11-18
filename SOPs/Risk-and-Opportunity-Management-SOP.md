---
slug: Risk-and-Opportunity-Management-SOP
revision: r2
type: SOP
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/SOPs/Risk-and-Opportunity-Management-SOP.md
---

# **SOP – Risk and Opportunity Management**

# **1. Purpose**

This SOP defines the method for identifying, evaluating, prioritizing, addressing, and reviewing **risks** and **opportunities** that may affect the Quality Management System (QMS), product/service conformity, customer satisfaction, or organizational performance.

It ensures consistent application of **risk-based thinking** per ISO 9001:2015 §6.1.

---

# **2. Scope**

### **2.1 Applicability**

This procedure applies to all QMS-related processes and activities, including:

* Software development and technical operations
* Process and quality planning
* Supplier and external provider management
* Document control
* Strategic and operational decision-making

### **2.2 Exclusions**

This SOP does **not** govern:

* Implementing improvements or changes, which are covered under **Change-Control-SOP**.
* Risk management for medical devices (ISO 14971)

---

# **3. References**

* ISO 9001:2015 — Clause 6.1
* ISO 31000:2018 — Risk Management (informative)
* SOP – Quality Planning
* SOP – Change Control
* SOP – Management Review
* WI – FLEY Action Management
* WI – GitHub-QMS-Setup

---

# **4. Definitions**

| Term                            | Definition                                                                                                                                                     |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Risk**                        | A potential *negative* effect of uncertainty. Risks may affect quality, service conformity, reliability, performance, compliance, or continuity.               |
| **Opportunity**                 | A potential *positive* effect of uncertainty that may lead to improvement if realized.                                                                         |
| **Improvement**                 | A planned and intentional positive change. If an opportunity is approved for implementation, it becomes an Improvement and follows the Change Control process. |
| **Tracked Item / Issue**        | A record used to document a risk or an opportunity in the QMS repository or tracking system.                                                                   |
| **Risk & Opportunity Register** | The controlled list of all active risk and opportunity records.                                                                                                |
| **Risk Level**                  | A qualitative evaluation of *severity × likelihood* (low/medium/high).                                                                                         |

---

# **5. Responsibilities**

| Role                    | Responsibilities                                                                                                                                 | Authority                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Top Management**      | Promote risk-based thinking; review significant risks/opportunities; approve major actions.                                                      | Approve actions affecting QMS strategy or major process changes.   |
| **Quality Manager**     | Maintain the Risk & Opportunity Register; ensure evaluations are appropriate; monitor action effectiveness; escalate as needed.                  | Approve risk assessment methodology and related QMS documentation. |
| **Process Owners**      | Identify risks/opportunities in their processes; perform evaluations; propose and implement mitigation or enhancement actions; maintain records. | Approve and implement actions within their processes.              |
| **All Employees**       | Report new risks; suggest opportunities; support mitigation or improvement activities as assigned.                                               | Request escalation or review of risk concerns.                     |

---

# **6. Procedure**

## **6.1 Identification of Risks and Opportunities**

Risks and opportunities may be identified from:

* Internal audits
* Nonconformances or CAPA activities
* Customer complaints or feedback
* Supplier evaluation or monitoring
* Process performance trends
* New tools, technologies, or infrastructure changes
* Strategic planning and project planning
* Staff suggestions and observations
* Management Review

### 6.1.1 Recording

Each Risk or Opportunity is logged as a **GitHub Issue**, containing:

1. Title
2. Description and context
3. Potential impact (risk) or benefit (opportunity)
4. Initial evaluation
5. Related Issues or linked Plans / Projects
6. Assigned owner

All active items collectively form the **Risk & Opportunity Register**.

## **6.2 Evaluation**

### 6.2.1 Risk Evaluation

Each risk is qualitatively evaluated based on:

* **Severity** — Low / Medium / High
* **Likelihood** — Low / Medium / High

Risks rated as **High** in either dimension require:

* Documented mitigation
* Monitoring
* Review during Management Review

Numerical scoring is optional and not required.

### 6.2.2 Opportunity Evaluation

Opportunities are evaluated for:

* Benefit
* Feasibility
* Effort

Lightweight evaluation is intentionally encouraged.

---

## **6.3 Decision and Response**

After evaluation, the owner selects a disposition.

---

### **6.3.1 Risk Responses**

When addressing risks, the following response types may be used:

* **Mitigate** — Reduce likelihood or severity
* **Avoid** — Modify processes to remove the risk entirely
* **Transfer** — Externalize exposure (e.g., outsourcing, contracts)
* **Accept** — Document decision to accept low or manageable risks

Mitigation actions may be documented:

* Within the same risk record
* As part of Change Control (if the action requires a process change)
* In the Action Tracker (if assigned through Management Review or planning)

---

### **6.3.2 Opportunity Responses**

#### **Option A — Not Pursued**

Reasons may include:

* Insufficient benefit
* Not feasible
* Not aligned with strategy
* Excessive effort for expected value

Closing an opportunity is **not** a nonconformance.

#### **Option B — Pursued**

If approved:

1. Approved opportunities that require planned changes, new controls, or enhancements constitute improvement actions under ISO 9001:2015 §10.1 and are implemented through the Change Control SOP.
2. The Opportunity record is either:
  * converted directly into a Change Request, or
  * linked to a newly created Change Request that will implement the improvement.
3. The opportunity record is updated with a note indicating approval.

---

## **6.4 Monitoring and Review**

The Quality Manager and Process Owners must monitor:

* Status of mitigation or enhancement actions
* Changing relevance of risks/opportunities
* New emerging items from feedback, audits, or changes

Effectiveness is reviewed during:

* Internal Audits
* Process performance reviews
* Management Review

Results are documented in the Risk & Opportunity Register.

---

# **7. Records**


| Record / Artifact               | Owner           | Storage Location                      | Retention              | Control Method                      |
| ------------------------------- | --------------- | ------------------------------------- | ---------------------- | ----------------------------------- |
| Risk & Opportunity Register     | Quality Manager | QMS Repository / Risk Tracking System | 10 years or per policy | Controlled access; revision history |
| Risk Assessments / Action Plans | Process Owners  | Attached to Risk Records              | 10 years               | Controlled record storage           |
| Improvements and Change Records | Quality Manager | Change Control System                 | Permanent              | Linked records / version control    |
| Management Review Outputs       | Top Management  | MR Documentation Repository           | Permanent              | Controlled meeting records          |
| Audit Findings related to Risks | Quality Manager | Audit Reports                         | 10 years               | Controlled repository               |
