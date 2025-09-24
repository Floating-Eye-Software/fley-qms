# **Red Witch Quality Plan (QP)**

## Purpose

Red Witch is a period tracking app for Android, iOS, and web platforms. It adheres to the highest standards of data protection, information security, and software quality to ensure user privacy, reliability, and satisfaction.

The Red Witch Quality Plan (QP) describes how the Red Witch project implements Floating Eye SOPs using the **Ontario Digital Framework (ODF)** and **GitHub** as the sole project management toolchain. It ensures compliance, traceability, and audit readiness at the project level.

---

## 1. Project Overview

* **Project Name**: Red Witch
* **Platform**: Android, iOS, Web
* **Framework**: ODF
* **Tools**: GitHub (issues, pull requests, project boards, repositories, Actions)
* **Regulatory Compliance**: SOPs from Floating Eye QM, GDPR, Ontario Digital and Data Directive

---

## 2. Design Control

* Conforms to Ontario's Digital Service Standard ([Service Design Playbook](https://www.ontario.ca/page/service-design-playbook))
* User needs drive design; ODF phases mapped to SOP deliverables
* GitHub Issues used to capture requirements (SRS) and design artifacts
* UX artifacts and journey maps stored in GitHub `/docs`
* Link: [Red Witch Design Control](Design-Control)


---

## 3. Project Management

* **Workflow**: Fully ODF + GitHub
* **SOP Mapping Table**: Markdown file in `/docs` folder, linking SOP requirements to GitHub artifacts
* Link: [Red Witch Project Management](Project-Management)

### SOP Mapping Table (Red Witch: ODF + GitHub)

| **SOP Requirement**                    | **ODF Deliverable**                                    | **GitHub Implementation**                                  |
| -------------------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- |
| Software Requirements (SRS)            | Discovery Phase – Findings Documentation               | Issues with REQ-IDs; Markdown files in `/docs`             |
| Traceability Matrix                    | Beta Phase – Traceability Update                       | GitHub Project linking issues → pull requests → commits    |
| Risk Management File (ISO 14971)       | Discovery – Policies/Barriers; Alpha – Process Changes | Issue type "Risk"; Project board for tracking              |
| Usability Engineering File (IEC 62366) | Alpha – Journey Maps, Usability Reports                | Markdown UX docs in `/docs`; linked issues for test cases  |
| Verification & Validation Reports      | Beta – Automated Testing, Accessibility Testing        | Pull requests for validation; GitHub Actions CI/CD reports |

---

## 4. Project Execution

* Team executes ODF phases using GitHub for planning, development, and release
* **Traceability**: Requirement → Issue → Commit → Pull Request → Test → Result → Risk Control
* All SOP deliverables maintained **entirely in GitHub**
* Changes and approvals handled via pull requests, review comments, and Actions logs

---

## 5. Information Security

* GitHub used to track:

  * Security-related issues
  * Access controls and permissions
  * Vulnerability reports
* Compliance artifacts stored in repository `/docs` for auditor access
* Link: [Red Witch Information Security](Information-Security)

---

## 6. Regulatory Compliance

* Ontario Digital and Data Directive
* GDPR (EU 2016/679)
* Floating Eye SOPs fully mapped to project deliverables within GitHub
* DPIA and privacy compliance documented in `/docs` folder

- **Ontario Digital and Data Directive**: Red Witch adheres to the Ontario [Digital and Data Directive](https://www.ontario.ca/page/ontarios-digital-and-data-directive-2021) of 2021, ensuring compliance with provincial data protection regulations and standards.

- **General Data Protection Regulation (GDPR)** [(EU) 2016/679](http://data.europa.eu/eli/reg/2016/679): Red Witch complies with the European Union GDPR requirements to safeguard user data and privacy rights.

---

## 7. International Standards

* IEC 82304-1:2016 – Health Software Product Safety
* ISO/TS 82304-2:2021 – Quality and Reliability for Health Apps
* ISO/IEC 27001:2013 – Information Security Management Systems
* ISO/IEC 27701:2019 – Privacy Information Management
* All evidence and artifacts stored in GitHub (issues, PRs, project boards, Markdown docs)

- **Health Software - Part 1: General Requirements for Product Safety** ([IEC 82304-1:2016](https://www.iso.org/standard/59543.html)): Red Witch meets the general safety requirements specified in IEC 82304-1 for health software products.

- **Health Software - Part 2: Health and Wellness Apps - Quality and Reliability** ([ISO/TS 82304-2:2021](https://www.iso.org/standard/78182.html)): Red Witch adheres to the quality and reliability standards outlined in ISO/TS 82304-2 for health and wellness apps.

- **Information Security Management Systems - Requirements** ([ISO/IEC 27001:2013](https://www.iso.org/standard/54534.html)): Red Witch implements ISO/IEC 27001 standards for information security management systems to ensure the confidentiality, integrity, and availability of user data.

- **Privacy Information Management - Requirements and Guidelines** ([ISO/IEC 27701:2019](https://www.iso.org/standard/71670.html)): Red Witch follows ISO/IEC 27701 guidelines for privacy information management to protect user privacy and comply with data protection regulations.

---

## 8. Audit Traceability

* SOP deliverables fully traceable from **requirement → issue → commit → pull request → CI/CD test results → risk control**
* Project board cards link SOP requirements to execution and evidence
* GitHub provides a complete, auditable trail for all regulatory and quality artifacts

---

## 9. Example Project Mapping

| **Project**   | **Framework + Tools** | **Regulatory Focus** | **SOP Traceability**                                                                    |
| ------------- | --------------------- | -------------------- | --------------------------------------------------------------------------------------- |
| Red Witch     | ODF + GitHub          | ISO 13485, IEC 62304 | SOP deliverables mapped to ODF phases, fully within GitHub                              |
| Other Project | Scrum + GitHub        | GDPR, HIPAA          | SOP deliverables mapped to Scrum ceremonies + GitHub issues; DPIA documented in `/docs` |

> Each project may differ operationally, but **audit trail always links back to Floating Eye SOPs entirely within GitHub**.
