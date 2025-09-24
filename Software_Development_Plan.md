# Software Development Plan (SDP) – Living Document

---

## Document Control

**Project:** Red Witch  
**Document Type:** Software Development Plan (SDP)  
**Status:** Draft / Living Document  
**Review Cycle:** Quarterly (until SOPs are finalized, then annually)  

### Revision History

| Version | Date       | Author           | Changes Made                          | Approved By |
|---------|------------|------------------|---------------------------------------|-------------|
| 0.1     | YYYY-MM-DD | Project Manager  | Initial draft created                 | –           |
| 0.2     | YYYY-MM-DD | Quality Lead     | Added traceability and compliance map | Exec Sponsor|

---

## 1. Introduction

* **Purpose of the SDP:**  
  Defines how software development for Red Witch will be managed and documented. Serves as the **central container for design inputs**.

* **Overview of the Project:**  
  Red Witch is a health/wellness app (Android, iOS, Web) focused on period tracking and health insights. Stakeholders include end users, developers, quality/compliance teams, and regulators.

* **Scope of the Project:**  
  *In-scope:* Mobile and web applications, supporting backend, data storage.  
  *Out-of-scope:* Third-party integrations not directly related to period tracking.

* **Regulatory Requirements:**  
  - IEC 62304 – Software lifecycle processes  
  - ISO 13485 – Medical device QMS (if classified as medical software)  
  - FDA 21 CFR Part 11 – Electronic records/signatures  
  - GDPR – Data privacy compliance  
  - ISO/IEC 27001 & 27701 – Information security & privacy management  

---

## 2. SDLC Overview

* **Development Methodology:** Agile (Scrum/Kanban hybrid).  
* **Roles and Responsibilities:** Updated in project wiki; PM, developers, QA, quality lead.  
* **Key Milestones:** Updated per release cycle (MVP, Beta, Live).  
* **Approvals Required:** Requirements review, design review, release approval.  

---

## 3. Work Instructions

* **Development Process:** Issues and sprints managed via GitHub Issues + Project Boards.  
* **Tools Used:** IDEs (Android Studio, Xcode, VS Code), GitHub Actions (CI/CD), testing frameworks, deployment pipelines.  
* **Traceability:**  
  Requirements → User stories/issues → Git commits → Test cases → Test results.  
* **User Complaints / Feedback:** Logged in GitHub Issues; traceability maintained.  
* **Recordkeeping Systems:** Red Witch Wiki, GitHub repositories.  

---

## 4. Risk Management

* **Identified Risks:** Linked to separate risk analysis documents.  
* **Mitigation Strategies:** Defined and updated as controls are applied.  
* **Monitoring Procedures:** Ongoing review in risk log.  

---

## 5. Configuration Management

* **Version Control Process:** Git branching model, PR reviews, release tagging.  
* **Configuration Identification:** Builds/releases labeled and archived.  
* **Recordkeeping:** GitHub Releases and release notes.  

---

## 6. Quality Management

* **Quality Processes:** Verification/validation per Quality Manual and SOPs.  
* **Verification & Validation Evidence:** Linked test plans, coverage reports, validation reports.  
* **Recordkeeping:** Stored in GitHub Wiki and quality repository.  

---

## 7. Training and Support

* **End-User Training:** Guides, onboarding docs, tutorial videos.  
* **Support Procedures:** Issues logged via GitHub Issues or helpdesk tool.  
* **Recordkeeping:** Logs of training sessions and support tickets.  

---

## 8. Documentation

* **Creation & Maintenance:** Managed in GitHub Wiki and repos.  
* **Required Documents per Release:** Release notes, updated risk files, validation summary.  
* **Links to Current Docs:** Insert references to user manuals and developer guides.  

---

## 9. Project Management

* **Communication & Reporting:** Weekly updates via project board.  
* **Roles & Responsibilities:** Updated as team changes.  
* **Dependencies & Interactions:** Tracked in GitHub Issues.  
* **Sprint / Iteration Plans:** Linked to GitHub Project boards.  

---

## 10. Conclusion

* **Summary of Key Points:** SDP is a living document and will be updated continuously.  
* **Approval & Sign-Off:** See approval table below.  

---

## 11. Approvals

| Role             | Name                | Signature | Date       |
|------------------|---------------------|-----------|------------|
| Project Manager  |                     |           |            |
| Quality Lead     |                     |           |            |
| Executive Sponsor|                     |           |            |

---

## Appendix A – Compliance Mapping

| Standard / Regulation         | SDP Section(s) Addressed                  |
|-------------------------------|--------------------------------------------|
| IEC 62304 (Software lifecycle)| 2 (SDLC Overview), 3 (Work Instructions), 5 (Config Mgmt) |
| ISO 13485 (Design & Dev)      | 1 (Introduction), 4 (Risk Mgmt), 6 (Quality Mgmt) |
| FDA 21 CFR Part 11             | 5 (Configuration Mgmt), 6 (Quality Mgmt)  |
| GDPR (Privacy)                | 1 (Introduction), 3 (User Complaints), 4 (Risk Mgmt) |
| ISO/IEC 27001 & 27701         | 1 (Introduction), 4 (Risk Mgmt), 6 (Quality Mgmt) |

---
