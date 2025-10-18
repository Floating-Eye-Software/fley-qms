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
    C2 -.->|"[Quality Planning SOP]"| C3
    O2 -.->|"[QMS Operations WI]"| O3
    D2 -.->|"[Design Control SOP]"| D3
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

| Process                           | Inputs                                 | Outputs                               | Resources                       | Responsible Roles               |
| --------------------------------- | -------------------------------------- | ------------------------------------- | ------------------------------- | ------------------------------- |
| **Operate the QMS**               | Context, risks, audits, feedback       | Updated objectives & actions          | Risk register, audit checklist  | Top Management, Quality Manager |
| **Create the QMS**                | ISO requirements, organizational needs | Approved QMS framework, SOPs & WIs    | Documentation tools, SME inputs | Quality Manager, SMEs           |
| **Develop Products (Red Witch)**  | Requirements, quality plans            | Verified releases                     | Design tools, project boards    | Project Manager, Dev Team       |
| **Document & Record Control**     | Draft docs, templates                  | Approved, version-controlled docs     | GitHub, templates               | Quality Manager                 |
| **Change Control**                | Change requests, issues                | Approved changes, updated documents   | GitHub, change log              | Project Lead, Quality Manager   |
| **Leadership / Management**       | Policy inputs, context                 | Objectives, management review outputs | Dashboards, meeting templates   | Top Management                  |
| **Risk & Opportunity Management** | Context, feedback                      | Updated risk register                 | Risk register tool              | Quality Manager, Process Owners |
| **Project Management**            | Requirements, resources                | Project deliverables                  | Scheduling tools, boards        | Project Manager                 |
| **Quality Planning**              | Policy, risks, context                 | Quality plans, objectives             | Planning tools                  | Quality Manager                 |
