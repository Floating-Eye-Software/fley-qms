3. Red Witch Example

Wiki: “Red Witch Development Process”

How to submit issues, use project boards, merge pull requests

Feature descriptions

Architecture diagrams

Examples of sprint planning for Red Witch

Formal SOPs:

“Design Control Process SOP” — explains steps, approvals, traceability requirements, etc.

“Document Change Control SOP” — applies to any project, not just Red Witch

Rule of thumb:

If it’s specific to how Red Witch is done, it goes in the wiki.
If it’s a general procedure that applies to multiple projects or is auditable, it goes in SOPs / controlled documentation.



Great — here’s a **Quality Plan template** you can use alongside your SDP. I’ve kept it structured but lightweight, so it complements the **living SDP** without duplicating it.

---

# **Quality Plan Template**

---

## **1. Introduction**

* **Purpose of the Quality Plan**
  *(Describe why this plan exists — to define how quality will be ensured for the project and organization.)*

* **Scope**
  *(Specify whether this plan is project-specific, e.g. Red Witch, or organization-wide.)*

* **Applicable Standards & Regulations**
  *(e.g., ISO 9001, ISO 9004, IEC 62304, GDPR, ISO 13485, internal SOPs.)*

---

## **2. Quality Objectives**

* **Continuous Improvement:** Complete ISO 9004 self-assessment and identify maturity gaps.
* **Compliance:** Establish and maintain a GDPR-compliant privacy process.
* **Project-Specific Objectives:**

  * Maintain requirements traceability (requirements ↔ code ↔ tests).
  * Achieve ≥95% unit test pass rate before release.
  * Ensure all high-risk requirements undergo formal design review.
* *(Add additional measurable objectives as needed.)*

---

## **3. Quality Processes**

* **Design & Development Quality:**
  *(Reference the Design Control SOP, coding standards, code reviews, testing standards.)*

* **Regulatory Compliance:**
  *(Describe how compliance with GDPR, security requirements, or industry standards will be verified.)*

* **Feedback & Complaints:**
  *(Link to process for handling user complaints and feeding issues back into backlog.)*

---

## **4. Metrics & Measurement**

* **Key Metrics:**

  * Defect density per release
  * Code coverage percentage
  * Audit findings closed within X days
  * Privacy compliance audits completed

* *(List KPIs to be tracked for quality monitoring.)*

* **Measurement Methods:**
  *(Define how and where metrics are collected — e.g., GitHub Actions reports, Jira dashboards, manual audits.)*

---

## **5. Quality Assurance Activities**

* **Reviews:**

  * Code reviews on all pull requests
  * Formal design reviews at milestones

* **Testing:**

  * Unit, integration, and system testing standards
  * Regression testing before each release

* **Audits:**

  * Internal audits of compliance with SOPs
  * GDPR privacy audits
  * ISO 9004 self-assessment

---

## **6. Roles & Responsibilities**

* **Quality Manager / Lead:** Responsible for maintaining the plan and reporting metrics.
* **Developers:** Follow coding standards, document test evidence.
* **Project Manager:** Ensure quality objectives are tracked and reported.
* **Privacy Officer (if applicable):** Oversee GDPR compliance activities.

---

## **7. Records & Documentation**

* **Where records are stored:**

  * Red Witch Wiki (development documentation)
  * GitHub (issues, code, test results)
  * Document Control System (SOPs, audits, compliance evidence)

* **Record Retention:**
  *(Define retention periods for quality records.)*

---

## **8. Continuous Improvement**

* **Improvement Cycles:**

  * Perform ISO 9004 self-assessment annually
  * Capture lessons learned in sprint retrospectives
  * Update SOPs and work instructions based on findings

* **Corrective & Preventive Actions (CAPA):**
  *(Describe how nonconformities and risks lead to corrective actions and process updates.)*

---

## **9. Approval**

* **Authorized By:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
* **Date:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
* **Review Cycle:** *(e.g., annual or per release)*

---

### ✅ How This Fits With Your SDP

* **SDP** → how the *software* is planned, built, tested.
* **Quality Plan** → how *quality and compliance* are ensured (objectives, metrics, audits, GDPR, ISO 9004).

