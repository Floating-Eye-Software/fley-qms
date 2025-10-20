# **TPL – Project Quality Plan (PQP) Template**

**Slug:** Project-Quality-Plan-Template  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Related SOP:** Quality-Planning-SOP, Project-Management-SOP  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Project-Quality-Plan-Template  

---

## **1. QMS Activity Configuration (Project-Specific)**

> The PQP defines how this project implements the Floating Eye Software (FLEY) Quality Management System (QMS).
> It specifies which **standards**, **SOPs**, **Work Instructions (WIs)**, and **tools** are applied to meet quality, regulatory, and operational requirements.
>
> This configuration ensures each project executes all required QMS activities while allowing flexibility in tools and frameworks.

Each project shall define its **QMS configuration**, identifying which **Work Instructions (WIs)** and **tools** implement each SOP.
All QMS activities are **mandatory**, even if achieved using different frameworks or infrastructures.

| SOP / QMS Activity                           | Selected Work Instruction / Method                                                                                          | Tool / Platform (if applicable) | Notes / Comments                                                            |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | --------------------------------------------------------------------------- |
| **Change-Control-SOP**                | `GitHub-Change-Control`                                                                                       | GitHub (PR workflow)            | All change requests handled via pull requests; approvals tracked in GitHub. |
| **Document-Control-SOP**              | `GitHub-Document-Control`, `GitHub-Version-Control`                                             | GitHub (repositories)           | Markdown docs under version control; approvals via PRs.                     |
| **Quality-Planning-SOP**              | `Red-Witch-Quality-Plan`                                                                                           | PQP in GitHub Wiki              | Defines objectives, risk linkage, and review cadence.                       |
| **Project-Management-SOP**            | `GitHub-Project-Management`                                                                                   | GitHub Projects                 | Milestones, issues, and boards for tracking.                                |
| **Risk-and-Opportunity-Management-SOP** | FLEY Risk Framework (current) → *upgrade planned to ISO 14971*                                                              | GitHub Issues / Risk Register   | Each risk tracked as Issue; migration planned to ISO 14971 structure.       |
| **Design-Control-SOP**  | `Ontario-Service-Design-WI` *(primary)* + `FLEY-Design-Control-WI` *(parallel)* | GitHub Wiki / Repo              | Ontario framework for design flow; FLEY WI ensures regulated traceability.  |
| **Continuous Improvement**        | *(To be determined; likely FLEY CI WI or GitHub retrospective process)*                                                     | GitHub Discussions / Confluence | Lessons learned and improvement tracking.                                   |

**Configuration Rules**

* All SOPs remain in effect; WIs/tools define *how* compliance is achieved.
* Configuration must be approved by the **Project Manager** and **Quality Representative** before project kickoff.
* Any configuration change must follow **Change Control SOP**.
* Standards and frameworks applied (e.g., ISO 9001, ISO 13485, ISO 14971) depend on the **intended use** and regulatory classification of the product/service.

---

## **2. Governance & Quality Planning**

* *[Project objectives and success criteria]*
* *[Roles & responsibilities]*
* *[Review cadence, stage gates, retrospectives]*
* *[Reference Quality-Planning-SOP for quality objectives & risk planning]*

---

## **3. Document & Record Control**

* *[Storage location for project documentation/artifacts]*
* *[Version control method]*
* *[Retention period per QMS/regulatory requirements]*
* Controlled per **Document-Control-SOP** using the methods defined in Section 1.

---

## **4. Training & Competence**

* *[Confirm team qualifications]*
* *[Record special training]*
* *[Maintain training records]*

---

## **5. Risk Management**

* *[Identify and track project risks]*
* *[Framework: FLEY Risk Management → ISO 14971 (if applicable)]*
* *[Define risk review cadence tied to milestones]*
* *[Maintain traceability to design and verification activities]*

---

## **6. Design & Development Control**

* *[Requirements capture method (user stories, specs, etc.)]*
* *[Design planning per Design-Control-SOP]*
* *[Traceability: Requirements → Design → V&V]*
* *[Document design reviews and key decisions]*

**Design Control Plan (DCP) Reference:** *[Link or attach DCP/WI]*

---

## **7. Change & Configuration Management**

* *[Tool(s) for version/configuration management]*
* *[Change workflow (PRs, change requests, approvals)]*
* *[Impact analysis prior to approval]*
* Controlled per **Change-Control-SOP** and selected GitHub WIs.

---

## **8. Supplier & External Resource Management**

* *[List suppliers/vendors]*
* *[Qualification/approval method]*
* *[Monitoring and acceptance criteria]*

---

## **9. Production, Release & Deployment**

* *[Release acceptance criteria]*
* *[Deployment/release process]*
* *[Sign-off authority and post-release monitoring]*

---

## **10. Verification, Validation & Testing**

* *[Acceptance criteria and testing approach]*
* *[Testing results, verification/validation evidence]*
* *[Link to DCP verification plan]*

---

## **11. Nonconformance & CAPA**

* *[Defect/deviation tracking]*
* *[Escalation path]*
* *[CAPA process and evidence]*

---

## **12. Audit & Continuous Improvement**

* *[Lessons learned and retrospectives]*
* *[Internal audit applicability, schedule, improvement tracking]*
* *[Metrics or KPIs monitored]*

---

## **13. Customer & Stakeholder Feedback**

* *[Feedback methods]*
* *[Integration into CAPA / improvement actions]*

---

## **14. Infrastructure, Security & Work Environment**

* *[Environment setup (dev/test/prod)]*
* *[Access control and data security measures]*
* *[Privacy and accessibility compliance]*
* *[Reference WI/NIST/Information-Security.md if applicable]*

---

### 💡 *Implementation Notes*

* The **QMS Activity Configuration** (Section 1) defines this project’s operational QMS profile.
* All SOPs apply; WIs/tools specify execution details.
* Any deviation requires a formal **Change Request**.
* The **Design Control Plan (DCP)** must reference this PQP to stay aligned with the approved configuration.
