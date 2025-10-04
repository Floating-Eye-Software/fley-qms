# 📝 Risk Register – Red Witch Project (FLEY)

## **1. Introduction**

This Risk Register identifies potential risks and opportunities arising from the **context of the organization (COTO)**.
It is maintained as part of the QMS to support **planning, risk-based thinking, and continual improvement** in accordance with **ISO 9001:2015 Clauses 4 & 6**.

**Scope:** Risks apply only to Red Witch. Other FLEY activities (NetHack server, blogs) are out of scope.

---

## **2. Risk Register Table**

| ID | Risk / Opportunity                                               | Source (COTO Issue)                          | Impact                          | Likelihood | Severity | Controls / Mitigation                                                                                        | Owner                       | Monitoring / Review                                   |
| -- | ---------------------------------------------------------------- | -------------------------------------------- | ------------------------------- | ---------- | -------- | ------------------------------------------------------------------------------------------------------------ | --------------------------- | ----------------------------------------------------- |
| R1 | Volunteer burnout / continuity risk                              | Internal: Startup / Lean, single developer   | Medium: Delays, missed releases | Medium     | Medium   | Maintain realistic milestones, document processes, automate where possible, encourage community contributors | Developer                   | Review quarterly; milestone closure check             |
| R2 | Insufficient technical capacity for new features                 | Internal: Startup / Lean                     | Medium                          | Medium     | Medium   | Prioritize MVP features, automate tests, use modular design                                                  | Developer                   | Review in sprint planning; project review             |
| R3 | Privacy/data breach                                              | Internal: Privacy & Trust                    | High                            | Low-Medium | High     | Data minimization, encryption, GDPR-compliant consent, DPIA, secure storage                                  | Developer / Privacy Officer | Continuous monitoring; annual privacy audit           |
| R4 | Regulatory noncompliance (GDPR, ISO 13485, IEC 62304, FDA/CE)    | External: Legal/Regulatory                   | High                            | Medium     | High     | Maintain QMS, risk management, traceability, stay informed of classification guidance                        | Quality Manager             | Management review, annual regulatory check            |
| R5 | Lack of clinical validation / unsafe predictions                 | Internal: Clinical & Regulatory              | High                            | Medium     | High     | Document assumptions, validation steps, risk-benefit analysis, consider collaboration with clinical advisors | Developer / Quality Manager | Design review, verification/validation logs           |
| R6 | Loss of user trust                                               | Internal: Privacy & Trust / External: Social | High                            | Medium     | High     | Transparency, open-source code, clear communication, secure data handling                                    | Developer / Quality Manager | Monitor feedback, bug reports, community discussions  |
| R7 | Sustainability of volunteer effort                               | Internal: Startup / Lean                     | Medium                          | Medium     | Medium   | Manage scope, document QMS processes, encourage external contributions                                       | Developer / Quality Manager | Annual review, milestone completion                   |
| R8 | Technical debt accumulation                                      | Internal: Startup / Lean                     | Medium                          | Medium     | Medium   | Code reviews, CI/CD automated testing, modular design                                                        | Developer                   | Continuous integration metrics; quarterly code review |
| R9 | Opportunity: Differentiation via ethical, privacy-first approach | Internal/External: Privacy & Trust, Social   | High                            | Medium     | Medium   | Highlight transparency and ad-free model, communicate ethical stance                                         | Developer / Quality Manager | Track adoption, user feedback, PR mentions            |

---

## **3. Risk Rating Legend**

* **Likelihood:** Low / Medium / High
* **Severity:** Low / Medium / High
* **Impact:** Combination of likelihood and severity, guides prioritization of mitigation

---

## **4. Review & Update**

* Risk Register is **reviewed at each major release** or **annually**, whichever comes first.
* New risks are added as context evolves (e.g., new regulations, volunteer changes, feature expansion).
* Mitigations and monitoring actions are updated to reflect lessons learned and audit outcomes.
* Documented in **Management Review Records**.

---
