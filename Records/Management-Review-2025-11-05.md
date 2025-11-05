# **Management Review – QMS Launch**

**Date:** 2025-11-05
**Period Covered:** Q4 2025 - QMS Establishment Phase

---

## **1. Review of Previous Actions**

This is the **first Management Review** since QMS implementation.
No previous actions exist.
The review is triggered by completion of the *FLEY-QMS Go-Live* milestone and verification of the controlled baseline (`FLEY-QMS_r1`).

---

## **2. Context and Interested Parties**

* Internal context per *Context-Analysis_r1* remains stable: single-person organization establishing foundational controls.
* External context includes regulatory alignment with ISO 9001 + Amd 1:2024, ISO 13485, IEC 62304, and GDPR.
* **GitHub Inc.** has been identified as a *critical external provider* supporting the controlled QMS repository and electronic records.
  Supplier qualification will occur once the Supplier-Control SOP is released as part of the *Audit-Ready QMS* milestone.

---

## **3. Strategic Direction and QMS Objectives**

### **Purpose and Strategic Intent**

Top Management confirms that the **FLEY QMS** exists to enable design, development, and maintenance of software products that may fall under medical-device and privacy regulations (ISO 13485 / IEC 62304 / GDPR).

### **Primary Objective**

Establish, validate, and operate a compliant Quality Management System as the foundation for regulated product development.

### **Initial QMS Objectives (2025–2026 Planning Horizon)**

1. Complete validation of the QMS intended use through the **Red Witch Pilot SOP Plan**.
2. Maintain and refine the **QMS Design-Control Plan** to define and govern the lifecycle of the QMS itself, including design, validation, and operational maintenance activities.
3. Develop and evolve the **Red Witch Project Quality Plan** to align product design and operations with the validated QMS.
4. Expand SOP coverage and achieve the *Audit-Ready QMS Documentation* milestone once foundational processes are stabilized.

---

## **4. QMS Performance and Effectiveness**

| Element                                      | Summary / Evidence                                                                                                                                   | Reference                   |
| -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- |
| **Customer satisfaction / feedback**         | Not applicable – no released product yet.                                                                                                            | —                           |
| **Quality objectives**                       | All Go-Live objectives achieved; QMS operational and controlled.                                                                                     | Repo-Migration-Plan_r2      |
| **Process performance & product conformity** | All migration PRs, branch protections, and baseline tagging completed successfully.                                                                  | FLEY-QMS Launch Milestone   |
| **Nonconformities / CAPA**                   | One contained nonconformance: *QMS-Authors* user merged PR without review due to GitHub single-user limitation. Root cause confirmed; risk recorded. | GitHub Issue fley-qms #4    |
| **Monitoring & measurement**                 | Metrics framework under development per Quality-Planning SOP.                                                                                        | Continuous-Improvement-Plan |
| **Audits**                                   | None yet; internal audit program to commence post *Audit-Ready QMS* milestone.                                                                       | Audit Schedule (TBD)        |
| **External provider performance**            | GitHub stable and functioning as intended. Supplier evaluation pending.                                                                              | Supplier Evaluation (TBD)   |

**Assessment:**
The QMS is **suitable, adequate, and effective** for its current scope.
Contained nonconformance managed; no active risks affecting operation.

---

## **5. Resources**

* Infrastructure (GitHub organization, repository protections) validated effective.
* Current human and digital resources sufficient for pilot and maintenance phases.
* Supplier-evaluation process to be established for hosted services and collaboration tools as dependencies evolve.

---

## **6. Risks, Opportunities, and Improvements**

