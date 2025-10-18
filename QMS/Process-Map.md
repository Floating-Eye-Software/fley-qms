# **QMS – FLEY Process Map**

**Slug:** Process-Map  
**Revision:** r1  
**Effective Date:** [YYYY-MM-DD]  
**Controlled Source:** https://github.com/mlehotay/redwitch/wiki/Process-Map  

---

## **1. QMS Structure Overview**

This diagram shows the **hierarchical structure of the FLEY Quality Management System**, from foundational documents through SOPs to operational implementation.

```mermaid
flowchart TD
    %% Core Definition Layer
    subgraph Core[Core Definition Layer]
        QM[Quality Manual]
        CA[Context Analysis]
        QP[Quality Policy]
        PM[Process Map]
        OC[Organizational Chart]
    end

    %% SOP Layer
    subgraph SOP[SOP Layer]
        SOP1[Document Control SOP]
        SOP2[Change Control SOP]
        SOP3[Leadership SOP]
        SOP4[Management Review SOP]
        SOP5[Quality Planning SOP]
        SOP6[Project Management SOP]
        SOP7[Risk and Opportunity Management SOP]
        SOP8[Design Control SOP]
        SOP9[Identification and Traceability SOP]
    end

    %% Operational Layer
    subgraph WI[Operational Layer]
        WISetup[WI: Set Up QMS in GitHub]
        WIOperate[WI: Operate QMS in GitHub]
        ProductBoards[Red Witch Project Boards]
    end

    %% Connections between Core and SOPs
    QM --> SOP1
    QM --> SOP2
    QM --> SOP3
    QM --> SOP4
    QM --> SOP5
    QM --> SOP6
    QM --> SOP7
    QM --> SOP8
    QM --> SOP9

    CA --> SOP5
    PM --> SOP6
    PM --> SOP8
    OC --> SOP3
    OC --> SOP4

    %% SOPs to Operational Layer
    SOP1 --> WISetup
    SOP2 --> WISetup
    SOP3 --> WIOperate
    SOP4 --> WIOperate
    SOP5 --> WIOperate
    SOP6 --> WIOperate
    SOP7 --> WIOperate
    SOP8 --> WIOperate
    SOP9 --> WIOperate

    %% Workflow progression
    WISetup --> WIOperate
    WIOperate --> ProductBoards
```

**Explanation:**

1. **Core Definition Layer:** Establishes the QMS scope, policies, context, and organizational structure.
2. **SOP Layer:** Standard Operating Procedures define **how activities are controlled**.
3. **Operational Layer:** Work Instructions implement the QMS in GitHub and manage **all product/project workflows**.

The diagram shows the **flow from definition → procedures → execution**, ensuring **traceability, control, and continual improvement**.

---

## **2. QMS Operational Workflow**

The following diagram illustrates the three primary workflows defined in the Quality Manual (§5. QMS Workflows).

Each workflow corresponds to a set of Standard Operating Procedures (SOPs) and Work Instructions that define how FLEY’s QMS is created, operated, and applied in product development.

Feedback loops between workflows support continual improvement in alignment with ISO 9001:2015 + Amd 1:2024.


```mermaid
flowchart TD
    %% --- QMS Workflows Overview ---
    subgraph Create[QMS Creation Workflow]
        C1[Design QMS Structure]
        C2[Develop SOPs & WIs]
        C3[Validate Framework]
        C1 --> C2 --> C3
    end

    subgraph Operate[QMS Operation Workflow]
        O1[Monitor Context & Risks]
        O2[Audits & CAPA]
        O3[Management Review]
        O1 --> O2 --> O3 --> O1
    end

    subgraph Develop[Product Development Workflow]
        D1[Requirements & Planning]
        D2[Design & Implementation]
        D3[Verification & Release]
        D1 --> D2 --> D3
    end

    %% --- Interactions Between Workflows ---
    C3 --> O1
    D3 --> O2
    O3 --> C1

    %% --- SOP references ---
    C2 -.->|"[[Quality Planning SOP]]"| C3
    O2 -.->|"[[Leadership SOP]], [[Management Review SOP]]"| O3
    D2 -.->|"[[Design Control SOP]]"| D3
```

