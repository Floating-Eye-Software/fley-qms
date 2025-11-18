**Slug:** Plan-Issue-Type-Rollout
**Revision:** r1
**Effective Date:** 2025-11-17
**Related SOP:** Quality-Planning-SOP
**Controlled Source:** [https://github.com/Floating-Eye-Software/fley-qms/blob/main/Templates/Quality-Plan-Template.md](https://github.com/Floating-Eye-Software/fley-qms/blob/main/Templates/Quality-Plan-Template.md)

---

# PLAN - Implement Plan Issue Type

## **1. Introduction**

* **Purpose:**
  Implement a formal **Plan Issue Type** in GitHub to serve as the governing record for all QMS Plans, including **Management Reviews**, major initiatives, and structured improvement activities. The Plan Issue Type will standardize planning, execution, and verification of effectiveness (VoE) across the QMS.

* **Scope:**
  Applies organization-wide for all QMS Plans, including MR cycles, improvement initiatives, and roadmap-driven projects executed in GitHub.

* **Applicable Standards & Regulations:**

  * ISO 9001:2015 (Quality Management Systems – Planning & Review)
  * Internal SOPs: Quality-Planning-SOP, Management-Review-SOP
  * WI – FLEY-Action-Management
  * WI – GitHub-QMS-Setup

---

## **2. Quality Objectives**

* Ensure all Plans are captured as `type:Plan` GitHub Issues.
* Enable milestone-driven visibility of QMS Plans on the roadmap.
* Standardize Verification of Effectiveness (VoE) at the Plan level.
* Improve traceability from Plan → actions → MR input → VoE results.
* Align all planning and execution with ISO 9001 requirements.
* Minimize ad-hoc, unstructured grouping of work.

---

## **3. Quality Processes**

* Create new `type:Plan` Issue Type in GitHub.
* Update templates: Quality-Plan-Template (document) and TPL-GH-Plan (issue template).
* Integrate Plan Issue Type into Management Review execution.
* Link milestones and dependent work for all Plans.
* Update supporting procedures (SOPs, WIs) to incorporate Plan Issue Type and related workflows.
* Establish bidirectional dependency framework (`blocks` / `blocked-by`) for traceability.

---

## **4. Metrics & Measurement**

* **Plan Coverage:** Number of active Plans versus total planned QMS activities.
* **Template Adoption:** Percentage of new Plans using the updated `type:Plan` templates.
* **VoE Completion Rate:** Percentage of Plans with completed VoE verification.
* **MR Integration:** Number of MR cycles executed via Plan Issue Type.
* **Audit Findings:** Number of nonconformities linked to Plan execution or documentation.

*Measurement Methods:*

* GitHub Issue labels, milestones, and project board reports.
* Internal audits of Plan Issue records and linked actions.
* Verification of VoE documentation and MR outputs.

---

## **5. Quality Assurance Activities**

* Conduct design reviews of Plan templates and SOP updates.
* Review all updated SOPs and WIs prior to rollout.
* Execute internal audits on a sample of Plan Issues.
* Test milestones, dependencies, and roadmap visibility in GitHub Projects.
* Conduct MR cycle using Plan Issues as a pilot to verify process compliance.

---

## **6. Roles & Responsibilities**

* **Quality Manager:** Approve Plan Issue Type rollout, verify compliance, and review VoE results.
* **Project Manager / Owner:** Implement Plan Issue Type, ensure templates and SOPs are updated, and manage rollout.
* **Development / Operations Team:** Create Plan Issues, link milestones, execute implementation tasks.
* **Privacy / Compliance Representative:** Verify regulatory and QMS compliance across Plan workflows.

---

## **7. Records & Documentation**

* GitHub Issues (`type:Plan`) and linked issues for milestones and dependencies.
* Updated SOPs: Quality-Planning-SOP, Management-Review-SOP.
* Work Instructions: WI – FLEY-Action-Management, WI – GitHub-QMS-Setup.
* Retention: Per internal document control policy (typically 5 years for QMS records).

---

## **8. Linkage to Execution**

* **Milestones:**

  * Plan Issue creation
  * Template updates
  * SOP and WI revisions
  * MR pilot cycle
  * VoE verification
* **Project Board / Tracking Tool:** GitHub Projects (Kanban/Roadmap view).
* **Pull Requests:** PRs updating templates, SOPs, and WIs.
* **Issues / CAPA:** Link MR outputs, improvement actions, and audit findings to Plan Issues.

---

## **9. Verification of Effectiveness**

* **Verification Date:** 2025-12-31

* **Summary:**

  * Confirm all Plan Issues are created, linked to milestones, and appear on the roadmap.
  * Validate MR cycles are executed via Plan Issue Type.
  * Ensure updated templates, SOPs, and WIs are approved and merged.
  * Confirm VoE for at least one Plan is completed and documented.

* **Evidence:**

  * Completed Plan Issues with milestones and dependencies in GitHub.
  * MR outputs linked to Plan Issues.
  * Signed-off SOPs and WIs.
  * VoE verification documentation.

* **Follow-up:**

  * Track residual issues and lessons learned.
  * Plan further refinements for broader adoption and continuous improvement.

* **Assessment:** Effective