| Type            | Description                                                                                           | Action / Status                                                                |
| --------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Risk**        | *Single-Person Approval Constraint* – inherent GitHub limitation on approvals.                        | Record in Risk Register; monitor until multi-reviewer configuration possible.  |
| **Risk**        | *Dependence on GitHub as critical external provider.*                                                 | Add to Risk Register; evaluate under Supplier-Control SOP.                     |
| **Risk**        | *Partial SOP coverage – key processes (CAPA, Audit, Complaint, Supplier Control) not yet documented.* | Track under *Audit-Ready QMS* milestone; complete once QMS Foundations closes. |
| **Opportunity** | Develop and release *Supplier Evaluation and Qualification Procedure*.                                | Planned after QMS Foundations milestone.                                       |
| **Opportunity** | Define QMS KPIs and effectiveness criteria.                                                           | Implement once Continuous-Improvement Plan framework validated.                |
| **Improvement** | Establish recurring Management Review schedule and Action Tracker per MR SOP §6.6.                    | Next review planned after Audit-Ready QMS documentation milestone.             |
| **Improvement** | Refine QMS-Design-Control Plan and Red-Witch-Quality Plan based on pilot feedback.                    | Planned; see §9 Outputs.                                                       |

---

## **7. QMS Lifecycle and Plan Integration**

Management reconfirms the following Quality Plans as the governing structure for the FLEY QMS lifecycle:

| Plan                                  | Purpose                                                                                                       | Current Status                 | Management Decision                                                                                                 |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| **Red-Witch-Pilot-SOP-Plan**          | Active pilot for QMS design-validation and intended-use verification.                                         | Approved / In Execution        | Continue execution under design control.                                                                            |
| **Repo-Migration-Plan**               | Completed corrective design change establishing controlled QMS repository.                                    | Closed / Verified Effective    | Maintain as historical reference.                                                                                   |
| **Continuous-Improvement-Plan**       | Defines ongoing CI and CAPA framework.                                                                        | Active                         | Maintain and integrate metrics per §6.                                                                              |
| **QMS-Design-Control-Plan**        | Defines design-control framework for the QMS itself, covering design, validation, and maintenance activities. | Released r1 (Initial Baseline) | Continue under r1; plan revision r2 to refine scope and lifecycle definitions following QMS Foundations completion. |
| **Red-Witch-Project-Quality-Plan** | Product-specific quality plan aligning Red Witch with validated QMS processes.                                | Draft | Release revision r1 after QMS Foundations milestone.                               |

These plans confirm that the **QMS itself is treated as a controlled product**, with its own design, validation, and maintenance lifecycle.

---

## **8. SOP Coverage and Development Roadmap**

At QMS Launch, **nine foundational SOPs** are active, representing the *minimum operational baseline* required to launch and maintain a functional QMS framework:

1. Change-Control-SOP
2. Document-Control-SOP
3. Identification-and-Traceability-SOP
4. Leadership-SOP
5. Management-Review-SOP
6. Quality-Planning-SOP
7. Risk-and-Opportunity-Management-SOP
8. Project-Management-SOP
9. Design-Control-SOP

**Identified Gaps:**
The following SOPs are essential to achieve full ISO 9001 / 13485 coverage and will be developed as dependencies mature:

* CAPA
* Internal Audit
* Supplier Evaluation and Purchasing
* Training and Competence
* Complaint Handling and Feedback
* Control of Nonconforming Output
* Postmarket Surveillance (as applicable to future products)

These gaps will be closed during the **Audit-Ready QMS Documentation** milestone.
Management confirms that this staged, dependency-driven approach is intentional and risk-managed.

---

## **9. Outputs and Decisions**

| # | Decision / Action                                                                                                 | Owner          | Trigger / Dependency                         | Status  |
| - | ----------------------------------------------------------------------------------------------------------------- | -------------- | -------------------------------------------- | ------- |
| 1 | Record GitHub merge nonconformance and associated risks in Risk Register.                                         | mlehotay       | Immediately post-review                      | Open    |
| 2 | Establish initial Supplier Evaluation criteria for GitHub services.                                               | mlehotay       | After QMS-Foundations completion             | Planned |
| 3 | Define QMS metrics and effectiveness checklist per Quality-Planning SOP.                                          | mlehotay       | After Continuous-Improvement Plan validation | Planned |
| 4 | Prepare next Management Review and internal-audit readiness plan.                                                 | mlehotay       | Following Audit-Ready QMS milestone          | Planned |
| 5 | Refine and release **QMS-Design-Control-Plan r2** to clarify lifecycle definitions.                               | mlehotay       | After QMS-Foundations closure                | Planned |
| 6 | Release **Red-Witch-Project-Quality-Plan_r1** aligned with validated QMS baseline.                                 | mlehotay       | After Audit-Ready QMS documentation          | Planned |
| 7 | Approve continuation of QMS implementation under current set of Quality Plans.                                    | Top Management | Immediate                                    | Closed  |
| 8 | Approve Red Witch project as official pilot for QMS validation and SOP testing.                                   | Top Management | Immediate                                    | Closed  |
| 9 | Develop missing core SOPs (CAPA, Audit, Complaints, Supplier Control, etc.) as part of Audit-Ready QMS milestone. | mlehotay       | After QMS-Foundations closure                | Planned |
| 10 | Update Leadership SOP to describe the organization's casual/dependency-based work culture and how it is controlled within the QMS. | mlehotay | After MR approval    | Planned |


