# ✅ Updated Process Map and Interactions – FLEY QMS

---

## **1. Overview**

The Floating Eye Software (FLEY) Quality Management System (QMS) is composed of **three interrelated workflows** that together ensure quality, compliance, and continual improvement:

1. **Operate the QMS (Continuous Improvement)** – The ongoing system that maintains and improves the QMS, manages risks, conducts audits, and drives maturity.
2. **Create the QMS (Establishment Project)** – The temporary project that designs, documents, and implements the QMS framework itself.
3. **Develop Products (Red Witch Project)** – Application of the QMS to plan, design, develop, verify, and release software products.

Supporting processes (Document & Record Control, Change Control, Traceability, Post-Market Surveillance, Information Security) enable and interact with these three core workflows.

---

## **2. High-Level Process Map**

```mermaid
flowchart TD
    subgraph A1[Operate the QMS (Continuous Improvement)]
        A11[Context & Risk Review]
        A12[Audits & CAPA]
        A13[Management Review]
    end

    subgraph A2[Create the QMS (Establishment Project)]
        A21[Design & Approve QMS Structure]
        A22[Develop SOPs, WIs, Manual]
        A23[Validate Framework via Pilot]
    end

    subgraph A3[Develop Products (Red Witch Project)]
        A31[Requirements & Planning]
        A32[Design & Implementation]
        A33[Verification & Release]
    end

    A11 --> A21
    A21 --> A31
    A33 --> A12
    A12 --> A13
    A13 --> A11

    A31 -->|Design Inputs / Issues| A32
    A32 -->|Change Requests / Risks| A12
    A32 -->|Documentation| D1[Document & Record Control]
    A32 -->|Trace Links| D2[Traceability]
    A32 -->|Security Data| D3[Information Security]
    A33 -->|Feedback| D4[Post-Market Surveillance]
```

**Notes:**

* The **Operate QMS workflow** governs and reviews the other two workflows.
* The **Create QMS workflow** establishes the system framework; once complete, it feeds into Operate QMS.
* The **Develop Products workflow** applies QMS controls and provides real-world feedback for continual improvement.

---

## **3. Process Interaction and Responsibilities**

| Process / Workflow            | Inputs                                    | Outputs                                         | Responsible Roles               | Key Controls / Methods                          | Intended Result                                | Linked Processes               |
| ----------------------------- | ----------------------------------------- | ----------------------------------------------- | ------------------------------- | ----------------------------------------------- | ---------------------------------------------- | ------------------------------ |
| **Operate the QMS**           | Context, risks, audits, CAPA data         | Updated objectives, actions, improved processes | Top Management, Quality Manager | Audit program, management review, risk register | Sustained compliance and continual improvement | All                            |
| **Create the QMS**            | ISO 9001 requirements, organization needs | Approved QMS Manual, SOPs, WIs                  | Quality Manager, Team Leads     | Planning SOP, Project Management SOP            | Established and validated QMS framework        | Operate QMS, Develop Products  |
| **Develop Products**          | Quality Plans, requirements, risks        | Released product and evidence                   | Project Manager, Developers     | Design & Development SOPs, verification WIs     | Product meets requirements and compliance      | Operate QMS, PMS, Traceability |
| **Document & Record Control** | Draft docs, records                       | Controlled versions                             | Quality Manager                 | Versioning in GitHub / Wiki                     | Accurate, retrievable documentation            | All                            |
| **Change Control**            | Change requests, issues                   | Approved changes                                | Developer, Quality Manager      | PR review workflow                              | Controlled product and process changes         | Dev, Operate QMS               |
| **Traceability**              | Requirements, tests, risks                | Trace matrices                                  | QA, Developer                   | Automated tracking tools                        | End-to-end traceability                        | Dev, Operate QMS               |
| **Post-Market Surveillance**  | Feedback, complaints                      | PMS reports, inputs for change                  | Quality Manager                 | PMS SOP, review schedule                        | Data-driven improvement                        | Operate QMS, Develop Products  |
| **Information Security**      | GDPR/NIST requirements                    | Security controls, logs                         | Privacy Officer                 | ISMS SOP, training                              | Secure data handling                           | All                            |

---

## **4. Workflow Interactions**

| From             | To               | Information Flow / Feedback                     |
| ---------------- | ---------------- | ----------------------------------------------- |
| Operate QMS      | Create QMS       | Requirements for system design, lessons learned |
| Create QMS       | Operate QMS      | Completed QMS framework for ongoing use         |
| Develop Products | Operate QMS      | Quality data, audits, post-market feedback      |
| Operate QMS      | Develop Products | Policies, objectives, approved procedures       |
| Develop Products | Create QMS       | Validation feedback for QMS design              |

---

## **5. Documented Information**

* **SOPs and Work Instructions** – define each process.
* **Quality Plans** – establish objectives, deliverables, and metrics.
* **Records** – provide evidence of performance and compliance.
* **Repositories** – GitHub Issues, Wiki, and source control ensure traceability and version control.

---

## **6. References**

* `Quality-Manual.md` – QMS overview and workflow description
* `SOPs/` – Process procedures
* `WIs/` – Tool-specific methods
* `Plans/` – Quality and project plans
* `Compliance/` – Standards mapping and trace matrix
* `Risk-Register.md` – Context and risk linkages

---
