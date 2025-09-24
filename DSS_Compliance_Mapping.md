# Appendix B – Ontario DSS Compliance Mapping (Red Witch Project)

This appendix maps the Ontario Digital Service Standard (DSS) phases and deliverables to the Red Witch project documentation and processes.

| DSS Phase | DSS Deliverables / Requirements | Red Witch Corresponding Deliverables / Processes | Documentation Location |
|-----------|--------------------------------|-----------------------------------------------|-----------------------|
| **Discovery** | Conduct user research; identify user groups & needs; assess existing services; identify policies & barriers; document findings | User research sessions, personas, needs analysis, feasibility research, identified barriers | GitHub Wiki: Discovery Notes, User Personas, Feasibility Reports |
| | Designate product manager; establish agile workflow | Assigned PM; Agile boards, sprint planning | GitHub Project Boards; SDP §2, §3 |
| **Alpha** | Work with users to co-create solutions; build & test prototypes; validate technical & financial feasibility; plan for process changes | Prototypes, journey maps, user testing reports; initial project plan; financial & technical feasibility documentation | GitHub Wiki: Alpha Phase, Prototypes, Journey Maps; SDP §3 & §6 |
| **Beta** | Build MVP; continuously test service with users; device validation; accessibility testing; measure KPIs; resolve technical/process issues; privacy/security report; automated testing; WCAG compliance; branding; maintenance plan | MVP implementation; automated test suites; accessibility tests; KPIs tracked; privacy & security documentation; branding applied; maintenance plan developed | GitHub Wiki: Beta Phase, Test Reports, Accessibility Reports, KPI Dashboard; SDP §3, §4, §6 |
| **Live** | Service & maintenance; ongoing user research; release feature updates; monitor KPIs; evaluate complaints; continuous improvement; publish open data; recovery plan | Production service; user feedback surveys; backlog updates; web analytics monitoring; performance metrics; disaster recovery plan; open data outputs | GitHub Wiki: Live Phase Notes, Analytics Dashboard, Backlog Updates, Open Data Repository; SDP §3, §6, §7 |
| **Principles** | User needs prioritized; transparency; equitable access; data-informed; continuous improvement | Accessibility testing (AODA/WCAG); public-facing documentation; privacy & data protection; iterative SDLC; SOPs development | GitHub Wiki: Accessibility Reports, SOP Drafts, SDLC Artifacts; Quality Manual §3-7 |
| **Digital Governance** | DSS assessment at each phase; evaluation through governance processes (Digital First Assessment, ARB) | Review checkpoints at end of each phase; internal governance meetings; approval sign-offs | SDP §2, §9; Quality Manual §5, §8 |
| **Measurement** | Define KPIs upfront; service analytics; monitor performance; report on benefits | KPIs defined in Beta; analytics dashboards; quarterly reporting on performance metrics | SDP §3, §6, §9; GitHub Wiki: KPI Reports |
| **Data / Open Data** | Transparent, accurate, timely, accessible, open; adhere to exemptions (PHIPA, FOI, etc.) | Anonymized usage statistics, aggregated reports; privacy compliance; open data publications | GitHub Wiki: Open Data Repository; Privacy & Security SOPs; Quality Manual §6 |

### Notes on Usage

1. Each DSS phase is **mapped to concrete Red Witch deliverables**, ensuring traceability from regulatory expectations → project outputs.  
2. Links to **GitHub Wiki pages and SDP sections** allow auditors to verify compliance easily.  
3. This appendix is a **living document** and should be updated iteratively as Red Witch evolves.

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

Perfect ✅ — let’s create a **Global Compliance Matrix** that takes every **Floating Eye SOP deliverable** and shows how it maps across **FDA (21 CFR 820 / 11), EU MDR (Annex II & III), ISO 13485, ISO 14971, IEC 62304, and IEC 62366**.

This becomes your “single table of truth” you can show auditors from **any region** (FDA, EU, Canada, Japan, etc.).

---

# 🌍 **Global Compliance Matrix for Floating Eye SOP Deliverables**

