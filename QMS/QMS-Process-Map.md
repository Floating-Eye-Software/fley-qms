# QMS Process Map and Interactions – FLEY

---

## **1. Overview**

The Floating Eye Software (FLEY) QMS provides a **structured system of interrelated processes** to ensure consistent delivery of **high-quality, safe, and compliant products**.

It is organized around two **core workflows**:

1. **QMS Creation, Maintenance, and Improvement** – developing, operating, and continually improving the QMS itself.
2. **Project Implementation (Red Witch Development)** – applying the QMS to design, develop, verify, and release products.

Supporting processes (Document & Record Control, Change Control, Traceability, Post-Market Surveillance, Information Security) provide **resources, documentation, and controls** that enable the core workflows to operate effectively.

---

## **2. High-Level Process Map**

```mermaid
flowchart TD
    A[Market Needs & Feedback<br>(Post-Market Surveillance)] --> B[Quality Planning]
    B --> C[Design & Development<br>(Red Witch Project)]
    C --> D[Release & Deployment]
    D --> A
    C -->|Records, Documentation| E[Document & Record Control]
    C -->|Change Requests| F[Change Control]
    C -->|Requirements, Tests, Risks| G[Traceability]
    A -->|Inputs for Design| C
    H[QMS Improvement<br>(Audits, Assessments, CAPA)] --> B
    H --> C
    H --> E
    H --> F
```

**Notes:**

* Feedback loops (Post-Market Surveillance, audits, CAPA) inform both **planning** and **development**, ensuring that lessons learned are incorporated.
* Documentation generated at every stage provides **evidence of process operation**, compliance, and decision-making.

---

## **3. Process Interaction and Responsibilities**

| Process                       | Inputs                                                     | Outputs                                      | Responsibilities & Resources                                | Key Controls / Methods                          | Intended Result                                         | Linked Processes                                        |
| ----------------------------- | ---------------------------------------------------------- | -------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| **Quality Planning**          | Market needs, regulatory requirements, internal objectives | Project Plans, Quality Plans, Milestones     | Project Manager, Quality Manager; planning tools, templates | SOPs/WIs for planning, checklists               | Approved, actionable plans aligned to QMS & regulations | Design & Development, QMS Improvement                   |
| **Design & Development**      | Project Plans, requirements, risk registers                | Verified product, release-ready code         | Developer, QA; CI/CD, traceability matrix                   | Verification & validation SOPs, automated tests | Product meets requirements, safety, quality             | Document & Record Control, Traceability, Change Control |
| **Document & Record Control** | Draft docs, templates, approvals                           | Controlled, versioned documents, records     | Developer, Quality Manager; GitHub, wiki                    | Versioning, approval, access control            | Traceable, retrievable, accurate documentation          | All processes                                           |
| **Change Control**            | Change requests, issues                                    | Authorized changes, updated docs             | Developer, Quality Manager; GitHub PRs                      | Change SOPs, review/approval criteria           | Controlled, auditable changes                           | Design & Development, QMS Improvement                   |
| **Traceability**              | Requirements, design outputs, tests, risks                 | Trace matrices, verification evidence        | Developer, Quality Manager; traceability tools              | SOPs for mapping inputs/outputs                 | Full traceability from requirements to product          | Design & Development, PMS                               |
| **Post-Market Surveillance**  | Feedback, complaints, market data                          | PMS reports, design inputs                   | Quality Manager, Developer; issue tracker                   | Data collection SOP, review frequency           | Continuous feedback for product improvement             | Design & Development, QMS Improvement                   |
| **QMS Improvement**           | Audits, CAPA, assessment results                           | Updated QMS documents, SOPs, WIs             | Quality Manager; audit tools                                | Internal audit procedures, PDCA cycle           | Continually improved QMS                                | All processes                                           |
| **Information Security**      | GDPR/NIST requirements, internal policies                  | Security policies, evidence, mitigation logs | Developer, Privacy Officer; security tools                  | Privacy & security SOPs, training               | Secure, compliant data handling                         | QMS, Development                                        |

---

## **4. Documented Information**

The FLEY QMS **relies on documented information** to:

* **Support operation of processes:** Each SOP, Work Instruction, Plan, and template defines how a process should be carried out.
* **Provide evidence:** Records demonstrate that activities are performed as planned, supporting audits and regulatory compliance.
* **Enable traceability:** Inputs, outputs, and decisions are linked across processes for transparency and accountability.
* **Drive continual improvement:** Documentation of findings, CAPA actions, and lessons learned feed back into planning and process updates.

All documented information is maintained in **controlled repositories** (GitHub wiki, source code, and project tracking tools) and is regularly reviewed for relevance, accuracy, and completeness.

---

## **5. References**

* `QMS/Quality-Manual.md` – System description
* `SOPs/` – Operating procedures
* `WIs/` – Work instructions
* `Plans/` – Project-specific tailoring
* `Compliance/` – Standards mapping
* `QMS/Risk-Register.md` – Risk mapping from context
