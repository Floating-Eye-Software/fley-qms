# **FLEY Quick Start**

*A fast, practical guide to running projects, phases, and MR cycles in FLEY.*

```mermaid
flowchart TD
    P[Plan Issue] --> O[Objectives]
    P --> M[Milestones]
    M --> PH[Milestone Phase Issues]
    PH --> A[Actions]
    A --> DEP[Issue Dependencies]

    P --> T[Traceability Links]
    P --> VOE[Verification of Effectiveness]

    VOE --> RR[Residual Risks & Lessons Learned]
    VOE --> MR[Management Review (MR) Cycle - Plan Issue]

    style P fill:#4C6EF5,color:#fff
    style M fill:#ffea99
    style PH fill:#ffd866
    style A fill:#d4ffd4
    style DEP fill:#ffcccc
    style T fill:#b3d9ff
    style VOE fill:#ffb380
    style RR fill:#ffe2b3
    style MR fill:#d6ccff
```

---

## **1. Create a Planning Issue**

Use a **Planning Issue** for any structured activity:

* Projects / initiatives
* Milestone phases
* Management Review (MR) cycles

Inside the Planning Issue, define:

* **Objectives**
* **Milestones**
* **Linked Actions**
* **Dependencies** (issue → issue)
* **Traceability** (SOPs, standards, controlled docs)

If the work is regulated or high-impact:
→ Create a **Quality Plan** (controlled document) and link it.

---

## **2. Add Milestones + Phase Planning Issues**

* **Milestones** group related Actions
* **Milestone Phase Planning Issues** allow milestones to be sequenced

Use a Phase Planning Issue when:

* The phase must unblock another phase/project/MR cycle
* You want dependencies between phases
* Closing the phase should trigger something (e.g., next MR cycle)

Hierarchy:
**Actions → Phase Planning Issues → Milestones → Planning Issues**

---

## **3. Add & Coordinate Actions**

Each piece of work is a standard GitHub Issue using the **Plan label**.

For every Action:

* Link it to the parent **Planning Issue**
* Assign it to the appropriate **Milestone**
* Optionally: link it to a **Phase Planning Issue** so it can participate in sequencing

Actions inherit traceability + sequencing from their parent Planning Issue.

---

## **4. Set Dependencies (Sequencing)**

GitHub only allows **issue → issue**, so the sequencing patterns are:

* Planning → Planning
* Planning → Phase Planning
* Phase Planning → Phase Planning
* Action → Action or Phase Planning

These build the roadmap sequencing and automatic blockers.

---

## **5. Management Review (MR) Cycles**

Each MR cycle is a **Planning Issue**.

MR cycle Planning Issues:

* Receive VoE outputs from completed Planning Issues
* Pull forward risks & lessons learned
* May be automatically unblocked by Phase Planning Issues
  (e.g., “Release Validation Complete” → unblocks next MR cycle)

---

## **6. Verification of Effectiveness (VoE)**

Performed at the completion of:

* A Planning Issue
* A Phase Planning Issue
* An MR cycle

VoE confirms:

* Objectives were met
* All Actions are complete or dispositioned
* Traceability is intact
* Risks + lessons learned are documented

VoE outputs automatically feed MR cycles.

---

## **7. Close the Loop**

Every Planning Issue ends with:

1. VoE completed
2. Lessons + risks pushed to the next MR cycle
3. Residual Work (if any) converted into new Planning Issues or Actions

This ensures continuous improvement across cycles.
