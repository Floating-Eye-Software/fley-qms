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
