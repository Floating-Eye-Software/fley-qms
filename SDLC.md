# Red Witch Software Development Life Cycle

https://www.ontario.ca/page/ontario-digital-service  
https://www.reddit.com/r/OntarioPublicService/comments/1boev99/ontario_digital_service_is_officially_dead/  

https://github.com/ongov/Ontario.ca-Jamstack-Toolkit  
https://github.com/ongov/Ontario.ca-Jamstack-Toolkit/wiki/Getting-started-with-the-Ontario.ca-Jamstack-Toolkit  

https://designsystem.ontario.ca/docs/documentation/for-developers/getting-started.html  


https://www.ontario.ca/document/open-data-guidebook-guide-open-data-directive-2019  
https://www.ontario.ca/page/open-government-licence-ontario  
https://www.ontario.ca/page/ontarios-open-data-directive  
https://www.ontario.ca/page/ontarios-digital-and-data-directive-2021  

https://www.ontario.ca/page/build-ontario-government-services  

Can you write me a software development lifecycle procedure that complies with ISO 13485 and IEC 62304?
Can you also make it comply with IEC 27001, IEC 27701, and the EU GDPR?
Also comply with IEC 62366 and ISO 14971
Can you update this for use by an agile software development team? Please comply with AAMI TIR45.



Sure, here's an updated software development lifecycle (SDLC) procedure that complies with ISO 13485, IEC 62304, IEC 27001, IEC 27701, the EU GDPR, IEC 62366, ISO 14971, and AAMI TIR45 for an agile software development team:
	1. Planning Phase: In this phase, the software development team identifies the software's intended use and intended users, defines the software requirements, and determines the safety requirements.
	• Define the project scope, objectives, and timeline, and establish a product roadmap.
	• Develop a product backlog and prioritize user stories based on the importance and urgency of each requirement.
	• Identify and document the software requirements, including user needs, functional requirements, and performance requirements, in collaboration with the product owner.
	• Define the intended use and intended users of the software and identify potential safety risks and mitigation strategies.
	• Establish the team's development and testing standards, including coding and testing guidelines.
	2. Development Phase: In this phase, the software development team designs, implements, and verifies the software while ensuring safety and usability.
	• Create a high-level software architecture that meets the safety and usability requirements and define the system's interfaces and interactions.
	• Develop, test, and deliver user stories in iterations, with each iteration focused on delivering a shippable product increment.
	• Conduct risk assessments and incorporate mitigation strategies as necessary, in collaboration with the product owner and the risk management team.
	• Implement and verify the usability engineering activities as per IEC 62366, in collaboration with the product owner and the usability engineering team.
	• Ensure that each increment is tested thoroughly, with automated testing wherever possible, to ensure that the software meets functional and safety requirements.
	3. Release Phase: In this phase, the software development team prepares the software for release, obtains regulatory approval, and ensures compliance with safety and usability requirements.
	• Conduct user acceptance testing, with the product owner and end-users, to ensure that the software meets user needs and expectations.
	• Obtain regulatory approval, including submitting the software documentation to regulatory authorities for review and approval.
	• Conduct a final review to ensure compliance with safety and usability requirements, including IEC 62366's usability validation and ISO 14971's risk management review.
	• Create a shippable release package that includes all necessary documentation and instructions for installation, deployment, and configuration.
	4. Maintenance Phase: In this phase, the software development team maintains and updates the software to ensure ongoing safety, effectiveness, and usability.
	• Continuously monitor the software in use, including collecting feedback from users and monitoring performance and safety.
	• Prioritize and address issues or bugs based on their severity and potential impact on safety and effectiveness.
	• Update and enhance the software in response to changing user needs and technological advancements while ensuring safety and usability.
	• Document the results of maintenance activities, including any changes made to the software and the rationale behind them.
