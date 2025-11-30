---
slug: Quality-Manual
revision: r2
type: QMS
status: draft
effective: null
controlled_source: https://github.com/Floating-Eye-Software/fley-qms/blob/main/QMS/Quality-Manual.md
---

# **QMS - Quality Manual – Floating Eye Software (FLEY)**

## **1. Purpose**

This Quality Manual defines the structure, scope, and operation of the Quality Management System (QMS) for **Floating Eye Software (FLEY)**.

The QMS is aligned with **ISO 9001:2015**, including **Amendment 1:2024 (Climate Action)**, and incorporates:

* **Process approach**
* **Plan-Do-Check-Act (PDCA) cycle**
* **Risk-based thinking**

The QMS ensures that activities under its scope are **planned, implemented, monitored, and continually improved** to meet customer, regulatory, and ethical requirements.

---

## **2. Organization Overview**

FLEY is a **sole proprietorship**, founded in 2021 in Toronto, Canada.
It develops ethical, privacy-first digital tools. Non-QMS activities (NetHack servers, blogs, websites) are **outside the QMS**.

The **Red Witch** project is the first initiative formally managed under the QMS.

See [Context Analysis](Context-Analysis.md) for the full organizational context.

---

## **3. QMS Scope**

The QMS applies to all **Red Witch–related activities** impacting:

* Product safety, quality, and effectiveness
* User privacy and data protection
* Regulatory compliance

**Activities Covered:**

* Software, product, and system design & development
* Project and operational execution
* Risk management and quality planning
* Verification, validation, and release activities
* Post-release maintenance, retirement, and CAPA tracking

**Boundaries:**

* Excludes non-Red Witch FLEY activities (NetHack, blogs, etc.)
* All ISO 9001 clauses apply. No exclusions are claimed.

---

## **4. Organizational Identity**

**Purpose**

Floating Eye Software (FLEY) exists to **empower individuals to manage and understand uterine health** through **private, safe, and effective** digital solutions that respect autonomy and dignity.

**Values**

FLEY’s work is guided by a commitment to:

* **Ethics and Privacy:** Protecting user data and personal information as a fundamental right.
* **Transparency:** Ensuring that processes, algorithms, and intentions are openly communicated.
* **Inclusivity:** Serving all individuals affected by uterine health needs, regardless of gender identity or background.
* **Integrity and Quality:** Building trustworthy tools that prioritize user well-being over profit or exploitation.
* **Sustainability:** Considering environmental and social impacts in all operational decisions.

**Strategic Direction**

FLEY will **develop and maintain free, ethical, privacy-first digital tools**, beginning with *Red Witch*, while progressively aligning with **regulatory and ethical standards** as the organization grows.

See also the approved [Quality Policy](Quality-Policy.md) for FLEY’s top-level commitments.

---

## **5. QMS Workflows**

FLEY’s QMS consists of three interrelated workflows:

| Workflow                            | Description                                                 | Key SOP / WI              | Example Outputs                                         |
| ----------------------------------- | ----------------------------------------------------------- | ------------------------- | ------------------------------------------------------- |
| **QMS Creation**                    | Establishing and documenting the framework                  | [Quality Planning SOP](../SOPs/Quality-Planning-SOP.md)  | SOPs, Quality Manual, initial audit                     |
| **QMS Operation**                   | Maintaining, monitoring, auditing, and improving the system | [GitHub QMS Operations](../WIs/GitHub/GitHub-QMS-Operations.md) | Context updates, Risk Register, CAPA, Improvement logs  |
| **Product Development (Red Witch)** | Designing, developing, and maintaining Red Witch            | [Design Control SOP](../SOPs/Design-Control-SOP.md)    | Design records, verification results, release artifacts |

The three workflows operate cyclically and interdependently:

 * The **QMS Creation** workflow defines and documents the structure of the management system.
 * The **QMS Operation** workflow maintains, monitors, and improves that structure over time.
 * The **Product Development** workflow applies the QMS framework to the Red Witch product lifecycle.

For a high-level visual of workflows and interactions, see [Process Map](Process-Map.md).

---

## **6. Process Approach, PDCA, and Risk-Based Thinking**

* **Process Approach:** Enables planning and interaction of all QMS processes
* **PDCA Cycle:**

  * **Plan:** Define context, objectives, risks
  * **Do:** Implement processes per SOPs and WIs
  * **Check:** Monitor, audit, and analyze results
  * **Act:** Apply improvements, corrective actions, and updates
