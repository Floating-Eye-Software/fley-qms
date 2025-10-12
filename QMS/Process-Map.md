# **Process Map – FLEY QMS**

## 1. Overview
The QMS comprises three core workflows supported by enabling processes.

1. **Operate the QMS (Continuous Improvement)**  
2. **Create the QMS (Establishment Project)**  
3. **Develop Products (Red Witch Project)**  

---

## 2. High-Level Diagram
```mermaid
flowchart TD
    subgraph Operate[Operate the QMS – Continuous Improvement]
        A1[Context & Risk Review] --> A2[Audits & CAPA] --> A3[Management Review]
    end
    subgraph Create[Create the QMS – Establishment Project]
        B1[Design QMS Structure] --> B2[Develop SOPs/WIs] --> B3[Validate Framework]
    end
    subgraph Develop[Develop Products – Red Witch Project]
        C1[Requirements & Planning] --> C2[Design & Implementation] --> C3[Verification & Release]
    end
    A3 --> A1
    A1 --> B1
    B3 --> A1
    C3 --> A2
````

---

## 3. Process Interactions

| Process               | Inputs                       | Outputs                      | Responsible Roles | Key Controls               | Intended Result       |
| --------------------- | ---------------------------- | ---------------------------- | ----------------- | -------------------------- | --------------------- |
| **Operate the QMS**   | Context, risks, audits       | Updated objectives & actions | Top Management    | Risk register, Mgmt Review | Continual improvement |
| **Create the QMS**    | ISO requirements, org needs  | Approved manual, SOPs & WIs  | Quality Manager   | Planning SOP               | Validated framework   |
| **Develop Products**  | Quality plans & requirements | Verified releases            | Project Mgr / Dev | Design SOP                 | Compliant product     |
| **Support Processes** | Docs / records               | Controlled info              | Quality Mgr       | GitHub control rules       | Traceable records     |

---

## 4. References

* `Quality-Manual.md` – overview
* `SOPs/` and `WIs/` – detailed methods
* `records/` – objective evidence