Overall, this agile SDLC procedure should be flexible, iterative, and collaborative, with regular communication and feedback loops between the software development team, product owner, risk management team, and usability engineering team. It should also prioritize safety and usability, with risk management and usability engineering activities integrated into the development process. Finally, it should adhere to AAMI TIR45 guidance for applying agile practices in the development of medical device software.

Can you write work instructions to implement this procedure using git, jira, and confluence?
Traceability should be maintained between requirements, stories, git commits, test cases, and test results.

You're absolutely right. Maintaining traceability between requirements, user stories, Git commits, test cases, and test results is critical for ensuring that software development is compliant with regulatory standards and best practices. Here are work instructions to implement traceability throughout the software development lifecycle:
	1. Planning Phase: a. Create a requirements document in the Confluence space that lists all the software requirements and their respective ID numbers. b. Create a product backlog in Jira and link each user story to the corresponding requirement in the Confluence space using the requirement ID. c. Create a traceability matrix in the Confluence space that shows the relationship between each requirement and its corresponding user story. d. Establish the team's development and testing standards, including coding and testing guidelines, in the Confluence space.
	2. Development Phase: a. Create a new branch in the Git repository for each user story. b. In the commit message for each Git commit, reference the corresponding user story ID from Jira. c. Create a new test case in Jira for each user story and link it to the corresponding user story using the user story ID. d. Implement the test case and document the test results in Jira, including pass/fail status, test date, and any defects found. e. Once the user story is complete and tested, merge the branch back into the main branch in Git.
	3. Release Phase: a. Create a new release branch in Git for each release. b. Conduct user acceptance testing, with the product owner and end-users, in the release branch to ensure that the software meets user needs and expectations. c. Create a traceability matrix in the Confluence space that shows the relationship between each requirement, user story, Git commit, test case, and test result. d. Obtain regulatory approval, including submitting the software documentation to regulatory authorities for review and approval, and document the results in the Confluence space.
	4. Maintenance Phase: a. Create a new branch in Git for each maintenance task or bug fix. b. In the commit message for each Git commit, reference the corresponding Jira issue ID. c. Create a new test case in Jira for each maintenance task or bug fix and link it to the corresponding Jira issue using the issue ID. d. Implement the test case and document the test results in Jira, including pass/fail status, test date, and any defects found. e. Once the maintenance task or bug fix is complete and tested, merge the branch back into the main branch in Git.
Overall, these work instructions should provide a clear and organized process for implementing traceability throughout the software development lifecycle, ensuring that all software requirements, user stories, Git commits, test cases, and test results are linked and tracked to ensure compliance with regulatory standards and best practices.


Can you write a project management plan including an outline of the required roles tasks to be performed, and interdependencies between the tasks?

Sure, here is a high-level project management plan that outlines the required roles, tasks, and interdependencies:
Project Title: [Project Name]
Project Manager: [Name]
Project Description: [Brief description of the project]
Objectives: [List of project objectives]
Scope: [Description of the project scope]
Deliverables: [List of project deliverables]
Assumptions: [List of project assumptions]
Constraints: [List of project constraints]
Risks: [List of project risks]
Roles and Responsibilities:
	• Project Manager: Overall responsibility for the project, including planning, execution, and monitoring.
	• Business Analyst: Responsible for gathering and documenting requirements, analyzing business processes, and identifying areas for improvement.
	• Software Developer: Responsible for coding, testing, and implementing software components.
	• Quality Assurance Analyst: Responsible for testing and ensuring the software meets quality standards.
	• Technical Writer: Responsible for creating project documentation, including user manuals and help guides.
Tasks:
	1. Project Initiation
	• Define project scope, objectives, and deliverables
	• Identify project stakeholders
	• Develop project charter
	• Develop project plan
	2. Requirements Gathering and Analysis
	• Gather and document requirements
	• Analyze business processes
	• Identify areas for improvement
	3. Design and Development
	• Develop software architecture and design
	• Develop software components
	• Conduct code reviews
	4. Testing and Quality Assurance
	• Develop test cases and plans
	• Conduct unit testing, integration testing, and system testing
	• Conduct user acceptance testing
	• Ensure compliance with regulatory standards and best practices
	5. Documentation and Training
	• Create user manuals and help guides
	• Develop training materials for end-users
	• Conduct end-user training sessions