* **Risk-Based Thinking:** Identifies factors that could cause deviations, guiding preventive controls and opportunity capture

QMS Processes and their interactions are defined in [Process Map](Process-Map.md).

---

## **7. Roles and Responsibilities**

| Role                           | Key Responsibilities                                    |
| ------------------------------ | ------------------------------------------------------- |
| **Top Management / QMS Owner** | Leadership, policy, objectives, management review       |
| **Quality Manager**            | Maintains QMS, audits, risk register, change control    |
| **Project Manager**            | Plans and tracks product development                    |
| **Process Owner**              | Oversees operational processes, ensures documentation   |
| **All Employees**              | Follow procedures, report issues, engage in improvement |

Detailed roles are documented in [Organizational Chart](Organizational-Chart.md).

---

## **8. Risk and Opportunity Management**

* Identified through audits, incidents, CAPAs, feedback, metrics, planning, and process reviews.
* Risks are assessed for **severity** and **likelihood**; significant items require documented actions and MR review.
* Opportunities are evaluated for **benefit** and **feasibility**; pursued items follow the **Change Control SOP**.
* Risk responses: **mitigate**, **avoid**, **transfer**, or **accept**. Actions are tracked in the Risk Register or related change records.
* Action effectiveness is monitored by the Quality Manager and Process Owners and reviewed in **Management Review**.

Risks and Opportunities are documented and managed per [Risk and Opportunity Management SOP](../SOPs/Risk-and-Opportunity-Management-SOP.md).

---

## **9. Documentation Structure**

| Level       | Description                                           | Examples                                               |
| ----------- | ----------------------------------------------------- | ------------------------------------------------------ |
| **Level 1** | Quality Manual (this document) and [Quality Policy](Quality-Policy.md) | Top-level commitments and framework                    |
| **Level 2** | SOPs                                                  | Leadership SOP, Planning SOP, Design & Development SOP |
| **Level 3** | WIs / Records                                         | GitHub QMS Operation WI, Project boards                |
| **Level 4** | Forms / Evidence                                      | Risk Register, Audit logs, Meeting minutes             |

All documents are controlled per [Document Control SOP](../SOPs/Document-Control-SOP.md).

---

## **10. Management Review and Continual Improvement**

Improvement is achieved through corrective actions, results of risk/opportunity management, management review decisions, and achievement of quality objectives.
The organization conducts **Management Reviews** to evaluate the continuing suitability, adequacy, and effectiveness of the Quality Management System (QMS) and to drive continual improvement.
Management Reviews are performed according to the [Management Review SOP](../SOPs/Management-Review-SOP.md).

### **10.1 Review Frequency and Triggers**

Management Review follows an **event-driven, dependency-based review-cycle**, initiated when one or more defined triggers occur (e.g., completion of major initiatives, maturity milestones, or significant risks/nonconformities).
If no trigger occurs within twelve (12) months, a review is held proactively to maintain conformance with ISO 9001:2015 §9.3.

Top Management confirms the start of each review cycle.

---

## **11. References**

* ISO 9001:2015 + Amendment 1:2024 (Climate Action)
* ISO 9000:2015 – Fundamentals & Vocabulary
* GDPR (2016/679) – Privacy reference
* Internal QMS SOPs, Work Instructions, and Records
* [Quality Policy](Quality-Policy.md) – Top-level commitment statement

---

## **12. Revision and Control**

* This manual is **controlled** and maintained in the QMS repository.
* Revisions are approved by the QMS Owner and tracked in the Document Control Register.

---

### **Appendix A — Workflow Links & Kanban Boards**

| Workflow                        | Reference / Link          | Kanban Board                                              |
| ------------------------------- | ------------------------- | --------------------------------------------------------- |
| QMS Creation                    | [Quality Planning SOP](../SOPs/Quality-Planning-SOP.md)  | [FLEY QMS](https://github.com/orgs/Floating-Eye-Software/projects/1)  |
| QMS Operation                   | [GitHub QMS Operations](../WIs/GitHub/GitHub-QMS-Operations.md) | [FLEY QMS](https://github.com/orgs/Floating-Eye-Software/projects/1)  |
| Product Development (Red Witch) | [Design Control SOP](../SOPs/Design-Control-SOP.md)    | TBD |
