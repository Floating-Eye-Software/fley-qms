# Red Witch Work Instructions

## **1. Purpose**
This document defines standardized work instructions for Red Witch development, including design control, project management, change control, risk management, and quality processes. All activities align with:

- Ontario Digital Service Standard (DSS)
- ISO 9001 / ISO 90003 (QMS and software)
- IEC 62304 / IEC 62366 / ISO 82304 (health software)
- ISO 13485 / ISO 14971 (medical device quality & risk)
- ISO/IEC 27001 / 27701 (information security & privacy)
- FDA 21 CFR Part 11 (electronic records)

It integrates GitHub tools for **collaboration, version control, workflow automation, and traceability**.

---

## **2. Scope**
Applies to all contributors and activities in the Red Witch project:

- Software development (Android, iOS, Web)
- Feature design, testing, and maintenance
- Risk and change management
- Traceability and documentation
- Governance and compliance with regulatory frameworks

---

## **3. Roles & Responsibilities**

| Role | Responsibilities |
|------|-----------------|
| Project Manager | Maintain Work Instructions, coordinate QMS compliance, manage Kanban board and sprint planning |
| Developers | Implement features per Branching Policy, submit PRs, follow traceability procedures |
| Reviewer(s) | Review PRs for quality, security, traceability, and regulatory compliance |
| Quality Lead | Facilitate audits, ISO/IEC compliance checks, SOP alignment |
| Product Manager | Define user needs, prioritize backlog, approve features |

---

## **4. DSS Phase-Based Workflow**

### **Discovery Phase**
- Conduct user research and identify primary user groups
- Capture requirements, personas, and barriers
- Document findings in Red Witch Wiki
- Assign Product Manager
- Establish Agile workflow with GitHub Projects (Kanban)

**Deliverables:**
- User research report
- Market/regulatory/feasibility research
- Agile Kanban board setup

### **Alpha Phase**
- Co-create solutions with stakeholders
- Build multiple prototypes and test with users
- Validate technical and financial feasibility
- Identify required process or policy changes
- Produce usability report and journey map

**Deliverables:**
- Tested prototypes and mockups
- Journey map of user experience
- Initial project plan with technical, financial, and service updates

### **Beta Phase**
- Build Minimum Viable Product (MVP) for live testing
- Perform device validation on all platforms
- Continuous usability and accessibility testing (WCAG, inclusive design)
- Measure KPIs and update features based on feedback
- Maintain privacy & security report

**Deliverables:**
- MVP with automated testing
- Accessibility testing reports
- Privacy & security documentation
- Maintenance and disaster recovery plans

### **Live Phase**
- Ongoing feature development and maintenance
- Monitor KPIs and collect user feedback
- Conduct usability testing every 3–4 months
- Ensure DSS and regulatory compliance
- Publish useful open data as applicable

**Deliverables:**
- Service maintenance logs
- Performance and analytics reports
- Updated SOPs and lessons learned

---

## **5. GitHub Tools & Workflow**