Interdependencies:
	• The success of the design and development tasks depends on the accuracy and completeness of the requirements gathered during the requirements gathering and analysis phase.
	• The testing and quality assurance tasks depend on the completion of the design and development tasks.
	• The success of the project depends on the successful completion of all tasks, with each task building on the completion of the previous tasks.
Overall, this project management plan provides a high-level overview of the required roles, tasks, and interdependencies for a software development project, with a focus on ensuring successful completion of all project objectives and deliverables.


Can you write a checklist of tasks that need to be performed for each sprint, and also for each software release?

Sure, here are checklists for tasks that need to be performed for each sprint and software release:
Sprint Checklist:
	1. Review and prioritize backlog items.
	2. Estimate the effort required for each backlog item.
	3. Define sprint goals and objectives.
	4. Assign tasks to team members based on their skills and availability.
	5. Develop and test software components.
	6. Review code and conduct code quality checks.
	7. Conduct unit testing and integration testing.
	8. Conduct a sprint review to demonstrate completed work to stakeholders.
	9. Conduct a sprint retrospective to identify areas for improvement.
Software Release Checklist:
	1. Review and prioritize backlog items for the release.
	2. Define release goals and objectives.
	3. Develop and test software components.
	4. Conduct user acceptance testing.
	5. Conduct regression testing to ensure new features do not impact existing functionality.
	6. Conduct performance testing to ensure the system can handle expected usage.
	7. Update documentation, including user manuals and help guides.
	8. Conduct end-user training sessions.
	9. Create release notes to document changes made in the release.
	10. Deploy the release to production environments.
It is important to note that these checklists should be tailored to fit the specific needs and requirements of the project and team. Additionally, the checklists should be reviewed and updated regularly to ensure they remain relevant and effective.


Can you write a template for a project charter that incorporates everything we have discussed?

Sure, here's a template for a project charter that incorporates the elements we've discussed:
Project Charter Template:
Project Title: [Project Name]
Project Manager: [Name]
Project Sponsor: [Name]
Date: [Date]
	1. Project Description: [Briefly describe the project, its purpose, and its goals.]
	2. Project Objectives: [List the project objectives.]
	3. Scope: [Define the project scope, including what is included and what is excluded.]
	4. Deliverables: [List the expected deliverables and outcomes of the project.]
	5. Assumptions: [List any assumptions made about the project, including resources, constraints, and risks.]
	6. Constraints: [List any limitations or constraints that may affect the project.]
	7. Risks: [List any risks that may impact the project and describe the risk management plan.]
	8. Stakeholders: [List the project stakeholders and describe their roles and responsibilities.]
	9. Project Approach: [Describe the project approach, including the methodology, tools, and techniques to be used.]
	10. Project Timeline: [Provide a high-level project timeline, including key milestones and deadlines.]
	11. Budget: [Outline the project budget, including resources and expenditures.]
	12. Communication Plan: [Describe the project communication plan, including the stakeholders, communication channels, and frequency of communication.]
	13. Quality Plan: [Describe the quality plan for the project, including the standards and processes to ensure the project deliverables meet the required quality standards.]
	14. Compliance Plan: [Describe the compliance plan for the project, including the regulations and standards that must be adhered to.]
	15. Project Team: [List the project team members and their roles and responsibilities.]
	16. Project Governance: [Describe the project governance structure, including the decision-making process and escalation procedures.]
	17. Approval: [Provide a space for the project sponsor to approve the project charter.]
Once the project charter is complete and approved by the project sponsor, it should be used as a reference throughout the project to ensure that the project stays on track and meets the objectives and goals.


