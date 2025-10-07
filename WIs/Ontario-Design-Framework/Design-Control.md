# Red Witch Design Control Plan

The Red Witch Project will comply with the Ontario [Digital and Data Directive](https://www.ontario.ca/page/ontarios-digital-and-data-directive-2021) by adhering to the [Digital Service Standard](https://www.ontario.ca/page/digital-service-standard) and the guidelines established in the [Service Design Playbook](https://www.ontario.ca/page/service-design-playbook).

## **Design Control Plan as per DSS**

### **1. Software Development Lifecycle (SDLC) Phases**

#### **Discovery Phase**
   - **User Research**: Conduct thorough user research to understand potential users and their needs.
   - **Primary User Groups**: Identify and document primary user groups, personas, needs, and expectations.
   - **Existing Services**: Check if there are existing or non-governmental services that meet user needs.
   - **Policies and Barriers**: Identify policies and other barriers that will make meeting user needs difficult.
   - **Findings Documentation**: Document all findings, including user research results, market/regulatory/feasibility research.
   - **Product Manager**: Designate a product manager.
   - **Agile Workflow**: Establish an [agile](https://www.ontario.ca/page/being-agile-ontario-public-service) workflow.

#### **Alpha Phase**
   - **Stakeholder Co-creation**: Work directly with end users and stakeholders to co-create solutions.
   - **Prototypes**: Build and test multiple prototypes of the service.
   - **User Testing**: Plan and conduct continuous user testing with real users.
   - **Technical and Financial Feasibility**: Demonstrate that the service is technically and financially feasible.
   - **Process Changes**: Identify existing processes or policies that need to change to support the service.
   - **Usability Report**: Create a usability report based on user testing.
   - **Journey Map**: Develop a journey map of the user experience.
   - **Initial Project Plan**: Create an initial project plan including technical approach, financial estimate, market surveillance, service, support, and updates.

#### **Beta Phase**
   - **Minimum Viable Product (MVP)**: Build a minimum viable product that can be used by the public in a live environment.
   - **Continuous Testing**: Continuously test the service with users to collect feedback and discover insights.
   - **Device Validation**: Perform device validation on all platforms.
   - **Accessibility Testing**: Include accessibility-challenged user testers using [inclusive design cards](https://www.ontario.ca/page/inclusive-design-cards).
   - **Key Performance Indicators (KPIs)**: Measure the service against key performance indicators.
   - **Technical and Process Challenges**: Resolve any remaining technical or process-related challenges.
   - **Privacy and Security Report**: Create and maintain a privacy and security report.
   - **Automated Testing**: Implement automated testing processes.
   - **WCAG Success Criteria**: Include [WCAG success criteria](https://www.w3.org/TR/WCAG21/) in UI testing.
   - **Consistent Branding**: Use consistent branding leveraging the [Ontario Design System](https://designsystem.ontario.ca/).
   - **Maintenance Plan**: Develop plans for maintenance releases, outages, service monitoring.

#### **Live Phase**
   - **Service and Maintenance**: Continue service and maintenance post-launch.
   - **Ongoing User Research**: Conduct ongoing user research and usability testing every three to four months.
   - **Improvements and Updates**: Continue building features from the backlog and releasing improvements to the service.
   - **Service Success Communication**: Communicate and celebrate the successes of the service.
   - **Compliance with DSS**: Ensure the service continues to meet the Digital Service Standard.
   - **Web Analytics**: Employ web analytics for product surveillance.
   - **User Feedback**: Evaluate user complaints from all sources and respond appropriately.
   - **Performance Metrics**: Calculate and monitor performance metrics.
   - **Recovery Plan**: Create a recovery plan for disastrous data loss.
   - **Open Data**: Publish useful and open data in accordance with the [Open Data Guidebook](https://www.ontario.ca/document/open-data-guidebook-guide-open-data-directive-2015).

### **2. Methodologies and Tools**
- **Agile Methodology**: Utilize [agile methodology](https://www.ontario.ca/page/being-agile-ontario-public-service) for iterative development and frequent updates.
- **Consistent Branding**: Leverage the [Ontario Design System](https://designsystem.ontario.ca/) for consistent UI and UX design.
- **Accessibility**: Ensure accessibility by including [WCAG success criteria](https://www.w3.org/TR/WCAG21/) in UI testing and using inclusive design practices.

### **3. Post-Launch Considerations**
- **Support and Maintenance**: Ensure continuous support and maintenance, including frequent updates and rollbacks.
- **Usability Testing**: Conduct regular usability testing as part of the support plan post-launch.
- **Service Performance**: Monitor service performance using web analytics and respond to user feedback.

### **4. Risk Management**
- **Quality and Security Plans**: Create plans for frequent iterations, including rollbacks and security fixes.
- **Server and Device Updates**: Establish processes for updating server software and client devices.
- **Recovery Plan**: Develop a recovery plan for catastrophic data loss.
- **Privacy and Security**: Maintain a comprehensive privacy and security report.

### **5. Data Management**
- **Open Data**: Ensure data is accurate, timely, and released in an open format according to the [Open Data Guidebook](https://www.ontario.ca/document/open-data-guidebook-guide-open-data-directive-2015).
- **Data Security**: Ensure data remains secure and managed responsibly.
- **Performance Metrics**: Define and calculate performance metrics early in the design process and monitor continuously.

### **6. Digital Governance**
- **Compliance**: Ensure all service development and delivery activities comply with applicable regulations and standards.
- **Assessment Against DSS**: Evaluate against the Digital Service Standard at each phase in the design cycle.
- **Governance Processes**: Participate in governance processes like Digital First Assessments and Architecture Review Board as required.

### **7. Measurement and Evaluation**
- **Evaluation and Analytics**: Establish evaluation and analytics approaches to support continuous improvement.
- **Service Analytics**: Use service analytics to understand user behavior and improve service.
- **Realization of Benefits**: Monitor and report on the realization and sustainment of benefits.

By addressing these elements comprehensively, Red Witch Design Control will align closely with the Ontario Service Design Framework, ensuring compliance and effective service delivery.

---

# Red Witch Regulatory & Standards Compliance Matrix (Updated)

This matrix maps **Ontario DSS phases**, **Red Witch deliverables**, and applicable **standards/regulations**, including optional ones, for audit, traceability, and SOP alignment.

| DSS Phase | Red Witch Deliverables / Activities | ISO 9001 / ISO 90003 | IEC 62304 | IEC 62366 | ISO 82304-1 / 2 | ISO 14971 | ISO 13485 | ISO/IEC 27001 | ISO/IEC 27701 | FDA 21 CFR Part 11 | Optional / Conditional Standards |
|-----------|-----------------------------------|---------------------|------------|------------|-----------------|-----------|------------|----------------|----------------|------------------|--------------------------------|
| **Discovery** | User research, personas, requirements capture, barrier assessment | QMS requirements; requirement specification; process approach | Software requirements lifecycle planning | Early usability considerations | Initial health software safety review | Hazard identification | QMS design controls | Security risk assessment | Privacy impact assessment | Data integrity for requirements capture | ISO 14155 (if clinical studies planned), IEC 60601-1 (if connected hardware) |
| **Alpha** | Prototypes, journey maps, technical/financial feasibility, stakeholder co-creation | Design & development planning; traceability | Detailed software design, risk management | Usability testing | Prototype safety and quality evaluation | Risk analysis of design options | Design verification, QMS records | Implement security controls, monitor access | Implement GDPR-aligned data handling | Audit trails for prototype testing & records | IEC 60601-1 (hardware), ISO 14155 (clinical trials) |
| **Beta** | MVP, continuous testing, device validation, accessibility, KPIs, privacy/security report | Implementation, verification, validation, traceability | Software implementation, unit/integration testing, verification | Usability validation (incl. AODA/WCAG) | Health & wellness app quality & reliability | Risk control implementation | QMS process adherence | Security monitoring, incident response | Privacy & data protection processes | e-records management, audit trail compliance | 21 CFR 820 (medical device QMS), IEC 60601-1 (if applicable) |
| **Live** | Service maintenance, feature releases, ongoing usability testing, web analytics, open data, disaster recovery | Continuous improvement, monitoring, corrective actions | Maintenance, software updates, verification & validation | Usability monitoring | Ongoing safety and quality metrics | Risk effectiveness monitoring | QMS process maintenance | Security monitoring, updates | Privacy monitoring, GDPR reporting | Ongoing electronic record integrity, e-signature tracking | 21 CFR 820 (if medical device), HIPAA (if U.S. patient data), IEC 60601-1 |

## Notes for Implementation

1. **Traceability:** Link all deliverables to GitHub Issues → Branch → Pull Request → Tests → Wiki evidence.
2. **Risk Management:** Maintain a Risk Log for all features and phases (ISO 14971 / IEC 62304).
3. **Quality & Safety:** Follow ISO 90003 guidance for software engineering; implement IEC 62304 lifecycle controls.
4. **Usability & Accessibility:** IEC 62366 + AODA/WCAG compliance for all UI elements.
5. **Security & Privacy:** ISO/IEC 27001 & 27701 for information security and personal data management.
6. **Medical Device Compliance:** ISO 13485, IEC 62304, ISO 14971, IEC 62366 apply if Red Witch qualifies as health software.
7. **Electronic Records:** FDA 21 CFR Part 11 applies to audit trails, approvals, and electronic data management.
8. **Optional / Conditional Standards:** IEC 60601-1, ISO 14155, 21 CFR 820, HIPAA depending on hardware, clinical studies, U.S. data, or medical device classification.
9. **Governance:** DSS approval checkpoints and phase reviews = management review points in QMS.

---

# **Design Control Deliverables Checklist Table — Ontario Framework**

| DSS Phase     | Deliverable                              | SOP-DC-001 Clause             | DSS Principle / Objective                      | Applicable Standards / Regulations                       | Completed (✓) | Reference / Record |
| ------------- | ---------------------------------------- | ----------------------------- | ---------------------------------------------- | -------------------------------------------------------- | ------------- | ------------------ |
| **Discovery** | User research report                     | 6.2 Design Inputs             | Prioritize user needs, data-informed decisions | ISO 9001:2015 (8.3), ISO 90003, ISO/IEC 27001, ISO 14971 |               |                    |
|               | Personas & primary user groups           | 6.2, 6.3                      | Prioritize user needs, equitable access        | ISO 9001:2015, IEC 62366                                 |               |                    |
|               | Needs & requirements analysis            | 6.2                           | Prioritize user needs                          | ISO 9001:2015, ISO 90003                                 |               |                    |
|               | Market / regulatory / feasibility study  | 6.2, 6.3                      | Data-informed, transparency                    | Ontario DSS, ISO 9001:2015                               |               |                    |
|               | Product manager assignment               | 5 Roles & Responsibilities    | Governance, accountability                     | ISO 9001:2015                                            |               |                    |
|               | Agile workflow setup                     | 6.1, 6.3                      | Continuous improvement, iterative design       | Ontario DSS, ISO 90003                                   |               |                    |
| **Alpha**     | Co-creation session notes                | 6.3, 6.4                      | Prioritize user needs, transparency            | IEC 62366, ISO 9001:2015                                 |               |                    |
|               | Prototypes / mockups                     | 6.3 Design Execution          | Iterative design, user feedback                | ISO 90003, IEC 62304                                     |               |                    |
|               | User testing plan                        | 6.3, 6.4                      | User-centered design, data-informed            | IEC 62366, ISO 9001:2015                                 |               |                    |
|               | Usability testing reports                | 6.4 Verification              | User-centered design, accessibility            | IEC 62366, AODA/WCAG                                     |               |                    |
|               | Journey map                              | 6.3                           | Prioritize user needs                          | ISO 9001:2015, Ontario DSS                               |               |                    |
|               | Technical feasibility assessment         | 6.2, 6.3                      | Data-informed, transparency                    | ISO 90003, IEC 62304                                     |               |                    |
|               | Financial feasibility assessment         | 6.3                           | Data-informed                                  | ISO 9001:2015                                            |               |                    |
|               | Initial project plan                     | 6.1, 6.3                      | Governance, transparency                       | ISO 9001:2015                                            |               |                    |
| **Beta**      | Minimum Viable Product (MVP)             | 6.3, 6.4                      | Iterative design, continuous improvement       | ISO 90003, IEC 62304, IEC 62366, ISO 13485               |               |                    |
|               | Continuous user testing results          | 6.4 Verification & Validation | User-centered design                           | IEC 62366, AODA/WCAG                                     |               |                    |
|               | Device validation                        | 6.4 Verification              | Accessibility, user needs                      | IEC 62366, WCAG                                          |               |                    |
|               | Accessibility testing                    | 6.4 Verification              | Equitable access                               | IEC 62366, AODA/WCAG                                     |               |                    |
|               | KPIs and performance metrics             | 6.4 Verification              | Data-informed, transparency                    | ISO 9001:2015                                            |               |                    |
|               | Privacy & security report                | 6.3, 6.4                      | Data-informed, transparency                    | ISO/IEC 27001, ISO/IEC 27701                             |               |                    |
|               | Automated testing results                | 6.4 Verification              | Continuous improvement                         | ISO 90003, IEC 62304                                     |               |                    |
|               | Branding compliance                      | 6.3                           | Transparency, consistent design                | Ontario Design System                                    |               |                    |
|               | Maintenance & update plan                | 6.5 Design Changes            | Continuous improvement                         | ISO 9001:2015, IEC 62304                                 |               |                    |
| **Live**      | Service maintenance logs                 | 6.5, 6.6 Records              | Continuous improvement                         | ISO 9001:2015, IEC 62304                                 |               |                    |
|               | Ongoing usability testing                | 6.4, 6.6                      | User-centered, accessibility                   | IEC 62366, WCAG                                          |               |                    |
|               | Feature backlog updates                  | 6.3, 6.5                      | Iterative design                               | ISO 90003                                                |               |                    |
|               | Web analytics reports                    | 6.4 Verification & Validation | Data-informed                                  | ISO 9001:2015                                            |               |                    |
|               | Performance metrics                      | 6.4, 6.6                      | Data-informed                                  | ISO 9001:2015                                            |               |                    |
|               | Open data publication                    | 6.6 Records                   | Transparency, equitable access                 | Open Data Guidebook, ISO/IEC 27001                       |               |                    |
|               | Disaster recovery / recovery plan        | 6.3, 6.5                      | Continuous improvement, data-informed          | ISO/IEC 27001, ISO 9001:2015                             |               |                    |
|               | Lessons learned / continuous improvement | 6.6, 6.1                      | Continuous improvement                         | ISO 9001:2015                                            |               |                    |

---

### **Instructions for Use**

1. Place a **checkmark (✓)** when the deliverable is complete and approved.
2. Include **reference / record link** (e.g., GitHub Issue, Wiki page, PR, test report).
3. Ensure that all DSS outputs are mapped to **SOP clauses and standards** for **audit readiness**.
4. Use this checklist throughout the project lifecycle to maintain full traceability.