| **Floating Eye SOP Deliverable**                                       | **FDA 21 CFR 820**                                | **FDA 21 CFR 11**                          | **EU MDR (Annex II/III)**                              | **ISO 13485**                                  | **ISO 14971**                        | **IEC 62304**                                 | **IEC 62366**                         |
| ---------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------ | ---------------------------------------------- | ------------------------------------ | --------------------------------------------- | ------------------------------------- |
| **Software Requirements Specification (SRS)**                          | 820.30(c) Design Inputs                           | 11.10 (audit trail of changes)             | Annex II 2.3 (Design & manufacturing info)             | 7.3.2 (Design inputs)                          | —                                    | 5.2 (Software requirements)                   | —                                     |
| **Risk Management File (RMF)**                                         | 820.30(g) Risk analysis                           | 11.10 (secure storage, audit trails)       | Annex I (General Safety & Performance), Annex II 2.4.4 | 7.1 (Risk management)                          | Entire standard                      | 7.1.2 (Risk control in development)           | —                                     |
| **Usability Engineering File (UEF)**                                   | 820.30(f) Design Verification (usability testing) | 11.10                                      | Annex I (Usability & safety), Annex II 6.1             | 7.3.3 (Design outputs)                         | Supports risk controls               | —                                             | Full coverage (all clauses)           |
| **Software Architecture & Design Spec**                                | 820.30(d) Design Outputs                          | 11.10                                      | Annex II 2.4 (Design solutions)                        | 7.3.3 (Design outputs)                         | —                                    | 5.3 (Software architecture design)            | —                                     |
| **Traceability Matrix (REQ → Code → Test)**                            | 820.30(j) Design History File                     | 11.10 (electronic records, audit trail)    | Annex II 2.4.3 (Verification & validation)             | 7.3.9 (Design traceability)                    | 3.4 (Risk traceability)              | 5.1, 5.2, 5.7 (traceability across lifecycle) | —                                     |
| **Verification Test Plan & Results**                                   | 820.30(f) Verification                            | 11.10 (electronic records of test results) | Annex II 6.1 (V\&V)                                    | 7.3.6 (Design verification)                    | Supports verification of mitigations | 5.7.1 (Unit, integration, system testing)     | 5.7 (Usability verification)          |
| **Validation Test Plan & Results**                                     | 820.30(g) Design Validation                       | 11.10                                      | Annex II 6.2 (Validation)                              | 7.3.7 (Design validation)                      | Supports validation of mitigations   | 5.7.4 (System validation)                     | 5.9 (Usability validation)            |
| **Release Package (incl. release notes, install/deploy instructions)** | 820.70 Production & Process Controls              | 11.10 (secure records)                     | Annex II 6.2 (Release documentation)                   | 7.5 (Production & service provision)           | —                                    | 5.8 (Software release)                        | —                                     |
| **Configuration & Change Records**                                     | 820.30(i) Design Changes                          | 11.10 (audit trail of changes)             | Annex II 2.4.2 (Changes to design)                     | 7.3.9 (Design changes)                         | 7.4 (Risk mgmt of changes)           | 5.8.3 (Configuration mgmt)                    | —                                     |
| **CAPA (Corrective & Preventive Action) Log**                          | 820.100 CAPA                                      | 11.10 (audit trail of CAPA records)        | Annex III PMS (link to CAPA)                           | 8.5.2 / 8.5.3 (Corrective & preventive action) | 7.4 (Risk control effectiveness)     | —                                             | —                                     |
| **Post-Market Surveillance (PMS) Report**                              | 820.198 Complaint Handling                        | 11.10                                      | Annex III PMS, Art. 83–86                              | 8.2.1 (Feedback), 8.2.2 (Complaint handling)   | 9 (Post-production info)             | —                                             | —                                     |
| **Design History File (DHF)**                                          | 820.30(j) DHF                                     | 11.10 (audit trail)                        | Annex II (Technical Documentation)                     | 4.2.5 (Medical device file)                    | 3.5 (Risk mgmt file reference)       | 5.1–8.0 (SDLC artifacts)                      | Annex C (link usability to tech docs) |
| **Device Master Record (DMR)**                                         | 820.181 DMR                                       | 11.10                                      | Annex II (Tech Doc = DMR equivalent)                   | 4.2.3, 4.2.4                                   | —                                    | —                                             | —                                     |
| **Device History Record (DHR)**                                        | 820.184 DHR                                       | 11.10                                      | Annex II + III (manufacturing & PMS history)           | 8.2.3, 8.5.1                                   | —                                    | —                                             | —                                     |
| **Training Records**                                                   | 820.25 Training                                   | 11.10 (audit trail of training records)    | Annex II (Quality mgmt system reference)               | 6.2 (Competence, training)                     | —                                    | —                                             | —                                     |

---

## 🔑 How to Use This Matrix

* **Auditors**: You can show this table to FDA, EU Notified Body, or MDSAP auditor — it demonstrates that every SOP deliverable maps to a regulatory requirement.
* **Projects**: Each project (Red Witch, or others) fills in *where* each deliverable is implemented (GitHub, Jira, Confluence, etc.).
* **Evidence storage**: Confluence = DHF/Tech File, Jira = traceability/testing, GitHub = code/config mgmt.

---

✅ With this single matrix:

* You prove compliance to **FDA QSR (820) + Part 11**
* You prove compliance to **EU MDR Annex II/III**
* You meet **ISO 13485/14971/62304/62366** (which are the globally harmonized standards used in Canada, Australia, Brazil, Japan, etc.).

---