Can you we write work instructions for the maintenance phase? User complaints should be uniquely identifiable and traceable to code that fixes the problem.
Please add the roles for each task and also add recordkeeping in confluence and jira

Sure, here are the revised work instructions with the roles and recordkeeping added:
Maintenance Phase Work Instructions:
	1. Record User Complaints: The customer support team should record user complaints in Jira, creating a new issue with all relevant information, including user feedback, system logs, and any other data that may help identify the cause of the issue. The issue should be linked to a Confluence page that documents the complaint and includes all supporting information.
	2. Assign Complaints to Developers: The project manager should assign the issue to a developer for investigation and resolution. The developer should be provided with all relevant information, including user feedback, system logs, and any other data that may help identify the cause of the issue. The developer should also update the Confluence page with their findings and proposed solution.
	3. Investigate the Issue: The assigned developer should investigate the issue thoroughly, including analyzing the code and system logs to identify the root cause of the problem. They should also evaluate the severity of the issue and prioritize it based on its impact on users. The developer should document their findings in Confluence and update the Jira issue with their proposed solution.
	4. Develop and Test a Fix: The developer should develop a fix and test it thoroughly to ensure that it resolves the issue without introducing new problems. They should also document the code changes and update any affected documentation in Confluence. The developer should mark the Jira issue as "In Progress" and update it with the details of the fix.
	5. Implement the Fix: The developer should implement the fix in the system, following the established deployment process. They should verify that the fix has been deployed correctly and that it resolves the issue as expected. The developer should update the Jira issue with the details of the fix and mark it as "Resolved."
	6. Retest the System: The system should be retested to ensure that it is functioning correctly and that the issue has been resolved. The assigned developer should perform this testing and update the Confluence page with the results.
	7. Monitor the System: After the issue has been resolved, the system should be monitored to ensure that the fix is effective and that it does not introduce any new issues. The assigned developer should perform periodic maintenance checks to ensure that the system is functioning correctly and that it remains compliant with all applicable standards and regulations. The results of these checks should be documented in Confluence.
By following these work instructions, user complaints can be uniquely identified and traceable to the code that fixes the problem, and all recordkeeping can be done in Confluence and Jira, making it easier to maintain and improve the system over time.



Can you write work instructions creating a new release to resolve a complaint, deploying it to the test and producion enviroments? Make sure to maintain traceability throughout.

Sure, here are the work instructions for creating a new release to resolve a complaint and deploying it to the test and production environments, while maintaining traceability:
	1. Create a New Release: The project manager should create a new release in Jira and assign a release version number. They should also create a Confluence page for the release, documenting the reason for the release, the issues it addresses, and any other relevant information.
	2. Develop and Test the Release: The development team should develop and test the release, ensuring that it addresses the issue reported in the user complaint. They should update the Confluence page with information about the release, including any code changes, documentation updates, and test results.
	3. Deploy the Release to the Test Environment: The release should be deployed to the test environment for further testing. The deployment should be done using a controlled process that is documented in Confluence. The testing team should test the release thoroughly, using the test cases and test results documented in Jira.
	4. Verify the Release: The testing team should verify that the release is functioning correctly and that it resolves the user complaint. They should update the Confluence page and the Jira issues with their findings and test results.
	5. Deploy the Release to the Production Environment: Once the release has been verified in the test environment, it should be deployed to the production environment. The deployment should be done using a controlled process that is documented in Confluence. The deployment team should verify that the release is functioning correctly in the production environment and that it resolves the user complaint.
	6. Update the Traceability Matrix: Throughout the process, the traceability matrix should be updated to maintain traceability between the user complaint, the issues addressed in the release, the code changes, the test cases, and the test results. The traceability matrix should be stored in Confluence and maintained by the project manager.