**Workflow Summary:**

1. **Operate the QMS:**

   * Monitor context, risks, and opportunities
   * Conduct audits, CAPA, and management reviews
   * Feed outcomes into improvements and updates

2. **Create the QMS:**

   * Design and document QMS structure
   * Develop SOPs and Work Instructions
   * Validate framework for approval

3. **Develop Products (Red Witch):**

   * Collect requirements and plan
   * Execute design, implementation, and verification
   * Release product outputs while feeding insights into QMS operation

---

## **3. QMS Process Table**

| Process                           | Inputs                                 | Outputs                                 | Resources                                                   | Responsible Roles                 | Risks & Opportunities                                                    | Monitoring & Control                                       | Documented Information / Retention                                                                 |
| --------------------------------- | -------------------------------------- | --------------------------------------- | ----------------------------------------------------------- | --------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Operate the QMS**               | Context, risks, audits, feedback       | Updated objectives & actions            | Risk register, audit checklist, management review templates | Top Management, Quality Manager   | Ineffective CAPA, missed improvements / Proactive improvements           | Audit schedule, CAPA closure tracking, Mgmt review minutes | SOPs: Leadership, Risk & Opportunity, Change Control; WI: Operate QMS; Retain in GitHub / records/ |
| **Create the QMS**                | ISO requirements, organizational needs | Approved Quality Manual, SOPs & WIs     | Documentation tools, SME inputs                             | Quality Manager, SMEs             | Scope gaps, misalignment with ISO / Efficient QMS implementation         | Document review & approval process, validation checklist   | SOP: Quality Planning; WI: Setup QMS; Quality-Manual.md; Retain in GitHub                          |
| **Develop Products (Red Witch)**  | Requirements, quality plans            | Verified releases                       | Design software, project boards, testing facilities         | Project Manager, Development Team | Missed requirements, design errors / Early validation, design automation | Verification & validation reviews, milestone checks        | SOP: Design & Development; WI: Operate QMS, Product Dev; Product records in GitHub                 |
| **Document & Record Control**     | Draft docs, templates                  | Approved, version-controlled docs       | Document management system, GitHub                          | Quality Manager                   | Unauthorized edits, outdated docs / Controlled documentation             | Review & approval workflow, version check                  | SOP: Document & Record Control; WI: GitHub Setup; Retain in GitHub                                 |
| **Change Control**                | Change requests, issues                | Approved PRs, updated docs              | GitHub, change log                                          | Quality Manager, Project Lead     | Unreviewed changes / Controlled updates                                  | PR review workflow, approval check                         | SOP: Change Control; WI: GitHub PR Workflow; Retain in GitHub                                      |
| **Leadership / Management**       | Org. context, policy inputs            | Quality objectives, Mgmt review outputs | Meeting templates, dashboards                               | Top Management                    | Weak commitment, unclear direction / Improved engagement                 | Completion of management reviews, action tracking          | SOP: Leadership; Meeting minutes in GitHub                                                         |
| **Risk & Opportunity Management** | Context, process feedback              | Updated risk register                   | Risk register tool                                          | Quality Manager, Process Owners   | Unidentified risks, over-control / Risk mitigation, opportunity capture  | Risk review schedule, update log                           | SOP: Risk & Opportunity; WI: Update Risk Register; Retain in GitHub                                |
| **Project Management**            | Requirements, resources                | Project deliverables, reports           | Project boards, scheduling tools                            | Project Manager                   | Schedule delays, unclear scope / Efficient execution                     | Milestone tracking, progress reporting                     | SOP: Project Management; WI: Red Witch Boards; Retain in GitHub                                    |
| **Quality Planning**              | Policy, risks, context                 | Quality plans, objectives               | Templates, planning tools                                   | Quality Manager                   | Unrealistic objectives / Alignment with ISO                              | Objective tracking, review of plans                        | SOP: Quality Planning; WI: Plan Quality Objectives; Retain in GitHub                               |
| **Training Management**           | Training needs                         | Trained personnel                       | Learning platform, training materials                       | HR / Quality Manager              | Skills gaps / Competency improvement                                     | Training completion records, competency checks             | Training records in GitHub                                                                         |
