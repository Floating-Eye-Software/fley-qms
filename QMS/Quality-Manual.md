# **QMS - Quality Manual – Floating Eye Software (FLEY)**

**Slug:** Quality-Manual  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Quality-Manual  

---

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

See [[Context Analysis]] for the full organizational context.

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

See also the approved [[Quality Policy]] for FLEY’s top-level commitments.

---

## **5. QMS Workflows**

FLEY’s QMS consists of three interrelated workflows:

| Workflow                            | Description                                                 | Key SOP / WI              | Example Outputs                                         |
| ----------------------------------- | ----------------------------------------------------------- | ------------------------- | ------------------------------------------------------- |
| **QMS Creation**                    | Establishing and documenting the framework                  | [[Quality Planning SOP]]  | SOPs, Quality Manual, initial audit                     |
| **QMS Operation**                   | Maintaining, monitoring, auditing, and improving the system | [[GitHub QMS Operations]] | Context updates, Risk Register, CAPA, Improvement logs  |
| **Product Development (Red Witch)** | Designing, developing, and maintaining Red Witch            | [[Design Control SOP]]    | Design records, verification results, release artifacts |

The three workflows operate cyclically and interdependently:

 * The **QMS Creation** workflow defines and documents the structure of the management system.
 * The **QMS Operation** workflow maintains, monitors, and improves that structure over time.
 * The **Product Development** workflow applies the QMS framework to the Red Witch product lifecycle.

For a high-level visual of workflows and interactions, see [[Process Map]].

---

## **6. Process Approach, PDCA, and Risk-Based Thinking**

* **Process Approach:** Enables planning and interaction of all QMS processes
* **PDCA Cycle:**

  * **Plan:** Define context, objectives, risks
  * **Do:** Implement processes per SOPs and WIs
  * **Check:** Monitor, audit, and analyze results
  * **Act:** Apply improvements, corrective actions, and updates
* **Risk-Based Thinking:** Identifies factors that could cause deviations, guiding preventive controls and opportunity capture

QMS Processes and their interactions are defined in [[Process Map]].

---

## **7. Roles and Responsibilities**

| Role                           | Key Responsibilities                                    |
| ------------------------------ | ------------------------------------------------------- |
| **Top Management / QMS Owner** | Leadership, policy, objectives, management review       |
| **Quality Manager**            | Maintains QMS, audits, risk register, change control    |
| **Project Manager**            | Plans and tracks product development                    |
| **Process Owner**              | Oversees operational processes, ensures documentation   |
| **All Employees**              | Follow procedures, report issues, engage in improvement |

Detailed roles are documented in [[Organizational Chart]].

---

## **8. Risk and Opportunity Management**

* Managed via a **GitHub-based Risk Register** covering:

  * Product risks (safety, privacy, reliability)
  * QMS risks (resource, documentation, climate)
  * Improvement opportunities (automation, maturity growth)
* Reviewed during **Management Review**
* Mitigation and improvement actions documented in [[Quality Planning SOP]] and [[Continuous Improvement Plan]]

---

## **9. Documentation Structure**

| Level       | Description                                           | Examples                                               |
| ----------- | ----------------------------------------------------- | ------------------------------------------------------ |
| **Level 1** | Quality Manual (this document) and [[Quality Policy]] | Top-level commitments and framework                    |
| **Level 2** | SOPs                                                  | Leadership SOP, Planning SOP, Design & Development SOP |
| **Level 3** | WIs / Records                                         | GitHub QMS Operation WI, Project boards                |
| **Level 4** | Forms / Evidence                                      | Risk Register, Audit logs, Meeting minutes             |

All documents are controlled per [[Document Control SOP]].

---

## **10. Management Review and Continual Improvement**

* Conducted annually or following major releases
* Inputs: Context updates, audit results, KPI performance, user feedback, risk changes, climate considerations
* Outputs: Action plans, improvement projects, resource adjustments
* Logged in [[Continuous Improvement Plan]] and [[GitHub QMS Operations]]

---

## **11. References**

* ISO 9001:2015 + Amendment 1:2024 (Climate Action)
* ISO 9000:2015 – Fundamentals & Vocabulary
* GDPR (2016/679) – Privacy reference
* Internal QMS SOPs, Work Instructions, and Records
* [[Quality Policy]] – Top-level commitment statement

---

## **12. Revision and Control**

* This manual is **controlled** and maintained in the QMS repository.
* Revisions are approved by the QMS Owner and tracked in the Document Control Register.

---

### **Appendix A — Workflow Links & Kanban Boards**

| Workflow                        | Reference / Link          | Kanban Board                                              |
| ------------------------------- | ------------------------- | --------------------------------------------------------- |
| QMS Creation                    | [[Quality Planning SOP]]  | [FLEY QMS](https://github.com/users/mlehotay/projects/3)  |
| QMS Operation                   | [[GitHub QMS Operations]] | [FLEY QMS](https://github.com/users/mlehotay/projects/3)  |
| Product Development (Red Witch) | [[Design Control SOP]]    | [Red Witch](https://github.com/users/mlehotay/projects/4) |