By following these work instructions, a new release can be created and deployed to resolve a user complaint, with traceability maintained throughout the process. This helps ensure that the system remains compliant with all applicable standards and regulations, and that it continues to meet the needs of its users.




Can you combine all of the above into one work instruction?
Customer complaints are handled in an unnamed CRM. Only the development team use git, jira, and confluence.
The testing team uses a different test management system to perform testing.
Actually, sometimes the testing team uses JIRA for test management. Please update to allow use of any testing system.


Sure, here are the updated work instructions that allow the testing team to use any test management system:
	1. Define Requirements: The project manager, development team, and stakeholders should work together to define and document the requirements for the software system. The requirements should be documented in Jira and Confluence, with traceability maintained between the requirements, user stories, and test cases.
	2. Plan and Schedule the Project: The project manager should use Jira to plan and schedule the project, assigning tasks to team members and tracking progress. The project plan should be documented in Confluence, with updates made as needed to reflect changes in the project schedule.
	3. Develop the Software: The development team should use Git to develop the software, following the software development lifecycle procedure that complies with ISO 13485, IEC 62304, IEC 27001, IEC 27701, EU GDPR, IEC 62366, and ISO 14971. They should maintain traceability between the code changes, requirements, and test cases, using Jira and Confluence to document their work.
	4. Perform Testing: The testing team should use their test management system to develop and document test cases, and perform testing to ensure that the software meets the requirements and functions as intended. They should maintain traceability between the test cases, requirements, and test results, using their test management system to document their work. If the testing team uses Jira for test management, they can integrate their test management system with Jira to maintain traceability between the requirements, test cases, and test results.
	5. Handle User Complaints: If a user complaint is received, the project manager should document the complaint in the CRM system and create a Confluence page to track the investigation and resolution of the complaint. The development team should use Git to develop a fix for the issue and update the Confluence page with information about the fix. The testing team should verify that the fix resolves the issue, using their test management system to document their work.
	6. Maintain the Software: During the maintenance phase, user complaints should continue to be tracked in the CRM system and Confluence. The development team should use Git to develop fixes for any issues, and the testing team should verify that the fixes resolve the issues. Traceability should be maintained between the user complaints, code changes, and test results.
	7. Release the Software: When a new release is ready, the project manager should create a new release in Jira and assign a release version number. They should also create a Confluence page for the release, documenting the reason for the release, the issues it addresses, and any other relevant information. The development team should develop and test the release, updating the Confluence page with information about the release, including any code changes, documentation updates, and test results. The release should be deployed to the test environment and verified by the testing team using their test management system before being deployed to the production environment. Traceability should be maintained between the user complaint, the issues addressed in the release, the code changes, the test cases, and the test results.
By following these work instructions, a comprehensive software development process can be implemented, with traceability maintained throughout. This helps ensure that the system remains compliant with all applicable standards and regulations, and that it continues to meet the needs of its users.


Please provide a list of documents that need to be created or updated for as software release

Sure, here's a list of documents that should be created or updated for a software release:
	1. Release plan: This document outlines the scope of the release, the tasks that need to be completed, and the timeline for completion.
	2. User stories: These are the individual requirements for the release, broken down into manageable chunks of work.
	3. Test cases: These are the specific steps that need to be taken to test each user story to ensure that it meets the requirements.
	4. Test results: These are the outcomes of each test case, documenting whether the user story has been successfully implemented.
	5. Bug reports: These documents track any bugs that are identified during testing and include steps to reproduce the issue.
	6. Change request forms: These forms are used to document any changes that are made to the software during development or testing.
	7. Deployment plan: This document outlines the steps needed to deploy the software to the production environment.
	8. Training materials: These documents are used to train end-users on how to use the new software features.
	9. User documentation: These documents provide users with information on how to use the new features.
	10. Release notes: These documents provide an overview of the changes made in the release, including any new features, bug fixes, or known issues.
	11. Configuration management documents: These documents track changes made to the software code and ensure that different versions are properly identified and managed.
	12. Risk management documents: These documents identify potential risks associated with the release and outline mitigation strategies.
	13. Compliance documentation: These documents demonstrate that the software release meets any regulatory or compliance requirements.