They reference each other but serve distinct purposes.

---

Would you like me to **merge this into a Markdown version**, so you can paste it into the Red Witch wiki alongside the SDP template?





Excellent — let’s frame this as your **first Quality Plan**, written as a forward-looking “design memo” but in the right structure so it can grow into a controlled quality document. It uses **Red Witch as the pilot project** to generate and refine your SOPs, while also embedding the other quality goals you mentioned.

---

# **Quality Plan – Phase 1 (Red Witch Project)**

---

## **1. Purpose**

This plan defines the initial quality objectives and approach for the Red Witch software development project. It establishes Red Witch as both a product development effort and a pilot activity for creating the organization’s quality management framework, including the development of Standard Operating Procedures (SOPs).

---

## **2. Scope**

* **Project-specific:** Red Witch software development activities.
* **Organization-wide quality foundation:** Processes and practices identified in Red Witch will be generalized into SOPs for future projects.
* **Compliance objectives:** Continuous alignment with applicable standards and regulations (ISO 9004, GDPR, ISO/IEC 62304, ISO 9001 as relevant).

---

## **3. Quality Objectives**

1. **Establish SOP Framework through Red Witch:**

   * Use Red Witch’s project-level documents (Software Development Plan, Pull Request Procedure, Risk Management activities, etc.) as inputs for drafting general-purpose SOPs.
   * Identify which practices are repeatable and scalable across projects.
   * Publish first versions of:

     * Design Control SOP
     * Project Management SOP
     * Risk Management SOP
     * Configuration/Change Control SOP

2. **ISO 9004 Self-Assessment:**

   * Perform an organizational self-assessment against ISO 9004 to evaluate quality maturity.
   * Use findings to identify improvement opportunities and align SOP development.

3. **GDPR-Compliant Privacy Process:**

   * Establish a process for handling personal data in compliance with GDPR.
   * Apply this to Red Witch (if applicable) as a test case.
   * Formalize as a Privacy and Data Protection SOP.

4. **Quality Metrics (initial):**

   * Traceability from requirements → code → tests.
   * Pull request review coverage (≥ 1 review per PR).
   * Compliance evidence collected (ISO 9004 self-assessment record, GDPR checklist).

---

## **4. Quality Processes**

* **Development Process:** Governed by the Red Witch Software Development Plan (SDP).
* **Review & Approval:** PR reviews and design reviews are mandatory for all high-risk changes.
* **Feedback Loop:** Lessons learned during Red Witch are captured and classified as either:

  * *Project-specific guidance*, or
  * *Candidate SOP material*.
* **Audit & Assessment:**

  * Internal self-assessment against ISO 9004.
  * GDPR compliance audit for Red Witch project practices.

---

## **5. Responsibilities**

* **Project Manager:** Maintain this plan, coordinate collection of project lessons for SOP development.
* **Developers:** Follow project-level procedures, provide feedback on process strengths/weaknesses.
* **Quality Lead (interim):** Facilitate ISO 9004 self-assessment, GDPR compliance process, and ensure traceability.

---

## **6. Records & Documentation**

* **Red Witch Wiki and GitHub** – repository of project-level procedures, deliverables, and lessons learned.
* **Quality System Folder (to be created):** Storage for draft and finalized SOPs.
* **Assessment Reports:**

  * ISO 9004 self-assessment results
  * GDPR compliance checklist and risk log

---

## **7. Continuous Improvement Plan**

* After Red Witch’s first release, conduct a retrospective focused on process effectiveness.
* Generalize repeatable methods into formal SOP drafts.
* Review and revise this Quality Plan to incorporate new quality objectives.
* Schedule follow-up ISO 9004 self-assessment within 12 months.

---

## **8. Approval**

Authorized by: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
Date: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
Review cycle: Quarterly (until SOPs are established, then annually).

---

✅ This way, the **Red Witch project doubles as a development effort and a process prototype**. You’ll generate both a working product and your first generation of SOPs.

---

Do you want me to also draft a **living “lessons learned → candidate SOP” log template** you can maintain during Red Witch (so you’re systematically capturing what should be generalized)?