### **5.1 Repositories**
- Store all project source code, documentation, and assets in GitHub
- Maintain clear repository structure
- Apply GitFlow for branching (main, develop, feature/*, release/*, hotfix/*)
- Use descriptive commit messages for traceability

### **5.2 Issues**
- Track tasks, bugs, and features via GitHub Issues
- Include detailed descriptions, steps to reproduce, and expected outcomes
- Assign issues, apply labels, and link to PRs and project boards

### **5.3 Pull Requests**
- Create PRs for all changes to `main`
- Include related issue reference, testing summary, and impact analysis
- Require at least one reviewer (two for high-risk changes)
- CI/CD checks must pass before merge
- Use **Squash & Merge** and delete feature branch after merge
- Update linked issues and Kanban board

### **5.4 Discussions**
- Use GitHub Discussions for stakeholder and community engagement
- Document ideas, feedback, and decisions

### **5.5 Actions**
- Automate CI/CD testing for all commits and PRs
- Configure deployment pipelines (staging/production)
- Implement monitoring and alerts for failures

### **5.6 Projects**
- Use Kanban boards to visualize workflow
- Track milestones and categorize tasks with labels
- Update progress as tasks move from *To Do* → *In Progress* → *Done*

### **5.7 Wiki**
- Central repository for design documents, SOPs, and FAQs
- Maintain versioned, structured documentation

### **5.8 Security**
- Enable dependency scanning and vulnerability alerts
- Regularly update dependencies and fix identified issues
- Maintain logs and audit trails for compliance (ISO 27001 / 27701 / 21 CFR Part 11)

### **5.9 Insights**
- Monitor contributor activity, repository traffic, and KPIs
- Adjust workflows based on metrics

### **5.10 Repository Settings**
- Configure access control according to role
- Manage integrations for automated workflows

---

## **6. Risk Management**
- Maintain Risk Log per feature/sprint
- Identify hazards and implement mitigation strategies (ISO 14971 / IEC 62304)
- Review risks at each sprint planning session

---

## **7. Change & Configuration Management**
- Follow GitFlow branching and PR review procedures
- Tag releases and maintain version history
- Track changes in configuration management records
- Update all affected documentation

---

## **8. Quality & Verification**
- Perform unit, integration, and automated testing
- Document results in Wiki and CI/CD reports
- Maintain traceability: Requirements → Code → Tests → Validation
- Conduct retrospective reviews to improve processes

---

## **9. Security & Privacy**
- Implement ISO/IEC 27001 & 27701 controls
- Conduct GDPR/PHIPA assessments
- Maintain privacy and security reports per sprint
- Monitor and log all access and system changes

---

## **10. Documentation & Records**
- All project documentation stored in:
  - GitHub Wiki
  - SDP and SOPs
  - Risk logs and QA reports
- Maintain versioned history for audit purposes
- Include evidence for ISO, IEC, and FDA compliance

---

## **11. Training & Support**
- Developers and stakeholders trained on SOPs, GitFlow, DSS workflow, and accessibility guidelines
- Maintain onboarding guides and training records
- Document support tickets and issue resolution

---

## **12. Continuous Improvement**
- Retrospectives every sprint
- Lessons learned → update SOPs and work instructions
- Conduct periodic audits and ISO 9004/ISO 90003 self-assessments

---

## **13. References**
- [Ontario DSS / Service Design Playbook](https://www.ontario.ca/page/service-design-playbook)  
- [ISO 9001 / ISO 90003](https://www.iso.org/standard/62085.html)  
- [IEC 62304 / IEC 62366 / ISO 82304](https://www.iso.org/standard/72342.html)  
- [ISO 13485 / ISO 14971](https://www.iso.org/standard/59752.html)  
- [ISO/IEC 27001 / 27701](https://www.iso.org/standard/73906.html)  
- [FDA 21 CFR Part 11](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/part-11-electronic-records-electronic-signatures)

---


Yes — that’s exactly the right move. Right now your **ODF (Ontario Digital Framework) Work Instructions** are excellent for public-sector service design, but they’re *missing the regulatory rigor* from the org-level **SDLC SOP** (ISO 13485, IEC 62304, 62366, 14971, 27001/27701, GDPR, AAMI TIR45).

What I can do is **revise and extend the Red Witch Work Instructions** so they:

* **Keep the ODF/DSS phases** (Discovery, Alpha, Beta, Live) to stay aligned with Ontario’s framework, **and**
* **Embed the regulatory SDLC artifacts and activities** (SRS, Intended Use, Risk Log, Usability File, Traceability Matrix, Release Package, CAPA, etc.) so they are compliant with your org SOP.

Here’s a merged version:

---

# **Red Witch Work Instructions (Aligned with Org SDLC SOP)**

## **1. Purpose**

This document defines standardized work instructions for Red Witch development, combining:

* **Ontario Digital Service Standard (DSS)** phases for public-sector service design
* **Regulatory-compliant SDLC SOP** (ISO 13485, IEC 62304, IEC 62366, ISO 14971, ISO/IEC 27001/27701, GDPR, AAMI TIR45)

It ensures:

* User-centered design (per DSS/ODF)
* Regulatory-grade quality, risk, usability, and security processes
* Full traceability from requirements → stories → commits → tests → results

---

## **2. Scope**

Applies to all contributors and activities in the Red Witch project, covering:

* Software development (Android, iOS, Web)
* Requirements, risk, and change management
* Usability, accessibility, and safety validation
* Documentation and regulatory evidence generation
* Governance and compliance with regulatory frameworks

---

## **3. Roles & Responsibilities**

*(expanded to include regulatory oversight)*

| Role                  | Responsibilities                                                                                       |
| --------------------- | ------------------------------------------------------------------------------------------------------ |
| Project Manager       | Maintain Work Instructions, manage DSS/SDLC compliance, Kanban & sprint planning, phase exit approvals |
| Product Manager       | Define intended use, user needs, backlog priorities, approve features                                  |
| Business Analyst      | Document requirements (Confluence SRS), maintain traceability                                          |
| Developers            | Implement features, follow branching policy, commit with requirement/story IDs                         |
| Reviewer(s)           | Review PRs for quality, traceability, and compliance                                                   |
| Quality Lead          | Maintain QMS alignment, risk file, usability engineering file, CAPA                                    |
| Security/Privacy Lead | Ensure compliance with ISO 27001/27701, GDPR/PHIPA                                                     |
| Technical Writer      | Maintain documentation, release notes, training guides                                                 |

---

## **4. DSS Phase-Based Workflow (Mapped to SDLC SOP)**

### **Discovery Phase (Planning Phase in SOP)**

* Conduct user research (personas, barriers, needs) → **Confluence Requirements Document** (`REQ-###`)
* Define intended use and intended users (SOP 13485/62304)
* Identify hazards, safety classification (ISO 14971, IEC 62304) → **Initial Risk Log**
* Document market/regulatory feasibility
* Create product backlog in Jira → link each story to requirement ID
* Set coding/testing standards in Confluence
* Assign Product Manager

**Deliverables:**

* Requirements Specification (Confluence, version-controlled)
* Intended Use Statement
* Initial Risk Log (Confluence or Jira Risk Register)
* Traceability Matrix (Req ↔ Jira Story)

---

### **Alpha Phase (Development Phase – Early Iterations)**

* Co-create solutions with stakeholders
* Build and test multiple prototypes
* Develop **high-level architecture** (Confluence Architecture Doc)
* Refine requirements, update SRS and Risk Log
* Create Jira stories linked to requirements, branches in Git
* Implement usability engineering activities (journey maps, use-error analysis → Usability File)
* Define verification & validation strategy in Confluence

**Deliverables:**

* Architecture Document
* Usability Engineering File (draft)
* Updated Risk Log
* Traceability Matrix (Req ↔ Story ↔ Branch)
* Tested Prototypes

---

### **Beta Phase (Development → Release Prep)**

* Build MVP with validated safety/functional features
* Create Git branches for each story, commits referencing Jira ID + REQ ID
* Implement automated/manual tests, link Jira Test Cases to requirements
* Perform device validation and accessibility testing (WCAG, inclusive design)
* Maintain **Privacy & Security Report** (Confluence)
* Conduct sprint risk reviews → update mitigation strategies
* Conduct interim usability validation

**Deliverables:**

* Minimum Viable Product
* Updated Traceability Matrix (Req ↔ Story ↔ Commit ↔ Test Case ↔ Result)
* Risk Management File (per ISO 14971)
* Usability Engineering File (IEC 62366)
* Privacy & Security Documentation
* Test Evidence Reports

---

### **Live Phase (Release + Maintenance)**

* Create Release Branch in Git
* Conduct UAT → log results in Jira linked to requirements
* Compile Release Package (SRS, Risk Review, Traceability, Test Results, Release Notes) in Confluence
* Obtain regulatory sign-off before production release (per SOP)
* Post-release: continuous monitoring, feedback capture, CAPA process
* Perform usability validation every 3–4 months
* Maintain PMS (Post-Market Surveillance) plan in Confluence

**Deliverables:**

* Release Package (tagged in Git, documented in Confluence)
* Final Traceability Matrix
* CAPA Records (linked to Jira Issues)
* Service Maintenance Logs, Analytics Reports
* Periodic Usability & Risk Review Reports

---

## **5. Traceability Workflow (Git + Jira + Confluence)**

* **Requirements**: Confluence → assigned IDs (`REQ-###`)
* **Stories**: Jira Story links to `REQ-###`
* **Branches**: `feature/JIRA-123_REQ-001`
* **Commits**: `[JIRA-123][REQ-001] Short change description`
* **Tests**: Jira Test Cases linked to Stories & Requirements
* **Test Results**: Stored in Jira, linked to Test Cases
* **Matrix**: Confluence Traceability Matrix auto-updated per sprint/release

---

## **6. Risk Management**

* Maintain Risk Log in Confluence, link risks to requirements and tests
* Score risks (Severity × Occurrence × Detectability)
* Verify mitigations in each sprint
* Document residual risk acceptance at release

---

## **7. Change & Configuration Management**

* Use GitFlow branching (feature, release, hotfix)
* Require PR reviews (≥1 for low risk, ≥2 for high risk)
* Tag all releases, link to Release Package in Confluence
* Track changes in configuration management records

---

## **8. Quality & Verification**

* Perform unit, integration, and system testing
* Document results in Jira + Confluence Test Evidence pages
* Maintain bidirectional traceability: Requirement → Story → Commit → Test → Result → Risk

---

## **9. Security & Privacy**

* Conduct DPIA (Data Protection Impact Assessment) in Discovery/Alpha
* Maintain Privacy & Security Reports in each sprint
* Enable dependency scanning, vulnerability alerts, logging

---

## **10. Documentation & Records**

* **Confluence**: SRS, Risk Log, Traceability Matrix, Release Packages, Training Records
* **Jira**: Stories, Tests, Results, Defects, CAPA tracking
* **Git**: Code, commit history, tagged releases

---

## **11. Training & Support**

* Train contributors on SOP compliance, Git/Jira/Confluence workflows, accessibility guidelines
* Document onboarding guides in Confluence
* Log support tickets in Jira → link to CAPA

---

## **12. Continuous Improvement**

* Sprint retrospectives → update SOP/Work Instructions
* Conduct ISO self-assessments annually
* Feed lessons learned back into project & org SOP

---

✅ With this update, the **ODF phases (Discovery, Alpha, Beta, Live)** now map cleanly to the **SOP SDLC phases (Planning, Development, Release, Maintenance)**.
✅ Each DSS deliverable is tied to a regulatory artifact (SRS, Risk Log, Usability File, Traceability Matrix, Release Package).
✅ Git + Jira + Confluence provide the evidence trail for **audit readiness**.

---

# **ODF → SDLC SOP → Tooling Compliance Mapping**

| **ODF / DSS Phase & Deliverable**        | **SOP SDLC Artifact / Regulatory Requirement**              | **Implementation in Tools (Git / Jira / Confluence)**                           |
| ---------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Discovery**                            | **Planning Phase** (ISO 13485 / IEC 62304)                  |                                                                                 |
| User research report, personas           | Intended Use, Intended Users (IEC 62304 §5.1)               | Confluence page: *Requirements Document* (REQ-IDs)                              |
| Market / regulatory feasibility research | Feasibility analysis (ISO 13485 §7.3.2)                     | Confluence: Feasibility Report                                                  |
| Backlog setup in Jira                    | Software Requirements Specification (SRS)                   | Jira Epics/Stories linked to `REQ-###` in Confluence                            |
| Agile workflow definition                | Development & testing standards (ISO 13485 §7.3.3)          | Confluence: Standards page (coding/testing)                                     |
| Initial Risk log                         | Initial Hazard Analysis (ISO 14971, IEC 62304 §7)           | Confluence: Risk Register linked to REQ-IDs                                     |
| **Alpha**                                | **Development Phase – Early Iterations**                    |                                                                                 |
| Prototypes & mockups                     | Preliminary Architecture, Usability Engineering (IEC 62366) | Confluence: Architecture Doc; Usability File (use-error analysis, journey maps) |
| Journey map                              | Usability Engineering File (ISO 62366 §5.4–5.7)             | Confluence: UX section                                                          |
| Initial project plan                     | Quality Plan (ISO 13485 §7.1)                               | Confluence: Project Plan                                                        |
| User testing evidence                    | Verification evidence (IEC 62304 §5.7)                      | Jira Test Cases + Confluence Usability Report                                   |
| Updated backlog                          | Requirements refinement (ISO 13485 §7.3.3)                  | Jira backlog items linked to Confluence                                         |
| **Beta**                                 | **Development → Release Preparation**                       |                                                                                 |
| MVP build                                | Software Detailed Design + Implementation evidence          | Git branches (`feature/JIRA-123_REQ-001`)                                       |
| Automated testing reports                | Verification & Validation Evidence (IEC 62304 §5.7)         | Jira Test Runs + Confluence Test Evidence page                                  |
| Accessibility test reports               | Usability Validation (IEC 62366 §5.7)                       | Confluence: Accessibility Test Reports; Jira Issues                             |
| Privacy & security report                | Data Protection Impact Assessment (GDPR / ISO 27701)        | Confluence: Privacy & Security Report                                           |
| Risk log updates                         | Risk Control Verification (ISO 14971 §6–7)                  | Jira Risks linked to Stories; Confluence Risk File                              |
| Traceability links updated               | Traceability Matrix (ISO 13485 §7.3.2)                      | Confluence Traceability Matrix (Req → Story → Commit → Test → Result)           |
| **Live**                                 | **Release & Maintenance Phase**                             |                                                                                 |
| UAT reports                              | User Acceptance Testing evidence (ISO 13485 §7.3.6)         | Jira UAT Results linked to REQ-IDs                                              |
| Release notes                            | Release Package (ISO 13485 §7.3.6, FDA 21 CFR Part 11)      | GitHub/Git tag; Confluence Release Notes                                        |
| Final risk review                        | Residual Risk Report (ISO 14971 §9)                         | Confluence Risk File (residual risk acceptance)                                 |
| Usability validation every 3–4 months    | Post-Market Surveillance (ISO 13485 §8.2, IEC 62366 §5.9)   | Confluence PMS/Usability Validation page                                        |
| Maintenance logs                         | CAPA & Maintenance Records                                  | Jira Issues labeled CAPA; Confluence CAPA Log                                   |
| Analytics & KPIs                         | PMS effectiveness monitoring                                | Confluence: KPI Dashboard; Jira reports                                         |
| Lessons learned                          | Continuous Improvement (ISO 9001/90003)                     | Confluence: Retrospectives; SOP update record                                   |

---

## 🔗 Key Traceability Flow

* **Confluence**: Source of truth for requirements (REQ-IDs), risk log, usability file, traceability matrix, release packages.
* **Jira**: Execution layer — Stories, Tests, Risks, CAPA — all linked back to `REQ-IDs`.
* **Git**: Implementation history — branch names and commit messages reference Jira IDs and REQ-IDs.

Example commit message:

```
[JIRA-123][REQ-001] Implement login validation with risk mitigation control RISK-05
```

This enables auto-generation of a compliance-ready **traceability matrix**.

---

✅ With this table, you can demonstrate to auditors:

* Every **ODF deliverable** maps to a **regulatory artifact**.
* Every artifact is **implemented and traceable** in Git, Jira, and Confluence.
* DSS phases become **phase gates** aligned with ISO 13485 / IEC 62304 lifecycle.

---