It's important to note that not all of these documents may be necessary for every software release, and the specific documentation needs may vary depending on the project and organization.

Please write a template for a software development plan for this sdlc and work instructions.

Sure, here's a template for a Software Development Plan (SDP) that includes the SDLC and work instructions:
	1. Introduction
		○ Purpose of the SDP
		○ Overview of the software development project
		○ Scope of the software development project
		○ Relevant regulatory requirements
	2. SDLC Overview
		○ Description of the software development life cycle (SDLC) to be used
		○ Roles and responsibilities of the development team members
		○ Key milestones in the SDLC
		○ Required approvals at each stage of the SDLC
	3. Work Instructions
		○ Description of the work instructions to be used for each stage of the SDLC
		○ Details of the tools and software to be used for development, testing, and deployment
		○ Procedures for maintaining traceability between requirements, user stories, test cases, git commits, and test results
		○ Procedures for handling user complaints and maintaining traceability to code fixes
		○ Recordkeeping requirements for Confluence and JIRA
	4. Risk Management
		○ Identification of potential risks associated with the software development project
		○ Strategies for mitigating these risks
		○ Procedures for monitoring and managing risks throughout the SDLC
	5. Configuration Management
		○ Description of the configuration management processes to be used
		○ Procedures for managing and identifying different versions of the software code
		○ Recordkeeping requirements for configuration management documents
	6. Quality Management
		○ Description of the quality management processes to be used
		○ Procedures for ensuring that the software meets the necessary quality standards
		○ Recordkeeping requirements for quality management documents
	7. Training and Support
		○ Procedures for training end-users on the new software features
		○ Procedures for providing ongoing support for the software
		○ Recordkeeping requirements for training and support documents
	8. Documentation
		○ Procedures for creating and updating documentation throughout the SDLC
		○ Description of the specific documents that need to be created or updated for each software release
	9. Project Management
		○ Procedures for managing the project, including communication and reporting requirements
		○ Roles and responsibilities of the project team members
		○ Procedures for managing interdependencies between tasks
	10. Conclusion
		○ Summary of the key points of the SDP
		○ Approval and sign-off procedures
Note that this template is a starting point and should be customized to fit the specific needs and requirements of the software development project.

---

# 📝 **Floating Eye SOP → Project Compliance Mapping Form (with FDA + EU MDR/MDD)**

**Project Title:**
**Project Manager:**
**Framework / Methodology:** (e.g., ODF, Scrum, Kanban)
**Toolchain:** (e.g., GitHub, Jira, Confluence)
**Applicable Regulations / Standards:**

* [ ] ISO 13485
* [ ] IEC 62304
* [ ] IEC 27001 / 27701
* [ ] GDPR
* [ ] HIPAA
* [ ] IEC 62366 (Usability)
* [ ] ISO 14971 (Risk Management)
* [ ] FDA 21 CFR Part 820 (QMS)
* [ ] FDA 21 CFR Part 11 (Electronic Records & Signatures)
* [ ] EU MDR (2017/745)
* [ ] MDD (93/42/EEC, if legacy device)
* [ ] Other: \_\_\_\_\_\_\_\_\_\_

---

## **Section 1 – SOP Deliverables Mapping (Extended)**

