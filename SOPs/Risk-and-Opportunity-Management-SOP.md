---
slug: Risk-and-Opportunity-Management-SOP
revision: r2
type: SOP
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/SOPs/Risk-and-Opportunity-Management-SOP.md
---

# **SOP – Risk and Opportunity Management**

## **1. Purpose**

This SOP defines how the organization identifies, evaluates, prioritizes, addresses, and reviews **risks** and **opportunities** that may affect the Quality Management System (QMS), product or service conformity, customer satisfaction, or organizational performance.

This procedure ensures consistent application of **risk-based thinking** in accordance with ISO 9001:2015 §6.1.

---

## **2. Scope**

### **2.1 Applicability**

This SOP applies to all activities within the QMS where risks or opportunities may arise, including:

* Process and quality planning
* Software development and technical operations
* Supplier and external provider management
* Document and data control
* Internal audits and corrective action
* Strategic, operational, and project-level decision-making

### **2.2 Exclusions**

This SOP does **not** govern:

* Product safety risk management for regulated domains (e.g., ISO 14971)

---

## **3. References**

* ISO 9001:2015 — Clause 6.1
* ISO 31000:2018 — Risk Management (informative)
* SOP – Quality Planning
* SOP – Change Control
* SOP – Management Review
* WI – FLEY Action Management
* Relevant platform-specific WIs (e.g., for repository or issue tracking tools)

---

## **4. Definitions**

| Term                            | Definition                                                                                                                           |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Risk**                        | A potential negative effect of uncertainty that may impact quality, conformity, reliability, performance, compliance, or continuity. |
| **Opportunity**                 | A potential positive effect of uncertainty that may enable improvement if realized.                                                  |
| **Improvement**                 | A deliberate positive change. Approved opportunities that lead to changes follow the Change Control SOP.                             |
| **Record**                      | A tracked item maintained in the QMS repository or tracking system that documents a risk or opportunity and its status.              |
| **Risk & Opportunity Register** | The controlled list of all active risk and opportunity records.                                                                      |
| **Risk Level**                  | A qualitative evaluation of *severity × likelihood* (Low / Medium / High).                                                           |

---

## **5. Responsibilities**

| Role                | Responsibilities                                                                                                                       | Authority                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **Top Management**  | Promote risk-based thinking; review significant risks and opportunities; approve major actions or escalations.                         | Approve actions affecting QMS strategy or significant changes.       |
| **Quality Manager** | Maintain the Risk & Opportunity Register; ensure evaluations are consistent; monitor action effectiveness; escalate high-impact items. | Approve risk assessment method and related procedural documentation. |
| **Process Owners**  | Identify risks and opportunities in their processes; evaluate and maintain related records; propose and implement actions.             | Approve and execute actions within their process areas.              |
| **All Personnel**   | Report risks and propose opportunities; participate in mitigation or enhancement activities.                                           | Request review or escalation of risk concerns.                       |

---

## **6. Procedure**

### **6.1 Identification**

Risks and opportunities may be identified through:

* Internal audits and assessments
* Nonconformities, incidents, or CAPA activities
* Customer complaints or feedback
* Supplier or external provider monitoring
* Performance metrics or trend analysis
* Planning activities (strategic, operational, or project-based)
* Staff suggestions
* Process reviews and Management Reviews

#### **6.1.1 Recording**

Each risk or opportunity is documented as a **record in the QMS tracking system**, capturing at minimum:

1. Title
2. Description and context
3. Potential impact (risk) or potential benefit (opportunity)
4. Initial evaluation (severity, likelihood, or benefit)
5. Owner
6. Related QMS elements (processes, plans, changes, or other records)

The set of all active records forms the **Risk & Opportunity Register**.

> *Tool-specific fields or templates are defined in Work Instructions, not in this SOP.*

### **6.2 Evaluation**

#### **6.2.1 Risk Evaluation**

Each risk is assessed qualitatively based on:

* **Severity** — Low / Medium / High
* **Likelihood** — Low / Medium / High

Risks with **High severity** or **High likelihood**, or both, require:

* Documented response
* Monitoring
* Inclusion as an input to Management Review
* Consideration in planning and decision-making

*Numerical scoring is optional and not required.*

#### **6.2.2 Opportunity Evaluation**

Opportunities are evaluated for:

* Potential benefit
* Feasibility
* Effort or resource requirement

Evaluations are intentionally lightweight unless the opportunity is pursued.

### **6.3 Decision and Response**

After evaluation, the owner selects an appropriate response.

#### **6.3.1 Responses to Risks**

Valid responses include:

* **Mitigate** – Reduce likelihood or severity
* **Avoid** – Change processes to eliminate the risk
* **Transfer** – Shift the exposure (e.g., contractual or supplier-based controls)
* **Accept** – Retain the risk with justification, typically for low-level risks

Actions may be documented:

* Within the risk record
* As part of Change Control (when the action requires a process change)
* Through action-tracking records (e.g., corrective actions, planned actions)

#### **6.3.2 Responses to Opportunities**

**Option A - Not Pursued**
A decision may be made to not pursue an opportunity for reasons such as limited benefit, low feasibility, resource constraints, or misalignment with strategy.

Closing an opportunity is **not** a nonconformance.

**Option B — Pursued**
When approved:

1. The opportunity becomes an **improvement activity** per ISO 9001:2015 §10.1.
2. If implementation requires changes, a **Change Request** is created through the Change Control SOP.
3. The opportunity record is updated to reference the resulting plan or change record.

### **6.4 Monitoring and Review**

The Quality Manager and Process Owners monitor:

* The status of mitigation or enhancement actions
* Changes in likelihood, severity, or relevance
* New risks or opportunities emerging from process performance

Effectiveness of actions is reviewed during:

* Internal audits
* Process reviews
* Quality Planning and Change Control
* Management Review

The Risk & Opportunity Register is updated accordingly.

---

## **7. Records**

| Record / Artifact            | Owner           | Storage Location                 | Retention                   | Control Method                |
| ---------------------------- | --------------- | -------------------------------- | --------------------------- | ----------------------------- |
| Risk & Opportunity Register  | Quality Manager | QMS Repository / Tracking System | Per document control policy | Revision-controlled list      |
| Risk and Opportunity Records | Process Owners  | Stored with the tracking system  | Per policy                  | Controlled record management  |
| Related Change Records       | Quality Manager | Change Control System            | Permanent                   | Linked record control         |
| Management Review Outputs    | Top Management  | Management Review Repository     | Permanent                   | Controlled leadership records |
| Audit Findings               | Quality Manager | Audit Reports                    | Per audit record policy     | Controlled repository         |