---

## **10. Attachments / References**

**QMS:**  
 * [Management-Review-SOP_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Management-Review-SOP_r1/SOPs/Management-Review-SOP.md)
 * [Quality-Manual_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Quality-Manual_r1/QMS/Quality-Manual.md)
 * [Context-Analysis_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Context-Analysis_r1/QMS/Context-Analysis.md)
 * [Process-Map_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Process-Map_r1/QMS/Process-Map.md)
 * [Organizational-Chart_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Organizational-Chart_r1/QMS/Organizational-Chart.md)
 * [Quality-Policy_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Quality-Policy_r1/QMS/Quality-Policy.md)


**Records:**  
 * [GitHub Issue fley-qms #4](https://github.com/Floating-Eye-Software/fley-qms/issues/4) – Nonconformance Record
 * QMS [Verification of Effectiveness](https://github.com/Floating-Eye-Software/fley-qms/blob/Repo-Migration-Plan_r2/Plans/Repo-Migration-Plan.md#9-verification-of-effectiveness) (2025-11-01)


**Plans:**  
 * [Red-Witch-Pilot-SOP-Plan_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Red-Witch-Pilot-SOP-Plan_r1/Plans/Red-Witch-Pilot-SOP-Plan.md)
 * [Repo-Migration-Plan_r2](https://github.com/Floating-Eye-Software/fley-qms/blob/Repo-Migration-Plan_r2/Plans/Repo-Migration-Plan.md)
 * [Continuous-Improvement-Plan_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/Continuous-Improvement-Plan_r1/Plans/Continuous-Improvement-Plan.md)
 * [QMS-Design-Control-Plan_r1](https://github.com/Floating-Eye-Software/fley-qms/blob/QMS-Design-Control-Plan_r1/Plans/QMS-Design-Control-Plan.md)
 * Red Witch Project Quality Plan (TBD)


**Milestones:**  
 * [FLEY-QMS Launch](https://github.com/Floating-Eye-Software/fley-qms/milestone/1)
 * [QMS Foundations](https://github.com/Floating-Eye-Software/redwitch/milestone/1)
 * [Audit-Ready QMS](https://github.com/Floating-Eye-Software/redwitch/milestone/2)
 * [Compliance Backbone](https://github.com/Floating-Eye-Software/redwitch/milestone/3)
---

## **11. Conclusion**

The inaugural Management Review confirms that:

1. The **QMS has been successfully established** and verified effective for its current scope.
2. Management **formally authorizes continuation** of QMS implementation under existing Quality Plans.
3. The **Red Witch project** is approved as the official pilot for QMS validation and SOP testing.
4. The **QMS-Design-Control-Plan** and **Red-Witch-Project-Quality-Plan** will be refined and executed to complete the design-control lifecycle structure.
5. **Nine foundational SOPs** provide a functional minimum operational framework; missing SOPs will be added under the *Audit-Ready QMS Documentation* milestone.
6. One contained nonconformance has been documented; residual risk remains low and monitored.
7. Supplier-evaluation and KPI framework development are in progress.
8. Progress will remain milestone-driven and flexible, consistent with the organization’s dependency-based work culture.

**Assessment:** ✅ QMS remains *suitable, adequate, and effective* for its current intended purpose.
**Next Management Review:** Triggered by completion of the *Audit-Ready QMS Documentation* milestone.