| **Floating Eye SOP Deliverable**          | **Framework Equivalent**                   | **Tool Implementation (Where Stored / How Linked)**           | **Responsible Role** | **Regulatory Compliance (FDA/EU)**                     |
| ----------------------------------------- | ------------------------------------------ | ------------------------------------------------------------- | -------------------- | ------------------------------------------------------ |
| Software Requirements Specification (SRS) | ODF Discovery findings                     | Confluence REQ pages with IDs                                 | Business Analyst     | **820.30 Design Inputs**, **MDR Annex II (2.3)**       |
| Risk Management File                      | ODF Discovery/Alpha                        | Confluence Risk Register, Jira “Risk” type                    | QA/RA Lead           | **ISO 14971**, **MDR Annex I (3)**                     |
| Usability Engineering File                | ODF Alpha (journey maps, usability report) | Confluence UX folder                                          | UX Lead              | **IEC 62366**, **MDR Annex I (5)**                     |
| Software Architecture & Design            | ODF Alpha project plan/prototypes          | Confluence design docs; Git diagrams                          | Architect            | **820.30 Design Outputs**, **MDR Annex II (2.4)**      |
| Traceability Matrix                       | ODF Beta traceability                      | Confluence table linking REQ → Story → Commit → Test → Result | QA Lead              | **820.30(e), (j)**, **MDR Annex II (2.4.3)**           |
| Verification & Validation Evidence        | ODF Beta (testing, accessibility reports)  | Jira Test Cases & Runs; GitHub Actions logs                   | QA Analyst           | **820.30(f), (g)**, **MDR Annex II (6)**               |
| Release Package                           | ODF Live (release notes, privacy/security) | GitHub Releases; Confluence notes                             | Project Manager      | **820.70**, **MDR Annex II (6.2)**                     |
| CAPA / PMS Logs                           | ODF Live (analytics, maintenance logs)     | Jira CAPA issues; Confluence PMS log                          | RA Lead              | **820.100**, **MDR Annex III PMS**, **MDR Art. 83–86** |

---

## **Section 2 – Regulatory Cross-Reference**

| **Regulation / Standard**  | **Relevant SOP Requirement**                                  | **Project Artifact / Evidence Source**                        |
| -------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| FDA 21 CFR Part 820        | Design Controls, CAPA, Document Control                       | Confluence Design Docs, Jira CAPA Issues, Traceability Matrix |
| FDA 21 CFR Part 11         | Audit trails, electronic records/signatures                   | Git signed commits, Jira audit logs, Confluence approvals     |
| EU MDR Annex II (Tech Doc) | Device description, design & manufacturing info, risk/benefit | Confluence Tech File, Jira Trace Matrix                       |
| EU MDR Annex III (PMS)     | Post-market surveillance plan & report                        | Confluence PMS log, Jira CAPA tickets                         |
| MDD Annex VII (legacy)     | Essential requirements checklist, technical documentation     | Confluence ER checklist, Design History File                  |

---

## **Section 3 – Traceability & Audit Plan**

* **Requirements** (Confluence REQ-IDs) → **User Stories** (Jira Epics/Stories) → **Code** (Git commits referencing Story IDs) → **Tests** (Jira Test Cases & Results) → **Release Evidence** (GitHub/Confluence)
* **Audit Trail**: Jira and Confluence logs satisfy **21 CFR Part 11**; Git signed commits ensure authenticity.
* **Design Dossier (MDR)**: Confluence space configured as **Device Technical Documentation repository**.
* **CAPA & PMS**: Jira Issues labeled CAPA, linked to PMS log in Confluence.

---

## **Section 4 – Project Governance**

* **Phase Gates**: Planning → Development → Release → Maintenance, with QA/RA approvals.
* **Review Boards**: Architecture, Regulatory/Clinical, Digital First.
* **Escalation**: Deviations from SOP require RA/QA approval (logged in Jira).
* **Audit Storage**: Confluence = **Design History File** + **MDR Technical Documentation**.

---

✅ This ensures:

* **FDA 21 CFR 820** → Design Controls, CAPA, Production controls.
* **FDA 21 CFR 11** → Audit trails, e-signatures, electronic records.
* **EU MDR Annex II & III** → Technical Documentation, PMS, risk/benefit justification.
* **MDD** → Only if project is a legacy device, map artifacts against Essential Requirements.

---

# **Software Development Plan (SDP) – Living Document Template**

---

## **1. Introduction**

* **Purpose of the SDP:**
  *(Describe the purpose of this document and its role as the central container for design inputs.)*

* **Overview of the Project:**
  *(High-level description of the software system, its goals, and stakeholders.)*

* **Scope of the Project:**
  *(Boundaries of the system, in-scope vs. out-of-scope functionality.)*

* **Regulatory Requirements:**
  *(List applicable standards and regulations, e.g., IEC 62304, ISO 13485, FDA 21 CFR Part 11, etc.)*

---

## **2. SDLC Overview**

* **Development Methodology:**
  *(Scrum, Kanban, Waterfall, Hybrid, etc.)*

* **Roles and Responsibilities:**
  *(List team members and their roles.)*

* **Key Milestones:**
  *(Insert current milestones, update as project evolves.)*

* **Approvals Required:**
  *(Define approval gates: requirements review, design review, release approval.)*

---

## **3. Work Instructions**

* **Development Process:**
  *(Describe how issues, sprints, and commits are managed — e.g., GitHub Issues + Project Board.)*

* **Tools Used:**
  *(List IDEs, CI/CD, testing tools, deployment pipelines — update continuously.)*

* **Traceability:**

  * Requirements → User stories/issues → Git commits → Test cases → Test results
  * *(Insert links to traceability matrices or GitHub boards.)*

* **User Complaints / Feedback:**
  *(Insert links to complaint log, bug reports, and traceability back to fixes.)*

* **Recordkeeping Systems:**
  *(E.g., Red Witch Wiki, GitHub, Confluence, JIRA. Update with actual URLs.)*

---

## **4. Risk Management**

* **Identified Risks:**
  *(Insert links to risk analysis document(s). Continuously update as new risks are found.)*

* **Mitigation Strategies:**
  *(Describe and update as new controls are implemented.)*

* **Monitoring Procedures:**
  *(Link to risk log and status reports.)*

---

## **5. Configuration Management**

* **Version Control Process:**
  *(Describe Git branching model, release tagging, code review process.)*

* **Configuration Identification:**
  *(Define how builds and releases are labeled and stored.)*

* **Recordkeeping:**
  *(Link to configuration records, release notes, and GitHub release history.)*

---

## **6. Quality Management**

* **Quality Processes:**
  *(Link to test plans, QA standards, and SOPs for verification/validation.)*

* **Verification & Validation Evidence:**
  *(Insert links to test results, coverage reports, and validation reports.)*

* **Recordkeeping:**
  *(Reference where QA documentation is stored.)*

---

## **7. Training and Support**

* **End-User Training:**
  *(Insert training guides, video tutorials, onboarding material.)*

* **Support Procedures:**
  *(Describe support workflow and link to issue tracker.)*

* **Recordkeeping:**
  *(Insert logs of training sessions or support tickets.)*

---

## **8. Documentation**

* **Creation & Maintenance:**
  *(Describe how documentation is created and updated — e.g., GitHub wiki pages.)*

* **Required Documents per Release:**
  *(List documents like release notes, updated risk files, validation summary.)*

* **Links to Current Docs:**
  *(Continuously insert links to user manuals, developer guides, etc.)*

---

## **9. Project Management**

* **Communication & Reporting:**
  *(Define frequency and medium of project updates.)*

* **Roles & Responsibilities:**
  *(Update as team members change.)*

* **Dependencies & Interactions:**
  *(Maintain list of interdependent tasks and teams.)*

* **Sprint / Iteration Plans:**
  *(Insert links to GitHub Project boards, sprint backlogs, and retrospectives.)*

---

## **10. Conclusion**

* **Summary of Key Points:**
  *(Summarize status periodically.)*

* **Approval & Sign-Off:**
  *(Maintain signatures/approvals of responsible authorities — electronic or documented.)*

---

---
